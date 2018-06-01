# Порядок установки грантов \(grants\) dbms\_java.grant\_permission

Была ситуация когда все гранты указанные в [Инструкции » Заработная плата](http://wiki.bsoft.biz/xwiki/bin/view/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D0%B8/%D0%97%D0%B0%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BD%D0%B0%D1%8F+%D0%BF%D0%BB%D0%B0%D1%82%D0%B0) созданы, однако программа работала не корректно. Точная причина не установлена, однако в случае с персучетом помогла следующая последовательность действий.

1. Удалить все гранты на каталог, &lt;&lt;ALL FILES&gt;&gt;, writeFileDescriptor, readFileDescriptor.   [Инструкция по удалению здесь](http://wiki.bsoft.biz/xwiki/bin/view/%D0%90%D0%B4%D0%BC%D0%B8%D0%BD%D0%B8%D1%81%D1%82%D1%80%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5/Grants%28%D0%B3%D1%80%D0%B0%D0%BD%D1%82%D1%8B%29+-+dbms_java.grant_permission)

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



