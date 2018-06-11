# Через временную таблицу \(tms\_syss\_unlock\)

Политика на запрет редактирования справочников syss \(`LOCK_EDIT_POLICY`\).

**По умолчанию политика закрывает всем пользователям системы права на редактирование.**

Правила для предоставления доступа к изменению справочников по типам реализованы в функции `get_edit_tms_syss`.

Для разрешения доступа на редактирование нужно в RunSql на пользователе или на группе пользователей добавить строки с опр. значениями в таблицу `tms_syss_unlock`.

Примеры runSql для доступа пользователей к редактированию:

на все справочники:

```sql
-- unlock Edit SysS All --
insert into tms_syss_unlock(tip)
values (null);
```

по определенному типу:

```sql
-- unlock Edit SysS Tip=R --
insert into tms_syss_unlock(tip)
values ('R');
```

по определенному типу и коду:

```sql
-- unlock Edit SysS Tip=R, Cod=18 --
insert into tms_syss_unlock(tip, cod)
values ('R', 18);
```

