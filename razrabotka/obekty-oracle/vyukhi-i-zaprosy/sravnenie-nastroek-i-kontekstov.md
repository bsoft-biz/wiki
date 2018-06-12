# Сравнение настроек и контекстов

 Сравнение контекстов из `a$env` через Link

```sql
select a.*,
(select denumirea from vms_univers@dev_link where cod = un$to_number(value))
from a$env@dev_link a 
where name in
(select upper(name) from a$env@dev_link where not (lower(name) like '%perev%')
minus
select upper(name) from a$env)
```

 Сравнение секций General через Link

```sql
select name from a$adm a,a$adp$v p
where p.obj_id=a.obj_id
and a.section=nvl(upper(:p_section),'WEB_ORDERS')
minus
select name from a$adm@dev_link a,a$adp$v@dev_link p
where p.obj_id=a.obj_id
and a.section=nvl(upper(:p_section),'WEB_ORDERS')

select lower(name) from a$adm@dev_link a,a$adp$v@dev_link p
where p.obj_id=a.obj_id
and a.section=nvl(upper(:p_section),'WEB_ORDERS')
minus
select lower(name) from a$adm a,a$adp$v p
where p.obj_id=a.obj_id
and a.section=nvl(upper(:p_section),'WEB_ORDERS')
```



