# Цвет строк в гридах

Цвет строк в гридах \(bgcolor\)

выполнить в Alt+F11:

```sql
select rownum, pkg_docs_util.decode_color(rownum) bgcolor 
from dual connect by level <= 64
```

потом поставить галку "Use BG Color" в Alt+D

Пример определения цвета строки:

```sql
case when dtcant1<0 then 224*65536+180*256+255
when dtcant1>0 then 220*65536+255*256+200
end bgcolor
```



