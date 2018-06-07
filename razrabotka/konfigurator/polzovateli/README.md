# Пользователи

**Права пользователей**

В программе существует несколько групп пользователей с разными правами доступа, которые можно редактировать. В зависимости от того, в какой группе находится пользователь, тем набором прав он и обладает. Данную функцию выполняет системный администратор либо программист, заранее согласовав список групп пользователей и права доступа с администрацией компании-клиента. 

Администратор в программе имеет доступ ко всем разделам, может изменять настройки программы и так далее. Он может также создавать новых пользователей, назначать права доступа, изменять их свойства и удалять ненужных пользователей. 

В представленной ниже таблице описаны свойства, необходимые для создания пользователей. Таблица свойства разделена на  две части, обязательные являются важными для создания учетной записи пользователя.

| **Название свойства** | **Тип** | **Описание**  | **Значение для примера**  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|   |   | **Обязательные свойства:** |   |
| `Enabled` | `Boolean` | Значение true говорит о том, что учетная запись пользователя активна.  \(Если `True`, настройки пользователя видимы для приложения Universal Accounting, если `False` – объект игнорируется\) | `true` |
| `ID` | `Integer` | Идентификационный номер пользователя \(соответствует значению поля \[`UserID`\]  таблицы документов для записей документов пользователя\) | `1001` |
| `UserName` | `String` | Логин пользователя.  \(Имя пользователя. Вводится в поле `UserID` при запуске приложения Universal Accounting\) | `petrov` |
| `Encoded` | `Integer` | \(Авто\) Закодированный пароль пользователя. |   |
| `PassDate` | `Date` | \(Авто\) После определения пароля автоматически проставляется дата.  |   |
|   |   |  **Дополнительные свойства:** |   |
| `Admin`  | `String`  | Если значение=1, то пользователь обладает правами администратора.   | `1` |
| `AllowGridDesign`  | `Boolean`  | Разрешить изменение дизайнов \(применяется для пользователей, у которых нет прав администратора, но которым нужно разрешить изменение дизайнов\).  | `true`  |
| `AutoFreeMemory`   | `Boolean`  | Выгружать неисп. `DLL`. Выгружать из памяти неиспользуемые динамические библиотеки \(`DLL` и `BPL`\).   | `true`   |
| `Familia Numele Prenumele`  | `String`  | Фамилия, имя, отчество пользователя.  \(информативное поле\)  | `Петров Иван Сергеевич`  |
| `ConfirmExit`  | `Boolean` |   | `false`  |
| `InitSQL`  | `Memo`  | Права, прописанные программно в коде программы.  | `begin:res:=2; envun4.EnvSetValue                                  ('restricted_syss_tip','tip in (''R'')                                                                    and cod in (502,18,61)'); envun4.            EnvSetValue('restricted_syss_tip', 'tip in (''S'') and cod in (14)');end;` |
| `LACSetupBlockSections`  | `String`  | Список всех журналов, справочников, находящихся на верхней функциональной панели.  Используется для облегченного интерфейса. Список объектов Формы \(имена соответствующих узлов\), не доступных группе пользователей. \(Список секций форм и справочников, которые пользователю видеть запрещено\).   | `J_MATERIAL ,J_CONFIRMARE, J_CLASIFICATOARE,                                                        F_CLASIFICATOARE, J_RAPOARTE,F_FORME, cl_tms_order_inf_supliment,                                                  J_CONFIRMARF` |
| `LACSetupBlockSections_old` | `String`  |   | `0:0:ActeOrdere,0:1:ActeOrdere,                             f_ruta_agent,f_ruta_client`  |
| `PeriodStart`  | `String`  | Период, с которого пользователь имеет право видеть документы. Частная дата начала периода редактирования документов. Допускается `SQL`-выражение. Если значение параметра отсутствует, вместо него используется значение параметра `GlobalPeriodStart`. | `01.01.2012`  |
| `PeriodEnd`  | `String`   | Частная дата окончания периода редактирования документов. Допускается `SQL`-выражение. Если значение параметра отсутствует, вместо него используется значение параметра `GlobalPeriodEnd`  |  `01.12.2012` |
| `PeriodFinish`  | `String`  | Период окончания, с которого пользователь не имеет право видеть документы.  | `01.12.2012`  |
| `PassAttempts`  | `Integer`  |  Количество попыток ввода неправильного пароля | `5` |
| `LACReportsSelectedOnly`  | `Boolean`  | Интерпретировать параметр  `LacSetupBlockReports` как список разрешенных секций. | `true` |
| `LACSetupBlockReports`  | `String`   | Список секций отчетов, которые пользователю видеть запрещено. | `R_MATERIAL` |
| `LACSetupBlockObjects`  | `String`  | Список объектов, с которыми пользователю работать запрещено.  | `NRSET`  |
| `LACSectionsSelectedOnly`  | `Boolean`   | Интерпретировать параметр `LacSetupBlockSections`  как список разрешенных секций.   | `true` |
| `LACObjectsSelectedOnly`  | `Boolean`  | Интерпретировать параметр `LACSetupBlockObjects` как список разрешенных секций.  | `true`  |
| `Language`  | `String`  | Язык интерфейса.  Значения:  0-англ.яз.  1-рум.яз.  2-русский  По умолчанию стоит 1-рум.яз.   | `2`  |
| `DataEmpty`  | `Boolean`  | Если `True`, игнорируется значение по умолчанию поля \[`Дата`\] таблицы документов при вводе документов пользователем  | `false` |
| `DesignGroup`  | `Integer`  | Номер группы дизайнов \(ненулевое значение позволяет пользователю иметь персональные дизайны, переводы, схемы отчетов и т.п.\). Администратор может менять себе этот номер во время выполнения программы \(через интерфейс меню\).  |   |
| `Password`  | `String`  | Пароль пользователя. Вводится в поле Password при запуске приложения Universal Accounting  |   |
| `seqNRMANDisableChanges`  | `Boolean` | Запретить пользователю изменять поле `NRMANUAL`.  | `true` |
| `DEF_JOURNAL`  | `String`  | Журнал \(фильтр на документы\), устанавливаемый по умолчанию при запуске приложения Universal Accounting  | `J_BANK`  |
| `Docs View Mode`  | `String`  | 0- All documents – пользователям доступны все документы 1- All group documents – пользователям доступны только документы пользователей группы 2- Private documents – пользователям доступны только личные документы  | `2`  |
| `Docs edit mode`  | `Integer` | 0 - All documents - все документы   1 - All group documents - документы группы  2 -Private documents-документы пользователя \(только свои\)  Если выбран режим 1 - документы группы, то необходимо на группе создать свойство - `UserGroupList`  | `2`  |
| `DivVisible`  | `Boolean`  |   | `false`  |
| `GridPropCacheLimit`   | `Integer`   | Размер кеша дизайнов. Максимальный размер кеша дизайнов в памяти. За единицу берется один тип  документа, один узел дерева отчетов, одна форма или справочник.  | `100` |
| `GridDisableNumberSearch`   | `Boolean`   | Запрет числового поиска. Режим текстового поиска даже в числовых полях грида \(вместо числового поиска\).  | `true` |
| `RepairGridDesign`   | `Boolean`   | Исправление ошибок. Режим автокоррекции загружаемых дизайнов \(бывает нужен при работе с ORACLE 9i\).   | `true`  |
| `RepDataStart`  | `String`  | Дата начала периода просмотра данных в отчетах. Допускается `SQL`-выражение. Если значение параметра отсутствует, вместо него используется значение параметра `PeriodStart`. |   |
| `RepDataEnd`  | `String`  | Дата окончания периода просмотра данных в отчетах. Допускается `SQL`-выражение. Если значение параметра отсутствует, вместо него используется значение параметра `PeriodEnd`.  |   |
| `ReportTreeSorting`   | `Boolean`   | Сортировка узлов. Режим сортировки узлов дерева отчетов по алфавиту.   | `true` |
| `StartupReportNode`   | `String`   | Стартовый узел. Имя секции отчета, на котором позиционировать дерево отчетов сразу после открытия  окна менеджера отчетов.  |   |
| `RepTestRecordCount`  | `Boolean`   | Проверять к-во записей. Режим проверки количества записей в наборе данных отчета \(для `F1Reports`\):   при очень большом количестве записей выдается предупреждающее сообщение, имеется возможность  отменить построение отчета или вручную ограничить количество выводимых записей.  Предельное количество записей для отчетов `Master/Detail` - 1000, только `Master` - 10000.  | `true` |
| `RepDeleteTempTables`   | `Boolean`   | Удалять врем. таблицы. Режим удаления временных таблиц `ORACLE` после построения отчета \(можно выключить\).   | `true`     |
| `LangDontLoad`   | `Boolean`   | Не загружать переводы. Не пытаться загружать тексты переводов из `ORACLE` \(для уменьшения  траффика\).  | `true` |
| `LoadCaptionsSep`   | `Boolean`   | Заголовки отдельно. Режим раздельной загрузки переводов заголовков столбцов и дизайнов  \(для совместимости с переводами заголовков столбцов, сохраненными в предыдущих версиях `SL`\).  | true  |
| `UserGroupList`  | `String`  | Список кодов пользователей \(через запятую\), составляющих группу, используемую в параметрах `Docs View Mode` и `Docs edit mode`. Этот параметр удобно заводить на уровне секции группы пользователей.В таком случае пользователи будут видеть документы пользователей, входящих в группу.  | `1,2,3,4,7,15`  |
| `UseDotInCont`   | `Boolean`   | Точка в счете. Использовать точку в значении счета \(формат 99.99\) - удобно для ПМР.  | `true`   |
| `UseSmartTab`   | `Boolean`   | "Умный" &lt;Tab&gt;. Режим интеллектуального поведения клавиши &lt;Tab&gt;: переход от поля к полю по всему  активному окну.  | `true` |
| `UseSpeedSearch`   | `Boolean`  | Быстрый поиск в справ.. Режим быстрого поиска в выпадающих справочниках.   | `true`   |
| `UseSmartEnter`   | `Boolean`   | "Умный" &lt;Enter&gt;. Режим интеллектуального поведения клавиши &lt;Enter&gt; на дополнительной \(цифровой\)  клавиатуре:  при редактировании таблиц - переход к следующему полю или \(из последнего столбца\)  завершение редактирования и вставка новой записи.  | `true` |
| `UseSmartEnterNotebook` | `Boolean` |   | `true`  |
| `UnivListReadOnly` | `Boolean` |   | `false` |
| SmartEnterLikeTab  | Boolean |   | `true`  |
| `USER_SC`  | `Integer`  | Код пользователя из универс. Чтобы получить этот код в клиенте  \(добавляем приставку `param_`\)`:sys_context('envun4', 'param_user_sc')`  | `25820`  |
| `UseCMX`  | `Boolean` |   | `false`  |
| `PassUnique`  | `Boolean` | Пользователю/ям можно повторять пароль   | `false` |
| `ToolBarFormSections`  | `String`   | Пример 2-х уровневого меню форм \(даже с переводами: см. "Cliente,Клиенты"\)   | `*Producte,F_PROD_GR,F_PRODUCTS,                            *"Cliente,Клиенты", F_CLIENTS,F_AGENTS,                              *Rute,F_ROUTES,F_RUTE_DESF,*, F_UM,F_TT,F_PRICE,F_INF_SUPLIMENT, F_TIP_DOC, F_CAUZA_RETUR,F_BANKS,*"Facture",                        F_DEBLOCAREA_NN, F_STRICTPAPER_DOCS`  |
| `ToolBarFormSections_`  | `String`  |   | `*Producte,F_PROD_GR,F_PRODUCTS,                           *"Cliente,Клиенты", F_CLIENTS,F_AGENTS,*Rute,F_ROUTES, F_RUTE_DESF,*, F_UM,F_TT,F_PRICE,F_INF_SUPLIMENT, F_TIP_DOC, F_CAUZA_RETUR,F_BANKS,*"Facture",                         F_DEBLOCAREA_NN, F_STRICTPAPER_DOCS`  |
| `ToolBarFormSections__`  | `String`   |   | `F_PROD_GR,F_PRODUCTS,F_CLIENTS,                      F_AGENTS,F_ROUTES, F_RUTE_DESF,F_UM,F_TT,  F_PRICE,F_INF_SUPLIMENT, F_BANKS,F_CERT`  |
| `TBDocCmd`  | `Boolean` |   | `true`  |
| `TBForms`  | `Boolean` |   | `false`  |
| `HideErrorLevel`   | `Integer`  | 2 =&gt; все ошибки показываются в статус баре; 1 =&gt; в статус баре показываются все ошибки, кроме msg.  Меню Сервис-&gt;журнал ошибок. \(`DblClick` по статус-бару\)  | `2`  |
| `HideMenuDict`   | `Boolean` | Меню справочников. Отображение меню "Справочники" \(по умолчанию включено\).  | `true`   |
| `HideMenuReps`   | `Boolean` | Меню отчетов. Отображение меню "Отчеты" \(по умолчанию включено\).   | `true` |
| `HideMenuForms`   | `Boolean` | Меню форм. Отображение меню "Формы" \(по умолчанию включено\).   | `true`   |
| `ViewFromToday`   | `Integer`   | Ограничение периода. Ограничение периода отображаемых документов  как смещение на указанное  число дней назад от текущей даты.  |   |
| `ViewBegin`   | `String`   | Ограничение снизу. Минимальная дата отображаемых документов |   |
| `ViewEnd`   | `String`    | Ограничение сверху. Максимальная дата отображаемых документов   |   |
| `LastRecord`  | `Boolean` | К последнему документу. При открытии журнала документов переходить на последний видимый  документ.  | `true`  |
| `ORDER BY`   | `String`   | Порядок сортировки. Порядок сортировки документов \(список имен полей, разделенных запятыми\).   |   |
| `OraLoaderModeDML`  | `Boolean` | Режим загрузки данных. Использование `DML` при загрузке данных из текстового файла или таблицы `BDE`.  Этот режим снижает скорость загрузки, но позволяет обойти некоторые ограничения.  | `true`   |
| `DataAutomat`  | `Boolean` | `DATAMANUAL` как в пред.. Автозаполнение даты документов при вводе на основании даты предыдущего документа.  | `true`  |
| `DataCurrent`  | `Boolean` | `DATAMANUAL` сегодня. Автозаполнение даты документов при вводе на основании текущей даты.   | `true`   |
| `DataEmpty`   | `Boolean` | Пустая `DATAMANUAL`. Отменить для пользователя автозаполнение поля `DATAMANUAL`  \(отмена глобальных параметров `DataAutomat` и `DataCurrent`\).  | `true`  |
| `PXCMSimpleEditing`   | `Boolean` | Режим быстрой правки. Режим быстрой правки проводок документов версии PX.   | `true`  |
| `Backup`   | `Boolean` | Архив документов. Режим сохранения документов в архиве перед их удалением.  | `true`   |
| `XDEF_BGFILTER`  | `String`   | Фильтр по умолчанию. Начальное значение фильтра по `NrSet`: здесь нужно перечислить  через запятую коды тех позиций фильтра, которые должны быть изначально включены.  \(Имеются в виду коды, которые можно увидеть в последнем столбце верхней таблицы в  окне установки фильтра по `NrSet` - колонка "№"\). Вместо списка кодов можно ввести символ "\*", что означает "включить все".  |  `1,2,3,1226` |
| `XDEF_NRSET`   | `String`   | `NrSet` по умолчанию. Начальное значение `NrSet` по умолчанию.  |   |
| `XDEF_NRSET_VIEW`   | `String`   | Ограничение по `NrSet`. Список кодов `NrSet`, которыми ограничиваются права пользователя.   |   |
| `HideNrsetFilter`   | `Boolean` | Скрыть фильтр по `NrSet`. Не отображать установленный фильтр по `NrSet`.   | `true`   |
| `__XDEF_NRSET`  | `Integer` |   | `201`  |
|   |   |  Панели инструментов: |   |
| `TBIconStyle`  | `Integer`   | Расположение значков. Число от 0 до 3 означает положение значка относительно пункта главного меню: 0 - Значки не выводятся на экран \(в меню - только надписи\);  1 - Надписи не выводятся на экран \(в меню - только значки\);   2 - Значки выводятся на экран слева от соответствующих надписей;  3 - Значки выводятся на экран над соответствующими надписями.  | `3`   |
| `TBIconSize`   | `Integer`    | Размер значков. Число от 0 до 2 означает размер значков в главного меню:  0 - Мелкие значки;  1 - Средние значки;  2 - Крупные значки.   | `2`  |
| `TBPeriod`  | `Boolean` | Панель периодов. Отображать на экране панель ввода периодов.   | `true` |
| `TBWindowList`   | `Boolean` | Панель открытых окон. Отображать на экране панель открытых окон.   | `true` |
| `HideDocPreview` | `Boolean` |   | `true`  |
| `HideDocsActive` | `Boolean` |  | `false` |
| `HideDocsBarCode` | `Boolean` |  `` | `true`   |
| `HideDocsDesign`  | `Boolean` |  | `true` |
| `HideDocsDublare`  | `Boolean` |  `` | `true`     |
| `HideDocsEditare`  | `Boolean` |  | `true` |
| `HideDocsFact`  | `Boolean`   |  `` | `true`   |
| `HideDocsHeadLine`  | `Boolean` |  | `true` |
| `HideDocsLang`  | `Boolean` |  `` | `true`     |
| `HideDocsLich`  | `Boolean` |  | `true` |
| `HideDocsPeriod` | `Boolean` |  | `true`  |
| `HideDocsSalvare` | `Boolean` |  | `true` |
| `HideDocsSold`  | `Boolean` |  `` | `true`   |
| `HideDocsSpec`  | `Boolean` |  | `true` |
| `HideDocsSwitch`  | `Boolean` |  `` | `true`  |
| `HideDocsTabAdd`  | `Boolean` |  | `true` |
| `HideDocsTabCM`  | `Boolean` |  `` | `true`    |
| `HideDocsTabLog`  | `Boolea`  |  | `true` |
| `HideDocsTabMain`  | `Boolean` |  `` | `true`      |
| `HideDocsTabObj`  | `Boolean` |  | `true` |
| `HideDocsTabXL`  | `Boolean` |  `` | `true`  |
| `HideDocsToolBar`  | `Boolean` |  | `true` |
| `HideDocsTotals`  | `Boolean` |  `` | `true`    |
| `HideDocsWizard`  | `Boolean` |  | `true` |
| `HideF1Buttons`  | `Boolean`   |  `` | `true`   |
| `HideMemory`  | `Boolean` |  | `true` |
| `HideMenuDoc`  | `Boolean` |  `` | `true`  |
| `HideMenuHelp`  | `Boolean` |  | `true` |
| `HideMenuUtil`  | `Boolean` |  `` | `true`  |
| `HideMenuWindow` | `Boolean` |  | `true` |
| `HideNaviPDC`  | `Boolean`    |  `` | `true`  |
| `HideNaviSQL`  | `Boolean` |  | `true` |
| `HideNaviSysS`  | `Boolean` |  `` | `true`    |
| `HideNaviUniv`  | `Boolean` |  | `true` |
| `HideStatusBar`  | `Boolean` |  `` | `true`      |
| `HideToolCalc`  | `Boolean` |  | `true` |
| `HideToolInf`  | `Boolean` |  `` | `true`        |
| `HideToolLang`  | `Boolean` |  | `true` |
| `HideToolMsg`  | `Boolean` |  `` | `true`          |
| `HideToolNavi`  | `Boolean` |  | `true` |
| `HideToolSet`  | `Boolean` |  `` | `true`  |
| `HideToolSys`  | `Boolean` |  | `true` |
| `GotoDocumentEditing`  | `Boolea`  |  `` | `true`    |
|   |   | **Скрытие пункта меню "Журналы"**  |   |
| `HideMenu`   | `Boolean` |  `` | `true`   |
| `HideMenuJrnlStd`  | `Boolean` |  | `true` |
| `TBJournals`  | `Boolean` |  `` | `true`  |
|   |   | Включение кнопки `SubSet` в `EasyInterface` | Примечание: в `LACSetupBlockObjects` не должно быть `NRSET`  \(если при этом `LACObjectsSelectedOnly` не объявлено или =`false`\)  \(если на нашем уровне `LACSetupBlockObjects` пустой, тогда возьмется с уровня выше. так что вместо пустого надо задать значение: -\)  |
| `BG_FILTER_SECTION`  | `String` |   | `1`  |
| `HideDocGrid`  | `Boolean`  |   | `false`   |
| `HideNrsetFilte`  | `Boolean` |   | `false`   |
| `HideToolbar`  | `Boolean`  |   | `false`   |
| `InitSQL`  | `Memo`   |   | `begin  :res:=2; Bg_Policy.INITFILTER_NRSET_TREE    ('ID IN (1,2,3)');end;`  |



