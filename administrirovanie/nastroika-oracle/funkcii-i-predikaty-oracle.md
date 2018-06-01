# Функции и предикаты oracle

**Функции и предикаты oracle**

- Функция удаляет все спец. символы:

```sql
select regexp_replace('AQ83D 29 EU/B<>!//\!!sg,. ?','\W?','',1,0,'i') 
from dual
```

- Пересекающиеся интервалы дат:

```sql
select 1 from dual 
where (sysdate,sysdate+1) overlaps (sysdate+2,sysdate+3);
```

{% hint style="info" %}
 [http://www.orafaq.com/node/2067](http://www.orafaq.com/node/2067)
{% endhint %}

{% hint style="info" %}
 [http://www.sql.ru/forum/actualthread.aspx?tid=389945](http://www.sql.ru/forum/actualthread.aspx?tid=389945)
{% endhint %}



 [Работа с датами.](http://wiki.bsoft.biz/xwiki/bin/view/Oracle.+%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B8+%D0%B8+%D0%B2%D0%BE%D0%B7%D0%BC%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D0%B8./%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0+%D1%81+%D0%B4%D0%B0%D1%82%D0%B0%D0%BC%D0%B8)

