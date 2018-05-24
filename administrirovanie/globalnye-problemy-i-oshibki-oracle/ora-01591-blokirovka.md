# ORA-01591: блокировка

Возникла ошибка в уне:

ORA-01591: блокировка, удерживаемая распред.транзакцией 28.19.482515, находящейся в неопр. сост

SQL text:

SELECT VMDB\_DOCS.\* FROM VMDB\_DOCS

WHERE DATAMANUAL BETWEEN '01.01.2016' AND '30.09.2016' 

ORDER BY COD ASC

Проверил - нет связи с пос-кассами!  
[http://www.sql.ru/forum/848072/ora-01591-blokirovka-uderzhivaemaya-raspred-tranzakciey-xx-nahodyashheysya-v-neopr-sost](http://www.sql.ru/forum/848072/ora-01591-blokirovka-uderzhivaemaya-raspred-tranzakciey-xx-nahodyashheysya-v-neopr-sost)  
помогло это:

```sql
grant FORCE any TRANSACTION to thk
```

```sql
BEGIN
FOR f IN (SELECT *
FROM dba_2pc_pending where state = 'prepared')
LOOP
execute immediate ('rollback FORCE '''||f.LOCAL_TRAN_ID||'''');
END LOOP;
END;
```

 Похоже, что проблема возникла в момент выключения компов на фирме1, т.к. в это время шел обмен.  
Логи:  
[https://yadi.sk/i/d8NcA8aftBExA](https://yadi.sk/i/d8NcA8aftBExA)

 _**Ошибка ORA-01591**_

ORA-01591: lock held by in-doubt distributed transaction 6.58.10015

/ блокировка, удерживаемая распред. транзакцией 6.58.10015,

находящейся в неопр. сост.

**По документации:**

**Причина:** Была попытка доступа к ресурсу, заблокированному "повисшей" распределенной транзакцией, находящейся в состоянии подготовки.

**Действие:** Для того, чтобы определить связь баз данных и состояние транзакции,  сравните номер транзакции в сообщении со столбцом GLOBAL\_TRAN\_ID таблицы DBA\_2PC\_PENDING. Попытайтесь исправить сетевое соединение для координатора и узла точки завершения транзакции, если это необходимо. Если исправление временно невозможно, обратитесь к  администратору базы данных узла точки завершения транзакции \(если она известна\), чтобы "протолкнуть" ожидающую какого-то действия транзакцию.

**Из практики:**

**Причина:** Ошибка диагностирует возникновение «смертельных объятий», зацикливании процессов друг на друге. Может возникнуть при попытке удалить из мастер-группы_дест-сайт_, если одна из БД других сайтов остановлена.

**Действие:** Запустите БД всех сайтов и в состоянии мастер-группы **NORMAL** повторите операцию.

Справка по теме:

[http://docs.oracle.com/cd/B19306\_01/server.102/b14231/ds\_txnman.htm\#i1007799](http://docs.oracle.com/cd/B19306_01/server.102/b14231/ds_txnman.htm#i1007799)

[http://docs.oracle.com/cd/B14117\_01/server.101/b10739/ds\_txnman.htm](http://docs.oracle.com/cd/B14117_01/server.101/b10739/ds_txnman.htm)

