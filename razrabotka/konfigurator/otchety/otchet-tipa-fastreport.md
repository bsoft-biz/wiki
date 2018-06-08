# Отчет типа FastReport

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| :--- | :---: | :--- | :--- |
|  |  | **SQLs** |  |
| vCodLP | Integer |  | 4021 |
| vCodVed | Integer |  | 3998 |
| vSysfid | String | sysfid платежной ведомости | 50412 |
|  |  | **Общая** |  |
| Admin | Boolean | Если значение True, выводит Админ. панель в окне параметров для доступа к конструктору формы параметров |  |
| DLL ID | Integer | Идентификационный номер DLL | 9002 |
| Filt1A | String |  | 0 |
| Filt1B | String |  | CASA,CASSA |
| Filt1Tip | String | S- sysS, U- univers | U |
| Filt2A | String |  | S |
| Filt2B | String |  | 3 |
| Filt2Tip | String | S- sysS, U- univers | S |
| Report ID | String | Идентификатор печатной формы в DLL | univ |
| ReportKemel | String |  | 1 |
| ReportType | String |  | 2 |
| SingleDate | Boolean |  | false |
| Template | String | Шаблон | CashBook\_A\_val.frf |
| Tip | String | Тип отчета: Мастер - детайл или мастер | 0 |
| TipDetail | String |  | 1 |
| TipMaster | String |  | 0 |
| TitleCaption | String | Заголовок отчета | Registrul de casa |
| XLRPARAMS\_TITLE | String |  |  |
| extrep | String | Тип расширения файла шаблона \(0-xls,1-vts\) | 1 |
| filt1Caption | String | Заголовок проверки условия | Casa |
| filt1Visible | String | Отображение / скрытие проверки условия | 1 |
| filt2Caption | String | Заголовок проверки условия | Valuta |
| filt2Visible | String | Отображение / скрытие проверки условия | 1 |
| parameter1Caption | String |  | Foaia |
| parameter1Visible | String |  | 1 |
|  |  | **Типы справочников** |  |
| SQLAllinOne | Memo |  | `declare vside boolean:=true; v_val boolean:=true; begin un$vp$rep.cash_book_ot                             (:datastart,:dataend, :filt1,:filt2,vside, :parameter1, :ini_vSysfid,:sqlmaster, :sqldetail); end;` |

