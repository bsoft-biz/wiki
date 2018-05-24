# Глобальные настройки

**Способы задания глобальных настроек:**

Глобальные настройки программы могут задаваться различными способами,   
причем каждый из способов имеет свой приоритет:

* File: Файл **"startup.ini"**Текстовый файл в каталоге запуска программы.  Имеет самый низкий приоритет, но некоторые параметры можно задать только в этом файле.  Если в каталоге WINDOWS существует файл **"un4.ini"**, то он будет использован вместо файла **"startup.ini"** в каталоге запуска программы.Sys: Раздел **"System settings"**Группа секций администратора, в которой задаются настройки программы, общие для всех пользователей и групп. По умолчанию используется секция "General".  Имеет более высокий приоритет. Многие параметры можно задать только здесь.Grp: Секция **группы пользователей**Секция администратора, где обычно задаются атрибуты прав пользователей.  Имеет еще более высокий приоритет по отношению к предыдущим пунктам.Usr: Секция **пользователя**Секция администратора, где описываются атрибуты пользователя системы.  Имеет самый высокий приоритет среди постоянных способов задания.Mnu: **Меню** программыВо время выполнения программы можно менять некоторые параметры.  Имеет наивысший приоритет, но время действия настроек ограничено сеансом.

**Полный список всех глобальных настроек:**



