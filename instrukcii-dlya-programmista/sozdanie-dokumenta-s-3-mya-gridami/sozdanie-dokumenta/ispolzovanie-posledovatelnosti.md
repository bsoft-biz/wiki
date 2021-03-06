# Использование последовательности

##  **7.4 Использование последовательности**

 Для использования последовательности \(_SEQ_\) нажмем на кнопку

![](../../../.gitbook/assets/pravka.png)

 \(либо на горячие клавиши **Ctrl+~**\) для начала редактирования документа.

![](../../../.gitbook/assets/screenshot228.png)

 Отроем запрос к первому гриду с помощью горячих клавиш \(**Alt+Q**\) и допишем на вкладке

![](../../../.gitbook/assets/sql-update.png)

 в поле

![](../../../.gitbook/assets/insert2%20%282%29.png)

следующую строку:

"_`RETURNING NRDOC1 INTO :NRDOC1`_". После сохраним изменения с помощью галочки

![](../../../.gitbook/assets/save-on-exit-4%20%282%29.png)

 и нажмём кнопку

![](../../../.gitbook/assets/ok3%20%281%29.png)

![](../../../.gitbook/assets/screenshot230.png)

 Отроем запрос ко второму гриду с помощью горячих клавиш \(**Alt+Q**\) и допишем на вкладке

![](../../../.gitbook/assets/sql-update%20%281%29.png)

 в поле

![](../../../.gitbook/assets/insert2%20%283%29.png)

следующую строку:

"_`RETURNING NRDOC2 INTO :NRDOC2`_". После сохраним изменения с помощью галочки

![](../../../.gitbook/assets/save-on-exit-4%20%287%29.png)

 и нажмём кнопку

![](../../../.gitbook/assets/ok3.png)

![](../../../.gitbook/assets/screenshot231.png)

 Цифра в колонке _NRDOC_ записана в колонке _COD_ таблицы _TMDB\_DOCS_ \(где одна запись приравнивается к одному документу\). Цифра в колонке _NRDOC1_ появляется благодаря последовательности, которая используется триггерами. На скриншоте ниже показано значение _NRDOC1_, которое равно 141, оно уже использовано, и следующее значение в последовательности используется 142.

![](../../../.gitbook/assets/screenshot233.png)

 Таким образом запись в колонке _NRDOC2_, которая добавлена сразу после записи в первом гриде\(_NRDOC1_-141\) использует цифру 142.

![](../../../.gitbook/assets/screenshot234.png)

