# Логирование используется для docs и univers \(un$xlog\)

  
un$xlog - Пакет содержит процедуру логирования.

```sql
procedure inlog (inobj varchar2,inprop varchar2,inevent varchar2,icoment varchar2:='',
vexcluderepeated boolean:=true)
is
tmpvar number;
cc number;
minid number;
userid1 number;
begin
select userid into userid1 from tparams;
if vexcluderepeated
and userid1=nvl(userid2,-1) and inobj=nvl(inobj2,' ')
and inprop=nvl(inprop2,' ') and inevent=nvl(inevent2,' ')
and round(sysdate2,'mi')=round(sysdate,'mi')
then null;
else
inobj2:=inobj;inprop2:=inprop;inevent2:=inevent;sysdate2:=sysdate;userid2:=userid1;
insert into xlog (iobject,iproperty,ievent,itime,userid,nrrec,coment)
select inobj ,inprop  ,inevent,sysdate,userid1,id_xlog.nextval,icoment from dual;
end if;
end inlog;
```

 Таблица для хранения логов:

```sql
create table xlog
(
iobject    varchar2(20 byte),
iproperty  varchar2(50 byte),
ievent     varchar2(10 byte),
itime      date,
userid     number(5),
nrrec      number(10),
coment     varchar2(4000 byte),
terminal   varchar2(16 byte) default sys_context('userenv','terminal',16),
machine    varchar2(64 byte) default sys_context('userenv','host',64),
os_user    varchar2(30 byte) default sys_context('userenv','os_user',30),
ip_addr    varchar2(15 byte) default sys_context('userenv','ip_address',15),
module     varchar2(48 byte) default sys_context('userenv','module',48)
)
```

 Триггер на tms\_univers для логирования изменений.

```sql
create or replace trigger xtriglogunivers 
after insert or update or delete on tms_univers
for each row
begin
if inserting then
un$xlog.inlog('UNIV',:new.cod,'insert');
elsif updating then
un$xlog.inlog('UNIV',:new.cod,'update');
else
un$xlog.inlog('UNIV',:old.cod,'delete');
end if;
exception when others then
null;
end;
```

 Триггер на tmdb\_docs для логирования изменений.

```sql
create or replace trigger xtriglogdocs 
after insert or update or delete on tmdb_docs
for each row
begin
if inserting then
un$xlog.inlog('DOCS',:new.cod,'insert');
elsif updating
then un$xlog.inlog('DOCS',:new.cod,'update');
else
un$xlog.inlog('DOCS',:old.cod,'delete');
end if;
exception when others then
null;
end;
/
```