| Название | Тип | По умолч. | Смысл значения | File | Sys | Grp | Usr | Mnu |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [Language](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Language) | String |   | Язык интерфейса | + | + | + | + | + |
|  Загрузка настроек, дизайнов, переводов и т.п.: |  |  |  |  |  |  |  |  |
| [LogParams](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LogParams) | Boolean |   | Контроль настроек | + |   |   |   | + |
| [NewDesignMethod](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#NewDesignMethod) | Boolean | true | Быстрая загрузка | + |   |   |   |   |
| [UsePackedIni](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UsePackedIni) | Boolean |   | Паковать настройки | + |   |   |   |   |
| [TardyLoading](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#TardyLoading) | Boolean |   | Отложенная загрузка | + |   |   |   |   |
| [UseLocalCache](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UseLocalCache) | Boolean |   | Файловый кеш дизайнов | + |   |   |   |   |
| [GridPropCacheLimit](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#GridPropCacheLimit) | Integer |   | Размер кеша дизайнов | + | + | + | + | + |
| [RepairGridDesign](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RepairGridDesign) | Boolean |   | Исправление ошибок | + | + | + | + | + |
| [LangDontLoad](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LangDontLoad) | Boolean |   | Не загружать переводы | + | + | + | + | + |
| [LoadCaptionsSep](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LoadCaptionsSep) | Boolean |   | Заголовки отдельно | + | + | + | + | + |
|  Ограничение прав пользователей  \(анализируются только секции пользователей и групп!\): |  |  |  |  |  |  |  |  |
| [ADMIN](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ADMIN) | Integer |   | Права администратора |   |   | + | + |   |
| [AllowGridDesign](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#AllowGridDesign) | Boolean |   | Разрешить дизайн |   |   | + | + |   |
| [DesignGroup](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DesignGroup) | Integer |   | Групповые дизайны |   |   | + | + | + |
| [LACSetupBlockSections](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACSetupBlockSections) | String |   | Ограничение форм |   |   | + | + |   |
| [LACSetupBlockReports](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACSetupBlockReports) | String |   | Ограничение отчетов |   |   | + | + |   |
| [LACSetupBlockObjects](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACSetupBlockObjects) | String |   | Ограничение объектов |   |   | + | + |   |
| [LACSectionsSelectedOnly](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACSectionsSelectedOnly) | Boolean |   | Тип ограничения |   |   | + | + |   |
| [LACReportsSelectedOnly](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACReportsSelectedOnly) | Boolean |   | Тип ограничения |   |   | + | + |   |
| [LACObjectsSelectedOnly](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACObjectsSelectedOnly) | Boolean |   | Тип ограничения |   |   | + | + |   |
| [seqNRMANDisableChanges](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#seqNRMANDisableChanges) | Boolean |   | Запрет на NRMANUAL |   |   | + | + |   |
| [GlobalPeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#GlobalPeriodStart) | String |   | Общая дата начала |   | + |   |   |   |
| [GlobalPeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#GlobalPeriodEnd) | String |   | Общая дата конца |   | + |   |   |   |
| [PeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#PeriodStart) | String | [GlobalPeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_GlobalPeriodStart) | Частная дата начала |   |   | + | + |   |
| [PeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#PeriodEnd) | String | [GlobalPeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_GlobalPeriodEnd) | Частная дата конца |   |   | + | + |   |
| [Docs view mode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Docs_view_mode) | Integer |   | Ограничение просмотра |   |   | + | + |   |
| [Docs edit mode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Docs_edit_mode) | Integer |   | Ограничение изменений |   |   | + | + |   |
| [UserGroupList](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UserGroupList) | String |   | Список пользователей |   |   | + | + |   |
|  Настройки форм и справочников системы: |  |  |  |  |  |  |  |  |
| [NewSyntax](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#NewSyntax) | Boolean |   | Синтаксис справочников |   | + |   |   |   |
| [HideMenuDict](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#HideMenuDict) | Boolean | true | Меню справочников | + | + | + | + |   |
| [HideMenuReps](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#HideMenuReps) | Boolean | true | Меню отчетов | + | + | + | + |   |
| [HideMenuForms](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#HideMenuForms) | Boolean | true | Меню форм | + | + | + | + |   |
|  Панели инструментов: |  |  |  |  |  |  |  |  |
| [TBIconStyle](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#TBIconStyle) | Integer |   | Расположение значков | + | + | + | + | + |
| [TBIconSize](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#TBIconSize) | Integer |   | Размер значков | + | + | + | + | + |
| [TBPeriod](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#TBPeriod) | Boolean |   | Панель периодов | + | + | + | + | + |
| [TBWindowList](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#TBWindowList) | Boolean |   | Панель открытых окон | + | + | + | + | + |
|  Стартовая форма, [фильтр по NrSet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/nrset.html) и т.п.: |  |  |  |  |  |  |  |  |
| [AutoShowForm](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#AutoShowForm) | String |   | Стартовая форма |   | + |   |   |   |
| [BG\_FILTER\_SECTION](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#BG_FILTER_SECTION) | String |   | Форма [фильтра по NrSet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/nrset.html) |   | + |   |   |   |
| [XDEF\_BGFILTER](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#XDEF_BGFILTER) | String |   | Фильтр по умолчанию | + | + | + | + |   |
| [XDEF\_NRSET](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#XDEF_NRSET) | String |   | NrSet по умолчанию | + | + | + | + |   |
| [XDEF\_NRSET\_VIEW](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#XDEF_NRSET_VIEW) | String |   | Ограничение по NrSet | + | + | + | + |   |
| [HideNrsetFilter](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#HideNrsetFilter) | Boolean |   | Скрыть [фильтр по NrSet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/nrset.html) | + | + | + | + |   |
|  Настройки окна регистра документов  \(в разделе "System settings" используется секция "Docs"\): |  |  |  |  |  |  |  |  |
| [ViewFromToday](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ViewFromToday) | Integer |   | Ограничение периода | + | + | + | + |   |
| [ViewBegin](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ViewBegin) | String |   | Ограничение снизу | + | + | + | + | + |
| [ViewEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ViewEnd) | String |   | Ограничение сверху | + | + | + | + | + |
| [DEF\_JOURNAL](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DEF_JOURNAL) | String |   | Стартовый журнал | + | + | + | + |   |
| [LastRecord](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LastRecord) | Boolean |   | К последнему документу | + | + | + | + |   |
| [ORDER BY](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ORDER_BY) | String |   | Порядок сортировки | + | + | + | + |   |
| [DataAutomat](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DataAutomat) | Boolean |   | DATAMANUAL как в пред. | + | + | + | + |   |
| [DataCurrent](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DataCurrent) | Boolean |   | DATAMANUAL сегодня | + | + | + | + |   |
| [DataEmpty](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DataEmpty) | Boolean |   | Пустая DATAMANUAL | + |   | + | + |   |
| [ColorDisabledDocs](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ColorDisabledDocs) | Integer | clAqua | Цвет неактивных док. |   | + |   |   |   |
| [DefaultModule](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DefaultModule) | String |   | TIP по умолчанию |   | + |   |   |   |
| [DefValuta](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DefValuta) | String |   | VALUTA по умолчанию |   | + |   |   |   |
| [PXCompatibile](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#PXCompatibile) | Boolean |   | Документы из версии PX |   | + |   |   |   |
| [PXCMSimpleEditing](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#PXCMSimpleEditing) | Boolean |   | Режим быстрой правки | + | + | + | + | + |
| [Backup](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Backup) | Boolean |   | Архив документов | + | + | + | + |   |
| OnDeleteCMName |  String |   | Объект из которого будут удалятся проводки в документе |   | +  |   |   |   |
| Настройки окна менеджера отчетов: |  |  |  |  |  |  |  |  |
| [RepDataStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RepDataStart) | String | [PeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PeriodStart) | Дата начала периода |   | + | + | + | + |
| [RepDataEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RepDataEnd) | String | [PeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PeriodEnd) | Дата конца периода |   | + | + | + | + |
| [RepTemplatesPath](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RepTemplatesPath) | String | m:\templates.ora\ | Размещение шаблонов |   | + |   |   |   |
| [RepTreeFromSysS](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RepTreeFromSysS) | Boolean |   | Отчеты из справочника | + |   |   |   |   |
| [ReportTreeSorting](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ReportTreeSorting) | Boolean |   | Сортировка узлов | + | + | + | + |   |
| [StartupReportNode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#StartupReportNode) | String |   | Стартовый узел | + | + | + | + |   |
| [RepTestRecordCount](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RepTestRecordCount) | Boolean | true | Проверять к-во записей | + | + | + | + | + |
| [RepDeleteTempTables](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RepDeleteTempTables) | Boolean | true | Удалять врем. таблицы | + | + | + | + | + |
|  Разные настройки: |  |  |  |  |  |  |  |  |
| [GridDisableNumberSearch](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#GridDisableNumberSearch) | Boolean |   | Запрет числового поиска | + | + | + | + | + |
| [UseSmartTab](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UseSmartTab) | Boolean |   | "Умный" &lt;Tab&gt; | + | + | + | + | + |
| [UseSmartEnter](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UseSmartEnter) | Boolean |   | "Умный" &lt;Enter&gt; | + | + | + | + | + |
| [UseSpeedSearch](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UseSpeedSearch) | Boolean |   | Быстрый поиск в справ. | + | + | + | + | + |
| [AutoFreeMemory](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#AutoFreeMemory) | Boolean |   | Выгружать неисп. DLL | + | + | + | + |   |
| [UseDotInCont](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UseDotInCont) | Boolean |   | Точка в счете | + | + | + | + |   |
| [ContFormat](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ContFormat) | String |   | Формат поля счета |   | + |   |   |   |
| [LengthCont](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LengthCont) | Integer | 4 | Длина счета |   | + |   |   |   |
| [LengthPachet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LengthPachet) | Integer | 2 | Длина номера пачки |   | + |   |   |   |
| [LengthCont1](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LengthCont1) | Integer |   | Длина субсчета |   | + |   |   |   |
| [UnivDLL](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UnivDLL) | Integer | 100 | Код DLL карточек |   | + |   |   |   |
| [EnableBDE](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#EnableBDE) | Boolean |   | Поддержка старой версии | + |   |   |   |   |
| [NoCheckLocale](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#NoCheckLocale) | Boolean |   | Проверка при старте | + |   |   |   |   |
| [NoCheckFreeSpace](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#NoCheckFreeSpace) | Boolean |   | Проверка при старте | + |   |   |   |   |
| [OraLoaderModeDML](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#OraLoaderModeDML) | Boolean |   | Режим загрузки данных | + | + | + | + |   |
|  Установка соединения: |  |  |  |  |  |  |  |  |
| [CheckOraVersion](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#CheckOraVersion) | Boolean |   | Проверка версии БД | + |   |   |   |   |
| [CheckSecurityMode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#CheckSecurityMode) | Boolean | true |   | + |   |   |   |   |
| [ShowLogin](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#ShowLogin) | Boolean | true |   | + |   |   |   |   |
| [OraHome](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#OraHome) | Integer |   |   | + |   |   |   |   |
| [Server](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Server) | String |   |   | + |   |   |   |   |
| [Login](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Login) | String |   |   | + |   |   |   |   |
| [Password](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Password) | String |   |   | + |   |   |   |   |
| [OraUserName](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#OraUserName) | String |   |   | + |   |   |   |   |
| [OraPassword](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#OraPassword) | String |   |   | + |   |   |   |   |
| [WindowsLogon](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#WindowsLogon) | Boolean |   |   | + |   |   |   |   |
| [LockUserName](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LockUserName) | Boolean |   |   | + |   |   |   |   |
| [SetLogo](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#SetLogo) | Integer |   |   | + |   |   |   |   |
| [LogoPath](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LogoPath) | String |   |   | + |   |   |   |   |
|  Отладочные возможности: |  |  |  |  |  |  |  |  |
| [RunMaximized](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#RunMaximized) | Integer | 1 | Окно во весь экран | + |   |   |   |   |
| [AutoRunCmd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#AutoRunCmd) | String |  | Стартовое действие | + |   |   |   |   |
| [AutoLoadScript](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#AutoLoadScript) | String |   | Файл скрипта | + |   |   |   |   |
| [SQLMonitorLog](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#SQLMonitorLog) | Boolean |   | Запись в журнал | + |   |   |   |   |
| [SQLMonitorLogFile](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#SQLMonitorLogFile) | String | monitor.log | Имя файла | + |   |   |   |   |
| [SQLMonitorLogUnique](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#SQLMonitorLogUnique) | Boolean |   | Уникальность | + |   |   |   |   |
| [SQLMonitorLogLimit](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#SQLMonitorLogLimit) | Integer | 100 | Нижний предел | + |   |   |   |   |
| [SQLMonitorActive](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#SQLMonitorActive) | Boolean |   | Включение SQLMonitor | + |   |   |   | + |
| [UseProfiler](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UseProfiler) | Boolean |   | Замер быстродействия | + |   |   |   |   |
| [MeasureTraffic](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#MeasureTraffic) | Boolean |   | Изменение траффика | + |   |   |   |  |





**Подробнее о каждом параметре:**

[Language](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Language)

Язык интерфейса задается либо цифрой \(0, 1, 2\), либо буквой \(E, M, R\). Язык окна регистрации задается только методом File. Если язык не задан ни одним из методов, система переводов выключается на весь сеанс работы.   
Удобно ввести это свойство в Администраторе как список значений:  
  
\[ZZZ\]

Language=2

.type.Language=Integer

.listValue.Language=0,1,2

.listTextValue.Language=English,Moldavian,Russian

**Загрузка настроек, дизайнов, переводов и т.п.:**

[LogParams](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LogParams)

Режим записи в текстовый файл всех считываемых настроек \(до и после обработки и фильтрации\).

[NewDesignMethod](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_NewDesignMethod)

Режим быстрой загрузки настроек и дизайнов \(использование хранимых процедур и меток времени\). Требуется новый пакет ORACLE UN$USERPARAMS.

[UsePackedIni](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UsePackedIni)

Режим загрузки настроек в запакованном виде. Требуется новый пакет ORACLE UN$USERPARAMS, сервер упаковки PackSrv должен быть запущен.

[TardyLoading](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_TardyLoading)

Режим отложенной загрузки настроек. Настройки отчетов загружаются только при первом открытии окна менеджера отчетов.

[UseLocalCache](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UseLocalCache)

Режим использования файлового кеша для сохранения настроек и дизайнов.

[GridPropCacheLimit](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_GridPropCacheLimit)

Максимальный размер кеша дизайнов в памяти. За единицу берется один тип документа, один узел дерева отчетов, одна форма или справочник.

[RepairGridDesign](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RepairGridDesign)

Режим автокоррекции загружаемых дизайнов \(бывает нужен при работе с ORACLE 9i\).

[LangDontLoad](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LangDontLoad)

Не пытаться загружать тексты переводов из ORACLE \(для уменьшения трафика\).

[LoadCaptionsSep](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LoadCaptionsSep)

Режим раздельной загрузки переводов заголовков столбцов и дизайнов \(для совместимости с переводами заголовков столбцов, сохраненными в предыдущих версиях SL\).  


**Ограничение прав пользователей:**

[ADMIN](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ADMIN)

Ненулевое значение дает пользователю права администратора

[AllowGridDesign](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_AllowGridDesign)

Разрешить изменение дизайнов \(применяется для пользователей, у которых нет прав администратора, но которым нужно разрешить изменение дизайнов\).

[DesignGroup](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_DesignGroup)

Номер группы дизайнов \(ненулевое значение позволяет пользователю иметь персональные дизайны, переводы, схемы отчетов и т.п.\). Администратор может менять себе этот номер во время выполнения программы \(через интерфейс меню\).

[LACSetupBlockSections](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LACSetupBlockSections)

Список секций форм и справочников, которые пользователю видеть запрещено.

[LACSetupBlockReports](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LACSetupBlockReports)

Список секций отчетов, которые пользователю видеть запрещено.

[LACSetupBlockObjects](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LACSetupBlockObjects)

Список объектов, с которыми пользователю работать запрещено.

[LACSectionsSelectedOnly](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LACSectionsSelectedOnly)

Интерпретировать параметр 

[LACSetupBlockSections](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACSetupBlockSections) 

как список разрешенных секций.

[LACReportsSelectedOnly](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LACReportsSelectedOnly)

Интерпретировать параметр 

[LACSetupBlockReports](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACSetupBlockReports) 

как список разрешенных секций.

[LACObjectsSelectedOnly](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LACObjectsSelectedOnly)

Интерпретировать параметр 

[LACSetupBlockObjects](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#LACSetupBlockObjects) 

как список разрешенных секций.

[seqNRMANDisableChanges](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_seqNRMANDisableChanges)

Запретить пользователю изменять поле NRMANUAL.

[GlobalPeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_GlobalPeriodStart)

Общая дата начала периода редактирования документов. _Допускается SQL-выражение._

[GlobalPeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_GlobalPeriodEnd)

Общая дата окончания периода редактирования документов. _Допускается SQL-выражение._

[PeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PeriodStart)

Частная дата начала периода редактирования документов. _Допускается SQL-выражение._ Если значение параметра отсутствует, вместо него используется значение параметра [GlobalPeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_GlobalPeriodStart)

[PeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PeriodEnd).

Частная дата окончания периода редактирования документов. _Допускается SQL-выражение._ Если значение параметра отсутствует, вместо него используется значение параметра [GlobalPeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_GlobalPeriodEnd).

[Docs view mode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Docs_view_mode)

Значение 2 означает, что пользователь может видеть только свои документы \(те, которые были созданы под тем же именем пользователя\).   
Значение 1 означает, что пользователь может видеть только документы своей группы \(те, у которых поле USERID соответствует параметру [UserGroupList](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UserGroupList)\)   
Удобно ввести это свойство в Администраторе как список значений:  
  
\[ZZZ\]

Docs view mode=0

.type.Docs view mode=Integer

.listValue.Docs view mode=0,1,2

.listTextValue.Docs view mode="All documents","All group documents","Private documents"

  
[Docs edit mode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Docs_edit_mode)

Значение 2 означает, что пользователь может редактировать только свои документы \(те, которые были созданы под тем же именем пользователя\) либо документы, у которых поле USERID не заполнено.   
Значение 1 означает, что пользователь может редактировать только документы своей группы \(те, у которых поле USERID соответствует параметру [UserGroupList](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#UserGroupList)\) либо документы, у которых поле USERID не заполнено.   
Удобно ввести это свойство в Администраторе как список значений:  
  
\[ZZZ\]

Docs edit mode=0

.type.Docs edit mode=Integer

.listValue.Docs edit mode=0,1,2

.listTextValue.Docs edit mode="All documents","All group documents","Private documents"

  
[UserGroupList](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UserGroupList)

Список кодов пользователей \(через запятую\), составляющих группу, используемую в параметрах [Docs view mode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Docs_view_mode) и [Docs edit mode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Docs_edit_mode). Этот параметр удобно заводить на уровне секции группы пользователей.  


**Настройки форм и справочников системы:**

[NewSyntax](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_NewSyntax)

Названия секций, описывающих настройки справочников, используют вместо символа подчеркивания символ решетки \('\#'\). В этом режиме дизайны гридов справочников сохраняются под этим же именем секции, что позволяет переносить их вместе с секцией справочника методом "Экспорт в XML".

[HideMenuDict](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_HideMenuDict)

Отображение меню "Справочники" \(по умолчанию включено\).

[HideMenuReps](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_HideMenuReps)

Отображение меню "Отчеты" \(по умолчанию включено\).

[HideMenuForms](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_HideMenuForms)

Отображение меню "Формы" \(по умолчанию включено\).  


**Панели инструментов:**

[TBIconStyle](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_TBIconStyle)Число от 0 до 3 означает положение значка относительно пункта главного меню:   
0 - Значки не выводятся на экран \(в меню - только надписи\);   
1 - Надписи не выводятся на экран \(в меню - только значки\);   
2 - Значки выводятся на экран слева от соответствующих надписей;   
3 - Значки выводятся на экран над соответствующими надписями.   
Удобно ввести это свойство в Администраторе как список значений:  
  
\[ZZZ\]

TBIconStyle=0

.type.TBIconStyle=Integer

.listValue.TBIconStyle=0,1,2,3

.listTextValue.TBIconStyle="Captions only","Icons only","Icons and Captions","Icons above Captions"

  
[TBIconSize](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_TBIconSize)

Число от 0 до 2 означает размер значков в главного меню:   
0 - Мелкие значки;   
1 - Средние значки;   
2 - Крупные значки.   
Удобно ввести это свойство в Администраторе как список значений:  
  
\[ZZZ\]

TBIconSize=0

.type.TBIconSize=Integer

.listValue.TBIconSize=0,1,2

.listTextValue.TBIconSize="Small Icons","Meduim Icons","Large Icons"

  
[TBPeriod](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_TBPeriod)

Отображать на экране панель ввода периодов.

[TBWindowList](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_TBWindowList)

Отображать на экране панель открытых окон.  


**Стартовая форма, фильтр по NrSet и т.п.:**

[AutoShowForm](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_AutoShowForm)

Имя секции формы, которую нужно показывать сразу после запуска программы.   
Этот параметр не обрабатывается, если указан параметр [BG\_FILTER\_SECTION](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#BG_FILTER_SECTION).

[BG\_FILTER\_SECTION](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_BG_FILTER_SECTION)

Если этот параметр не пустой, то сразу после запуска программы открывается окно установки [фильтра по NrSet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/nrset.html) либо \(при непустом значении параметра [XDEF\_BGFILTER](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#XDEF_BGFILTER)\) фильтр по NrSet устанавливается автоматически и форма не показывается.

[XDEF\_BGFILTER](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_XDEF_BGFILTER)

Начальное значение фильтра по NrSet: здесь нужно перечислить через запятую коды тех позиций фильтра, которые должны быть изначально включены. \(Имеются в виду коды, которые можно увидеть в последнем столбце верхней таблицы в окне установки [фильтра по NrSet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/nrset.html#WIN2) - колонка "№"\). Вместо списка кодов можно ввести символ "\*", что означает "включить все".

[XDEF\_NRSET](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_XDEF_NRSET)

Начальное значение NrSet по умолчанию.

[XDEF\_NRSET\_VIEW](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_XDEF_NRSET_VIEW)

Список кодов NrSet, которыми ограничиваются права пользователя.

[HideNrsetFilter](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_HideNrsetFilter)

Не отображать установленный [фильтр по NrSet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/nrset.html).  


**Настройки окна регистра документов:**

[ViewFromToday](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ViewFromToday)

Ограничение периода отображаемых документов как смещение на указанное число дней назад от текущей даты.

[ViewBegin](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ViewBegin)

Минимальная дата отображаемых документов

[ViewEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ViewEnd)

Максимальная дата отображаемых документов

[DEF\_JOURNAL](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_DEF_JOURNAL)

Имя секции журнала, который надо открывать сразу после запуска программы.

[LastRecord](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LastRecord)

При открытии журнала документов переходить на последний видимый документ.

[ORDER BY](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ORDER_BY)

Порядок сортировки документов \(список имен полей, разделенных запятыми\).

[DataAutomat](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_DataAutomat)

Автозаполнение даты документов при вводе на основании даты предыдущего документа.

[DataCurrent](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_DataCurrent)

Автозаполнение даты документов при вводе на основании текущей даты.

[DataEmpty](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_DataEmpty)

Отменить для пользователя автозаполнение поля DATAMANUAL \(отмена глобальных параметров [DataAutomat](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DataAutomat) и [DataCurrent](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#DataCurrent)\).

[ColorDisabledDocs](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ColorDisabledDocs)

Цвет дезактивированных документов.

[DefaultModule](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_DefaultModule)

Значение поля TIP по умолчанию.

[DefValuta](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_DefValuta)

Значение поля VALUTA по умолчанию.

[PXCompatibile](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PXCompatibile)

Режим использования документов версии PX.

[PXCMSimpleEditing](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PXCMSimpleEditing)

Режим быстрой правки проводок документов версии PX.

[Backup](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Backup)

Режим сохранения документов в архиве перед их удалением.OnDeleteCMNameПараметр для указания объекта из которого будут удалятся проводки в документе.  


**Настройки окна менеджера отчетов:**

[RepDataStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RepDataStart)

Дата начала периода просмотра данных в отчетах. _Допускается SQL-выражение._ Если значение параметра отсутствует, вместо него используется значение параметра [PeriodStart](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PeriodStart)

[RepDataEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RepDataEnd)

Дата окончания периода просмотра данных в отчетах. _Допускается SQL-выражение._ Если значение параметра отсутствует, вместо него используется значение параметра [PeriodEnd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_PeriodEnd)

[RepTemplatesPath](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RepTemplatesPath)

Каталог, в котором размещаются файлы шаблонов для построения отчетов.

[RepTreeFromSysS](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RepTreeFromSysS)

Добавлять в дерево отчетов список отчетов из системного справочника \(SysS\).

[ReportTreeSorting](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ReportTreeSorting)

Режим сортировки узлов дерева отчетов по алфавиту.

[StartupReportNode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_StartupReportNode)

Имя секции отчета, на котором позиционировать дерево отчетов сразу после открытия окна менеджера отчетов.

[RepTestRecordCount](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RepTestRecordCount)

Режим проверки количества записей в наборе данных отчета \(для F1Reports\): при очень большом количестве записей выдается предупреждающее сообщение, имеется возможность отменить построение отчета или вручную ограничить количество выводимых записей. Предельное количество записей для отчетов Master/Detail - 1000, только Master - 10000.

[RepDeleteTempTables](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RepDeleteTempTables)

Режим удаления временных таблиц ORACLE после построения отчета \(можно выключить\).  


**Разные настройки:**

[GridDisableNumberSearch](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#__GridDisableNumberSearch)

Режим текстового поиска даже в числовых полях грида \(вместо числового поиска\).

[UseSmartTab](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UseSmartTab)

Режим интеллектуального поведения клавиши &lt;Tab&gt;: переход от поля к полю по всему активному окну.

[UseSmartEnter](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UseSmartEnter)

Режим интеллектуального поведения клавиши &lt;Enter&gt; на дополнительной \(цифровой\) клавиатуре: при редактировании таблиц - переход к следующему полю или \(из последнего столбца\) завершение редактирования и вставка новой записи.

[UseSpeedSearch](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UseSpeedSearch)

Режим быстрого поиска в выпадающих справочниках.

[AutoFreeMemory](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_AutoFreeMemory)

Выгружать из памяти неиспользуемые динамические библиотеки \(DLL и BPL\).

[UseDotInCont](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UseDotInCont)

Использовать точку в значении счета \(формат 99.99\) - удобно для ПМР.

[ContFormat](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ContFormat)

Формат поля счета.

[LengthCont](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LengthCont)

Длина счета \(обычно 4, но для бюджетных предприятий - 3\).

[LengthPachet](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LengthPachet)

Длина номера пачки.

[LengthCont1](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LengthCont1)

Длина субсчета.

[UnivDLL](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UnivDLL)

Код DLL для отображения карточек универсального справочника \(должно быть 100\).

[EnableBDE](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_EnableBDE)

При старте программы инициализировать подсистему BDE \(рекомендуется\).

[NoCheckLocale](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_NoCheckLocale)

При старте программы не проверять региональные настройки.

[NoCheckFreeSpace](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_NoCheckFreeSpace)

При старте программы не проверять свободное место на дисках.

[OraLoaderModeDML](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_OraLoaderModeDML)

Использование DML при загрузке данных из текстового файла или таблицы BDE. Этот режим снижает скорость загрузки, но позволяет обойти некоторые ограничения.  


**Установка соединения:**

[CheckOraVersion](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_CheckOraVersion)

Проверка версии БД \(пользовательской схемы и UN4PUBLIC\). В случае, если имеющаяся версия ниже требуемой, вход в программу запрещен.

[CheckSecurityMode](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_CheckSecurityMode)

Режим привязки локального компьютера к имени пользователя \(можно выключить\)

[ShowLogin](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_ShowLogin).

Показывать окно регистрации \(можно отключить, если задать параметры Server, Login и Password\).

[OraHome](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_OraHome)

Выбор ORACLE Client для установки соединения с сервером ORACLE

[Server](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Server)

Сервер ORACLE по умолчанию

[Login](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Login)

Имя пользователя по умолчанию

[Password](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_Password)

Пароль по умолчанию

[OraUserName](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_OraUserName)

Имя схемы ORACLE по умолчанию

[OraPassword](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_OraPassword)

Пароль схемы ORACLE по умолчанию

[WindowsLogon](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_WindowsLogon)

Имя пользователя по умолчанию брать из операционной системы.

[LockUserName](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LockUserName)

Запретить изменение имени пользователя \(оно должно быть задано заранее параметром [Login](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#Login) или [WindowsLogon](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#WindowsLogon)\).

[SetLogo](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_SetLogo)

Включение режима случайного выбора логотипа на окне регистрации.

[LogoPath](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_LogoPath)

Размещение файлов с логотипами для режима SetLogo.  


**Отладочные возможности:**

[RunMaximized](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_RunMaximized)

Запуск программы в полноэкранном режиме \(можно отменить\).

[AutoRunCmd](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_AutoRunCmd)

Команда, которую надо выполнить сразу после запуска программы.

[AutoLoadScript](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_AutoLoadScript)

Файл скрипта, который надо загрузить сразу после запуска программы.

[SQLMonitorLog](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_SQLMonitorLog)

Режим протоколирования обращений к серверу \(работает при включенном параметре [SQLMonitorActive](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#SQLMonitorActive)\).

[SQLMonitorLogFile](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_SQLMonitorLogFile)

Имя файла протокола обращений к серверу. Можно задать или только имя файла \(в этом случае файл будет создан в каталоге для временных файлов\), или полный путь с указанием имени диска и каталога.

[SQLMonitorLogUnique](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_SQLMonitorLogUnique)

Режим генерации уникального имени файла протокола обращений к серверу.

[SQLMonitorLogLimit](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_SQLMonitorLogLimit)

Минимальный размер сообщения, подлежащего протоколированию \(отсечение "мусора"\).

[SQLMonitorActive](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_SQLMonitorActive)

Включить SQLMonitor \(соединение с программой SQLMonitor и протоколирование обращений к серверу\).

[UseProfiler](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_UseProfiler)

Режим измерения быстродействия программы.

[MeasureTraffic](file:///D:/UNA/UNA.md-130409-4.1.5.052/un4setup/init.html#_MeasureTraffic)

Режим измерения траффика и вывода отладочных сообщений.

