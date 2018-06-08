# Формы

Формы служат для работы пользователя с данными, представляющими специализированную справочную информацию, используемую при работе с системой \(прайс-листы, регистры курсов валют, регистры норм затрат и др.\), либо сугубо для выполнения определенных действий по обработке данных.

Конфигурирование типовой формы включает настройки интерфейсной части и части обработки данных – действия. Объекты действия аналогичны объектам doc-action. Свойства этих объектов позволяют определять процедуры обработки данных.

Схема разработки новых форм аналогична созданию новых документов и отчетов и включает программную разработку, включение в список форм нового объекта типа форма, связывание этого объекта с программной реализацией посредством указания программных идентификаторов \(идентификатор bpl, идентификатор отчета в bpl\) и, возможно, определение для формы общих и специализированных настроек.

Доступные формы отображаются в меню Forme приложения Universal Accounting.

`Объекты типа Формы определяет стандартные набор настроек, свойств.`

| **Название свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  **** |  **** | **Основные свойства:** |   |
| Active | Boolean | Если значение False, объект игнорируется | true |
| Caption | String | Подпись формы | UniForm \(универсальная форма\) |
| DLL ID | Integer | Идентификационный номер DLL | 8101 |
| DLL FormName | String | Идентификатор формы в DLL \(определяет тип формы\) | FSal1p01 |
|   |   | **Дополнительные свойства:** |   |
| HideActions | Boolean | Скрывает кнопку Action на тулбаре форм | true |
| HidePrinter | Boolean | Скрывает кнопку Printer на тулбаре форм | true |
| HideTitluri | Boolean | Скрывает кнопку Titluri на тулбаре форм | true |
| RefreshOnActivate | Boolean | Обновление формы | true |
| SQL\_Refresh | Memo |  |  |
| XSQL\_Refresh | Memo  |  |  |

Главные \(идентификационные\) параметры формы: DLL ID и DLL FormName, эти параметры определяют внешний вид формы.

Форма типа DLL ID=8101, DLL FormName=FSal1p01 - это универсально настраиваемая форма. Она имеет свойства для настройки элементов управления формы \(фильтры, гриды, панели\) и их расположения, отображения и скрытия элементов управления, установки их подписей, установки значений по умолчанию для элементов управления. 

**Типы идентификатор формы \(DLL FormName\):**

**DLL ID = 8101**

[FSal1p01 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p01)- универсальная форма

[FSal1p02 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p02)- справочник сотрудников

[FSal1p03 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p03)- просто форма

[FSal1p04 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p04)- форма отображает таблицу VUN9COSTDEP

[FSal1p05 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p05)- форма содержит действие и используется для работы с таблицей VTF\_PROCURA

[FSal1p06 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p06)- дублирование/удаление артикула 

[FSal1p07 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p07)- параметры исчисления подоходного налога

[FSal1p08 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p08)- процентные ставки надбавок по выслуге лет

[FSal1p09 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p09)- учет бланков строгой отчетности

[FSal1p010 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p010)- простая форма для выполнения предопределенных действий

[FSal1p011 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p011)- импорт данных сканера штрих-кодов

[FSal1p012 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p012)- журнал производства \(по данным сканера штрих кодов\)

[FSal1p013 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p013)- учет контрактов, пакетов и услуг по клиентам

[FSal1p014 ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fsal1p014)- объединение дублирующихся позиций справочника

**DLL ID = 8000**

[fCurs ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/fcurs)- Валютные курсы

[TehComplect ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/tehcomplect)- Техническая комплектация

**DLL ID = 8200**

[salariulSECOND ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/salariulsecond)- Дополнительные начисления и удержания

**DLL ID = 0**

[SysS ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/syss)- ссылка на справочник SysS

[Univers ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/univers)- ссылка на справочник Univers

Дочерние объекты формы такие же как и у документов:

 - [Action  ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/deistviya-action)\(выполнение определенных действий с данными при работе с соответствующей формой\)

 - [Print form](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/pechatnye-formy-printforms) \(служат для настройки печатных форм\)

[Модальные формы](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/modalnye-formy) 

[UnFSal1Properties](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/unfsal1properties)

[Восстановить дизайн формы](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/formy/vosstanovit-%20%20dizain-formy) \(после обновления конфигуратора\)