Действия над учетными записями в конфигураторе UniConf:**Свойства, установленные для группы пользователей, распространяются на всех пользователей группы.**

1\) [Создание учетной записи пользователя](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/polzovateli/sozdanie-uchetnoi-zapisi-polzovatelya)

Иногда полезно временно получить права админа под текущим пользователем. Для этого можно использовать комбинацию клавиш Ctrl+F12. Запрашиваемый пароль настраивается в Settings-&gt;General следующим свойством:

| **Название свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- |
| Tmpadminpass | String | временные права админа под текущим пользователем | aaa |

[Настройка ограничения доступа на изменение универсального справочника](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/polzovateli/nastroika-ogranicheniya-dostupa-na-izmenenie-universalnogo-spravochnika)

[Настройка ограничения доступа к проводкам \(tmdb\_cm\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/polzovateli/nastroika-ogranicheniya-dostupa-k-provodkam)

_Подсказка:_

[Как скрыть пароль](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/polzovateli/kak-skryt-parol)

[Настройка прав на редактирование справочников UNIVERS](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/polzovateli/nastroika-ogranicheniya-dostupa-na-izmenenie-universalnogo-spravochnika)

[Настройка прав на редактирование справочников SYSS](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/spravochniki/syss/cherez-vremennuyu-tablicu-tms_syss_unlock)

[Интерфейс](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/polzovateli/interfeis)

Новые возможности по [ограничению паролей пользователей](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/polzovateli/ogranichenie-parolei-polzovatelei)

