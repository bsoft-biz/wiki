# FGA

```sql
-- если это дает ошибку то добавляем, удаляем строку, а потом удаляем полиси
exec DBMS_FGA.DROP_POLICY('BUILT2', 'YPCOUNTS', 'YPCOUNTS_ACCESS');
select * from fga$
begin
dbms_fga.add_policy (
object_schema=>'BUILT2',
object_name=>'YPCOUNTS',
policy_name=>'YPCOUNTS_ACCESS');
end;
/
DELETE FGA$
WHERE PNAME = 'YPCOUNTS_ACCESS'
AND ROWNUM < 2;
-- наша полиси
begin
dbms_fga.add_policy (
object_schema=>'BUILT2',
object_name=>'YPCOUNTS',
policy_name=>'YPCOUNTS_ACCESS',
statement_types => 'DELETE');
end;
/
select * from fga_log$
truncate table fga_log$
```

Пример запросов:

```sql
SELECT STATEMENT_TYPE, SQL_BIND, sql_text
extended_timestamp,
os_user,
userhost,
(select denumirea from built.vms_univers where cod = to_number(substr(sql_bind,-5,5))) prod
FROM DBA_COMMON_AUDIT_TRAIL
WHERE  SQL_BIND LIKE '%1(7):' ||:cod||'%'
select
extended_timestamp vr,
os_user,
userhost,
(select denumirea from built.vms_univers where cod = to_number(substr(sql_bind,-5,5))) prod,
SQL_BIND
from DBA_COMMON_AUDIT_TRAIL
where EXTENDED_TIMESTAMP BETWEEN :d1 and :d2
and os_user =  'spqr'
```



