# History

{% hint style="info" %}
 Этот файл ведется для разработчиков \(тех, кому понятно его содержимое\)
{% endhint %}



\# По всем вопросам обращаться к ним или лично к разработчикам

Build 4.1.5.052 \(09.04.2013\) Private DB version 617, Public DB version 613

:Public DB version

 - Добвалены изменения в процедуру CashBook

:uniacCLNT

 - Добавлен новый параметр DATETIMEX в Actions, который должен давать 

   возможность редактировать дату и время в процессе выполнения Action

 - Добавлена возможность переключаться из Action формы в любую другую секцию

   установив текстовые свойства\(TargetType и TargetSection\)соответствующими значениями

 - Добавлен новый параметр для выполнения скриптов :shell \(Действует как: BATCH, VBSCRIPT, XLSCRIPT\)

:SimpleControls5.bpl

 - Исправлен глюк установки формата даты при запуске клиента

:unDG1.bpl

 - Добавлен DG1p26 настраиваемый Tabel de pontaj

Build 4.1.5.051 \(18.03.2013\) Private DB version 617, Public DB version 613

:uniacCLNT

 - Добавлены переводы в DbNavigator

 - Добавлено логическое свойство DontEditReport, значение true, которого 

   запрещает редактирование отчета \(FormulaOne, FastReport2, FastReport4\)

:Asagi4.bpl

 - Исправлена проблема двойного клика по загаловку грида

:Asagi4ag.bpl

 - Исправлена проблема TDBRadioGroup

Build 4.1.5.050 \(27.02.2013\) Private DB version 617, Public DB version 613

GOOD СОБРАН В ОС WINDOWS-7

:Fr25.bpl

 - Добавлены функция abs в  FastReport 2.5

:Asagi4.bpl

 - Добавлено свойство UnPrepareFloatFieldKey type=bool в TStaticDBGrid для обработки вводимых значений в полях грида       типа ftFloat

:F1Report.bpl

 - Оптимизирована процедура выгрузки в excel

Build 4.1.5.049 \(04.02.2013\) Private DB version 617, Public DB version 613

:uniacCLNT

 - Исправлен баг снятия фильтра на вкладке CMX

 - Исправлен баг просмотра  OleObject на вкладке объектов

:F1Report.bpl

 - Добавлены система установки логотипа в отчетах:

   1. В templates добавить файл vts, в который надо встаить картинку логотипа.

   2. В администраторе добавить текстовое свойство LogoPath и указать путь к файлу логотипа.

   3. В шаблоне в ячейке сделать метку \[logo,height,width\].

:unDBr.bpl

 - Добавлено свойство UseAlexComScales type=string\(Values:true,false\) для использования 

   AlexCOM.exe драйвера для весов в DllName=ALFA\_NISTRU\_CINTAR.

:std.pak

 - Изменены обьекты модуля заявок

Build 4.1.5.048 \(17.01.2013\) Private DB version 616, Public DB version 613

:uniacCLNT

 - Добавлены переводы в стандартные справочники

:unFSal2.bpl

 - Добавлено 10 лет в форму по зарплате "Календарь"

:std.pak

 - Изменен триггер TRIG\_TMDB\_CM\_AINS

Build 4.1.5.047 \(26.12.2012\) Private DB version 616, Public DB version 613

:unRG1.bpl

 - Исправлен баг перестроения универсального отчета.

 - Исправлен баг выбора полей универсального отчета по CMX.

Build 4.1.5.046 \(11.12.2012\) Private DB version 616, Public DB version 613

:unFSal1.bpl

 - Добавлено сво-во UseNrsetFilter типа Boolean, указывается на уровне формы "Справочник сотрудников",

   на базе должна быть функция MAKE\_TMS\_NRSET\_FILTER, которая идет в сборке нового гуда - эти два элемнта 

   позволяют фильтровать выпадающий справочник nrset на форме зарплаты

 - Исправлен глюк открытия справочника сотрудников из документов.

 - Исправлен баг функции Drag&Drop в EasyInterface.

