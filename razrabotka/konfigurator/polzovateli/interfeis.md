# Интерфейс

| **Название свойства** | **Тип** | **Описание** | **Значение для примера** |
| :--- | :---: | :--- | :--- |
| TBForms | Boolean | Отобразить тулбар Формы: все секции из ToolBarFormSections. | false |
| TBJournals | Boolean | Отобразить тулбар Журналы. Меню журналы выводится в строку. | true |
| TBWindowList | Boolean |  | false |
| TBDocCmd | Boolean |  | true |
| TBPeriod | Boolean | Отобразить тулбар Период: текущая дата, перод просмотра и редактирования. | true |
| TBIconSize | String |  | 3 |
| TBIconStyle | String |  | 2 |
| ToolBarFormSections | String | Список секций, кот будут отображены в тулбаре формы | \*Producte,F\_PROD\_GR, F\_PRODUCTS, \*"Cliente,Клиенты",              F\_CLIENTS, F\_AGENTS, \*Rute,F\_ROUTES, F\_RUTE\_DESF,\*,F\_UM |

Скрыть элементы пользовательского интерфейса можно с помощью свойств **Hide**:

| **Имя свойства** | **Тип** | **Описание** | **Внешний вид** |
| :--- | :---: | :--- | :--- |
|  |  | **Пункты главного меню:** |  |
| HideMenuDoc | Boolean | Действия над документом | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/doc.png?raw=true) |
| HideMenuDict | Boolean | Справочники | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/spr.png?raw=true) |
| HideMenuSysS | Boolean | Справочник SysS \(по умолчанию включено\) | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/sys.png?raw=true) |
| HideMenuReps | Boolean | Отчеты | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/rep.png?raw=true) |
| HideMenuRepSelect | Boolean | Дерево отчетов в меню "Отчеты" |  |
| HideMenuForms | Boolean | Формы | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/form.png?raw=true) |
| HideMenuUtil | Boolean | Сервис | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/service.png?raw=true) |
| HideMenuWindow | Boolean | Окна | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/win.png?raw=true) |
| HideMenuHelp | Boolean | Помощь | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/win.png?raw=true) |
| HideMenuJrnlStd | Boolean | Скрывает журнал Все, если true |  |
|  |  | **Кнопки на главной панели инструментов:** |  |
| HideToolBar | Boolean | Вся панель инструментов |  |
| HideToolNavi | Boolean | Навигатор | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/10.png?raw=true) |
| HideToolLang | Boolean | Языки | ![N](https://github.com/prbsoft/wiki/blob/master/src/interface/11.png?raw=true) ![N](https://github.com/prbsoft/wiki/blob/master/src/interface/31.png?raw=true) |
| HideToolSet | Boolean | Галки | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/12.png?raw=true) |
| HideToolCalc | Boolean | Калькулятор | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/calc.png?raw=true) |
| HideToolMsg | Boolean | Сообщения | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/14.png?raw=true) |
| HideToolSys | Boolean | Второй клиент |  |
| HideToolInf | Boolean | Имя сервера | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/16.png?raw=true) |
| HideToolOrder | Boolean | Авто-заявка |  |
| BG\_FILTER\_SECTION | Boolean | Управление NRSET |  |
| DivVisible | Boolean | Выбор филиала | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/40.png?raw=true) |
| FMEnabled | Boolean | Управление F/M | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/41.png?raw=true) |
| FOnlyEnabled | Boolean | Красная кнопка F/M | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/42.png?raw=true) |
|  |  | **Информация на строке состояния:** |  |
| HideStatusBar | Boolean | Вся строка состояния | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/44.png?raw=true) |
| HideMemory | Boolean | Индикатор памяти | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/45.png?raw=true) |
|  |  | **Кнопки на панели управления выбранным документом:** |  |
| HideDocsEditare | Boolean | Кнопка редактирования документа | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/18.png?raw=true) |
| HideDocsLich | Boolean | Две кнопки удаления проводок | ![N](https://github.com/prbsoft/wiki/blob/master/src/interface/19.png?raw=true) ![N](https://github.com/prbsoft/wiki/blob/master/src/interface/20.png?raw=true) |
| HideDocsDublare | Boolean | Кнопка дублирования документа | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/38.png?raw=true) |
| HideDocsDeriva | Boolean | Кнопка документа на основании | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/34.png?raw=true) |
| HideDocsTotals | Boolean | Кнопка просмотра итогов | ![N](https://github.com/prbsoft/wiki/blob/master/src/interface/39.png?raw=true), ![N](https://github.com/prbsoft/wiki/blob/master/src/interface/23.png?raw=true) |
| HideDocsWizard | Boolean | Кнопка мастера \(по умолчанию скрыта\) |  |
| HideDocsSpec | Boolean | Кнопка Special Actions | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/22.png?raw=true) |
| HideDocsActive | Boolean | Кнопка активации/дезактивации | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/32.png?raw=true) |
| HideDocsFact | Boolean | Кнопка окна фактуры | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/21.png?raw=true) |
| HideDocsSold | Boolean | Кнопка окна остатков | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/Кнопка%20остатков.png?raw=true) |
| HideDocsBarCode | Boolean | Кнопка окна считывателя штрих кодов |  |
| HideDocsDesign | Boolean | Кнопка настройки дизайна CST | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/46.png?raw=true) |
| HideDocsLang | Boolean | Кнопка настройки переводов | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/33.png?raw=true) |
| HideDocsHeadLine | Boolean | Цветная полоса над документом | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/24.png?raw=true) |
|  |  | **Ярлычки вкладок документа:** |  |
| HideDocsTabCM | Boolean | Вкладка "Проводки" | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/26.png?raw=true) |
| HideDocsTabMain | Boolean | Вкладка "Специфика" |  |
| HideDocsTabAdd | Boolean | Вкладка "Информация" | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/27.png?raw=true) |
| HideDocsTabObj | Boolean | Вкладка "Объект" | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/28.png?raw=true) |
| HideDocsTabLog | Boolean | Вкладка "История" | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/29.png?raw=true) |
| HideDocsTabXL | Boolean | Вкладка "Excel" | ![](https://github.com/prbsoft/wiki/blob/master/src/interface/30.png?raw=true) |
| UseCMX \(секция Docs\) | Boolean | Вкладка CMX |  |

