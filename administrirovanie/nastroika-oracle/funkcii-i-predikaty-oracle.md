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



 Работа с датами.

