# Действия \(action\)

**Объекты типа** Action

Действия \(action\) представляют собой дочерние объекты документов со своими свойствами. Эти объекты служат для выполнения определенных действий по обработке данных, как правило, для генерации проводок или изменения данных в определенных таблицах. Список доступных действий отображается в окне Document/Form Action клиентского приложения Universal Accounting.

Перед выполнением каждого выражения программа пытается автоматически заполнить значения его параметров и макросов, а после выполнения - использовать значения выходных параметров \(см. [также](https://bsoft.gitbook.io/wiki/razrabotka/obekty-oracle/parametry-i-makrosy-sql-zaprosov)\)

Конфигурирование типовой формы включает настройки интерфейсной части и части обработки данных – действия. Объекты действия аналогичны объектам doc-action. Свойства этих объектов позволяют определять процедуры обработки данных.

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| :--- | :---: | :--- | :--- |
|  |  | **Основные свойства:** |  |
| ActionType | String | Тип действия,   0 - стандартное \(можно менять\),    3 - всегда активное.   Галочка стоит, но экшен серый   и его нельзя отменить | 0 |
| Caption | String | Подпись для действия в списке действий | Просто действие \(со всеми параметрами\) |
| ID | Integer | Порядковый номер действия в окне   Document Action.  Список Actions формы   сортируется на экране по значению   параметра ID, а при отсутствии этого   параметра его значение принимается   равным нулю. Actions с одинаковым ID   сортируются по Caption \(по алфавиту\) | 1 |
| RefreshNeed | Boolean | Флаг обновления формы | false |
| SQL1 | Memo | Содержит SQL команду обработки данных,   причем сначала выполниться SQL1 потом SQL2 и т.д. |  |
| SQL2 | Memo | Содержит SQL команду обработки данных |  |
| Visible | Boolean | Если значение True, действие доступно в   окне Document Action | true |
|  |  | Дополнительные свойства: |  |
| Active | Boolean | Если значение False, объект игнорируется | true |
| AutoOK | Boolean | Устанавливает активность действия \(выбор\)   \(т.е. сразу в списке действий, у него   будет стоять галочка\) | true |
| AutoSelect | Boolean | При нажатии на кнопку действия, не будет   списка действия,  а выполняться сразу те действия,   у которых активно это свойство,  работает в   сочетание со свойством AutoOK. | true |
| ButtonIndex | Integer | Индекс кнопки на панели | 1 |
| ButtonText | String | Наименование кнопки на панели | \[Генерировать проводки\] |
| ConfirmText | String | Запрос на подтверждение перед   выполнением действия | Generam formulele contabile? Сформировать проводки? |
| CONT | Integer | Cчет для проводок | 2111 |
| EAutoGfcSave | Boolean | Автосохранение после выполнения экшена | true |
| EAutoGFCOrder | String | Через запятую указываются экшены, которые   должны выполниться при   сохранении док-та \(свойства документа\) | 0 |
| EAutoGFCRun | Boolean | Включает автовыполнение экшенов про сохранении документа\(свойства документа\) | true |
| EAutoGFCInsert | String | Экшен, который нужно выполнить  при   создании документа | 5 |
| IDB | Integer |  |  |
| LoadFile | Boolean | Экшен, который открывает диалоговое   окно выбора файла. работает  в сочетание   со свойством LoadFileUnique. | true |
| LoadFileUnique | Boolean | При этом файл загружается в таблицу   `VMDB_DOCS_OLE`,  содержимое которой   можно посмотреть в документе на вкладке “Объект”. | true |
| NextActionID | Integer | Действие которое выполнится дополнительно | 1 |
| OraLoadFile1 | String | X:\Terminal\Priobr\_val\priobr\_val.txt |  |
| OraLoadScript1 | String | BEGIN   INSERT INTO TMS\_LOAD\_INFO   \(ID,DESCRIPTION\) VALUES\(1,'Strih-cod inventarizatia'\);   INSERT INTO TMS\_LOAD\_STRUCT   \(ID,COL,COLUMNNAME,TYPE,PREC\)   VALUES\(1,1,'COD','S',15\);  INSERT INTO TMS\_LOAD\_STRUCT  \(ID,COL,COLUMNNAME,TYPE,PREC\)   VALUES\(1,2,'CANT','I',10\);   END; |  |
| OraOutputCheck | Boolean | сохраняет `dbms_output` | true |
| OraOutputFile | String | сохраняет `dbms_output` в указанный файл.   Пример sql: v\_text := bon.get\_bon\_elicom\(:nrdoc\); | Z:\check.inp |
| PrintFormId | Integer | После выполнения Action сразу вызовется   печатная форма со свойством ID=1 | 1 |
| RefreshDDocNeed | Boolean | Для обновления содержимого документа | true |
| RefreshFullDocs | Boolean | Для обновления документа | true |
| RefreshList | String | Обновляет выбранный грид | sq01 |
| RefreshNeed | Boolean | Флаг обновления формы |  |
| TargetSection | String |  |  |
| TargetType | String |  |  |
| TextForUser | String | Подпись действия, видимая для пользователя   в окне Document Action |  |
| UseDataUniv | Boolean |  |  |
| Visible | Boolean | Если значение True, действие доступно   в окне Document Action | true |
| SQL1, SQL2,… | Memo | В текстах запросов Actions документов и   форм \(SQL1, SQL2 и т. д.\)   параметры заполняются значениями   на основании их \(параметров\) имен.   В запросах можно использовать следующие параметры: :RESULT - параметр не заполняется и не запрашивается у пользователя :NRDOC - номер выбранного документа :DATADOC - дата выбранного документа :DATAMANUAL - дата выбранного документа :DATEBEGIN - дата начала выбранного периода :DATEFINAL - дата конца выбранного периода  Выбранный период определяется в верхней части окна отчетов. При отсутствии окна отчетов выбранный период  определяется из настроек Администратора  \(секция General\) Значение параметра, имя которого осталось нераспознанным, запрашивается у пользователя непосредственно перед выполнением запроса. `DECLARE cTmp VARCHAR2(32):=&TXTQ#1; BEGIN YBMB_Terminal.Insert_Main(:NRDOC,cTmp,2); un$ttemp.DeleteTempTable(cTmp); END;` | Экшн, который выполняет  скрипт Настроено действие  "Экспорт заявки в EDI"  Его имя секции -  ZAIAVAKA\_POSU.MAKE\_XML Его SQL1 :begin ylnl\_edi\_order\_xml\(:order\); :batch:= 'move \oravirt\dpdump\order-':order'.xml' ' X:\EDI\ExiteSync\outbox\'chr\(13\)chr\(10\) 'X:'chr\(13\)chr\(10\) 'cd \EDI\ExiteSync\'chr\(13\)chr\(10\) 'main.bat';  end; / _order=field\_fmFS1c\_sq01\_NRDOC_ / |
| SQL1a | Memo | INSERT INTO VMDB\_ST201D\(NRDOC,CTSC,CANT\)   SELECT :NRDOC,COD,CANT FROM &TXT\#1 | Пример из дока \(48109\) Импорт |
| DeleteFCFromCM | Boolean | Если значение True, удаляет записи из   таблицы проводок для документа | true |
| DeleteALLFCFrom CM | Boolean | Автоматическое удаление проводок при   выполнении экшена | true |
| Enable | Boolean | Просто экшен, который по умолчанию работает | true |
| EAutoConfirm Document | String | На уровне документа, в котором   можно указать id экшенов в правильном   порядке, которые надо выполнять при   сохранении документа. Если это свойство   установлено и непустое, то при сохранении   документа появляется диалоговое окно с   вопросом: Утвердить ли документ? |  |
| OraCommit BeforeExec | Boolean | В action-ах на формах. Если =true, то перед   основным SQL \(SQL1 и т.п.\), который делается   в автономной транзакции, выполнится commit. | true |
| ExcelFileLoad | Boolean | Загрузка из xls | true |
| ExcelFileSheetIndex | Integer | №листа, который разобрать в таблицу | 5 |
| InsertOnTop | Boolean | ??? наверное связано с проводками | false |

