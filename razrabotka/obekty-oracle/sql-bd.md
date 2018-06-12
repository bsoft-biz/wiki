# SQL; BD

отчет CST =&gt; обращение к датам :datebegin, :datefinal

`select wm_concat(поле) from таблица` =&gt; получим значения поля через запятую

`user_source (или all_source под sys-ом)` - тексты пакетов, вьюшек и т.п.

`select … from таблица as of timestamp (systimestamp - interval '1' hour) a where …` =&gt; вытаскиваем данные из таблицы, которые в ней были 1 hour назад \(вместо hour может быть minute и т.п.\)

`tmdb_docs_add` - данные со вкладки "Информация" документов

`userid from tparams` \(текущий user клиента\) или `sys_context('envun4','param_userid')` -&gt; получим код текущего пользователя в клиенте. дальше можно вытащить его имя из xusers

`unp_ini.get_strings` =&gt; название документа по `sysfid`

`tmdb_cm.sptype =0`=&gt;основная проводка; `=1`=&gt;вспомогательная; `=2`=&gt;зарегистрированные остатки; `=3`=&gt; \(?\) П для А/П счетов

`un$valuta.getcurs` =&gt; курс валюты

`yimport.get_parameter` =&gt; курс евро

`un$currencytotxt.romspell` =&gt; сумма прописью на соответствующем языке

`un$xparamsintrepr.getparameter` =&gt; данные со вкладки General

`select ivalue from a$adp where obj_id=(select obj_id from a$docs$v where sysfid=48331) and key='TIPAUTOCOMPLETARE'` =&gt;свойство конфигуратора из узла соответствующего документа \(например,48331\)

`xgridprop` \(в старом администраторе\); a$lob \(в новом конфигураторе\) =&gt; таблицы с дизайнами

`xgridprop.objtype =0`=&gt;это дизайн; `=1`=&gt;это cst-документ; `=2`=&gt;это информация о проводках; `=3,5`=&gt;это выпадающий справочник,отчет

`select * from v$version; или select VERSION from V$INSTANCE` =&gt; \(выполнять под **sys**-ом\) получим версию oracle

`select* from NLS_Session_Parameters` =&gt; параметры сессии

`select * from a$act t where action='l' --and new_value<>'Login successful'` =&gt; лог входов в программу \(если используется новый конфигуратор\)

`SELECT trim(TO_CHAR(-1234567819.12,'999G999G999G999D99','NLS_NUMERIC_CHARACTERS = ''. '' ')) FROM DUAL;` =&gt; число выведется с разделениями по 3 цифры

`a$act` можно отследить историю изменений узлов в конфигураторе. Маленькие буквы в колонке action - это действия со свойствами. Большие - со всем узлом. d/D - удаление и т.п.

`tms_syssv.vpret` и т.д. это заголовки столбцов из `tms_syss`. Например, если колонка vpret непустая, то вместо PRET в выпад.справочнике `tms_syss` в клиента будет видно внесенное название

```sql
"select id,username,OBJ_ID,password||
(select old_value  
from a$act t 
where action='p' and  t.obj_id=a.obj_id 
and  stamp=(select max(t1.stamp) from a$act t1 
where t1.action='p' and  t.obj_id=t1.obj_id)) r 
from a$users$v a where enabled=1 --and admin=1
order by id" Пользователи в новом конфигураторе
"grant select on v_$context to public
select * from v$context
SELECT * FROM all_context"
```

