# Формы

Формы служат для работы пользователя с данными, представляющими специализированную справочную информацию, используемую при работе с системой \(прайс-листы, регистры курсов валют, регистры норм затрат и др.\), либо сугубо для выполнения определенных действий по обработке данных.

Конфигурирование типовой формы включает настройки интерфейсной части и части обработки данных – действия. Объекты действия аналогичны объектам doc-action. Свойства этих объектов позволяют определять процедуры обработки данных.

Схема разработки новых форм аналогична созданию новых документов и отчетов и включает программную разработку, включение в список форм нового объекта типа форма, связывание этого объекта с программной реализацией посредством указания программных идентификаторов \(идентификатор bpl, идентификатор отчета в bpl\) и, возможно, определение для формы общих и специализированных настроек.

Доступные формы отображаются в меню Forme приложения Universal Accounting.

Объекты типа Формы определяет стандартные набор настроек, свойств.

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

[FSal1p01](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A3%D0%BD%D0%B8%D0%B2%D0%B5%D1%80%D1%81%D0%B0%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F+%D1%84%D0%BE%D1%80%D0%BC%D0%B0+%28FSal1p01%29) - универсальная форма

[FSal1p02](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A1%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA+%D1%81%D0%BE%D1%82%D1%80%D1%83%D0%B4%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2+%28FSal1p02%29) - справочник сотрудников

[FSal1p03](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D1%80%D0%BE%D1%81%D1%82%D0%BE+%D1%84%D0%BE%D1%80%D0%BC%D0%B0+%28FSal1p03%29) - просто форма

[FSal1p04](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/FSal1p04) - форма отображает таблицу VUN9COSTDEP

[FSal1p05](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A4%D0%BE%D1%80%D0%BC%D0%B0+%28FSal1p05%29) - форма содержит действие и используется для работы с таблицей VTF\_PROCURA

[FSal1p06](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A4%D0%BE%D1%80%D0%BC%D0%B0+FSal1p06) - дублирование/удаление артикула 

[FSal1p07](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D0%B0%D1%80%D0%B0%D0%BC%D0%B5%D1%82%D1%80%D1%8B+%D0%B8%D1%81%D1%87%D0%B8%D1%81%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%BF%D0%BE%D0%B4%D0%BE%D1%85%D0%BE%D0%B4%D0%BD%D0%BE%D0%B3%D0%BE+%D0%BD%D0%B0%D0%BB%D0%BE%D0%B3%D0%B0+%28FSal1p07%29) - параметры исчисления подоходного налога

[FSal1p08](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D1%80%D0%BE%D1%86%D0%B5%D0%BD%D1%82%D0%BD%D1%8B%D0%B5+%D1%81%D1%82%D0%B0%D0%B2%D0%BA%D0%B8+%D0%BD%D0%B0%D0%B4%D0%B1%D0%B0%D0%B2%D0%BE%D0%BA+%D0%BF%D0%BE+%D0%B2%D1%8B%D1%81%D0%BB%D1%83%D0%B3%D0%B5+%D0%BB%D0%B5%D1%82+%28FSal1p08%29) - процентные ставки надбавок по выслуге лет

[FSal1p09](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A3%D1%87%D0%B5%D1%82+%D0%B1%D0%BB%D0%B0%D0%BD%D0%BA%D0%BE%D0%B2+%D1%81%D1%82%D1%80%D0%BE%D0%B3%D0%BE%D0%B9+%D0%BE%D1%82%D1%87%D0%B5%D1%82%D0%BD%D0%BE%D1%81%D1%82%D0%B8+%28FSal1p09%29) - учет бланков строгой отчетности

[FSal1p010](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D1%80%D0%BE%D1%81%D1%82%D0%B0%D1%8F+%D1%84%D0%BE%D1%80%D0%BC%D0%B0+%D0%B4%D0%BB%D1%8F+%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F+%D0%BF%D1%80%D0%B5%D0%B4%D0%BE%D0%BF%D1%80%D0%B5%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D1%85+%D0%B4%D0%B5%D0%B9%D1%81%D1%82%D0%B2%D0%B8%D0%B9+%28FSal1p010%29) - простая форма для выполнения предопределенных действий

