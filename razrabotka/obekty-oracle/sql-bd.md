# SQL; BD

отчет CST =&gt; обращение к датам :datebegin, :datefinal

select wm\_concat\(поле\) from таблица =&gt; получим значения поля через запятую

user\_source \(или all\_source под sys-ом\) - тексты пакетов, вьюшек и т.п.

select … from таблица as of timestamp \(systimestamp - interval '1' hour\) a where … =&gt; вытаскиваем данные из таблицы, которые в ней были 1 hour назад \(вместо hour может быть minute и т.п.\)

tmdb\_docs\_add - данные со вкладки "Информация" документов

userid from tparams \(текущий user клиента\) или sys\_context\('envun4','param\_userid'\) -&gt; получим код текущего пользователя в клиенте. дальше можно вытащить его имя из xusers

unp\_ini.get\_strings =&gt; название документа по sysfid

tmdb\_cm.sptype =0=&gt;основная проводка; =1=&gt;вспомогательная; =2=&gt;зарегистрированные остатки; =3=&gt; \(?\) П для А/П счетов

un$valuta.getcurs =&gt; курс валюты

yimport.get\_parameter =&gt; курсевро

un$currencytotxt.romspell =&gt; сумма прописью на соответствующем языке

un$xparamsintrepr.getparameter =&gt; данные со вкладки General

select ivalue from a$adp where obj\_id=\(select obj\_id from a$docs$v where sysfid=48331\) and key='TIPAUTOCOMPLETARE' =&gt;свойство конфигуратора из узла соответствующего документа \(например,48331\)

xgridprop \(в старом администраторе\); a$lob \(в новом конфигураторе\) =&gt; таблицы с дизайнами

xgridprop.objtype =0=&gt;это дизайн; =1=&gt;это cst-документ; =2=&gt;это информация о проводках; =3,5=&gt;это выпадающий справочник,отчет

select \* from v$version; или select VERSION from V$INSTANCE =&gt; \(выполнять под sys-ом\) получим версию oracle

select\* from NLS\_Session\_Parameters =&gt; параметры сессии

select \* from a$act t where action='l' --and new\_value&lt;&gt;'Login successful' =&gt; лог входов в программу \(если используется новый конфигуратор\)

SELECT trim\(TO\_CHAR\(-1234567819.12,'999G999G999G999D99','NLS\_NUMERIC\_CHARACTERS = ''. '' '\)\) FROM DUAL; =&gt; число выведется с разделениями по 3 цифры

a$act можно отследить историю изменений узлов в конфигураторе. Маленькие буквы в колонке action - это действия со свойствами. Большие - со всем узлом. d/D - удаление и т.п.

tms\_syssv.vpret и т.д. это заголовки столбцов из tms\_syss. Например, если колонка vpret непустая, то вместо PRET в выпад.справочнике tms\_syss в клиента будет видно внесенное название

"select id,username,OBJ\_ID,password\|\|\(select old\_value  from a$act t where action='p' and  t.obj\_id=a.obj\_id 

and  stamp=\(select max\(t1.stamp\) from a$act t1 where t1.action='p' and  t.obj\_id=t1.obj\_id\)\) r 

from a$users$v a where enabled=1 --and admin=1

order by id" Пользователи в новом конфигураторе

"grant select on v\_$context to public

select \* from v$context

SELECT \* FROM all\_context"

