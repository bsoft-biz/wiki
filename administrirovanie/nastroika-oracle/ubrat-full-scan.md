# Убрать FULL SCAN

При выборе из таблицы проводок происходил full scan даже когда запрос делался по индексу.

Помогло обновление статистики.

```sql
analyze table tmdb_cm compute statistics;
```



