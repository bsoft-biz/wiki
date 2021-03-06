# startup.ini

| **Имя свойства**  | **Тип**  | **Описание**  | **Значение для примера**  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Language | String  | Язык интерфейса. Язык интерфейса задается либо цифрой \(0, 1, 2\), либо буквой \(E, M, R\).  Язык окна регистрации  задается только методом File. Если язык не задан ни одним из методов,  система переводов выключается на весь сеанс работы. |  2 |
|   |   | **Загрузка настроек, дизайнов, переводов и т.п.:** |   |
| LogParams  | Boolean  | Контроль настроек. Режим записи в текстовый файл всех считываемых настроек \(до и после обработки  и фильтрации\). | `true` |
| NewDesignMethod  | Boolean  | Быстрая загрузка. Режим быстрой загрузки настроек и дизайнов \(использование хранимых процедур и  меток времени\).  Требуется новый пакет ORACLE `UN$USERPARAMS`. | `true` |
| UsePackedIni  | Boolean  | Паковать настройки. Режим загрузки настроек в запакованном виде.  Требуется новый пакет ORACLE `UN$USERPARAMS`, сервер упаковки `PackSrv` должен быть запущен.  | `true` |
| TardyLoading  | Boolean  | Отложенная загрузка. Режим отложенной загрузки настроек.  Настройки отчетов загружаются только при первом открытии окна менеджера отчетов.  | `true` |
| UseLocalCache  | Boolean  | Файловый кеш дизайнов. Режим использования файлового кеша для сохранения настроек и дизайнов.  | `true`  |
| GridPropCacheLimit  | Integer  | Размер кеша дизайнов. Максимальный размер кеша дизайнов в памяти.  За единицу берется один тип  документа, один узел дерева отчетов, одна форма или справочник. | 100  |
| RepairGridDesign  | Boolean  | Исправление ошибок. Режим автокоррекции загружаемых дизайнов \(бывает нужен при работе с ORACLE 9i\).  | `true` |
| LangDontLoad  | Boolean  | Не загружать переводы. Не пытаться загружать тексты переводов из ORACLE \(для уменьшения  траффика\). | `true`  |
| LoadCaptionsSep  | Boolean  | Заголовки отдельно. Режим раздельной загрузки переводов заголовков столбцов и дизайнов  \(для совместимости с переводами заголовков столбцов, сохраненными в предыдущих версиях SL\).  | `true` |
|   |   | **Настройки форм и справочников системы:**  |   |
| HideMenuDict  | Boolean  | Меню справочников. Отображение меню "Справочники" \(по умолчанию включено\).  | `true`  |
| HideMenuReps  | Boolean  | Меню отчетов. Отображение меню "Отчеты" \(по умолчанию включено\).  | `true`  |
| HideMenuForms  | Boolean  | Меню форм. Отображение меню "Формы" \(по умолчанию включено\).  | `true`  |
|   |   |  **Панели инструментов:** |   |
| TBIconStyle  | Integer  | Расположение значков. Число от 0 до 3 означает положение значка относительно пункта главного меню: 0 - Значки не выводятся на экран \(в меню - только надписи\);  1 - Надписи не выводятся на экран \(в меню - только значки\);   2 - Значки выводятся на экран слева от соответствующих надписей;  3 - Значки выводятся на экран над соответствующими надписями. | 3  |
| TBIconSize  | Integer  | Размер значков. Число от 0 до 2 означает размер значков в главного меню:  0 - Мелкие значки;  1 - Средние значки;  2 - Крупные значки.  | 2  |
| TBPeriod  | Boolean  | Панель периодов. Отображать на экране панель ввода периодов.  | `true`  |
| TBWindowList  | Boolean  | Панель открытых окон. Отображать на экране панель открытых окон.  | `true`  |
|   |   | **Стартовая форма, фильтр по `NrSet` и т.п.:** |   |
| XDEF\_BGFILTER  | String  | Фильтр по умолчанию. Начальное значение фильтра по `NrSet`: здесь нужно перечислить  через запятую коды тех позиций фильтра, которые должны быть изначально включены.  \(Имеются в виду коды, которые можно увидеть в последнем столбце верхней таблицы в  окне установки фильтра по `NrSet` - колонка "№"\). Вместо списка кодов можно ввести символ "\*", что означает "включить все". |   |
| XDEF\_NRSET  | String  | `NrSet` по умолчанию. Начальное значение `NrSet` по умолчанию.  |   |
| XDEF\_NRSET\_VIEW  | String  | Ограничение по `NrSet`. Список кодов `NrSet`, которыми ограничиваются права пользователя.  |   |
| HideNrsetFilter  | Boolean  | Скрыть фильтр по `NrSet`. Не отображать установленный фильтр по `NrSet`.  | `true`  |
|   |   | **Настройки окна регистра документов \(в разделе "System settings" используется секция "Docs"\):** |   |
| ViewFromToday  | Integer  | Ограничение периода. Ограничение периода отображаемых документов  как смещение на указанное  число дней назад от текущей даты. |   |
| ViewBegin  | String  | Ограничение снизу. Минимальная дата отображаемых документов  | 01.01.2014  |
| ViewEnd  | String  | Ограничение сверху. Максимальная дата отображаемых документов  | 31.01.2014  |
| DEF\_JOURNAL  | String  | Стартовый журнал. Имя секции журнала, который надо открывать сразу после запуска программы.   |   |
| LastRecord  | Boolean  | К последнему документу. При открытии журнала документов переходить на последний видимый  документ. | `true` |
| ORDER BY  | String  | Порядок сортировки. Порядок сортировки документов \(список имен полей, разделенных запятыми\).  |   |
| DataAutomat  | Boolean  | DATAMANUAL как в пред.. Автозаполнение даты документов при вводе на основании даты предыдущего документа. | `true`  |
| DataCurrent  | Boolean  | DATAMANUAL сегодня. Автозаполнение даты документов при вводе на основании текущей даты.  | `true`  |
| DataEmpty  | Boolean  | Пустая DATAMANUAL. Отменить для пользователя автозаполнение поля DATAMANUAL  \(отмена глобальных параметров DataAutomat и DataCurrent\). | `true`  |
| PXCMSimpleEditing  | Boolean  | Режим быстрой правки. Режим быстрой правки проводок документов версии PX.  | `true`  |
| Backup  | Boolean  | Архив документов. Режим сохранения документов в архиве перед их удалением.  | `true`  |
|   |   | **Настройки окна менеджера отчетов:** |   |
| RepTreeFromSysS  | Boolean  | Отчеты из справочника. Добавлять в дерево отчетов список отчетов из системного справочника \(`SysS`\).  | `true`  |
| ReportTreeSorting  | Boolean  | Сортировка узлов. Режим сортировки узлов дерева отчетов по алфавиту.  | `true`  |
| StartupReportNode  | String  | Стартовый узел. Имя секции отчета, на котором позиционировать дерево отчетов сразу после открытия  окна менеджера отчетов. |   |
| RepTestRecordCount | Boolean  | Проверять к-во записей. Режим проверки количества записей в наборе данных отчета \(для F1Reports\):   при очень большом количестве записей выдается предупреждающее сообщение, имеется возможность  отменить построение отчета или вручную ограничить количество выводимых записей.  Предельное количество записей для отчетов Master/Detail - 1000, только Master - 10000. | `true`  |
| RepDeleteTempTables  | Boolean  | Удалять врем. таблицы. Режим удаления временных таблиц ORACLE после построения отчета \(можно выключить\).  | `true`  |
|   |   |  **Разные настройки:** |   |
| GridDisableNumberSearch  | Boolean  | Запрет числового поиска. Режим текстового поиска даже в числовых полях грида \(вместо числового поиска\). | `true`  |
| UseSmartTab  | Boolean  | "Умный" &lt;Tab&gt;. Режим интеллектуального поведения клавиши &lt;Tab&gt;: переход от поля к полю по всему  активному окну. | `true` |
| UseSmartEnter  | Boolean  | "Умный" &lt;Enter&gt;. Режим интеллектуального поведения клавиши &lt;Enter&gt; на дополнительной \(цифровой\)  клавиатуре:  при редактировании таблиц - переход к следующему полю или \(из последнего столбца\)  завершение редактирования и вставка новой записи. | `true`  |
| UseSpeedSearch  | Boolean | Быстрый поиск в справ.. Режим быстрого поиска в выпадающих справочниках.  | `true`  |
| AutoFreeMemory  | Boolean  | Выгружать неисп. DLL. Выгружать из памяти неиспользуемые динамические библиотеки \(DLL и BPL\).  | `true`  |
| UseDotInCont  | Boolean  | Точка в счете. Использовать точку в значении счета \(формат 99.99\) - удобно для ПМР.  | `true`  |
| EnableBDE  | Boolean  | Поддержка старой версии. При старте программы инициализировать подсистему BDE \(рекомендуется\).  | `true`  |
| NoCheckLocale  | Boolean  | Проверка при старте. При старте программы не проверять региональные настройки.  | `true`  |
| NoCheckFreeSpace  | Boolean  | Проверка при старте. При старте программы не проверять свободное место на дисках.  | `true`  |
| OraLoaderModeDML  | Boolean  | Режим загрузки данных. Использование DML при загрузке данных из текстового файла или таблицы BDE.  Этот режим снижает скорость загрузки, но позволяет обойти некоторые ограничения. | `true`  |
|   |   | **Установка соединения:**  |   |
| CheckOraVersion  | Boolean  | Проверка версии БД. Проверка версии БД \(пользовательской схемы и `UN4PUBLIC`\).  В случае, если имеющаяся версия ниже требуемой, вход в программу запрещен. | `true`  |
| CheckSecurityMode  | Boolean  | Режим привязки локального компьютера к имени пользователя \(можно выключить\)  | `true`  |
| ShowLogin  | Boolean  | Показывать окно регистрации \(можно отключить, если задать параметры Server, Login и Password\).  | `true`  |
| OraHome  | Integer  | Выбор ORACLE Client для установки соединения с сервером ORACLE  |   |
| Server  | String  | Сервер ORACLE по умолчанию  | oratest  |
| Login  | String  | Имя пользователя по умолчанию  |  |
| Password  | String  | Пароль по умолчанию  |  |
| OraUserName  | String  | Имя схемы ORACLE по умолчанию  | `dev`  |
| OraPassword  | String  | Пароль схемы ORACLE по умолчанию  | `dev`  |
| WindowsLogon  | Boolean  | Имя пользователя по умолчанию брать из операционной системы.  |   |
| LockUserName  | Boolean  | Запретить изменение имени пользователя \(оно должно быть задано заранее параметром Login или WindowsLogon\). |   |
| SetLogo  | Integer  | Включение режима случайного выбора логотипа на окне регистрации.  | 1  |
| LogoPath  | String  | Размещение файлов с логотипами для режима SetLogo. \(Файл должен быть в формате .jpg\) | Logo.jpg  |
|   |   | **Отладочные возможности:**  |   |
| RunMaximized  | Integer  | Окно во весь экран. Запуск программы в полноэкранном режиме \(можно отменить\).  | 1 |
| AutoRunCmd  | String  | Стартовое действие. Команда, которую надо выполнить сразу после запуска программы.  |   |
| AutoLoadScript  | String  | Файл скрипта. Файл скрипта, который надо загрузить сразу после запуска программы.  |   |
| SQLMonitorLog  | Boolean  | Запись в журнал. Режим протоколирования обращений к серверу \(работает при включенном параметре  SQLMonitorActive\). |   |
| SQLMonitorLogFile  | String  | Имя файла. Имя файла протокола обращений к серверу. Можно задать или только имя файла  \(в этом случае файл будет создан в каталоге для временных файлов\), или полный путь с указанием имени диска и каталога.  | monitor.log  |
| SQLMonitorLogUnique  | Boolean  | Уникальность. Режим генерации уникального имени файла протокола обращений к серверу.  | `true`  |
| SQLMonitorLogLimit  | Integer  | Нижний предел. Минимальный размер сообщения, подлежащего протоколированию \(отсечение "мусора"\). | 100  |
| SQLMonitorActive  | Boolean | Включение SQLMonitor. Включить SQLMonitor \(соединение с программой SQLMonitor и протоколирование обращений к серверу\). | `true`  |
| UseProfiler  | Boolean  | Замер быстродействия. Режим измерения быстродействия программы.  | `true`  |
| MeasureTraffic  | Boolean  | Изменение трафика. Режим измерения трафика и вывода отладочных сообщений.  | `true`  |
|   |   |  **Быстрый вход:** |   |
| SpecLogin  | String  | Вход по Shift+F12 \(работает в паре с SpecPassword\) | admin  |
| SpecPassword  | String | Вход по Shift+F12 \(работает в паре с SpecLogin\)  | admin  |

