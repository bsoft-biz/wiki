# Некорректные остатки

Проблема: в универсальном отчете появился некорректный остаток на счете :cont.

Если на вьюхах `vmdb_cmr`, `vmdb_cmi` нет проводок, которые дают некорректные остатки,

то нужно проверить их в таблице **`tmdb_cm`.**

**Например:**

```sql
select *
from tmdb_cm 
where data between :datastart and :dataend
and (ct=:cont or dt=:cont)
```

Такие проводки могут возникнуть, если удаление было из `tmdb_cm` \(в жабе\).

Для решения этой проблемы, нужно удалить проводки проблемного документа через уну.

После удалить строки из `TMDB_CM`:

```sql
select *
from tmdb_cm 
where nrdoc = :nrdoc;
delete from tmdb_cm 
where nrdoc = :nrdoc;
```



