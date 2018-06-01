# Поиск кто заблокировал документ

Вариант 1

Две сессии:

в первой:

```sql
update tmdb_docs
set datamanual=datamanual
where cod=:nrdoc
```

во второй:

```sql
SELECT 
bs.username "Blocking User", 
bs.username "DB User", 
ws.username "Waiting User", 
bs.sid "SID", 
ws.sid "WSID", 
bs.sql_address "address", 
bs.sql_hash_value "Sql hash", 
bs.program "Blocking App", 
ws.program "Waiting App", 
bs.machine "Blocking Machine", 
ws.machine "Waiting Machine", 
bs.osuser "Blocking OS User", 
ws.osuser "Waiting OS User", 
bs.serial# "Serial#", 
DECODE(wk.TYPE, 
'MR', 'Media Recovery',   'RT', 'Redo Thread',  'UN', 'USER Name', 
'TX', 'Transaction',  'TM', 'DML', 'UL', 'PL/SQL USER LOCK', 
'DX', 'Distributed Xaction', 'CF', 'Control FILE', 'IS', 'Instance State', 
'FS', 'FILE SET', 'IR', 'Instance Recovery', 'ST', 'Disk SPACE Transaction', 
'TS', 'Temp Segment', 'IV', 'Library Cache Invalidation', 
'LS', 'LOG START OR Switch', 'RW', 'ROW Wait','SQ', 'Sequence Number', 
'TE', 'Extend TABLE', 'TT', 'Temp TABLE', wk.TYPE) lock_type, 
DECODE(hk.lmode, 0, 'None', 1, 'NULL',  2, 'ROW-S (SS)',  3, 'ROW-X (SX)', 
4, 'SHARE', 5, 'S/ROW-X (SSX)', 6, 'EXCLUSIVE', TO_CHAR(hk.lmode)) mode_held, 
DECODE(wk.request, 0, 'None', 1, 'NULL',  2, 'ROW-S (SS)',  3, 'ROW-X (SX)', 
4, 'SHARE', 5, 'S/ROW-X (SSX)', 6, 'EXCLUSIVE',  TO_CHAR(wk.request)) mode_requested, 
TO_CHAR(hk.id1) lock_id1, 
TO_CHAR(hk.id2) lock_id2 
FROM 
v$lock hk, v$session bs, 
v$lock wk, v$session ws 
WHERE 
hk.block  
AND  hk.lmode != 0 
AND  hk.lmode != 1 
AND  wk.request  != 0 
AND  wk.TYPE (+) = hk.TYPE 
AND  wk.id1 (+) = hk.id1 
AND  wk.id2 (+) = hk.id2 
AND  hk.sid = bs.sid (+)
AND  wk.sid = ws.sid (+)
ORDER BY 1
```

Вариант 2

в первой сессии:

1

```sql
select sid from v$mystat 
where rownum=1
-- например 492
```

2

```sql
update tmdb_docs
set datamanual=datamanual
where cod=132169
```

во второй сессии:

1 

```sql
select osuser, terminal
from v$session
where sid =
(select sid
from v$lock
where (id1, id2) in
(select id1, id2
from v$lock
where kaddr =
(select lockwait
from v$session
where sid=492))
and sid <> 492)
```

