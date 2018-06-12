# Модуль оператор пассажирских перевозок

Справочник вокзалов  O I AV в кодвечи стоит код вокзала из таблицы …

Для экспорта ведомостей:

```sql
create directory OPER_VEDOMOST as 'd:\vedomosti\';
begin
dbms_java.grant_permission( 'VIOLAN', 'SYS:java.io.FilePermission', 
'd:\vedomosti\vedomost.dbf', 'write' );
end;


```

 Создание синонимов на объекты схемы гара на том же сервере, что и бух. часть

```sql
CREATE OR REPLACE PUBLIC SYNONYM GRA FOR gara.GRA;
CREATE OR REPLACE PUBLIC SYNONYM MINK FOR gara.MINK;
CREATE OR REPLACE PUBLIC SYNONYM T0BILET FOR gara.T0BILET;
CREATE OR REPLACE PUBLIC SYNONYM T0BILET_ADD FOR gara.T0BILET_ADD;
CREATE OR REPLACE PUBLIC SYNONYM T0BILET_SUMS FOR gara.T0BILET_SUMS;
CREATE OR REPLACE PUBLIC SYNONYM T0INLESNIRI FOR gara.T0INLESNIRI;
CREATE OR REPLACE PUBLIC SYNONYM T0RUTA FOR gara.T0RUTA;
CREATE OR REPLACE PUBLIC SYNONYM T1RUTA_M FOR gara.T1RUTA_M;
CREATE OR REPLACE PUBLIC SYNONYM TMS_UNIVERS_G FOR gara.TMS_UNIVERS;
CREATE OR REPLACE PUBLIC SYNONYM V0_T0GARA FOR gara.V0_T0GARA;
CREATE OR REPLACE PUBLIC SYNONYM V1RUTA_M FOR gara.V1RUTA_M;
-- для pkg_oper_docs
CREATE OR REPLACE PUBLIC SYNONYM VMDB_AV_BILET for gara.t0bilet;
CREATE OR REPLACE PUBLIC SYNONYM VMDB_AV_BILET_SUMS for gara.t0bilet_sums;
CREATE OR REPLACE PUBLIC SYNONYM VMDB_AV_CASSA for gara.tmdb_cassa;
CREATE OR REPLACE PUBLIC SYNONYM VMDB_AV_CASSA_LENTA for gara.t1casalenta;
CREATE OR REPLACE PUBLIC SYNONYM VMDB_AV_DOCS for gara.tmdb_docs;
CREATE OR REPLACE PUBLIC SYNONYM VMDB_AV_RUTA_M for gara.t1ruta_m;
CREATE OR REPLACE PUBLIC SYNONYM VMDB_AV_SERVICES for gara.t0services;
CREATE OR REPLACE PUBLIC SYNONYM VMS_AV_CASSA for gara.t0cassa;
CREATE OR REPLACE PUBLIC SYNONYM VMS_AV_RUTA for gara.t0ruta;
```

Если не строится отчет в F1 \(например Raport zilnic\) надо зайти в BDE Administrator -&gt; Drivers -&gt; Native-&gt; Oracle-&gt; DLL32 выставить -&gt; SQLORA8.DLL сохранить, перезапустить дисптечер и все пойдет.

В таблице `t0casagroups` задается список с каких вокзалов каждый вокзал может реализовывать билеты.

