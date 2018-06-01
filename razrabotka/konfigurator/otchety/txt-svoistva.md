# TXT-свойства

**TXT-свойства.** 

Это свойства отчета в текстовом формате. Свойства поддерживаются всеми отчетами.

Настройка режима конвертации в текст заключается в создании набора параметров в секции отчета. Эти параметры приведены в следующей таблице:



| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|   |   | **Главный параметр, управляющий всеми остальными:** |   |
| TXTFixedPreview | Boolean | Этот параметр определяет, будет ли отчет или печатная форма конвертироваться в текстовый формат. Он позволяет временно выключить уже настроенный режим конвертации для построения отчета в исходном виде \(FormulaOne\) | false |
|   |   |  **Параметры, управляющие размером и видом печатной страницы:** |   |
| TXT\_VertSize | Integer | Этот параметр определяет количество строк, максимально помещаемых на одной странице.  При наличии явных разделителей страниц количество строк на некоторых страницах может быть меньше, но никак не больше указанного значения данного параметра. Количество выводимых строк данных зависит также от параметров TXT\_ShowGrands и TXT\_ShowBorders. Теряет свой смысл при включении параметра TXT\_Rulon | 60 |
| TXT\_HorzSize | Integer | Этот параметр определяет количество столбцов, максимально помещаемых на одной странице. Непомещающиеся остатки длинных строк будут сконвертированы в дополнительные страницы, визуально примыкающие справа к основным страницам | 300 |
| TXT\_Rulon | Boolean | Этот параметр включает режим непрерывного вывода строк без разделителей страниц и постраничных итогов. | false |
| TXT\_ShowGrands | Boolean | Этот параметр включает режим вывода постраничных итогов. Уменьшает количество строк данных, помещающихся на одной странице. Имеет смысл только при выключенном параметре TXT\_Rulon | false |
| TXT\_ShowBorders | Integer | Этот параметр управляет отображением линий границ ячеек. Уменьшает количество строк данных,помещающихся на одной странице. Допустимы три значения:0. "Никакие" - линии границ ячеек игнорируются \(не конвертируются\) 1. "Все, кроме точек" - конвертируются только сплошные линии 2. "Все" - конвертируются все линии границ ячеек | 1 |
|   |   | **Параметры, управляющие автоматизацией процесса конвертации:** |   |
| TXT\_AutoPrint | Boolean | Этот параметр включает режим автоматической отправки сконвертированного отчета на печать.  Для указания номера конкретного принтера используется параметр TXT\_PrinterID | false |
| TXT\_PrinterID | Integer | Этот параметр задает номер принтера в списке инсталлированных в системе принтеров.  Значение "0" означает "Принтер по умолчанию". Используется при включенном параметре TXT\_AutoPrint | 0 |
| TXT\_AutoCloseTXT | Boolean | Этот параметр автоматически закрывает окно сконвертированного отчета. Используется при включенном параметре TXT\_AutoPrint | false |
| TXT\_AutoCloseF1 | Boolean | Этот параметр автоматически закрывает окно исходного отчета \(F1Reports\).  Обычно используется для отладки текстовых отчетов, значение "false" позволяет видеть исходный отчет, который был сконвертирован в тестовый формат  | true |
|   |   |  **Параметры, управляющие источником и получателем данных:** |   |
| TXT\_SheetNum | Integer | Этот параметр позволяет указать номер листа рабочей книги, который нужно сконвертировать в текстовый формат | 1 |
| TXT\_group\_print | Boolean | Этот параметр включает режим добавления сконвертированного отчета в ранее построенный текстовый отчет. Используется для печати нескольких печатных форм в одним текстовый блок | false |
| TXT\_all\_sheets | Boolean | Этот параметр включает режим конвертации в текстовый формат всех листов исходной рабочей книги в один текстовый блок | false |
