# Перевод статьи utl\_http-and-ssl.php

Ссылка на источник: [http://www.oracle-base.com/articles/misc/utl\_http-and-ssl.php](http://www.oracle-base.com/articles/misc/utl_http-and-ssl.php)

Пример процедуры для выполнения запросов http/https.

```sql
CREATE OR REPLACE PROCEDURE show_html_from_url (p_url  IN  VARCHAR2) AS
  l_http_request   UTL_HTTP.req;
  l_http_response  UTL_HTTP.resp;
  l_text           VARCHAR2(32767);
BEGIN
  -- Make a HTTP request and get the response.
  l_http_request  := UTL_HTTP.begin_request(p_url);
  l_http_response := UTL_HTTP.get_response(l_http_request);
  -- Loop through the response.
  BEGIN
    LOOP
      UTL_HTTP.read_text(l_http_response, l_text, 32766);
      DBMS_OUTPUT.put_line (l_text);
    END LOOP;
  EXCEPTION
    WHEN UTL_HTTP.end_of_body THEN
      UTL_HTTP.end_response(l_http_response);
  END;
EXCEPTION
  WHEN OTHERS THEN
    UTL_HTTP.end_response(l_http_response);
    RAISE;
END show_html_from_url;
```

При попытке выполнить https запрос:

EXEC show\_html\_from\_url\('https://gb.redhat.com/'\);

Возникает ошибка:

ORA-29024: Certificate validation failure.

В этом случае необходимо добавить сертификат.

Используя браузер, нужно выгрузить сертификаты для сайта gb.redhat.com в файлы. \(для этого удобнее использовать mozilla\).

Далее Создаем Oracle Wallet, содержащий необходимые сертификаты.

Создаем новую папку Wallet. 

$ mkdir -p /u01/app/oracle/admin/DB11G/wallet

Создаем новый wallet.

$ orapki wallet create -wallet /u01/app/oracle/admin/DB11G/wallet -pwd WalletPasswd123 -auto\_login

После создания wallet, можно добавить сертификаты, которые мы ранее сохранили в файл:

$ orapki wallet add -wallet /u01/app/oracle/admin/DB11G/wallet -trusted\_cert -cert "/host/BaltimoreCyberTrustRoot.crt" -pwd WalletPasswd123

$ orapki wallet add -wallet /u01/app/oracle/admin/DB11G/wallet -trusted\_cert -cert "/host/CybertrustPublicSureServerSVCA.crt" -pwd WalletPasswd123

Далее тестируем процедуру для выполнения https запроса, заранее указываем где лежат сертификаты.

EXEC UTL\_HTTP.set\_wallet\('file:/u01/app/oracle/admin/DB11G/wallet', 'WalletPasswd123'\);

EXEC show\_html\_from\_url\('https://gb.redhat.com/'\);

