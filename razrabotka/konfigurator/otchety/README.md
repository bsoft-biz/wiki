# Отчеты

Объекты типа Отчеты содержат настройки соответствующих отчетов. Дерево отчетов отображается в окне \[`Raport manager`\] приложения Universal Accounting. Иерархия дерева отчетов текущей записи настроек – это логическая организация списка отчетов по их назначению. Число уровней вложенности узлов, служащих для логической группировки объектов, не ограничено.

`Большинство отчетов поддерживают следующие свойства (свойства группы Общая)`

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `DLL ID` | `Integer` | Идентификационный номер `DLL` | `9002` |
| `Index Fields` | `String` |  |  |
| `Master Fields` | `String` |   |  |
| `DontEditReport` | `Boolean` | Запрет редактирования отчета перед печатью. Запрет экспорта в `Excel`. |  `true` |
| `Report ID` | `String` | Идентификатор печатной формы в `DLL` | `univ` |
| `Report Type` | `String` | Типы отчетов: `FormulaOne, ExcelGL2, FastReport, MSWord` | `FastReport` |
| `SQLDetail` | `Memo` | Запрос, возвращающий данные в область `Detail` \(область данных подчиненной таблицы\) печатной формы |  |
| `SQLHeader` | `Memo` | Запрос, возвращающий данные в область `Header` \(область заголовка\) печатной формы |  |
| `SQLMaster` | `Memo` | Запрос, возвращающий данные в область `Master` \(область данных главной таблицы\) печатной формы |  |
| `Template` | `String` | Шаблон, используемый для генерации печатной формы | `log_cash_inc_ot.fr3` |
| `WindowCaption` | `String` | Подпись окна сгенерированной печатной формы |  |
| `PrintSpecialDevice` | `Boolean` |  | `true` |
| `PrintSpecialDeviceIndex` | `Integer` |  | `2` |
| `PrintSpecialDevicePort` | `String` | Внизу отчета появляются дополнительные настройки | `COM1` |
| `SQLBeforePrint` | `Memo` | При нажатии на принтер из печатной формы/отчета  выполнится скрипт из этого свойства |  |
| `DisableGotoNrdoc` | `Boolean` | Нельзя прыгать из отчетов в документ | `true` |

Новые отчеты создаются и настраиваются преимущественно на базе так называемого Универсального отчета \(`DLL ID = 2,` `Report ID = 1`\),

Нового Универсального отчета \(`DLL ID = 4201`, `Report ID = 12`\) и Отчета с произвольными параметрами \(`DLL ID = 9002`, `ReportID = univ`\)

**Некоторые отчеты поддерживают специфические свойства:**

[Свойства Универсального отчета](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/svoistva-universalnogo-otcheta)

[Свойства нового универсального отчета](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/svoistva-novogo-universalnogo-otcheta)

[Свойства отчета с произвольными параметрами](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/svoistva-otcheta-s-proizvolnymi-%20%20parametrami)

[Свойства сводной таблицы F1Reports](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/svoistva-svodnoi-tablicy-f1reports)

[TXT-свойства](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/txt-svoistva)

**Типы печатных форм:**

[Отчет типа Formula One](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/otchet-tipa-%20%20formula-one)

[Отчет типа ExcelGL2](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/otchet-tipa-excelgl2)

[Отчет типа FastReport](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/otchet-tipa-%20%20fastreport)

[Отчет типа FastReport4](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/otchet-tipa-%20%20fastreport4)

[Пример создания пивот отчета в РСЕ](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/primer-sozdaniya-pivot-otcheta-v-rse) 

[Опции отчетов в конфигураторе](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/opcii-%20%20otchetov-v-konfiguratore)

[Шаблоны Formula One](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/shablony-formula-one)

[Создание шаблона Fast Report с нуля.](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/sozdanie-shablona-fast-report)

[Финансовые отчеты](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/finansovye-otchety)

[Отчеты \(общее\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/otchety-obshee)

[Универсальный отчет \(RSE\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/universalnyi-%20%20otchet-rse)

[Оформление текстового материала \(ОТЧЕТ\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/oformlenie-tekstovogo-materiala-otchet)

[Универсальный отчет \(УО\)](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/universalnyi-%20%20otchet-uo)

[Настройка отчета](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/nastroika-otcheta)

[Конвертировать frf в fr3](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/konvertirovat-%20%20frf-v-fr3)

[Вычисление итогов для грида](https://bsoft.gitbook.io/wiki/razrabotka/konfigurator/otchety/vychislenie-%20%20itogov-dlya-grida)

