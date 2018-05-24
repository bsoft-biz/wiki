# Права доступа ACL

-- 1 создаем **ACL для курсов валют**

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.CREATE\_ACL\('acl\_for\_get\_curs.xml', 'ACL for getting curs', 'BOX', TRUE, 'connect'\);

-- даем права другой схеме на существующую ACL

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.ADD\_PRIVILEGE\('acl\_for\_get\_curs.xml', 'THK', TRUE, 'connect'\);

-- добавляем хосты в ACL

-- допускается добавление нескольких хостов в один acl

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.ASSIGN\_ACL\('acl\_for\_get\_curs.xml', '\*.cbpmr.net'\);

--

COMMIT;

--

-- 2 создаем **ACL для получения гугл-координат**

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.CREATE\_ACL\('acl\_for\_get\_crd.xml', 'ACL for getting coords', 'BOX', TRUE, 'connect'\);

-- даем права другой схеме на существующую ACL

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.ADD\_PRIVILEGE\('acl\_for\_get\_crd.xml', 'THK', TRUE, 'connect'\);

-- добавляем хосты в ACL

-- допускается добавление нескольких хостов в один acl

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.ASSIGN\_ACL\('acl\_for\_get\_crd.xml', '\*.googleapis.com'\);

--

COMMIT;

--

-- 3 создаем **ACL для отправки почты через stunnel \(localhost\)**

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.CREATE\_ACL\('acl\_for\_sendmail.xml', 'ACL for sending mail', 'BOX', TRUE, 'connect'\);

-- даем права другой схеме на существующую ACL

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.ADD\_PRIVILEGE\('acl\_for\_sendmail.xml', 'THK', TRUE, 'connect'\);

-- добавляем хосты в ACL

-- допускается добавление нескольких хостов в один acl

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.ASSIGN\_ACL\('acl\_for\_sendmail.xml', 'localhost', 465, 465\);

-- добавляем еще комбинацию хост-порт

EXECUTE DBMS\_NETWORK\_ACL\_ADMIN.ASSIGN\_ACL\('acl\_for\_sendmail.xml', 'localhost', 2525, 2525\);

--

COMMIT;

--

-- просмотр **списка схем, которые имеют права на использ. ACL**

select acl, principal, privilege, is\_grant, invert from dba\_network\_acl\_privileges;

-- проверка хостов, которые разрешены в ACL

select host, lower\_port, upper\_port, acl from dba\_network\_acls;

**Удаление ACL**

-- удаляем ACL

execute DBMS\_NETWORK\_ACL\_ADMIN.DROP\_ACL \('acl\_for\_send\_mail.xml'\);

--

COMMIT;

-- отключаем привязку к хосту

BEGIN

DBMS\_NETWORK\_ACL\_ADMIN.UNASSIGN\_ACL\(host=&gt; '\*.cbpmr.net'\);

END;

--

COMMIT;

-- Полный синтаксис отключения привязки к хосту:

DBMS\_NETWORK\_ACL\_ADMIN.UNASSIGN\_ACL \(

acl         IN VARCHAR2 DEFAULT NULL,

host        IN VARCHAR2 DEFAULT NULL,

lower\_port  IN PLS\_INTEGER DEFAULT NULL,

upper\_port  IN PLS\_INTEGER DEFAULT NULL\);

