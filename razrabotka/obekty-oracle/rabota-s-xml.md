# Работа с XML

  
**Источник: http://viralpatel.net/blogs/oracle-xmltable-tutorial/**

Пример nested: https://community.oracle.com/thread/2532826

```markup
-- Таблица с полем xmltype
create table t_xml_test
(id int not null, 
 xml_data xmltype);

insert into t_xml_test
values(1,
'
<SetGds>
 <item>
  <gds_cod>1001</gds_cod>
  <gds_name>Хлеб особый</gds_name>
  <barcode>41654165</barcode>
  <data>19.05.2015</data>
  <dtime>10:10:00</dtime>
  <shop_cod>1</shop_cod>
  <shop_name>Шериф1</shop_name>
  <flow_rate>126</flow_rate>
  <rest>22</rest>
 </item>
 <item>
  <gds_cod>1002</gds_cod>
  <gds_name>Хлеб тостовый</gds_name>
  <barcode>489615651</barcode>
  <data>19.05.2015</data>
  <dtime>20:20:00</dtime>
  <shop_cod>3</shop_cod>
  <shop_name>Шериф3</shop_name>
  <flow_rate>180</flow_rate>
  <rest>10</rest>
 </item>
</SetGds>');
-- Выборка всех элементов
   SELECT t.id, x.*
     FROM t_xml_test t,
          XMLTABLE ('/SetGds/item'
                    PASSING t.xml_data
                    COLUMNS gds_cod VARCHAR2(100) PATH 'gds_cod', 
                            gds_name VARCHAR2(100) PATH 'gds_name',
                            flow_rate number path 'flow_rate') x
    WHERE t.id = 1;
```

