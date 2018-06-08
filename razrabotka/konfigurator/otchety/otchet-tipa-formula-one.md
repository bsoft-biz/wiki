# Отчет типа Formula One

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| :--- | :---: | :--- | :--- |
|  |  | **Общая** |  |
| Admin | Boolean | Если значение True, выводит Админ. панель в окне параметров для доступа к конструктору формы параметров | false |
| DLL ID | Integer | Идентификационный номер DLL | 9002 |
| DateCaption | String | Заголовок даты |  |
| Excel | Boolean | Если не пусто, кнопка Excel нажата |  |
| Filt1A | String | Установка фильтра по полю "Тип" для записей универсального справочника | O |
| Filt1B | String | Установка фильтра по полю "Тип" для записей универсального справочника | I |
| Filt2A | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt2B | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt3A | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt3B | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt4A | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt4B | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt5A | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt5B | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt6A | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| Filt6B | String | Установка фильтра по полю "Тип" для записей универсального справочника |  |
| MacroAfterBuild | String | Макрос Visual Basic для xls-отчетов |  |
| Report ID | String | Идентификатор печатной формы в DLL | univ |
| ReportKernel | String | Ядро отчета |  |
| ReportType | String | Тип отчета | 0 |
| RseActiv | String | Если не пусто, то можно настраивать поля |  |
| SQLAllinOne | Memo | Анонимный блок на PL/SQL | `BEGIN pkg_income_reps.income_rp                                   (:SQLHeader, :SQLMaster, :datastart, :dataend); END;` |
| SingleDate | Boolean | Использование одиночной даты | false |
| TXTFixedPreview | Boolean | Автоматически выводит отчет и в текстовом формате наряду с основным \(Formula One Excel\) | false |
| TXT\_AutoCloseF1 | Boolean | Выводит отчет только в текстовом формате | true |
| TXT\_AutoCloseTXT | Boolean | Автоматически закрывает окно отчета в текстовом формате | false |
| TXT\_AutoPrint | Boolean | Автоматически запускает печать отчета в текстовом формате | false |
| TXT\_HorzSize | String | Устанавливает число строк одной страницы текстового отчета | 300 |
| TXT\_PrinterID | String | Номер принтера в списке \(0 означает "принтер по умолчанию"\) | 0 |
| TXT\_Rulon | Boolean | Использует рулон для печати текстового отчета, не разбивая отчет | true |
| TXT\_SheetNum | Integer | Номер листа рабочей книги, содержащий требуемые данные | 1 |
| TXT\_ShowBorders | String | Устанавливает режим вывода границ ячеек исходного шаблона в текстовом отчете: 0 - не отображает границы 1 - отображает все границы, за исключением точечных 2 - отображает все границы | 1 |
| TXT\_ShowGrands | Boolean | Вычисление постраничных итогов | false |
| TXT\_VertSize | String | Устанавливает число столбцов одной страницы текстового отчета | 60 |
| Template | String | Шаблон | perev\_income.vts |
| Tip | String | Тип отчета: Мастер - детайл или мастер | 0 |
| TipDetail | String | Тип отчета: Detail | 0 |
| TipMaster | String | Тип отчета: Master | 1 |
| cb1Visible | String | Отображение / скрытие проверки условия |  |
| cb1caption | String | Заголовок проверки условия |  |
| cb2caption | String | Заголовок проверки условия |  |
| cb2visible | Boolean | Отображение / скрытие проверки условия |  |
| extrep | String | Тип расширения файла шаблона \(0-xls,1-vts\) | 1 |
|  |  | **Значения** |  |
| dataendVisible | String | Отображение / скрытие конца периода |  |
| datastartVisible | String | Отображение / скрытие начала периода |  |
| filt1Visible | String | Отображение / скрытие элемента управления filt1 в окне параметров отчета | 1 |
| filt2Visible | String | Отображение / скрытие элемента управления filt2 в окне параметров отчета |  |
| filt3Visible | String | Отображение / скрытие элемента управления filt3 в окне параметров отчета |  |
| filt4Visible | String | Отображение / скрытие элемента управления filt4 в окне параметров отчета |  |
| filt5Visible | String | Отображение / скрытие элемента управления filt5 в окне параметров отчета |  |
| filt6Visible | String | Отображение / скрытие элемента управления filt6 в окне параметров отчета |  |
| parameter1Visible | String | Отображение / скрытие элемента управления parameter1 |  |
| parameter2Visible | String | Отображение / скрытие элемента управления parameter2 |  |
| parameter3Visible | String | Отображение / скрытие элемента управления parameter3 |  |
| parameter4Visible | String | Отображение / скрытие элемента управления parameter4 |  |
|  |  | **Заголовки** |  |
| Filt1Tip | String | S - sysS, U - univers | U |
| Filt2Tip | String | S - sysS, U - univers | U |
| Filt3Tip | String | S - sysS, U - univers | U |
| Filt4Tip | String | S - sysS, U - univers |  |
| Filt5Tip | String | S - sysS, U - univers |  |
| Filt6Tip | String | S - sysS, U - univers |  |
|  |  | **Видимость** |  |
| TitleCaption | String | Заголовок отчета |  |
| filt1Caption | String | Заголовок filt1 |  |
| filt2Caption | String | Заголовок filt2 |  |
| filt3Caption | String | Заголовок filt3 |  |
| filt4Caption | String | Заголовок filt4 |  |
| filt5Caption | String | Заголовок filt5 |  |
| filt6Caption | String | Заголовок filt6 |  |
| parameter1Caption | String | Заголовок parameter1 |  |
| parameter2Caption | String | Заголовок parameter2 |  |
| parameter3Caption | String | Заголовок parameter3 |  |
| parameter4Caption | String | Заголовок parameter4 |  |
|  |  | **Filters** |  |
| Filt1Text | String | Установка значений по умолчанию для элемента управления окна параметров Filt1 |  |
| Filt2Text | String | Установка значений по умолчанию для элемента управления окна параметров Filt2 |  |
| Filt3Text | String | Установка значений по умолчанию для элемента управления окна параметров Filt3 |  |
| Filt4Text | String | Установка значений по умолчанию для элемента управления окна параметров Filt4 |  |
| Filt5Text | String | Установка значений по умолчанию для элемента управления окна параметров Filt5 |  |
| Filt6Text | String | Установка значений по умолчанию для элемента управления окна параметров Filt6 |  |
| parameter1Text | String | Дополнительные параметры |  |
| parameter2Text | String | Дополнительные параметры |  |
| parameter3Text | String | Дополнительные параметры |  |
| parameter4Text | String | Дополнительные параметры |  |
|  |  | **8** |  |
| DetailSort | String | Порядок сортировки |  |
| DetailTempl | String | Порядок полей |  |
| FieldsHeader | Memo | Описание шапки | `0,an,"С",S,DataStart 0,an,"По",S,DataEnd 0,an,"Mag",S,Filt1` |
| FieldsMaster | Memo | Описание мастера | `0,an,"Дата док",S,DATA,row,"" 0,an,"№ док",S,NRDOC_MAN,row,"" 0,an,"cod Поставщик",,DTDEP,,"" 0,ref,"Поставщик",S,DENUMIREA, row,DTDEP,U,"DENUMIREA" 0,an,"Cont",,DT,,"" 0,an,"Suma",S,SUMA,data,"" 0,an,"Tip",S,TIP,column,""` |
| FieldsDetail | Memo | Описание детайла |  |
| HeaderSort | String | Порядок сортировки |  |
| HeaderTempl | String | Порядок полей |  |
| MasterSort | String | Порядок сортировки |  |
| MasterTempl | String | Порядок полей |  |
|  |  | **7** |  |
| SQLDetA | String | Только если тип дальн обр |  |
| SQLDetB | String | Только если тип дальн обр |  |
| SQLDetail | Memo | Запрос, возвращающий данные в область Detail \(область данных подчиненной таблицы\) отчета | 1 |
| SQLHeader | Memo | Запрос, возвращающий данные в область Header \(область заголовка\) отчета | 1 |
| SQLMastA | String | Только если тип дальн обр |  |
| SQLMastB | String | Только если тип дальн обр |  |
| SQLMaster | Memo | Запрос, возвращающий данные в область Master \(область данных главной таблицы\) отчета | 1 |