текст файла \(некоторые свойства\) startup.ini, который по необходимости надо создать в папке с гудом либо на уровень выше:

\[General\]

SQLMonitorActive=1

SQLMonitorLog=1

SQLMonitor

LogFile=sqlmon.log =&gt; monitor вкл-ся при запуске

WarnBackupDays=0 =&gt; при входе не спрашивает про backup. Убрать предупреждение Внимание отсутствует архив базы данных!

CheckDBVersion=0 =&gt; при входе не сообщает о несоответствии версий гуда и апгрейда

InitLog=1 в папке с гудом есть такой файлик uniacCLNT.log. Если он автоматически не создается, то надо добавить данное свойство

\[moldabela@catalog\] или \[General\]

SpecLogin=comenzi

SpecPassword=comenzi =&gt;вход по Shift+F12

12.01.2005

Настройка программы для работы с медленным каналом

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Такая настройка включает в себя следующие действия:

0. Ограничение записей un4sysdata в administrator настройкой св-ва

на уровне группы пользователей UserRecords, например UserRecords=1,2,3

1. Включение кеша дизайнов в ОЗУ

2. Включение файлового кеша дизайнов и настроек

3. Включение режима упакованных дизайнов и настроек

Для работы с новыми возможностями надо прописать свойство

NewDesignMethod=1

