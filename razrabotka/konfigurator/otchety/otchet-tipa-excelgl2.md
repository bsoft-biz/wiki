# Отчет типа ExcelGL2



| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  **** |  **** | **General** |   |
| OraFunction | String |   | P10xGetQuery |
| OraPackage | String |   |   |
|   |   | **Initial** |   |
| xCarteaMare | Integer |   | 1 |
| xContPassiv | Intege  |   | 0 |
| xCtDt | Integer |   | 0 |
| xRulajDt | Integer |   | 1 |
| xZeroInclusiv | Integer |   | 1 |
|   | Integer |   |  1 |
|   |   | **Oracle** |   |
| ActiveSheet | String |   | Pivot |
| DataSetHeader | String |   | NR |
| DataSetMaster | String |   | SQ |
| PivotCmd | String |   | Pivot\Dst=Pivot!R6C2\Name= Pivot\ColumnGrand\       NoPreserveFormatting |
| Range | String |   | Data |
| RseFieldList | Memo |   | 0,grp,"Столбцы слева" 1,an,"Дата" ,S,T\_DATE,ROW,DATA 2,ref,"Неделя",,T\_WEEK,ROW,DATA,Q,          "TRUNC\(DATA,'D'\)" 2,ref,"Месяц",,T\_MONTH,ROW,DATA,Q,              "TRUNC\(DATA, 'MM'\)" 2,ref,"Квартал",,T\_QUARTER,ROW,DATA,Q,        "TRUNC\(DATA, 'Q'\)" 2,ref,"Год",,T\_YEAR,ROW,DATA,Q,                         "TRUNC\(DATA, 'Y'\)" 1,an,"Счет",,CONT,ROW 2,ref,"Счет3",,Cont3,ROW,Cont,Q,                          "SUBSTR\(Cont, 1, 3\)" 1,an,"Субсчет",,CONT1,ROW 1,an,"SC",C,SC,ROW 2,ref,"SC Текст",,SC\_TEXT,ROW,SC,U,                 DENUMIREA\_\_1 2,ref,"SC Наименование",,SC\_DENUMIREA,  ROW,SC,U,DENUMIREA 2,ref,"SC Код",,SC\_CODVECHI,ROW,                  SC,U,CODVECHI 1,an,"DEP",C,DEP,ROW 2,ref,"DEP Текст",,DEP\_TEXT,ROW,DEP,U,         DENUMIREA\_\_1 2,ref,"DEP Наименование",,DEP\_DENUMIREA,  ROW,DEP,U,DENUMIREA 2,ref,"DEP Код",,DEP\_CODVECHI,ROW,           DEP,U,CODVECHI 1,an,"SC1",C,SC1,ROW 2,ref,"SC1 Текст",,SC1\_TEXT,ROW,SC1,U,         DENUMIREA\_\_1 2,ref,"SC1 Наименование",,SC1\_DENUMIREA, ROW,SC1,U,DENUMIREA 2,ref,"SC1 Код",,SC1\_CODVECHI,ROW,SC1,U,CODVECHI 0,grp,"Строки сверху" 1,an,"Тип",SD,GRP,COLUMN,GRPTEXT 1,an,"xСчет",S,xCONT,COLUMN 2,ref,"xСчет3",,xCont3,COLUMN,xCont,Q, "DECODE\(GRP, 2, SUBSTR\(xCont, 1, 3\), 4, SUBSTR\(xCont, 1, 3\), xCont\)" 1,an,"xСубсчет",,xCONT1,COLUMN 0,agr,"Сумма",SF{NVL\(SUMA,0\)&lt;&gt;0},SUMA,DATA,SUM TemplateOrder=T\_DATE,GRP,XCONT,SUMA |
| Template | String |   | RG1p10x.xls |
|   |   | **x1ReportG2** |   |
| IniCont | String |   | 2411 |
| IniCont1 | Integer |   |   |
| IniDep | Integer |   |   |
| IniSc | Integer |   |   |
| IniSc1 | Integer |   |   |
| IniXCont | String |   |   |
| IniXCont1 | Integer |   |   |
| IniXDep | Integer |   |   |
| IniXSc | Integer |   |   |
| IniXSc1 | Integer |   |   |
|  |  | **Общая** |  |
| Caption | String | Подпись отчета | Журналы-ордера с расшифровкой                     по датам |
| DLL ID | Integer | Идентификационный номер DLL | 4201 |
| Report ID | String | Идентификатор печатной формы в DLL | 10 |
| ReportType | String | Тип отчета | 1 |

