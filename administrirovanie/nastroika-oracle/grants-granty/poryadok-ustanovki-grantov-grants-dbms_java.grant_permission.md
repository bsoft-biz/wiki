# Порядок установки грантов \(grants\) dbms\_java.grant\_permission

Была ситуация когда все гранты указанные в Инструкции » Заработная плата созданы, однако программа работала не корректно. Точная причина не установлена, однако в случае с персучетом помогла следующая последовательность действий.

1. Удалить все гранты на каталог, &lt;&lt;ALL FILES&gt;&gt;, writeFileDescriptor, readFileDescriptor.   [Инструкция по удалению здесь](https://bsoft.gitbook.io/wiki/administrirovanie/nastroika-oracle/grants-granty)

2. Выполнить скрипт

```sql
DECLARE
 KEYNUM NUMBER;
BEGIN
  SYS.DBMS_JAVA.GRANT_PERMISSION(
     grantee           => 'ИМЯ СХЕМЫ'
    ,permission_type   => 'SYS:java.io.FilePermission'
    ,permission_name   => '/var/un4/Т000858/-'
    ,permission_action => 'read,write,delete'
    ,key               => KEYNUM
    );
END;
/
DECLARE
 KEYNUM NUMBER;
BEGIN
  SYS.DBMS_JAVA.GRANT_PERMISSION(
     grantee           => 'ИМЯ СХЕМЫ'
    ,permission_type   => 'SYS:java.io.FilePermission'
    ,permission_name   => '<<ALL FILES>>'
    ,permission_action => 'execute'
    ,key               => KEYNUM
    );
END;
/
DECLARE
 KEYNUM NUMBER;
BEGIN
  SYS.DBMS_JAVA.GRANT_PERMISSION(
     grantee           => 'ИМЯ СХЕМЫ'
    ,permission_type   => 'SYS:java.io.FilePermission'
    ,permission_name   => '<<ALL FILES>>'
    ,permission_action => 'read ,write, execute, delete'
    ,key               => KEYNUM
    );
END;
/
DECLARE
 KEYNUM NUMBER;
BEGIN
  SYS.DBMS_JAVA.GRANT_PERMISSION(
     grantee           => 'ИМЯ СХЕМЫ'
    ,permission_type   => 'SYS:java.lang.RuntimePermission'
    ,permission_name   => 'writeFileDescriptor'
    ,permission_action => ''
    ,key               => KEYNUM
    );
END;
/
DECLARE
 KEYNUM NUMBER;
BEGIN
  SYS.DBMS_JAVA.GRANT_PERMISSION(
     grantee           => 'ИМЯ СХЕМЫ'
    ,permission_type   => 'SYS:java.lang.RuntimePermission'
    ,permission_name   => 'readFileDescriptor'
    ,permission_action => ''
    ,key               => KEYNUM
    );
END;
/
```



