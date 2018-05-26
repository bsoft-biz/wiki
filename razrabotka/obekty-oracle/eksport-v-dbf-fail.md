# Экспорт в DBF файл

Экспорт данных в .dbf \(un$ora2dbf.make\_dbf\)

Экспорт данных без шаблона dbf.

```sql
make_dbf
(ora_table_name VARCHAR2, 
dbf_filename VARCHAR2,  
l_src_char_set VARCHAR2 DEFAULT NULL,
l_dst_char_set VARCHAR2 DEFAULT NULL, 
dbf_tmpl_filename VARCHAR2 DEFAULT NULL)
```

В функцию необходимо передать имя таблицы или вьюхи, а так же путь и имя создаваемого файла на сервере. Так же можно передать входящую и исходящую кодировку\(см. пример в описании пакета\).

Путь берется из параметров directory.

```sql
select directory_path into v_directory
from all_directories 
where directory_name = 'MAIL_DBF';
```

Для директории необходимо дать права.Для этого выполнить скрипт под SYS.

Например:

```sql
begin
dbms_java.grant_permission( 'DEV', 'SYS:java.io.FilePermission',
'/var/un4/mail_dbf/*',  'read,write' );
end;
```

Права вступают в силу в новых сессиях.

Пример вызова функции:

```sql
declare
v_directory long;
begin
select directory_path into v_directory
from all_directories 
where directory_name = 'MAIL_DBF';
```

```sql
un$ora2dbf.make_dbf('VMS_OPER_MARSH',v_directory||'/oper_marsh.dbf',null,
'RUSSIAN_CIS.CL8MSWIN1251');
end;
```

По умолчанию функция make\_dbf генерирует dbf-файл с заголовками столбцов, которые дополняются пробелами. 

Если нужно дополнять пустыми значениями - необходимо изменить функцию make\_dbf, то есть заменить в ней:

```sql
tmp_raw := utl_raw.cast_to_raw(RPAD(l_flds(i).NAME, 11, ' '));
```

 на

```sql
tmp_raw := utl_raw.cast_to_raw(RPAD(l_flds(i).NAME, 11, chr(0)));
```



