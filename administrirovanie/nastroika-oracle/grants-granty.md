# Grants\(гранты\)

```sql
begin 
dbms_java.grant_permission( 'Имя_схемы', 
'SYS:java.io.FilePermission', '/share/un4/client_bank', 'ALL' );
end;
```

-Добавляет грант на каталог client\_bank

```sql
begin
dbms_java.grant_permission( 'Имя_схемы', 
'SYS:java.io.FilePermission', '/share/un4/client_bank/*', 'ALL' );
end;
```

-Добавляет грант на каталог client\_bank и все файлы находящиеся в нём

```sql
begin
dbms_java.grant_permission( 'Имя_схемы', 
'SYS:java.io.FilePermission', '/share/un4/client_bank/-', 'ALL' );
end;
```

-Добавляет грант на каталог client\_bank и рекурсивно на все файлы и каталоги находящиеся в нём

  
Для удаления прав сначала запросом надо посмотреть гранты

```sql
select * from dba_java_policy
```

потом

```sql
dbms_java.revoke_permission 
('USER1','java.io.FilePermission','d:\temp\','read,write');
```

- переводит его в состояние DISABLED  


```sql
dbms_java.delete_permission(здесь SEQ отключеного гранта);
```

- удаляет его

-----------------------------------

{% hint style="info" %}
 Выполнять под SYS.
{% endhint %}

{% hint style="warning" %}
 Сделать COMMIT.
{% endhint %}

Перезапустить сессию \(уну\), где пытаемся создать/прочитать файл.

