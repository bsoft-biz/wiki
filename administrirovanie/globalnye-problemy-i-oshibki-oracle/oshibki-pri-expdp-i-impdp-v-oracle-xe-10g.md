# Ошибки при expdp и impdp в Oracle XE 10g

При вызове функции expdp появляются ошибки

   ORA-39006: internal error

   ORA-39213: Metadata processing is not available

Если ошибки возникли после перехода на однобайтную кодировку \(CL8MSWIN1251\) необходимо распаковать содержимое [архива ](https://yadi.sk/d/8EedrSYP3Wo3Jc)в папку rdbms согласно пути установки oracle.

Пример: D:\oracle\product\10.2.0\server\rdbms\

После распаковки архива необходимо выполнить запрос с правами SYS

SQL&gt; execute dbms\_metadata\_util.load\_stylesheets;

 Ссылка на архив: [xml.rar](https://yadi.sk/d/8EedrSYP3Wo3Jc)

