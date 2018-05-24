# Настройка базы

Настройка даты.

```sql
alter system flush shared_pool;
update sys.props$ set value$ = 'DD.MM.YYYY' where name = 'NLS_DATE_FORMAT';
commit;
alter system flush shared_pool;
shutdown immediate;
startup;
```

{% hint style="info" %}
 Подсказка:  При входе в БД ошибка ORA-00604, ORA-12705 =&gt;Мой компьютер-&gt;Свойства-&gt;Дополнительно-&gt;Переменные среды-&gt;добавить NLS\_LANG=AMERICAN\_RUSSIAN.CL8MSWIN1251. Если не поможет, то еще и в regedit-&gt;oracle-&gt;key…-&gt;добавить тот же параметр
{% endhint %}

Список серверов можно разместить здесь

HKEY\_CURRENT\_USER\Software\CoreLab\ODAC\Connect

или в файле

orases.xml