:std.pak

 - Добавлены обновленные пакеты по зарплате

Build 4.1.5.045 \(07.12.2012\) Private DB version 615, Public DB version 613

:uniacCLNT

 - Добавлено сво-во ViewFilesObjects типа Boolean ,включает режим просмотра файлов в документе 

   на вкладке Объект

 - Добавлен перевод для надписи подтверждения документа

 - Решена проблема с регистрацией FR 2.51

Build 4.1.5.044 \(29.11.2012\) Private DB version 615, Public DB version 613

:uniacCLNT

 - Добавлено текстовое сво-во EAutoConfirmDocument на уровне документа, в котором можно указать

   id Экшенов в правильном порядке, которые надо выполнять при сохранении документа.

   Если это свойство установлено и непустое, то при сохранении документа появляется диалоговое окно с вопросом:            

   Утвердить ли документ?

 - Добавлено логическое сво-во UseDropInsertDocument на уровне формы, значение true, которого позволяет 

   использовать Drag&Drop на форме\(Только EasyInterface\).

:unFSal2.bpl

 - Добавлено свойство CloseImmediateVideoCatch type=bool для закрытия unVideoCatch после получения фото.

:unFSal1.bpl

 - Добавлена поддержка Actions при нажатий Button в настраевомых формах из ts02

:unForms1.bpl

 - Добавлен таб tehcomplectTS10\(Дор. операций\) в tsTehComplect.

 - Добавлено свойство ControlParams type=memo

   ex:tehcomplectTS1:Hello1

      tehcomplectTS3:Hello2

где tehcomplectTS1 имя компонента

   Hello1 его Caption

 - Добавлены табы в tsTehComplect: Размотка, PrePrint, OffsetPrint,PostPrint.

Build 4.1.5.043 \(13.11.2012\) Private DB version 615, Public DB version 613

:unFSal2.bpl

 - Добавлено свойство UseAlexComScales type=bool для использования AlexCOM.exe 

   драйвера для весов.

 - Добавлено свойство DisableRealTimePreview для отключения видеозахвата с NetDVR камер

   и осуществления лишь фотографий

:uniacCLNT

 - В форму TimeLine\(Органайзер\) добавлен поиск по Event-ам

 - Добавлено логическое сво-во SaveToDoc, которое устанавливается на уровне печатной формы 

   и создает поток, данных который может быть сохранен в blob поле tmdb\_docs\_ole.

   Для вставки строки с blob полем необходимо перед формированием печатной формы добавить 

   инициализацию сисконтекстов \(streamtodocument\_caption, streamtodocument\_comment

   ,streamtodocument\_nrdoc\)

 - Stream\_Invisible - логическое свойство, которое устанавливается на уровне печатной формы. Значение true делает построение формы невидимым.

 - Сво-во frxEmbeddedFonts = true , добавляет Fonts в pdf \(только для FastReport\)

 - Сво-во frxStreamExt = '.pdf' определяет формат выгружаемого потока \(только для FastReport\)

 - Исправлен горизонтальный Splitter в uPDC \(Plan de conturi\)

 - Убраны кнопки навигатора и добавлены новые кнопки "Добавить документ" и "Дублировать документ"

 - Кнопка с переводами убрана в меню "Сервис"

 - Добавлено логоческое свойство, UseSensitiveDates, значение true,

   которого сразу меняет значение контекстов 'UN$REPDATASTART','UN$REPDATAEND'

   для конкретного отчета

:unFSal1.bpl

 - Добавлена возможность сортировки вкладок справочника сотрудников

   Сортировка производится в соответствии с указанием вкладок в сво-ве AuxVisibleTabs

:unFMAgr

-  Добавлено свойство DisablePrintFoils для Items в CashDesk

