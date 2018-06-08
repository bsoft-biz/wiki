# Настройка UnivList из нескольких типов

Справочник из нескольких типов нужно создавать в группе UNIV\_ALL.

Пример справочника: [univ\_p\_m.xml](https://yadi.sk/d/QPPFbzM13Wp8vq)

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| :------------- |:-------------:| :-----| :-----|
| Active | Boolean |  | true |
| AutoFilterTree1 | String | Открывать определенное дерево в справочнике | 1 |
| Caption | String | Подпись справочника | 1. Справочник товаров и материалов |
| DLL FormName | String |  |  |
| DLL ID | Integer | Идентификационный номер DLL |  |
| Gr1 | String | Значение поля GR1 из универса | TVR,2112 |
| ID | String |  | Prod&Mat |
| MainAttr | String |  | ATTR\_BAR |
| MenuAttr | String |  | ATTR\_PRC,ATTR\_MINMAX, ATTR\_STRGRP,ATTR\_MAU |
| SagiEditQuery | Boolean | Разрешить изменение запросов \(Alt+Q\) справочника | true |
| SpeedSearchQuery | String | Запрос для быстрого поиска,  который выполняется по нажатию Enter | SELECT cod,\(SELECT denumirea\_\_1 FROM vms\_univers u WHERE u.cod=t.cod \) denumirea\_\_1 FROM TMS\_MPT t WHERE |
| StartField | String | Поле позиционирования по умолчанию | STRIH1\_CODPRODUCER |
| Tip | String | Значение поля Tip из универса | P,M |

