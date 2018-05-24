# Настройка Oracle GateWays Windows

**Настройка Oracle GateWays для Windows.**

**Настройка oracle hs для версии oracle 10.X. \(подключение к sybase\)**

Для odbc драйвера установил SQL Anywhere 12 Developer Edition \(trial - 60 дней, т.к. ключ еще не пришел\).

Настроил ODBC:

Параметры sybase:

login = custom

pas = custom

server name = sqlMCRSSERV

database name = micros

database file = D:\MICROS\DATABASE\Data\micros.db

host=192.168.1.100;port=2638

Настроил HS:

1 в  файле

D:\oracle\product\10.2.0\db\_1\network\ADMIN\listener.ora

добавил в  SID\_LIST

\(SID\_DESC =

\(SID\_NAME = Micros\)

\(ORACLE\_HOME = D:\oracle\product\10.2.0\db\_1\)

\(PROGRAM = hsodbc\)

2 в файле

D:\oracle\product\10.2.0\db\_1\network\ADMIN\tnsnames.ora

добавил

MICROS =

\(DESCRIPTION =

\(ADDRESS = \(PROTOCOL = tcp\)\(HOST = 192.168.1.98\)\(PORT =

1521\)\)

\(CONNECT\_DATA =

  \(SID = Micros\)

\)

\(HS = OK\)\)

3 Создал файл

D:\oracle\product\10.2.0\db\_1\hs\admin\initmicros.ora с

содержанием

HS\_FDS\_CONNECT\_INFO = Micros

HS\_FDS\_TRACE\_LEVEL = off

HS\_FDS\_TRACE\_FILE\_NAME = AccessTraceLog.trc

4 Создал DBLINK

CREATE DATABASE LINK MICROS

CONNECT TO CUSTOM

IDENTIFIED BY 'CUSTOM'

USING 'micros';

5 Перезапустил LISTENER

6 Проверил связь с select \* from user\_objects@micros

**Настройка oracle GateWays для версии oracle 11.X \(подключение к FireBird\)**

1. Установил драйвер FireBird ODBC Driver.

2. Добавил новый источник данных \(ODBC\):

Имя источника \(DSN\): firebird

База данных: 192.168.0.37 :D:\Alex S&E\RECORDS.FDB

Клиент: D:\bs\firebird\_maestro\_executable\fbclient.dll

Пользователь SYSDBA, Пароль MasterKey

3. Установил Oracle GateWay 11g

4. Настроил файл oracle\product\11.2.0\tg\_1\hs\admin\initdg4odbc.ora

 \# This is a sample agent init file that contains the HS parameters that are

 \#

 HS\_FDS\_CONNECT\_INFO = firebird

 HS\_FDS\_TRACE\_LEVEL = ON

5. Настроил слушатель oracle listener:

LISTENER =

 \(ADDRESS\_LIST=

  \(ADDRESS=\(PROTOCOL=tcp\)\(HOST=server1.BMEZ.WJ\)\(PORT=1522\)\)

 \)

SID\_LIST\_LISTENER=

  \(SID\_LIST=

  \(SID\_DESC=

      \(SID\_NAME=dg4odbc\)

      \(ORACLE\_HOME=d:\oracle\product\11.2.0\tg\_1\)

      \(PROGRAM=dg4odbc\)

  \)

  \)

ADR\_BASE\_LISTENER = d:\oracle\product\11.2.0\tg\_1

6. Настроил tnsnames на клиенте и сервере:

\# tnsnames.ora Network Configuration File: d:\oracle\product\11.2.0\tg\_1\network\admin\tnsnames.ora

dg4odbc  =

  \(DESCRIPTION=

    \(ADDRESS=\(PROTOCOL=tcp\)\(HOST=server1\)\(PORT=1522\)\)

    \(CONNECT\_DATA=\(SID=dg4odbc\)\)

    \(HS=OK\)

  \)

7. Создал DBLink:

CREATE DATABASE LINK DG4ODBC

 CONNECT TO SYSDBA

 IDENTIFIED BY &lt;PWD&gt;

 USING 'DG4ODBC';

Внимание! При создании DATABASE LINKа необходимо указать пользователя и пароль с учетом регистра. Может понадобится создать имя пользователя в верхнем регистре.

