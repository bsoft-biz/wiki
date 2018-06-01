# Панель

Меню программы.

Во время выполнения программы можно менять некоторые параметры.

Имеет наивысший приоритет, но время действия настроек ограничено сеансом.

| **Имя свойства**  | **Тип**  | **Описание**  | **Значение для примера**  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Language  | String   | Язык интерфейса. Язык интерфейса задается либо цифрой \(0, 1, 2\), либо буквой \(E, M, R\). Язык окна регистрации  задается только методом File. Если язык не задан ни одним из методов,  система переводов выключается на весь сеанс работы.  | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%AF%D0%B7%D1%8B%D0%BA.png?raw=true) |
|   |   | **Загрузка настроек, дизайнов, переводов и т.п.:**  |   |
| LogParams   | Boolean   | Контроль настроек. Режим записи в текстовый файл всех считываемых настроек  \(до и после обработки  и фильтрации\).  | ![N](https://github.com/prbsoft/wiki/blob/master/src/LogParams.png?raw=true) |
| GridPropCacheLimit  | Integer   | Размер кеша дизайнов. Максимальный размер кеша дизайнов в памяти. За единицу берется один тип  документа, один узел дерева отчетов,  одна форма или справочник.  | ![N](https://github.com/prbsoft/wiki/blob/master/src/GridPropCacheLimit.png?raw=true) |
| RepairGridDesign   | Boolean   | Исправление ошибок. Режим автокоррекции загружаемых дизайнов \(бывает нужен при работе с ORACLE 9i\).   | ![RepairGridDesign.png](http://wiki.bsoft.biz/xwiki/bin/download/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D0%B0%D0%BD%D0%B5%D0%BB%D1%8C/RepairGridDesign.png) |
| LangDontLoad   | Boolean   | Не загружать переводы. Не пытаться загружать тексты переводов из ORACLE  \(для уменьшения  траффика\).  | ![N](https://github.com/prbsoft/wiki/blob/master/src/LangDontLoad.png?raw=true) |
| LoadCaptionsSep   | Boolean   | Заголовки отдельно. Режим раздельной загрузки переводов заголовков столбцов и дизайнов  \(для совместимости с переводами заголовков столбцов, сохраненными в предыдущих версиях SL\).   | ![N](https://github.com/prbsoft/wiki/blob/master/src/LoadCaptionsSep.png?raw=true) |
|   |   | **Ограничение прав пользователей:**  |   |
| DesignGroup  | Integer  | Номер группы дизайнов \(ненулевое значение позволяет пользователю иметь персональные  дизайны, переводы, схемы отчетов и т.п.\). Администратор может менять себе этот номер  во время выполнения программы \(через интерфейс меню\).  | ![N](https://github.com/prbsoft/wiki/blob/master/src/DesignGroup.png?raw=true) |
|   |   | **Панели инструментов:** |   |
| TBIconStyle  | Integer   | Расположение значков. Число от 0 до 3 означает положение значка относительно пункта главного меню: 0 - Значки не выводятся на экран \(в меню - только надписи\);  1 - Надписи не выводятся на экран \(в меню - только значки\);   2 - Значки выводятся на экран слева от соответствующих надписей;  3 - Значки выводятся на экран над соответствующими надписями.  | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%A2%D0%B8%D0%BF%20%D0%B7%D0%BD%D0%B0%D1%87%D0%BA%D0%BE%D0%B2.png?raw=true) |
| TBIconSize   | Integer   | Размер значков. Число от 0 до 2 означает размер значков в главного меню:  0 - Мелкие значки;  1 - Средние значки;  2 - Крупные значки.   | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%A0%D0%B0%D0%B7%D0%BC%D0%B5%D1%80%20%D0%B7%D0%BD%D0%B0%D1%87%D0%BA%D0%BE%D0%B2.png?raw=true) |
| TBPeriod   | Boolean   | Панель периодов. Отображать на экране панель ввода периодов.   | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%9F%D0%B5%D1%80%D0%B8%D0%BE%D0%B41.png?raw=true) |
| TBWindowList   | Boolean   | Панель открытых окон. Отображать на экране панель открытых окон.   | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA%20%D0%BE%D0%BA%D0%BE%D0%BD.png?raw=true) |
|   |   | **Настройка окна регистра документов:** |   |
| ViewBegin   | String   | Ограничение снизу. Минимальная дата отображаемых документов   | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%94%D0%B0%D1%82%D0%B0%20%D0%BD%D0%B0%D1%87%D0%B0%D0%BB%D0%B0%20%28%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%29.png?raw=true) |
| ViewEnd   | String   | Ограничение сверху. Максимальная дата отображаемых документов   | ![N](https://github.com/prbsoft/wiki/blob/master/src/%D0%94%D0%B0%D1%82%D0%B0%20%D0%BE%D0%BA%D0%BE%D0%BD%D1%87%D0%B0%D0%BD%D0%B8%D1%8F%20%28%D0%B4%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%29.png?raw=true) |
| PXCMSimpleEditing   | Boolean   | Режим быстрой правки. Режим быстрой правки проводок документов версии PX.   |   |
|   |   | **Настройка окна менеджера отчетов:** |   |
| RepDataStart  | String  | Дата начала периода просмотра данных в отчетах. Допускается SQL-выражение.  Если значение параметра отсутствует, вместо него используется значение параметра PeriodStart | ![&#x414;&#x430;&#x442;&#x430; &#x43D;&#x430;&#x447;&#x430;&#x43B;&#x430; \(&#x43E;&#x442;&#x447;&#x435;&#x442;\).png](http://wiki.bsoft.biz/xwiki/bin/download/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D0%B0%D0%BD%D0%B5%D0%BB%D1%8C/%D0%94%D0%B0%D1%82%D0%B0%20%D0%BD%D0%B0%D1%87%D0%B0%D0%BB%D0%B0%20%28%D0%BE%D1%82%D1%87%D0%B5%D1%82%29.png) |
| RepDataEnd  | String  | Дата окончания периода просмотра данных в отчетах. Допускается SQL-выражение.  Если значение параметра отсутствует, вместо него используется значение параметра PeriodEnd | ![&#x414;&#x430;&#x442;&#x430; &#x43E;&#x43A;&#x43E;&#x43D;&#x447;&#x430;&#x43D;&#x438;&#x44F; \(&#x43E;&#x442;&#x447;&#x435;&#x442;\).png](http://wiki.bsoft.biz/xwiki/bin/download/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9F%D0%B0%D0%BD%D0%B5%D0%BB%D1%8C/%D0%94%D0%B0%D1%82%D0%B0%20%D0%BE%D0%BA%D0%BE%D0%BD%D1%87%D0%B0%D0%BD%D0%B8%D1%8F%20%28%D0%BE%D1%82%D1%87%D0%B5%D1%82%29.png) |
| RepTestRecordCount  | Boolean   | Проверять к-во записей. Режим проверки количества записей в наборе данных отчета \(для F1Reports\):   при очень большом количестве записей выдается предупреждающее сообщение, имеется возможность  отменить построение отчета или вручную ограничить количество выводимых записей.  Предельное количество записей для отчетов Master/Detail - 1000, только Master - 10000.  | ![N](https://github.com/prbsoft/wiki/blob/master/src/RepTestRecCnt.png?raw=true) |
| RepDeleteTempTables   | Boolean   | Удалять врем. таблицы. Режим удаления временных таблиц  ORACLE после построения отчета \(можно выключить\).   | ![N](https://github.com/prbsoft/wiki/blob/master/src/RepDelTempTbl.png?raw=true) |
|   |   |  **Разные настройки:** |   |
| GridDisableNumberSearch   | Boolean   | Запрет числового поиска. Режим текстового поиска даже в  числовых полях грида \(вместо числового поиска\).  | ![N](https://github.com/prbsoft/wiki/blob/master/src/GridDisableNumberSearch.png?raw=true) |
| UseSmartTab   | Boolean   | "Умный" &lt;Tab&gt;. Режим интеллектуального поведения клавиши  &lt;Tab&gt;: переход от поля к полю по всему  активному окну.  | ![N](https://github.com/prbsoft/wiki/blob/master/src/UseSmartTab.png?raw=true) |
| UseSmartEnter   | Boolean  | "Умный" &lt;Enter&gt;. Режим интеллектуального поведения клавиши  &lt;Enter&gt; на дополнительной \(цифровой\)  клавиатуре:  при редактировании таблиц - переход к следующему полю или \(из последнего столбца\)  завершение редактирования и вставка новой записи.  | ![N](https://github.com/prbsoft/wiki/blob/master/src/UseSmartEnter.png?raw=true) |
| UseSpeedSearch   | Boolean  | Быстрый поиск в справ.. Режим быстрого поиска в выпадающих справочниках.   | ![N](https://github.com/prbsoft/wiki/blob/master/src/UseSpeedSearch.png?raw=true) |
|   |   |  **Отладочные возможности:** |   |
| SQLMonitorActive  | Boolean  | Включение SQLMonitor. Включить SQLMonitor  \(соединение с программой SQLMonitor и протоколирование обращений к серверу\).  | ![N](https://github.com/prbsoft/wiki/blob/master/src/SQLMonitorActive.png?raw=true) |

![&#x420;&#x438;&#x441;. 1. &#x41C;&#x435;&#x43D;&#x44E; &quot;&#x41D;&#x430;&#x441;&#x442;&#x440;&#x43E;&#x439;&#x43A;&#x438;&quot;](../../../.gitbook/assets/menyu.png)

 [Кнопка ](https://bsoft.gitbook.io/wiki/razrabotka/obekty-una/panel/knopka)\(button\)

