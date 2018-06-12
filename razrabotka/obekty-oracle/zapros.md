# Запрос

```sql
select s.* 
, 'create index '||s.table_name||'_'||replace(s.columnsa,', ','_')||'_i on '||s.table_name||'('||s.columnsa||');' cmd
from 
(
select decode( b.table_name, null, '****', 'ok' ) Status, a.owner,
       a.table_name, a.columns columnsa, b.columns columnsb
from 
( select a.owner,
         substr(a.table_name,1,30) table_name, 
         substr(a.constraint_name,1,30) constraint_name, 
         max(decode(position, 1,     substr(column_name,1,30),null)) || 
         max(decode(position, 2,', '||substr(column_name,1,30),null)) || 
         max(decode(position, 3,', '||substr(column_name,1,30),null)) || 
         max(decode(position, 4,', '||substr(column_name,1,30),null)) || 
         max(decode(position, 5,', '||substr(column_name,1,30),null)) || 
         max(decode(position, 6,', '||substr(column_name,1,30),null)) || 
         max(decode(position, 7,', '||substr(column_name,1,30),null)) || 
         max(decode(position, 8,', '||substr(column_name,1,30),null)) || 
         max(decode(position, 9,', '||substr(column_name,1,30),null)) || 
         max(decode(position,10,', '||substr(column_name,1,30),null)) || 
         max(decode(position,11,', '||substr(column_name,1,30),null)) || 
         max(decode(position,12,', '||substr(column_name,1,30),null)) || 
         max(decode(position,13,', '||substr(column_name,1,30),null)) || 
         max(decode(position,14,', '||substr(column_name,1,30),null)) || 
         max(decode(position,15,', '||substr(column_name,1,30),null)) || 
         max(decode(position,16,', '||substr(column_name,1,30),null)) columns
    from dba_cons_columns a, dba_constraints b
   where a.constraint_name = b.constraint_name
     and b.constraint_type = 'R'
   group by a.owner, substr(a.table_name,1,30), substr(a.constraint_name,1,30) ) a, 
( select table_owner owner, substr(table_name,1,30) table_name, substr(index_name,1,30) index_name, 
         max(decode(column_position, 1,     substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 2,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 3,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 4,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 5,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 6,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 7,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 8,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position, 9,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position,10,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position,11,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position,12,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position,13,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position,14,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position,15,', '||substr(column_name,1,30),NULL)) || 
         max(decode(column_position,16,', '||substr(column_name,1,30),NULL)) columns
    from dba_ind_columns 
   group by table_owner, substr(table_name,1,30), substr(index_name,1,30) ) b
where a.table_name = b.table_name  (+) 
  and b.columns  (+) like a.columns  || '%' 
) s
where status <> 'ok'
--  and owner = 'UN4'
```

Вместо `UN4` - нужное имя схемы

Выполнять под **sys**

Если имя индекса из скрипта получится &gt; 30 символов, доработать напильником

