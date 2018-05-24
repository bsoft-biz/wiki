# Настройка UnivList из нескольких типов

Справочник из нескольких типов нужно создавать в группе UNIV\_ALL.

Пример справочника: [univ\_p\_m.xml](http://wiki.bsoft.biz/xwiki/bin/download/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/UnivList+%D0%B8%D0%B7+%D0%BD%D0%B5%D1%81%D0%BA%D0%BE%D0%BB%D1%8C%D0%BA%D0%B8%D1%85+%D1%82%D0%B8%D0%BF%D0%BE%D0%B2/univ_p_m.xml)

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Active | Boolean |  | true |
| AutoFilterTree1 | String | Открывать определенное дерево в справочнике | 1 |
| Caption | String | Подпись справочника | 1. Справочник товаров и материалов |
| DLL FormName | String |  |   |
| DLL ID | Integer | Идентификационный номер DLL  |   |
| Gr1 | String | Значение поля GR1 из универса  | TVR,2112   |
| ID | String |   | Prod&Mat  |
| MainAttr | String |   | ATTR\_BAR  |
| MenuAttr | String |   | ATTR\_PRC,ATTR\_MINMAX, ATTR\_STRGRP,ATTR\_MAU  |
| SagiEditQuery | Boolean | Разрешить изменение запросов \(Alt+Q\) справочника   | true  |
| SpeedSearchQuery | String | Запрос для быстрого поиска,  который выполняется по нажатию Enter  | SELECT cod,\(SELECT denumirea\_\_1 FROM vms\_univers u WHERE u.cod=t.cod \) denumirea\_\_1 FROM TMS\_MPT t WHERE  |
| StartField | String | Поле позиционирования по умолчанию  | STRIH1\_CODPRODUCER  |
| Tip | String | Значение поля Tip из универса   | P,M  |

