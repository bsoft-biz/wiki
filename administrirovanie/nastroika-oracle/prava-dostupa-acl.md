# Права доступа ACL

-- 1 создаем **ACL для курсов валют**

























































































--

COMMIT;

-- Полный синтаксис отключения привязки к хосту:

DBMS\_NETWORK\_ACL\_ADMIN.UNASSIGN\_ACL \(

acl         IN VARCHAR2 DEFAULT NULL,

host        IN VARCHAR2 DEFAULT NULL,

lower\_port  IN PLS\_INTEGER DEFAULT NULL,

upper\_port  IN PLS\_INTEGER DEFAULT NULL\);
