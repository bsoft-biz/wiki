# Документы

Объекты Документы содержат настройки типов документов, с которыми работает приложение Universal Accounting.

Иерархия дерева документов текущей записи настроек – это логическая организация списка документов по их назначению. Число уровней вложенности узлов, служащих для логической группировки объектов, не ограничено.

Обычно верхний уровень дерева служит для группировки документов по модулям.

Свойства документов в конфигураторе:

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|   |   | **Standart:** |  |
| `DB ID` | Integer | Идентификационный номер типа документа. Соответствует значению поля \[SysfID\] в таблице документов | 1400 |
| `DLL ID` | Integer | Идентификационный номер DLL | 4000 |
| `DocName` | String | Идентификатор документа в DLL | DG1p21 |
| `Module` | String | Модуль, которому принадлежит документ. Соответствует значению поля \[m\] в таблице документов | M |
| `Use in DB` | Boolean | Если значение True, тип документа доступен в клиентском приложении | true |
|   |   |  **Интерфейс:** |  |
| `UseToolbar` | Boolean | Если значение True, то появляется панель с кнопками\(для печатных форм и действий\) | true |
| `UseToolBarBottom` | Boolean | Если значение True, то панель будет расположена внизу документа \(под вкладками Документ, Проводки, Информация\) | true |
| `HideOleBar` | Boolean | Скрывает стандартную панель инструментов на  вкладке объект и включает новые кнопки | true |
| `ViewFilesObjects` | Boolean | Убирает панель просмотра внизу, увеличивает значки файлов. При открытии - просмотр файлов. | true |
|   |   |  **Прочее:** |  |
| `EAutoGFCOrder` | String | Перечислить id экшенов, которые будут выбраны автоматически \(галочка на экшене по умолчанию\) | 1 |
| `EAutoGFCRun` | Boolean | Если значение True, запускается автоматическая генерация проводок при сохранении документа | true |
| `EOnlyPrivatePrintForms` | Boolean | Если значение True, документ использует только свои печатные формы | true |
| `EAutoPrintSave` | Boolean | \(скорее всего\) после построения печатной формы из документа произойдет выход из документа с сохранением | true |
| `EAutoGFCInsert` | String | Action, который нужно выполнить  при создании документа | 5 |
|   |   |  **Документ на основании \(дочерний документ\):** |  |
| `ChildDocs` | String | В конфигураторе на документ, из которого будем создавать дочерний, ставим свойство ChildDocs="сисфид или сисфиды через запятую", где "сисфид или сисфиды через запятую" - это sysfid/ы документа/ов, который/е будет/ут создаваться при нажатии на кнопку "На основании" | ChildDocs=48341 или ChildDocs=48341,48342\) |
| `ChildCancelOnError` | Boolean | Тогда, если в процессе создания дочернего документа возникнет ошибка, то он не создастся | true |
| `CreateChildSilent` | Boolean | При нажатии на кнопку не будет появляться вопрос типа "вы уверены, что хотите создать дочерний?.."Таким образом, при нажатии кнопки «На основании» происходит следующее:-создается новый документ-в tmdb\_docs\_add  в поле parent\_cod попадает номер родительского документа-далее может выполниться некий Action, в котором мы можем произвести, например, заполнение нового документа\(для этого в дочернем документе делается Action, на который ставится свойство UseByCreateChild=true\), | true |
| `UseByCreateChild` | Boolean | тогда при создании дочернего этот Action будет выполняться | true |
|   |  |  xBarCode - добавляет окно для сканирования и кнопку  \(F12\).  | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%97%D0%BD%D0%B0%D1%87%D0%B5%D0%BA%20%D1%88%D1%82%D1%80%D0%B8%D1%85-%D0%BA%D0%BE%D0%B4%D0%B0.png?raw=true) |
| `xBarCodeAutoPost` | Boolean |  | true |
| `xBarCodePrefix` | String |  |  |
| `xBarCodeQuery` | Memo |  | SELECT cod marfa, 1 cant, :barcode barcode  FROM vms\_mpt\_barcode  WHERE BARCODE =:BARCODE |

Базовый тип документа идентифицируется значениями свойств DLL ID и DocName:

[Свойства документа 201](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/svoistva-dokumenta-201) \(универсальный документ с одной таблицей и областью "шапки"\)

[Свойства документа DG1p21](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/svoistva-dokumenta-dg1p21) \(универсальный документ с тремя таблицами и областью "шапки"\)

[Свойства документов CST1 и CST2](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/svoistva-dokumentov-cst1-i-cst2) \(универсальный документ с двумя таблицами / двумя таблицами и областью "шапки"\)

У узла **Документы** могут быть подузлы:

[Действия \(action\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/deistviya-action)

[Печатные формы \(PrintForms\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/pechatnye-formy-printforms)

[Объекты типа Totals](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/obekty-tipa-totals)

[Окно остатков \(201\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/okno-ostatkov)

[Настройка документа](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/nastroika-dokumenta)

[Основные средства 5104: Ввод в эксплуатацию](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/osnovnye-sredstva-5104-vvod-v-ekspluataciyu)

[Абстрактный документ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/dokumenty/abstraktnyi-dokument)

