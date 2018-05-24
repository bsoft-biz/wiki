# Через временную таблицу \(TMS\_SYSS\_SEL\_UNLOCK\)

Политика на запрет редактирования справочников syss \(LOCK\_SELECT\_POLICY\).

**По умолчанию политика закрывает всем пользователям системы права на просмотр и редактирование.**

Правила для предоставления доступа к **просмотру и** изменению справочников по типам реализованы в функции get\_select\_tms\_syss.

Для разрешения доступа на **просмотр и** редактирование нужно в RunSql на пользователе или на группе пользователей добавить строки с опр. значениями в таблицу TMS\_SYSS\_SEL\_UNLOCK.

Примеры runSql для доступа пользователей к **просмотру и** редактированию:

```sql
--на все справочники:
-- unlock Edit SysS All --
insert into TMS_SYSS_SEL_UNLOCK(tip)
values (null);
--
--по определенному типу:
-- unlock Edit SysS Tip=R --
insert into TMS_SYSS_SEL_UNLOCK(tip)
values ('R');
--
--по определенному типу и коду:
-- unlock Edit SysS Tip=R, Cod=18 --
insert into TMS_SYSS_SEL_UNLOCK(tip, cod)
values ('R', 18);
--по определенному типу, коду и коду1:
-- unlock Edit SysS Tip=Z, Cod=1101, cod1=9  --
insert into TMS_SYSS_SEL_UNLOCK(tip,cod,cod1)
values ('Z',1101,9);
```



