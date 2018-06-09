# Действия \(action\)

**Объекты типа** Action

Действия \(action\) представляют собой дочерние объекты документов со своими свойствами. Эти объекты служат для выполнения определенных действий по обработке данных, как правило, для генерации проводок или изменения данных в определенных таблицах. Список доступных действий отображается в окне Document/Form Action клиентского приложения Universal Accounting. 

Перед выполнением каждого выражения программа пытается автоматически заполнить значения его параметров и макросов, а после выполнения - использовать значения выходных параметров \(см. [также](https://bsoft.gitbook.io/wiki/razrabotka/obekty-oracle/parametry-i-makrosy-sql-zaprosov)\)

Конфигурирование типовой формы включает настройки интерфейсной части и части обработки данных – действия. Объекты действия аналогичны объектам doc-action. Свойства этих объектов позволяют определять процедуры обработки данных.



| **Имя свойства**  |  **Тип** | **Описание** | **Значение для примера** |
| :------------- |:-------------:| :-----| :-----|
|  |   | **Основные свойства:** |  |
| ActionType | String | Тип действия, <br> 0 - стандартное \(можно менять\), <br>  3 - всегда активное. <br> Галочка стоит, но экшен серый <br> и его нельзя отменить | 0 |
| Caption | String | Подпись для действия в списке действий | Просто действие \(со всеми параметрами\) |
| ID | Integer | Порядковый номер действия в окне <br> Document Action.  Список Actions формы <br> сортируется на экране по значению <br> параметра ID, а при отсутствии этого <br> параметра его значение принимается <br> равным нулю. Actions с одинаковым ID <br> сортируются по Caption \(по алфавиту\) | 1 |
| RefreshNeed | Boolean | Флаг обновления формы | false |
| SQL1 | Memo | Содержит SQL команду обработки данных, <br> причем сначала выполниться SQL1 потом SQL2 и т.д. |  |
| SQL2 | Memo | Содержит SQL команду обработки данных |  |
| Visible | Boolean | Если значение True, действие доступно в <br> окне Document Action | true |
|   |   | Дополнительные свойства: |  |
| Active | Boolean | Если значение False, объект игнорируется | true |
| AutoOK | Boolean | Устанавливает активность действия \(выбор\) <br> \(т.е. сразу в списке действий, у него <br> будет стоять галочка\) | true |
| AutoSelect | Boolean | При нажатии на кнопку действия, не будет <br> списка действия,  а выполняться сразу те действия, <br> у которых активно это свойство,  работает в <br> сочетание со свойством AutoOK. | true |
| ButtonIndex | Integer | Индекс кнопки на панели | 1 |
| ButtonText | String | Наименование кнопки на панели | \[Генерировать проводки\] |
| ConfirmText | String | Запрос на подтверждение перед <br> выполнением действия | Generam formulele contabile? Сформировать проводки? |
| CONT | Integer | Cчет для проводок | 2111 |
| EAutoGfcSave | Boolean | Автосохранение после выполнения экшена | true |
| EAutoGFCOrder | String | Через запятую указываются экшены, которые <br> должны выполниться при <br> сохранении док-та \(свойства документа\) | 0 |
| EAutoGFCRun | Boolean | Включает автовыполнение экшенов про сохранении документа\(свойства документа\) | true |
| EAutoGFCInsert | String | Экшен, который нужно выполнить  при <br> создании документа | 5 |
| IDB | Integer |  |  |
| LoadFile | Boolean | Экшен, который открывает диалоговое <br> окно выбора файла. работает  в сочетание <br> со свойством LoadFileUnique. | true |
| LoadFileUnique | Boolean | При этом файл загружается в таблицу <br> `VMDB_DOCS_OLE`,  содержимое которой <br> можно посмотреть в документе на вкладке “Объект”. | true |
| NextActionID | Integer | Действие которое выполнится дополнительно | 1 |
| OraLoadFile1 | String | X:\Terminal\Priobr\_val\priobr\_val.txt |  |
| OraLoadScript1 | String | BEGIN <br> INSERT INTO TMS_LOAD_INFO <br> (ID,DESCRIPTION)<br>VALUES(1,'Strih-cod inventarizatia'); <br> INSERT INTO TMS_LOAD_STRUCT <br> (ID,COL,COLUMNNAME,TYPE,PREC) <br> VALUES(1,1,'COD','S',15);<br> INSERT INTO TMS_LOAD_STRUCT <br>(ID,COL,COLUMNNAME,TYPE,PREC) <br> VALUES(1,2,'CANT','I',10); <br> END;  |  |
| OraOutputCheck | Boolean | сохраняет `dbms_output` | true |
| OraOutputFile | String | сохраняет `dbms_output` в указанный файл. <br> Пример sql: v\_text := bon.get\_bon\_elicom\(:nrdoc\); | Z:\check.inp |
| PrintFormId | Integer | После выполнения Action сразу вызовется <br> печатная форма со свойством ID=1 | 1 |
| RefreshDDocNeed | Boolean | Для обновления содержимого документа | true |
| RefreshFullDocs  | Boolean | Для обновления документа | true |
| RefreshList | String | Обновляет выбранный грид | sq01 |
| RefreshNeed | Boolean | Флаг обновления формы |  |
| TargetSection | String |  |  |
| TargetType | String |  |  |
| TextForUser | String  | Подпись действия, видимая для пользователя <br> в окне Document Action |  |
| UseDataUniv | Boolean |  |  |
| Visible | Boolean | Если значение True, действие доступно <br> в окне Document Action | true |
| SQL1, SQL2,… | Memo | В текстах запросов Actions документов и <br> форм (SQL1, SQL2 и т. д.) <br> параметры заполняются значениями <br> на основании их \(параметров\) имен. <br> В запросах можно использовать следующие параметры:<br>:RESULT - параметр не заполняется и не запрашивается у пользователя<br>:NRDOC - номер выбранного документа<br>:DATADOC - дата выбранного документа<br>:DATAMANUAL - дата выбранного документа<br>:DATEBEGIN - дата начала выбранного периода<br>:DATEFINAL - дата конца выбранного периода<br> Выбранный период определяется в верхней части окна отчетов.<br>При отсутствии окна отчетов выбранный период <br>определяется из настроек Администратора<br> (секция General) Значение параметра, имя которого<br>осталось нераспознанным, запрашивается у пользователя непосредственно перед выполнением запроса.<br>`DECLARE cTmp VARCHAR2(32):=&TXTQ#1; BEGIN YBMB_Terminal.Insert_Main(:NRDOC,cTmp,2); un$ttemp.DeleteTempTable(cTmp); END;` | Экшн, который выполняет <br>скрипт Настроено действие<br> "Экспорт заявки в EDI" <br>Его имя секции -<br> ZAIAVAKA_POSU.MAKE_XML Его SQL1<br>:begin ylnl_edi_order_xml(:order); :batch:= 'move \\oravirt\dpdump\order-':order'.xml' ' X:\EDI\ExiteSync\outbox\'chr(13)chr(10) 'X:'chr(13)chr(10) 'cd \EDI\ExiteSync\'chr(13)chr(10) 'main.bat'; <br>end; /* order=field_fmFS1c_sq01_NRDOC */ |
|  SQL1a | Memo | INSERT INTO VMDB_ST201D(NRDOC,CTSC,CANT) <br> SELECT :NRDOC,COD,CANT FROM &TXT#1 | Пример из дока \(48109\) Импорт |
| DeleteFCFromCM | Boolean | Если значение True, удаляет записи из <br> таблицы проводок для документа | true |
| DeleteALLFCFromCM | Boolean | Автоматическое удаление проводок при <br> выполнении экшена | true |
| Enable | Boolean | Просто экшен, который по умолчанию работает | true |
| EAutoConfirmDocument | String | На уровне документа, в котором <br> можно указать id экшенов в правильном <br> порядке, которые надо выполнять при <br> сохранении документа. Если это свойство <br> установлено и непустое, то при сохранении <br> документа появляется диалоговое окно с <br> вопросом: Утвердить ли документ? |  |
| OraCommitBeforeExec | Boolean | В action-ах на формах. Если =true, то перед <br> основным SQL \(SQL1 и т.п.\), который делается <br> в автономной транзакции, выполнится commit. | true |
| ExcelFileLoad | Boolean | Загрузка из xls | true |
| ExcelFileSheetIndex | Integer | №листа, который разобрать в таблицу | 5 |
| InsertOnTop | Boolean | ??? наверное связано с проводками | false |

