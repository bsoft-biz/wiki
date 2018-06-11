# Docs

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| :--- | :---: | :--- | :--- |
| Backup | Boolean | Архив документов. Режим сохранения документов в архиве перед их удалением. | true \([настройка архивирования](https://bsoft.gitbook.io/wiki/administrirovanie/arkhivirovanie-backup-udalennykh-dokumentov)\) |
| CancelSilent | Boolean | При Anulare в документе не будет задаваться  вопрос "А вы уверены…?" | `true` |
| ColorDisabledDocs | Integer | Цвет неактивных \(дезактивированных\) документов. |  |
| CopyDocDateSilent | Boolean | При дублировании документа не  будет появляться окошко для выбора  даты нового документа и т.п. | `true` |
| DOCR\_Check! | Boolean |  | `true` |
| DOCR\_Message | Boolean |  | `true` |
| DataAutomat | Boolean | При создании документа в докс попадает  последняя использованная дата. | `true` |
| DataCurrent | Boolean | При создании документа в докс  попадает sysdate  \(использовать `sys_context('ENVUN4','UN$DATACURENT')`\) | `true` |
| DEF\_JOURNAL | String | Стартовый журнал. Имя секции журнала, который надо открывать сразу после запуска программы. |  |
| DefValuta | String | Значение поля VALUTA по умолчанию | LEI |
| DefaultModule | String | Значение поля TIP по умолчанию | M |
| DocsUseToolbarBottom | Boolean |  | `true` |
| FilterInit | Memo |  | `begin -- фиксированная дата --:datastart:='01.01.2006'; --наименьшее из "с начала открытого периода"                                                                                              и "полгода назад от системной даты" --:datastart:=least(to_date (sys_context                   ('envun4', 'UN$DATASTART')),                    add_months    (trunc(sysdate,'MM'),-6)); -- --наименьшее из                                    "с начала текущего      года" и    "полгода назад от системной даты" -- :datastart:=least (trunc(sysdate,'YYYY'), add_months( trunc(sysdate,'MM'),-3)); -- ТРИ МЕСЯЦА НАЗАД :datastart:=add_months (trunc(sysdate,'MM'),-4); end;` |
| FormsUseToolbarBottom | Boolean |  | `true` |
| LastRecord | Boolean | К последнему документу. При открытии журнала документов переходить на последний видимый  документ. | `true` |
| NodeType | String |  | Docs |
| ORDER BY | String | Порядок сортировки. Порядок сортировки документов \(список имен полей, разделенных запятыми\). | COD ASC |
| PXCompatibile | Boolean | Документы из версии PX. Режим использования документов версии PX. | `true` |
| PXCMSimpleEditing | Boolean | Режим быстрой правки проводок документов версии PX. | `true` |
| ShowDocsPanel | Boolean | Включает узкую полоску в верхней части панели  спецрегистра, которая является настраиваемой  панелью для доступа к Docs | `true` |
| ShowFacturaEnabled | Boolean | Отменяет глобальное свойство "HideDocsFact"  \(которое, в свою очередь прячет кнопку "F"  в документе/ах\) | `true` |
| SQLBeforeEdit | Memo | \(старый вариант BeforeEdit\) SQL, который  выполняется при входе в документ |  |
| ViewFromToday | Integer | Ограничение периода. Ограничение периода отображаемых документов  как смещение на указанное  число дней назад от текущей даты. |  |
| ViewBegin | String | Ограничение снизу. Минимальная дата отображаемых документов |  |
| ViewEnd | String | Ограничение сверху. Максимальная дата отображаемых документов |  |

