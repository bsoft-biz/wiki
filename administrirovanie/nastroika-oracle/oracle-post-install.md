# Oracle post install



The Database Control URL is 

http://poseidon.autovoczal.com:1158/em

chcp 1251

sqlplus sys/sys as sysdba

show parameter global\_names

alter system set global\_names=true;

show parameter sort\_area\_size

alter system set sort\_area\_size=655360 scope=spfile;

show parameter sga\_

alter system set sga\_max\_size=162M scope=spfile;

shutdown immediate;

startup mount;

alter database open;

//или просто startup

alter system set sga\_target=164M;

show parameter pga\_

alter system set pga\_aggregate\_target=18M;



Ставим жабу, sys/sys as sysdba -&gt; tablespaces -&gt;

sysaux -&gt; 500MB \(datafile size\)

system -&gt; 600MB \(datafile size\), 100MB \(additional\)

undo -&gt; 100MB \(datafile size\), 100MB \(additional\)

users -&gt; 100MB \(datafile size\), 10MB \(additional\)

-- Recovery

http://poseidon.autovoczal.com:1158/em

Maintance -&gt; Recovery Settings -&gt; галочка ARCHIVELOG Mode\*

Control panel -&gt; local security policy -&gt; local polices -&gt; user rights -&gt; log on as batch job -&gt; add user -&gt; добавляем юзера Slava

на сайте делаем apply, restart

select log\_mode from v$database;

В сервисах делаем рестарт консоли

В консоли В recovery settings - папка G:\Flash

В консоли В BackUp settings - папка G:\BackUp, потом делаем test backup вверху в Shedule Backup -&gt; Schedule Customized Backup: Options -&gt; 2 галочки возле delete

Ставим время, каждый день, бесконечно, ok.

Далее в maintance можно просмотреть Jobs

Cmd -&gt; rman -&gt; Connect  target // exit

show parameter db\_recovery\_file\_dest\_size

alter system set db\_recovery\_file\_dest\_size=2000M;

\(В режиме mount\)

Manage Current Backups - можно анализировать ситуацию

Если файлы заархивированы, то их можно удалить. Если случайно удалили и не заархивировали, то нажали select и crosscheck. Все с бэкапами делаем в консоли на этой вкладке.

shutdown immediate;

startup mount;

alter database recovery until cancel;

alter database open resetlogs;



G:\oracle\product\10.2.0\admin\virtual\bdump\alert\_virtual.log - можно просмотреть всю информацию о сервере.

В maintance -&gt; perform recovery.

recovery - это откат всех изменений а потом накат всех изменений из архивлога. ИфслГз делается утилитой exp.

Если что-то не получается, то нужно погасить БД, а потом перевести ее в режим моунт. Тогда можно будет делать ресторе и рековери. Так как какой-то файл \(sqlplus поругается\).

Далее нужно открыть БД.

------------------------------------------------------------------

Создаем схемы. Открываем скрипты в гуде - F:\Good071120-4.1.2.031\script\sys.

Предварительно нужно создать папки для этих файлов.

Желательно индексные табл пространства на один физич диск, а остальное на другие.

Указываем AUTOEXTEND ON NEXT 100M

Нажимаем F5.

Запускаем скрипт F:\Good071120-4.1.2.031\script\un4public

cd F:\Good071120-4.1.2.031\script\sys

user\_UN4$repozitar.sql --опциональный -надо добавить grant create any table

user\_UN4pack.sql

sys\_Traffic.sql

F:\Good071120-4.1.2.031\text\import\run.bat

chcp 1251

В нем правильно указываем сервер БД, новую и старую схему \(из которой был сделан экспорт\). Файл должен называться expdat.dmp .

\(содержание ran.dat imp1 virtual built built\)

После окончания импорта смотрим имплог.

Далее коннектимся к созданной схеме.

Компилируем представления, триггера, пакеты.

------------------------------------------------------------------

Устанавливаем corefiles.

BDE Administrator меняем:

1mpriv на C:\temp

на второй вкладке drivers\native\paradox\netdir на C:\temp

запускаем uniacclient из папки good  \(для ХК логин/пароль - dep/q\)

server - virtual, name in BD - новая схема.

Обязательно должен быть установлен принтер - хотя бы условный.

Excel-&gt; macros -&gt; безопасность - низкая // надежные издатели - галка у доверять visual basic projects/

тоже самое и в ворде.

Выполнить базовую проверку программы - сделать пару отчетов, заполнить справочники.

------------------------------------------------------------------

chcp 1251

rman

connect target;

crosscheck archivelog all;

delete expired archivelog all;

