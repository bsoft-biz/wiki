# Univers

Главные \(идентификационные\) параметры формы Univers:

| **Название свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Active | Boolean | действующий объект | true |
| Caption | Boolean | подпись формы | 04. Справочник автомобилей |
| DLL FormName | String | тип формы | Univers |
| DLL ID | Integer | идентификационный номер DLL | 0 |
| TIP | String | тип справочника SysS | T |
| TIP.GR1 | Integer | подгруппа справочника GR1 | AVTO |
| TIP.GR2 | Integer | подгруппа справочника GR2 |  |

**Важное замечание:**

Если UnivList создан без GR1 \(или с пустым\), то в форме для ссылки на такой справочник необходимо в поле TIP добавить еще одну \* \(звездочку\) после указания типа справочника: TIP=\*M\*\*ALL\_MAT

Например: форма ссылается на справочник \(UnivList\) Материалов с такими параметрами

| **Название свойства** | **Значение** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Active | true |
| Caption | Все материалы |
| DLL FormName |  |
| DLL ID |  |
| Gr1 |  |
| ID | ALL\_MAT |
| SagiEditQuery | True |

 тогда параметры формы должны выглядеть следующим образом

| **Название свойства** | **Значение** |
| --- | --- | --- | --- | --- | --- |
| Active | true |
| Caption | Справочник материалов |
| DLL FormName | Univers |
| DLL ID | 0 |
| TIP | \*M\*\*ALL\_MAT |
