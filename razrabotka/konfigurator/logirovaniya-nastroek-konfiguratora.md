# Логирования настроек конфигуратора

Настройки конфигуратора хранятся в таблицах с приставкой `a$` \(`a$adp, a$adm`\).

Пример просмотра настроек секции General:

```sql
select * 
 from a$adp 
where obj_id = 6  
-- значение для obj_id можно найти в свойствах узла General, поле Nr Ord.
```

 Пример поиска по свойствам конфигуратора:

```sql
select * 
 from a$adp
where lower(svalue) like '%pkg_test_vova%'
--lower(key) like '%sql%' and
```

На таблице `a$adp` есть триггер `A$ADP$TRA`, который логирует изменение значений конфигуратора в таблицу `a$act`.

Пример просмотра логов изменения свойств секции General:

```sql
select * from A$ACT where obj_id = 6 and trunc(stamp) = trunc(sysdate)  
-- значение для obj_id можно найти в свойствах узла General, поле Nr Ord.
```

 Пример просмотра логов по правам:

```sql
select * from A$ACT where obj_id = 3878 and lower(prop_key) 
in ('lacsetupblockreports','lacsetupblocksections')  
-- значение для obj_id можно найти в свойствах узла General, поле Nr Ord.
order by stamp
```

