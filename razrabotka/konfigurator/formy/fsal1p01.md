# FSal1p01

| **Название свойства** | **Тип** | **Описание**  | **Значение для примера**  |
| :------------- |:-------------:| :-----| :-----|
| UseDropInsertDocument | Boolean | На форму можно перетащить и бросить файл и будет предложено создать документ | true |
| SQL\_DOC\_FILTER | Memo | Используется если UseDropInsertDocument = true. Указывается sql фильтр сисфидов | true |
| Active | Boolean | Если значение False, объект игнорируется | true |
| Caption | String | Подпись для действия в списке действий | UniForm \(универсальная форма\) |
| DLL FormName | String | Идентификатор формы в DLL | FSal1p01 |
| DLL ID | Integer | Идентификационный номер DLL | 8101 |
| DateCaption1 | String | Подпись для даты начала \(DATAB caption\) | Дата начала  |
| DateCaption2 | String | Подпись для даты DATAF caption | Дата окончания |
| DateCount | Integer | Количество фильтров по дате\(0..2\) \(dates in header\) | 0 |
| DateOffset1 | Integer | смещение даты начала на N дней \(DATAB offset\) | 0 |
| DateOffset2 | Integer | смещение даты начала на N дней \(DATAF offset\) | 0 |
| DatePrefix | String | это имя \(например V\_\) необходимо для последующего обращения к датам: sys\_context\('ENVUN4','V\_DATAB'\) sys\_context\('ENVUN4','V\_DATAF'\)не только префикс даты, но и для SC и Dep | V\_ |
| SingleDate | Boolean | Если нужна одна дата, а не период | true |
| DesignFieldDetail | String | Master Field |  |
| DesignFieldDetail2 | String | Master Field |  |
| DesignFieldTab2Detail | String | Master Field |  |
| DesignFieldTab2Detail2 | String | Master Field |  |
| DesignFieldTab3Detail | String | Master Field |  |
| DesignFieldTab3Detail2 | String | Master Field |  |
| FilterDepCaption | String | подпись фильтра Dep в шапке \(в форме обращаться :dep\) |  |
| FilterDepVisible | Boolean | отображать фильтр в шапке | false |
| FilterSc1Caption | String | подпись фильтра Sc1 в шапке |  |
| FilterSc1Visible | Boolean | отображать фильтр в шапке | false |
| FilterScCaption | String | подпись фильтра Sc в шапке |  |
| FilterScVisible | Boolean | отображать фильтр в шапке | false |
| FormNoGrid | Boolean | параметр установленный в true, означает работу без таблиц.  0 grids \(yellow panel\) | false |
| FormUseDetail | Boolean | параметр установленный в true, означает работу с двумя  таблицами, причем основная  таблица становится Master-таблицей. \(2 grids\) \(использование подчиненного грида\) | false |
| FormUseDetail2 | Boolean | 3 grids \(1&lt;-2; 1&lt;-3\) | false |
| FormUseSubDetail | Boolean | 3 grids \(1&lt;-2&lt;-3\) | false |
| FormUseTab2Detail | Boolean | 2 grids | false |
| FormUseTab2Detail2 | Boolean | 3 grids \(1&lt;-2; 1&lt;-3\) | false |
| FormUseTab2SubDetail | Boolean | 3 grids \(1&lt;-2&lt;-3\) | false |
| FormUseTab3Detail | Boolean | 2 grids | false |
| FormUseTab3Detail2 | Boolean | 3 grids \(1&lt;-2; 1&lt;-3\) | false |
| FormUseTab3SubDetail | Boolean | 3 grids \(1&lt;-2&lt;-3\) | false |
| MasterSize | Integer | визуальный размер Master-таблицы \(&lt;0 means vertical\). Положительное значение параметра  MasterSize означает высоту Master-таблицы, при этом Detail-таблица будет расположена в  нижней части формы. Отрицательное значение параметра   MasterSize означает ширину Master-таблицы,  при этом Detail-таблица будет расположена в правой части формы. | 201 |
| MasterSize2 | Integer | высота мастера в форме \(&lt;0 means vertical\) | 161 |
| MasterSizeTab2 | Integer | высота мастера в форме \(&lt;0 means vertical\) | 161 |
| MasterSizeTab3 | Integer | высота мастера в форме \(&lt;0 means vertical\) | 161 |
| PanelAllowExit | Boolean |  Отключает необходимость обязательно нажимать "галку"\(подтвердить\) или "крестик"\(отменить\)  после редактирования значений в форме. Все внесённые изменения будут сохранены. |  true |
| PanelHeightMaster | Integer | Включение дополнительной панели элементов \(PanelHeightMaster = -100 панель будет справа\) \(если 1 грид\) \(PanelHeightMaster=+ панель и подчиненный грид\) | 100 |
| PanelHeightTab1 | Integer \(String\) | Если на форме FormUseDetail=true \(2 грида\) , то доп. панель включается свойством PanelHeightTab1   \(PanelHeightTab1=+   доп. грид полностью панель\) |   |
| PanelHeightTab1D | Integer |  |  |
| PanelHeightTab2 | Integer |  |  |
| PanelHeightTab2D | Integer |  |  |
| PanelHeightTab3 | Integer |  |  |
| PanelHeightTab3D | Integer |  |  |
| PeriodVisible | Boolean | Период дат \(DataStart-DataEnd\) | false |
| QueryMTransAuto | Boolean | Отключение автономных транзакций. По умолчанию в формах автономные транзакции включены.  | false  |
| QueryTab1aTransAuto | Boolean |  |  |
| QueryTab1bTransAuto | Boolean |  |  |
| QueryTab2aTransAuto | Boolean |  |  |
| QueryTab2bTransAuto | Boolean |  |  |
| QueryTab3aTransAuto | Boolean |  |  |
| QueryTab3bTransAuto | Boolean |  |  |
| SplitterMasterVisible | Boolean |  |  |
| SplitterTab1Visible | Boolean |  |  |
| SplitterTab2Visible | Boolean |  |  |
| SplitterTab3Visible | Boolean |  |  |
| RefreshRestorePos | Boolean |  Восстановить позицию курсора после выполнения экшена. |  true |
| Tab1Caption | String | Заголовок дополнительной вкладки \(число в имени свойства - номер вкладки\) |  |
| Tab2Caption | String | Заголовок дополнительной вкладки \(число в имени свойства - номер вкладки\) |   |
| Tab3Caption | String | Заголовок дополнительной вкладки \(число в имени свойства - номер вкладки\) |   |
| UseMaster | Boolean | Использование мастера | true |
| UseMasterDelay | Boolean |  |  |
| UseToolbar | Boolean | Включение Toolbar\(панель инструментов\)над гридом | true |
| HeaderPanel | Boolean | Включение шапки | true |
|   |   | **Автообновление формы\(время указывается в сек.\) - работает в комбинации трех свойств  \(RefreshPanelVisible, RefreshTimerEnabled, RefreshTimerInterval\)** |   |
| RefreshPanelVisible | Boolean | Включение  панели автообновления  | true |
| RefreshTimerEnabled | Boolean | Включение обновления | true |
| RefreshTimerInterval | Integer | Время обновления , через сколько обновить указывается в секундах. | 5 |

