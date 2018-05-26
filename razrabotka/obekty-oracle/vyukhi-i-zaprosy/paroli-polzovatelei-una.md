# Пароли пользователей UNA

  
Пароли пользователей\(если клиент на новом конфигураторе\)

```sql
select id,username,OBJ_ID,password||(select old_value  
from a$act t where action='p' and  t.obj_id=a.obj_id 
and  stamp=(select max(t1.stamp) from a$act t1 
where t1.action='p' and  t.obj_id=t1.obj_id)) r 
from a$users$v a 
where enabled=1 
--and admin=1
```