:unForms1.bpl

 - Добавлено свойство MasterDetailSQ type=Memo для определения компонентов Master Detail, образец свойства: gr01:pn02 

   где gr01 это TUnDBGrid и pn02 это TUnDBPanel.

 - Добавлена настраиваемая форма tsTehComplect

Build 4.1.5.042 \(24.09.2012\) Private DB version 615, Public DB version 613

:Public DB

-  Добавлен функция Tokenizer, которая позволяет из строки сделать делать 

   столбик используя любой указаный разделитель

:unFSal1.bpl

-  Добавлены настраиваемые вкладки ts02p1p11,ts02p1p12,ts02p1p13,ts02p1p14,

   ts02p1p15,ts02p1p16,ts02p8,ts02p9.

   ts02p1p 11-Comp Familiei,12-Familia,13-Carnet de munca,14-Document identitate,15-Generale,16-Militare 

   ts02p8 - Parametri, ts02p9 - Plan. 

-  Добавлено свойство FamilyShowPanel, для отображения настраиваемой панели на ts02p1p11

   type bool

-  Добавлено свойство FamilyPanHeight, для изменения высоты настраиваемой панели на ts02p1p11

   type string ex: 300

-  Добавлено свойство AuxVisibleTabs, для отображения настраиваемых вкладок

   type string ex: ts02p1p11,ts02p1p12,ts02p1p13,ts02p1p14,ts02p1p15,ts02p1p16,ts02p8,ts02p9

-  Добавлено свойство GenTabNavProp, для изменения позиций и размеров навигатора в ts02p1p15 

   type string

   Top:Left:Height:Width ex: 10:10:50:200

-  Добавлено свойство GenPanPProp, для изменения позиций и размеров настраиваемой панели в ts02p1p15

   type string

   Top:Left:Height:Width ex: 10:10:50:200

-  Добавлено свойство PlanPanVisible, для отображения настраиваемой панели на ts02p9

   type bool

-  Добавлено свойство FormMuncGridWidth, для изменения ширины левого грида 

   type string

   ex: 300

Build 4.1.5.040 \(24.09.2012\) Private DB version 615, Public DB version 612

:unFSal1.bpl

-  Добавлены настраиваемые вкладки ts02p1p11,ts02p1p12,ts02p1p13,ts02p1p14,

   ts02p1p15,ts02p1p16,ts02p8,ts02p9.

-  Добавлено свойство FamilyShowPanel, для отображения настраиваемой панели на ts02p1p11

-  Добавлено свойство FamilyPanHeight, для изменения высоты настраиваемой панели на ts02p1p11

-  Добавлено свойство AuxVisibleTabs, для отображения настраиваемых вкладок

-  Добавлено свойство GenTabNavProp, для изменения позиций и размеров навигатора в ts02p1p15 

-  Добавлено свойство GenPanPProp, для изменения позиций и размеров настраиваемой панели в ts02p1p15

-  Добавлено свойство PlanPanVisible, для отображения настраиваемой панели на ts02p9

Build 4.1.5.041 \(16.08.2012\) Private DB version 615, Public DB version 612

:unFMAgr.bpl

 - У элемента меню CashDesk добавлено свойство Hidden - "не показывать в меню"

 - У контролов типа TUnDBEdit, отражающих атрибуты платежа, использованы

   свойство DisableBtnPressForReadOnlyField и событие BeforeShowList

:Asagi4.bpl

 - У компонента TSagiEdit добавлено свойство DisableBtnPressForReadOnlyField

 - У компонента TSagiEdit добавлено событие BeforeShowList

Build 4.1.5.040 \(03.08.2012\) Private DB version 615, Public DB version 612

:unFSal1.bpl

 - Добавлено свойство UseRestoreGridPos, которое позволяет сохранять

   фокус на том же месте после REFRESH

:F1Report.bpl

 - Функция SendMessage была заменена на функцию SendNotifyMessage

Build 4.1.5.039 \(26.07.2012\) Private DB version 615, Public DB version 612

:uniacCLNT

