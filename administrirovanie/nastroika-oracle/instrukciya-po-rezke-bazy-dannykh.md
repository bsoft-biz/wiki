# Инструкция по резке базы данных

1 вначале настраиваем tablespaces все как на оригинальном сервере можно использовать un4Versions

```sql
CREATE TABLESPACE TABSPACE_ARHIV DATAFILE
'F:\oradata11\TABSPACE_ARHIV.DBO' SIZE 500M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TABSPACE_GARA DATAFILE
'F:\oradata11\TABSPACE_GARA.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_DB1 DATAFILE
'F:\oradata11\TBS_GARA_DB1.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_DB3 DATAFILE
'F:\oradata11\TBS_GARA_DB3.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_DB4 DATAFILE
'F:\oradata11\TBS_GARA_DB4.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_DB5 DATAFILE
'F:\oradata11\TBS_GARA_DB5.DBO' SIZE 1212800K AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_DBT DATAFILE
'F:\oradata11\TBS_GARA_DBT.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_IND2 DATAFILE
'F:\oradata11\TBS_GARA_IND2.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_IND2B0 DATAFILE
'F:\oradata11\TBS_GARA_IND2BO.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_IND2CM DATAFILE
'F:\oradata11\TBS_GARA_IND2CM.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_IND2RU DATAFILE
'F:\oradata11\TBS_GARA_IND2RU.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_SYS DATAFILE
'F:\oradata11\TBS_GARA_SYS.DBO' SIZE 100M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBS_GARA_SYS2 DATAFILE
'F:\oradata11\TBS_GARA_SYS2.DBO' SIZE 100M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBSROLLBIG DATAFILE
'F:\oradata11\TBSROLLBIG.DBO' SIZE 600M AUTOEXTEND ON NEXT 20M;
CREATE TABLESPACE TBSROLLSMALL DATAFILE
'F:\oradata11\TBSROLLSMALL.DBO' SIZE 200M AUTOEXTEND ON NEXT 20M;
```

2 потом ставим вспомогательные схемы - UN4PUBLIC,  ARHIV, ADM. Только не ставим схему GARA и un4public у автовокзала свой собственный - его надо брать со старого сервера. Все эти схемы можно переносить при помощи режима сравнения схем в un4Versions.

3 сделать документ с остатками. Вызывается процедура adm.close\_sold\(’01.01.2011’\); удаляет проводки и документы до указанной даты, предварительно создает копии проводок и документов в базе архив \(tmdb\_cm\_2011, tmdb\_docs\_2011\)

CLOSE\_SOLD\_REZKA – не удаляет проводки . Создает остатки с кодом 0, старому доку остатков присваивает nextval значение сиквенса.

4 экспортировать по фильтру, включив только этот документ и все более поздние операции. Вообще тема экспорта по фильтру по дате родилась именно на автовокзале и впервые была реализована для него - а потом адаптирована для бухгалтерии.

А. указываем параметры подключения. Выбираем схему GARA и оракл директори

Б. На вкладке “Резка базы” ставим дату \(например если нужно оставить весь 2011 год и остальные дата =01.01.2011\) и в списке документов указываем номер документа остатков \(например 1\), созданный на предыдущем шаге. Нажать кнопку “Установить фильтр для резки”

В результате это таблица докс отфильтруется  по такому условию:

Datamanual&gt;=to\_date\(’01.01.2012’\) or cod=1

Проверить фильтр можно на вкладке “Фильтр на таблицы”, нажав на галочку “Контроль вручную”.

В. Вернуться на вкладку “Действия” и нажать экспорт по фильтру.

5 импортировать полученный дамп на новом сервере. Импорт делается стандартно, согласно инструкции по импорту схему с помощью universions. Пересоздать индексы.

