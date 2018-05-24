# Универсальное логирование

 Таблицы для логирования:

```sql
create table x$chglog
(
id   integer,
tbl  varchar2(30 byte),
who  varchar2(30 byte),
cmd  char(1 byte),
dt   date
)
create table x$chglog_value
(
id   integer,
col  varchar2(30 byte),
new  char(1 byte),
chr  varchar2(4000 byte),
num  number,
dat  date
)
```

 Пример триггера для логирования изменений данных в таблице.

```sql
create or replace trigger tslrprm_scutiri_cl
before insert or update or delete on tslrprm_scutiri
for each row
disable
declare
v_cmd char(1):=case when inserting then 'I' when updating then 'U' else 'D' end;
v_id int;
begin
insert into x$chglog(tbl,cmd)values('TSLRPRM_SCUTIRI',v_cmd)
returning id into v_id;
if updating or deleting then
insert into x$chglog_value(id,col,new,chr,num)values
(v_id,'SC_MUNC','0',to_char(:old.sc_munc),:old.sc_munc);
insert into x$chglog_value(id,col,new,chr,dat)values
(v_id,'DATASTART','0',to_char(:old.datastart,'DD.MM.YYYY'||
case when :old.datastart<>trunc(:old.datastart) 
then ' HH24:MI:SS' end),:old.datastart);
insert into x$chglog_value(id,col,new,chr,dat)values
(v_id,'DATAEND','0',to_char(:old.dataend,'DD.MM.YYYY'||
case when :old.dataend<>trunc(:old.dataend) 
then ' HH24:MI:SS' end),:old.dataend);
insert into x$chglog_value(id,col,new,chr,dat)values
(v_id,'DATA_ZAIAV','0',to_char(:old.data_zaiav,'DD.MM.YYYY'||
case when :old.data_zaiav<>trunc(:old.data_zaiav) 
then ' HH24:MI:SS' end),:old.data_zaiav);
insert into x$chglog_value(id,col,new,chr)values
(v_id,'TIP_SCUTIRI','0',:old.tip_scutiri);
insert into x$chglog_value(id,col,new,chr,num)values
(v_id,'LUNSUMA_TOTAL','0',to_char(:old.lunsuma_total),:old.lunsuma_total);
insert into x$chglog_value(id,col,new,chr,num)values
(v_id,'LUNI_TIP','0',to_char(:old.luni_tip),:old.luni_tip);
end if;
if inserting or updating then
insert into x$chglog_value(id,col,new,chr,num)values
(v_id,'SC_MUNC','1',to_char(:new.sc_munc),:new.sc_munc);
insert into x$chglog_value(id,col,new,chr,dat)values
(v_id,'DATASTART','1',to_char(:new.datastart,'DD.MM.YYYY'||
case when :new.datastart<>trunc(:new.datastart) 
then ' HH24:MI:SS' end),:new.datastart);
insert into x$chglog_value(id,col,new,chr,dat)values
(v_id,'DATAEND','1',to_char(:new.dataend,'DD.MM.YYYY'||
case when :new.dataend<>trunc(:new.dataend) 
then ' HH24:MI:SS' end),:new.dataend);
insert into x$chglog_value(id,col,new,chr,dat)values
(v_id,'DATA_ZAIAV','1',to_char(:new.data_zaiav,'DD.MM.YYYY'||
case when :new.data_zaiav<>trunc(:new.data_zaiav) 
then ' HH24:MI:SS' end),:new.data_zaiav);
insert into x$chglog_value(id,col,new,chr)values
(v_id,'TIP_SCUTIRI','1',:new.tip_scutiri);
insert into x$chglog_value(id,col,new,chr,num)values
(v_id,'LUNSUMA_TOTAL','1',to_char(:new.lunsuma_total),:new.lunsuma_total);
insert into x$chglog_value(id,col,new,chr,num)values
(v_id,'LUNI_TIP','1',to_char(:new.luni_tip),:new.luni_tip);
end if;
end;
/
```

 Процедура для генерации скрипта на создание лог. триггера:

```sql
create or replace procedure p$chglog_make_trigger (p_table varchar2)authid
current_user as
```

```sql
procedure s(p_text varchar2)is
begin
dbms_output.put_line(p_text);
end;
```

```sql
procedure ins_cols(p_alias varchar2)is
v_new char(1):=case when lower(p_alias)='new' then '1' else '0' end;
v_col varchar2(40);
begin
for c in (select column_name n,data_type t from user_tab_columns
where table_name=upper(p_table)) loop
v_col:=':'||p_alias||'.'||c.n;
if c.t='NUMBER' then
s('  insert into x$chglog_value(id,col,new,chr,num)values(v_id,'''||c.n||''''||
','''||v_new||''',to_char('||v_col||'),'||v_col||');');
elsif c.t='DATE' then
s('  insert into x$chglog_value(id,col,new,chr,dat)values(v_id,'''||c.n||''''||
','''||v_new||''',to_char('||v_col||',''DD.MM.YYYY''||');
s('    case when '||v_col||'<>trunc('||v_col||') 
then '' HH24:MI:SS'' end),'||v_col||');');
elsif c.t in('CHAR','VARCHAR2') then
s('  insert into x$chglog_value(id,col,new,chr)values(v_id,'''||c.n||''''||
','''||v_new||''','||v_col||');');
end if;
end loop;
end;
```

```sql
begin
s('create or replace trigger '||p_table||'_cl');
s('before insert or update or delete on '||p_table);
s('for each row');
s('declare');
s(' v_cmd char(1):=case when inserting then ''I'' when updating then 
''U'' else ''D'' end;');
s(' v_id int;');
s('begin');
s(' insert into x$chglog(tbl,cmd)values('''||p_table||''',v_cmd)');
s(' returning id into v_id;');
s(' if updating or deleting then');
ins_cols('old');
s(' end if;');
s(' if inserting or updating then');
ins_cols('new');
s(' end if;');
s('end;');
s('/');
end;
/
```