-  Добавлено свойство charset типа String на уровне System-&gt;Setings, которое 

   меняет значение charset у всех визуальных компонентов программы, необходимо 

   для поддержки диакритических знаков в

:unFMAgr.bpl

-  Добавлено свойство AutomatOnly, которое позволяет автоматически заполнять

   нередактируемые атрибуты

:F1Report.bpl

-  Добавлена возможность запуска XLScript через кнопку выгрузки в Excel

-  добавлен обработчик значения ячейки, который устанавливает значение, 

   как текст, в случае, если значение более 18 символов

Build 4.1.5.038 \(01.06.2012\) Private DB version 615, Public DB version 612

:unSal01.bpl

-  В настраиваемую форму добавлено сво-во логического типа

   UseRefreshMaster, если true, то все мастер гриды обновляются

:unForms1.bpl

-  Добавлена новая форма SmartForm dll = 8000

:F1Report.bpl

-  Исправлен баг с отрисовкой точки в отчете FormulaOne

Build 4.1.5.037 \(21.05.2012\) Private DB version 615, Public DB version 612

:uniacCLNT.exe

-  Добавлено bool свойство EndEditDocLastRow, которое дает возможность перехода 

   на последний документ в списке, если значение true. Если значение false

   ,то focus остается на текущей строке. 

:unSal01.bpl

-  В справочнике сотрудников данные подгружаются только при открытой вкладке

:F1Report.bpl

-  Исправлен баг функции CopyCell при отрисовке отчетов

:Private DB version 

-  Добавлены новые объекты по зарплате.

Build 4.1.5.036 \(20.04.2012\) Private DB version 614, Public DB version 612

:uniacCLNT.exe

-  Добавлено изменение размеров формы в зависимости от кол-ва действий или печатных форм

:F1Report.bpl

-  Добавлено текстовое свойство на уровне General -&gt; DontUseTmpFile = true  запрещает 

   создание временных файлов. 

:unFMAgr

-  Добавлена возможность вносить поля типа "UNIV" в чеки

-  Удалено поле проверки кода в универсе \(cod\_ok\)

Build 4.1.5.035 \(09.04.2012\) Private DB version 613, Public DB version 612

:AllInOne.dll 

-  Переведена на с++ и добавлена в клиента.

:uniacCLNT.exe

-  Добавлено AllInOne.dll и исправлены вызовы ее

-  Изменен отступ между кнопками и краем формы в списке действий

-  Сделан фокус сразу на первое активное действие в списке действий

Build 4.1.5.034 \(23.03.2012\) Private DB version 613, Public DB version 612

:uniacCLNT.exe

-  Добавлено логическое свойство HideDeleteDocButton, которое скрывает кнопку удаления 

   документов в EasyInterface

-  Убраны на форме кнопки min/max

-  закрытие формы по клавише ESC

-  увеличено на пробел отступ слева до кнопок

-  более явное отличие цветов фона формы и кнопок

-  перемещение мышкой по кнопкам выделяется цветом и утоплением

-  отключенные \(недоступные\) действия выделяются серым цветом

-  шаблоны для форм печати открываются сочетанием клавиш Ctrl+Shift+t;

-  увеличено расстояние между кнопками по вертикали

-  перемещение по кнопкам с помощью клавиатуры - стрелки вверх/вниз, выбор по ENTER и пробел;

:F1Report.bpl

-  Добавлена обработка формата ячейки\(General\) для нормальной отрисовки в SpreadSheet

:UNIAksdk.bpl

-  Исправлена подгрузка LangSelector при открытии стандартной карточки

Build 4.1.5.033 \(07.03.2012\) Private DB version 613, Public DB version 612

:uniacCLNT.exe

-  В свойства DeleteALLFCFromCM,DeleteFCFromCM добавлено удаление из CMX

-  Добавлена возможность добавлять кнопки вставки и удаления документов 

   в форму в отсутствии Actions

:unUniv01.bpl

-  Добавлены переводы на некоторые позиции согласно заявке

:unSal01.bpl