в файле startup.ini

Включение кеша дизайнов в ОЗУ

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Для включения кеша дизайнов в ОЗУ надо прописать свойство

GridPropCacheLimit=20

Значение этого параметра - максимальное количество узлов, одновременно

кешируемых в оперативной памяти. Под узлом здесь понимается документ,

отчет или справочник. Документы одного типа \(общий SysFID\) используют

один и тот же узел кеша.

Свойство GridPropCacheLimit может быть прописано в файле startup.ini,

в 'System Settings', на уровне группы или отдельного пользователя

\(перечислено в порядке возрастания приоритета\).

Включение файлового кеша дизайнов и настроек

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Для включения файлового кеша дизайнов и настроек надо прописать свойство

UseLocalCache=1

в файле startup.ini

Включение этого свойства приводит к сохранению настроек и дизайнов

в специальном файле \(в каталоге для временных файлов\), откуда они

могут быть в дальнейшем загружены \(вместо закачки с сервера\).

Для каждого пользователя создается отдельный файл, поэтому настройки

не пересекаются. Каждый дизайн и каждый раздел настроек сохраняется

со своей меткой времени \(timestamp\). Таймстамп содержит дату и время

создания или последней модификации блока данных и хранится на сервере

вместе с каждым дизайном или разделом настроек. При внесении изменений

в настройки или при новом сохранении дизайна таймстамп изменяется,

и при следующем обращении программы к кешу тот обнаруживает изменение

и инициирует новую закачку с сервера, помещая результат вместо старой

информации.

Включение режима упакованных дизайнов и настроек

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Для включения режима упакованных дизайнов и настроек нужно сделать

следующее: на стороне сервера запустить сервер упаковки \(и обеспечить

его автоматический запуск при старте системы\), а на стороне клиента

прописать свойство

UsePackedIni=1

в файле startup.ini

Сервер упаковки - это программа PackSrv.exe

Настройка сервера упаковки выполняется при помощи файла PackSrv.ini

в том же каталоге, где и файл PackSrv.exe - при отсутствии этого файла

достаточно один раз запустить сервер упаковки и установить соединение

с требуемым сервером Oracle, и файл будет создан автоматически.

Сервер упаковки использует для соединения c Oracle схему UN4PUBLIC

Примечание

~~~~~~~~~~

Свойства NewDesignMethod, UseLocalCache и UsePackedIni

должны быть прописаны в файле startup.ini, так как их значения

должны быть известны до загрузки настроек.