[FSal1p011](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%98%D0%BC%D0%BF%D0%BE%D1%80%D1%82+%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85+%D1%81%D0%BA%D0%B0%D0%BD%D0%B5%D1%80%D0%B0+%D1%88%D1%82%D1%80%D0%B8%D1%85-%D0%BA%D0%BE%D0%B4%D0%BE%D0%B2+%28FSal1p011%29) - импорт данных сканера штрих-кодов

[FSal1p012](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%96%D1%83%D1%80%D0%BD%D0%B0%D0%BB+%D0%BF%D1%80%D0%BE%D0%B8%D0%B7%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%B0+%28%D0%BF%D0%BE+%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC+%D1%81%D0%BA%D0%B0%D0%BD%D0%B5%D1%80%D0%B0+%D1%88%D1%82%D1%80%D0%B8%D1%85+%D0%BA%D0%BE%D0%B4%D0%BE%D0%B2%29+%28FSal1p012%29) - журнал производства \(по данным сканера штрих кодов\)

[FSal1p013](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D1%80%D0%BE%D1%81%D1%82%D0%BE+%D1%84%D0%BE%D1%80%D0%BC%D0%B0+%28FSal1p03%29) - учет контрактов, пакетов и услуг по клиентам

[FSal1p014](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9E%D0%B1%D1%8A%D0%B5%D0%B4%D0%B8%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5+%D0%B4%D1%83%D0%B1%D0%BB%D0%B8%D1%80%D1%83%D1%8E%D1%89%D0%B8%D1%85%D1%81%D1%8F+%D0%BF%D0%BE%D0%B7%D0%B8%D1%86%D0%B8%D0%B9+%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA%D0%B0+%28FSal1p014%29) - объединение дублирующихся позиций справочника

**DLL ID = 8000**

[fCurs](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%92%D0%B0%D0%BB%D1%8E%D1%82%D0%BD%D1%8B%D0%B5+%D0%BA%D1%83%D1%80%D1%82%D1%8B+%28fCurs%29) - Валютные курсы

[TehComplect](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A2%D0%B5%D1%85%D0%BD%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F+%D0%BA%D0%BE%D0%BC%D0%BF%D0%BB%D0%B5%D0%BA%D1%82%D0%B0%D1%86%D0%B8%D1%8F) - Техническая комплектация

**DLL ID = 8200**

[salariulSECOND](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%94%D0%BE%D0%BF%D0%BE%D0%BB%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5+%D0%BD%D0%B0%D1%87%D0%B8%D1%81%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F) - Дополнительные начисления и удержания

**DLL ID = 0**

[SysS](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA+SysS) - ссылка на справочник SysS

[Univers](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BE%D1%87%D0%BD%D0%B8%D0%BA+Univers) - ссылка на справочник Univers

Дочерние объекты формы такие же как и у документов:

 - [Action](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%94%D0%B5%D0%B9%D1%81%D1%82%D0%B2%D0%B8%D1%8F+%28action%29)  \(выполнение определенных действий с данными при работе с соответствующей формой\)

 - [Print form](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D0%B5%D1%87%D0%B0%D1%82%D0%BD%D1%8B%D0%B5+%D1%84%D0%BE%D1%80%D0%BC%D1%8B+%28PrintForms%29) \(служат для настройки печатных форм\)

[Модальные формы](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9C%D0%BE%D0%B4%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5+%D1%84%D0%BE%D1%80%D0%BC%D1%8B) 

[UnFSal1Properties](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/UnFSal1Properties)

[Восстановить дизайн формы](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%92%D0%BE%D1%81%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%82%D1%8C+%D0%B4%D0%B8%D0%B7%D0%B0%D0%B9%D0%BD+%D1%84%D0%BE%D1%80%D0%BC%D1%8B) \(после обновления конфигуратора\)