-  Исправлен глюк обновления формы. Метод RefreshDates\(\).

:cxSpreadSheetVCLC5.bpl

-  Доработана сво-во Alignment для формата General

:dcldxPSCoreC5.bpl

-  Синхронизация FitToPage c Excel

Build 4.1.5.032 \(24.02.2012\) Private DB version 613, Public DB version 612

:uniacCLNT.exe

- UseDMLLastRow включает синхронизацию с регистром документов

  На вкладке XTT Summary указывается поле для синхронизации

  Пример: KEYFIELD="cod"

- Добавлена проверка версии Windows и отключение AllInOne если необходимо.

:cxSpreadSheetVCL5.bpl

- Произведены дороботки по форматам отображения SpreadSheet

- Добавлена передача параметров печати из FormulaOne в PrintingSystem

:ASAGI4ag

- Исправлена обработка поля TabOrder в настраиваемых панелях

Build 4.1.5.031 \(06.02.2012\) Private DB version 613, Public DB version 612

:uniacCLNT.exe

-  Добавлена функция FindWinControl для расширенного поиска компонентов

-  UseDMLLastRow bool 

-  Свойство выделяет последнюю строку первого грида после DML операций

-  Добавлено новое свойство UseEasyInterface bool

-  Переключает режим списка документов, в дальнейшем будет использоваться

   для определение характеристик принадлежащих только EasyInterface.

   versions

-  Убрали wm\_concat на ,rtrim\(extract\(SYS\_XMLAGG\(XMLELEMENT\("X",cols\|\|','\)\), 

   '//text\(\)'\).getStringVal\(\),','\) cols

-  TCmpInfo::MSCreateView\(\) переделана из ошибки в предупреждение

-  Добавлены новые компоненты SpreadSheet и PrintingSystem.

-  Добавлена возможность нестандартной обработки Insert в EasyInterface

Build 4.1.5.030 \(10.01.2012\) Private DB version 613, Public DB version 612

:uniacCLNT.exe

-  Добавлено bool свойство UseModalDocList, которое меняет внешний вид окна

   выбора документов. Свойство проставляется на уровне секции пользователя.

-  Добавлено String свойство SQL\_DOC\_FILTER на форме, при добавлении, которого на 

   форму в список действий добавляется кнопка \[Document\], которая позволяет 

   создавать документы

:unFSal1.bpl

-  Добавлено bool свойство, в секции формы UseClickFormRefresh, которое 

   обновляет уже открытую форму при переходе на нее форму.

:F1Report.bpl

-  Обработана ошибка при построении отчетов FormulaOne

   \(Access violation... in module 'TTF16.ocx'\) 

Build 4.1.5.029 \(26.12.2011\) Private DB version 613, Public DB version 612

:uniacCLNT.exe

-  iDbgrid добавлено для устранения проблемы загрузки дизайна подчиненного грида 

   в процессе загрузки базового  грида

-  Добавлено bool свойство UseEventList, которое меняет внешний вид окна

   для действий и печатных форм.

Build 4.1.5.028 \(26.12.2011\) Private DB version 613, Public DB version 612

:unFMAgr.bpl

-Доработан пункт меню Invoice, добавлено свойство InvoiceDesignPrefix

 ,которое позволяет сохранять свой дизайн для формы инвойс.

:uniacCLNT.exe

- Поправлено открытие форм по умолчанию в EasyInterface:

:un4Public

 Добавил исправленный пакет UN$G$UTIL

Build 4.1.5.027 \(19.12.2011\) Private DB version 612, Public DB version 611

:uniacCLNT.exe

- Доработано свойство SilentStartMode:

    исправлено закрытие формы с ошибками

    возможность открыть форму с ошибками через меню Service.

- Windows7 : отключен механизм подмены окна приложения

  заблокированным окном, которое отображается пользователям как

  белый экран.

:unUniv01.bpl

- Добавлена галочка "Вес" в карточку товара

- Добавлена восможность редактирования  в ospMPT\_TVR\(Comp-ta tehn\)

Build 4.1.5.026 \(17.11.2011\) Private DB version 612, Public DB version 611

:uniacCLNT.exe

- EasyInterface Устранен баг, возникающий при попытке входа в режим

  редактирования на тех этапах, где редактирование запрещено

 \(вместо открытия режима редактирования документа постоянно 

  открывается  контракт на поставку товаров в фирмой Fermina

 SRL\). Или исчезает верхнее меню журналов.

- EasyInterface  в одном журнале делаем действие для придания

  другого статуса. при этом док-ты закрывается для

  редактирования и док-т попадает в другой журнал. 

  Что бы действие вступило в силу необходимо обновить журнал документов.

  Добавлено свойство isRefreshDocs

Build 4.1.5.025 \(14.11.2011\) Private DB version 612, Public DB version 611

:unFSal1.bpl

 - расширен Edit для ввода фискального кода

:uniacCLNT.exe

 - Исправлен глюк перехода из отчета в документ по номеру

   двойным щелчком

 - Исправлен глюк перехода в режим редактирования шаблона из

   отчета нажатием Alt+B

 - Исправлен глюк открытия документа из форм Easy Interface

Build 4.1.5.024 \(04.11.2011\) Private DB version 612, Public DB version 611

:uniacCLNT.exe

 -Добавлен компонент FRTeeChart для построения диаграмм в FastReport4

 -Добавленf обработка свойства isMultiAccess, которое добавляет возможность

  одновременного редактирования

:unUniv01.bpl

 -Добавил поле barcode на вкладке ambalaj по умолчанию

Build 4.1.5.023 \(28.10.2011\) Private DB version 611, Public DB version 611

:uniVersion

 -Исправлен глюк со сво-вом ShemaList

 -Добавлены окна подтверждения при сохранении данных

:Asagi4.bpl

 -добавлена обработка первой строкой XML

:uniacCLNT.exe

 -Исправлен глюк с расширением иконок панели задач

Build 4.1.5.022 \(24.10.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

  -Добавлена возможность добавлять цифры как HotKey для журналов.

  -Добавлено поле ScreenShot в таблицу XLOG\_PRINT

  -Добавлено обработка свойства LogPrinting на уровне отчета

  -SQLBeforeRep сво-во администратора на уровне отчета

  ,группы отчетов и в General обрабатывает PL/SQL перед запуском отчетов.

   :SECTION параметр обрабатываемый в сво-ве SQLBeforeRep, 

   возвращает имя текущей секции.

   :ROOT\_SECTION параметр обрабатываемый в сво-ве SQLBeforeRep, 

   возвращает имя секции, в которой установлено свойство.

:pgUNIACsdk.bpl

 - В настраиваемой карточке на вкладках добавлена обработка свойства 

 -"Tab\(1\)PanelWidth"

Build 4.1.5.021 \(03.10.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - Добавлен новый пункт меню "Сервис" - "Атрибуты"

:unForms1.bpl

 - Добавлена новая форма Atribute

:unUniv01.bpl

 - Добавлена обработка InternalAction "attr"/"fmUn01sShowModal"

:pgUNIACsdk.bpl

 - В класс TUnivList добавлен метод fmUn01sShowModal\(\)

 - В настраиваемой карточке добавлена обработка свойства "PanelWidth"

Build 4.1.5.020 \(20.09.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - Добавлена обработка свойств "SilentStartMode" и "ShowErrorsModal"

Build 4.1.5.019 \(16.09.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - В модуле TdmvM1 добавлен обработчик GridPropCmpSetDisplayFormatNumeric\(\)

 - В методе TdmvM1::InitializeAll\(\) доб. обр. св-ва "DisplayFormatEnabled"

:ASAGI4ag.bpl

 - В методе TUnRseManager::MakeFilter\(\) добавлена проверка AFD-&gt;Selected

 - В методе ctAvFieldsStateChange\(\) добавлен вызов SetupFilterTotal\(\)

:SimpleControls5.bpl

 - В методе TUnPropClass::ApplyValues\(\) доб. обр-ка ошибки "ShowCheckbox mode"

:Asagi4.bpl

 - В классе TGridPropCmp добавлено свойство UseDefaultDisplayFormat

 - В классе TGridPropCmp добавлено событие OnSetDisplayFormatNumeric

 - В классе TGridPropCmp добавлен метод SetNumericDisplayFormat\(\)

 - В функции SetupFieldsAfterOpen\(\) добавлен вызов SetNumericDisplayFormat\(\)

Build 4.1.5.018 \(13.09.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - В методе TParamInfo::CheckValue\(\) доб. проверка новых свойств параметров

   \(.minlen., .maxlen. и .required., а также новый тип значения - alpha\)

:SimpleControls5.bpl

 - В методе TF1PivotData::JoinPivotCols\(\) исправлена ошибка с Objects == NULL

Build 4.1.5.017 \(09.09.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - Добавлено исправление кодовой страницы системных шрифтов в Windows profile

:Versions.exe

 - В методе TfrSchema::InternalSetXMLText\(\) добавлен учет свойства SchemaList

:ASAGI4ag.bpl

 - В классе TUnDBPanel добавлен контроль ошибки при установке св-ва DataField

Build 4.1.5.016 \(07.09.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - В конструкторе класса TParamInfo доб. обр. св-ва ".filter.???" для ctFile

   \(Пример: \[.filter.file=MS Excel files \(\*.xls\)\|\*.xls\|All files \(\*.\*\)\|\*.\*\]\)

 - В методе TParamInfo::GetWidth\(\) доб. обр. св-ва ".width.???"

 - В конструкторе класса TfParams доб. алгоритм подстройки ширины окна

 - В методе TfRegistru::GotoDocument\(\) доб. обр. св-ва "Editing"

:pgUNIACsdk.bpl

 - В методе TfUnivList::try1cEdit\(\) доб. обр. св-в "FormWidth" и "FormHeight"

Build 4.1.5.015 \(18.08.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - В методе TfSelNrSet::SetServerFilter\(\) проверка ошибки вынесена на сервер

:F1Reports.bpl

 - В методе TfrmPreviewF1::OpenBook\(\) доб. вызовы Show\(\) и Hide\(\)

Build 4.1.5.014 \(10.08.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - Добавлена обработка параметров типа file и filename - загрузка в BLOB

Build 4.1.5.013 \(04.08.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - В методе TfRegistru::DocsFixupChanges\(\) доработан алгоритм \(см. комм.\)

:unFMAgr.bpl

 - В кассовой форме добавлено свойство элемента меню NoTVA \(2011072810826\)

Build 4.1.5.012 \(28.07.2011\) Private DB version 611, Public DB version 611

:SimpleControls5.bpl

 - В методе TUnDevice::GetDateTime\(\) доработан алгоритм обработки ошибки

Build 4.1.5.011 \(05.07.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - Доработан механизм переходов на экшены и печатные формы экранных форм

Build 4.1.5.010 \(23.06.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - Исправлена работа с вкладкой "Объект" в режиме ReadOnly \(включены кнопки\)

:uniVersions.exe

 - В командном режиме для функций экспорта/импорта добавлен параметр DirPath

   \(сетевой путь к папке, на которую ссылается используемая Oracle Directory\)

Build 4.1.5.009 \(07.06.2011\) Private DB version 611, Public DB version 611

:unFSal1.bpl

 - В форме "Справочник сотрудников" исправлен порядок инициализации вкладок

Build 4.1.5.008 \(01.06.2011\) Private DB version 611, Public DB version 611

:unFMAgr.bpl

 - В кассовой форме учтены замечания по интерфейсу

 - В методе TdmFMAgrA::d8BookTest\(\) добавлена проверка даты последнего чека

:uniVersions.exe

 - Вынесены на интерфейс командные режимы CmpLog, Analyze, SrcCod и Compile

 - Добавлено управление св-вами экспорта "Компилировать" и "Сжимать сальдо"

:ASAGI4ag.bpl

 - В классе TUnDBPanel доб. метод KeyUp\(\) и сброс флага FUsingEnterLikeTab

:F1Reports.bpl

 - В окне просмотра отчета/печатной формы доб. обработка нажатия клавиши F12

 - В окне просмотра отчета/печатной формы доб. обработка флага SkipShowModal

 - В методе TfrmPreviewF1::Setup\(\) добавлено управление строкой состояния

:SimpleControls5.bpl

 - В методе TUnFiscalPrinter::Validate\(\) исправлена еще одна ошибка округления

 - В методе TUnFPMercury114::DoPrintCheckItem\(\) доб. проверка DocFiscal для 0

 - В классе TUnFPDummy удалено перепределение вирт. метода DoGetCashTotal\(\)

Build 4.1.5.007 \(24.05.2011\) Private DB version 611, Public DB version 611

:unFMAgr.bpl

 - В кассовой форме учтены замечания по интерфейсу

:F1Reports.bpl

 - Исправлены ошибки, возникающие при работе формы в модальном режиме

Build 4.1.5.006 \(16.05.2011\) Private DB version 611, Public DB version 611

:unFMAgr.bpl

 - В кассовой форме добавлено логирование операций синхронизации времени

Build 4.1.5.005 \(10.05.2011\) Private DB version 611, Public DB version 611

:unFMAgr.bpl

 - В кассовой форме добавлена обработка свойства "HideDivName"

Build 4.1.5.004 \(06.05.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - В модуле uTabCtrl исправлен алгоритм поиска следующего контрола

:unFMAgr.bpl

 - В печатных формах CashDesk добавлена обработка свойства "IsFactura"

 - В методе SWCCashDeskOpen\(\) критическая разница во времени ум. до 10 минут

Build 4.1.5.003 \(03.05.2011\) Private DB version 611, Public DB version 611

:unFMAgr.bpl

 - В методе TdmFMAgrA::sq8hdrBeforeInsert\(\) добавлена проверка D8CheckId

Build 4.1.5.002 \(28.04.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - В модуле uTabCtrl добавлено логирование всех шагов алгоритма

 - Доб. св-во "UseSmartTabLog" \(работает только в startup.ini при InitLog=1\)

:unFMAgr.bpl

 - В кассовой форме добавлен обработчик TdmFMAgrA::sq8hdrBeforeInsert\(\)

Build 4.1.5.001 \(21.04.2011\) Private DB version 611, Public DB version 611

:unFMAgr.bpl

 - В кассовой форме исправлена ошибка, связанная с пустой датой в истории

Build 4.1.5.000 \(21.04.2011\) Private DB version 611, Public DB version 611

:uniacCLNT.exe

 - Добавлен вызов TUnUpgMan-&gt;Execute\(false\) - автоматическое обновление

 - Добавлен вызов GetAppExeFileVersion\(\) - получение версии ехе-файла

:uniConf.exe

 - Добавлен вызов TUnUpgMan-&gt;Execute\(true\) - автоматическое обновление

 - Добавлен вызов GetAppExeFileVersion\(\) - получение версии ехе-файла

:uniVersions.exe

 - Добавлен вызов TUnUpgMan-&gt;Execute\(true\) - автоматическое обновление

 - Добавлен вызов GetAppExeFileVersion\(\) - получение версии ехе-файла

:un4Versions.exe

 - Файл переименован в uniVersions.exe

:Administrator.exe

 - Файл удален из сборки

:FinancialReports.exe

 - Файл удален из сборки

:ASAGI4ag.bpl

 - Добавлен компонент TUnUpgMan - автоматическое обновление програмных файлов

:SimpleControls5.bpl

 - Добавлен метод GetAppExeFileVersion\(\) - получение версии ехе-файла

