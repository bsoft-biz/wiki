# Редактирование запроса

##  **7.1 Редактирование запроса**

 Для изменения запроса воспользуемся горячими клавишами **Alt+Q** \(находясь в поле **Grid № 1**\).

![](../../../.gitbook/assets/screenshot105.png)

 Далее переходим на вкладку

![](../../../.gitbook/assets/sagi-properties-2%20%281%29.png)

 И записываем имя представления \(_`View`_\) `YVEINE_VMDB_INTAKE_LIST_A`. В фильтре на выборку записываем _`RDDOC=:COD`_, порядок сортировки по колонке _NRDOC1_ и список ключевых полей для обновления _`NRDOC`_и _`NRDOC1`_.

![](../../../.gitbook/assets/screenshot106.png)

 После чего переходим на вкладку

![](../../../.gitbook/assets/sql-generator%20%282%29.png)

 и нажимаем на кнопку

![](../../../.gitbook/assets/get-tables%20%282%29.png)

 для получения таблицы.

![](../../../.gitbook/assets/screenshot107.png)

Далее нажимаем на кнопку

![](../../../.gitbook/assets/get-table-fields%20%281%29.png)

для получения табличных полей.

![](../../../.gitbook/assets/screenshot108.png)

 После чего нажимаем на кнопку

![](../../../.gitbook/assets/generate-sql%20%282%29.png)

  для генерирования SQL запроса.

![](../../../.gitbook/assets/screenshot109.png)

 После проведённых выше действий сгенерировался запрос для добавления записей

![](../../../.gitbook/assets/insert2%20%282%29.png)

![](../../../.gitbook/assets/screenshot110.png)

 Изменения записей

![](../../../.gitbook/assets/update%20%281%29.png)

![](../../../.gitbook/assets/screenshot111.png)

 Удаления записей

![](../../../.gitbook/assets/delete%20%282%29.png)

 и

![](../../../.gitbook/assets/screenshot112.png)

Обновления записей 

![](../../../.gitbook/assets/refresh%20%282%29.png)

![](../../../.gitbook/assets/screenshot113.png)

На вкладке

![](../../../.gitbook/assets/sql%20%282%29.png)

 сгенерирован `SQL` запрос, который выбирает данные из вида \(_View_\) `YVEINE_VMDB_INTAKE_LIST_A`, где фильтр на выборку _`NRDOC =: COD`_ и сортируется по колонке _`NRDOC1`_.

![](../../../.gitbook/assets/screenshot114.png)

 Для сохранения изменений ставим галочку напротив

![](../../../.gitbook/assets/save-on-exit-12.png)

 и нажимаем на кнопку

![](../../../.gitbook/assets/ok-15.png)

 В результате чего все изменения будут сохранены при выходе.

![](../../../.gitbook/assets/screenshot115.png)

 Для редактирования запроса **Grid'a № 2** воспользуемся горячими клавишами **Alt+Q**. Далее переходим на вкладку

![](../../../.gitbook/assets/sagi-properties-2%20%283%29.png)

 и записываем имя представления \(_`View`_\) `YVEINE_VMDB_INTAKE_LIST_B`. В поле Фильтр на выборку записываем _`NRDOС=:NRDOC AND NRDOC1=:NRDOC1`_. В поле Порядок сортировке записываем _`NRDOC2`_. В поле Список ключевых полей для обновления записываем _`NRDOC`_`;`_`NRDOC1`_`;`_`NRDOC2`_`.`

![](../../../.gitbook/assets/screenshot128.png)

 Далее переходим на вкладку

![](../../../.gitbook/assets/sql-generator%20%281%29.png)

 и нажимаем на кнопку

![](../../../.gitbook/assets/get-tables.png)

![](../../../.gitbook/assets/screenshot129.png)

 Далее нажимаем на кнопку

![](../../../.gitbook/assets/get-table-fields%20%282%29.png)

![](../../../.gitbook/assets/screenshot130.png)

 После чего на кнопку

![](../../../.gitbook/assets/generate-sql%20%281%29.png)

![](../../../.gitbook/assets/screenshot131.png)

 В результате появился SQL запрос для добавления записей

![](../../../.gitbook/assets/insert2.png)

![](../../../.gitbook/assets/screenshot132.png)

 Обновления записей 

![](../../../.gitbook/assets/update%20%282%29.png)

![](../../../.gitbook/assets/screenshot133.png)

 Удаления записей

![](../../../.gitbook/assets/delete.png)

  и

![](../../../.gitbook/assets/screenshot138.png)

 Обновлении записей

![](../../../.gitbook/assets/refresh.png)

![](../../../.gitbook/assets/screenshot139.png)

 Для сохранения изменений ставим галочку напротив

![](../../../.gitbook/assets/save-on-exit-12%20%281%29.png)

 и нажимаем на кнопку

![](../../../.gitbook/assets/ok-15%20%281%29.png)

![](../../../.gitbook/assets/screenshot140.png)

 Далее приступаем для редактирования запроса для **Grid'a № 3**. Для этого открываем окно изменения запроса \(горячие клавиши **Alt+Q**\). Далее переходим на вкладку

![](../../../.gitbook/assets/sagi-properties-2%20%284%29.png)

 и записываем имя представления \(_`View`_\) `YVEINE_VMDB_INTAKE_LIST_C`. Напротив поля "Фильтр на выборку" записываем _`NRDOC=:NRDOC AND NRDOC1=:NRDOC1 AND NRDOC2=:NRDOC2`._ Напротив поля "Порядок сортировки" записываем поле _`NRDOC3`_. Напротив поля "Список ключевых полей для обновления" пишем _`NRDOC`_`;` _`NRDOC1`_`;` _`NRDOC2`_`;` _`NRDOC3`_.

![](../../../.gitbook/assets/screenshot153.png)

 Далее переходим на вкладку

![](../../../.gitbook/assets/sql-generator.png)

 и нажимаем на кнопку

![](../../../.gitbook/assets/get-tables%20%281%29.png)

![](../../../.gitbook/assets/screenshot154.png)

 Далее нажимаем на кнопку

![](../../../.gitbook/assets/get-table-fields.png)

![](../../../.gitbook/assets/screenshot155.png)

 После чего на кнопку

![](../../../.gitbook/assets/generate-sql.png)

![](../../../.gitbook/assets/screenshot156.png)

 В результате появился SQL запрос на добавление записей 

![](../../../.gitbook/assets/insert2%20%281%29.png)

![](../../../.gitbook/assets/screenshot157.png)

 Изменения записей

![](../../../.gitbook/assets/update.png)

![](../../../.gitbook/assets/screenshot158.png)

 Удаления записей

![](../../../.gitbook/assets/delete%20%281%29.png)

 и

![](../../../.gitbook/assets/screenshot159.png)

 Обновления записей

![](../../../.gitbook/assets/refresh%20%281%29.png)

![](../../../.gitbook/assets/screenshot160.png)

 На вкладке

![](../../../.gitbook/assets/sql.png)

 появился SQL запрос, который выбирает поля из вида \(_`View`_\) `YVEINE_VMDB_INTAKE_LIST_C`, где _`NRDOC=:NRDOC AND NRDOC1=:NRDOC1 AND NRDOC2=:NRDOC2`_ и сортирует по колонке _`NRDOC3`_.

![](../../../.gitbook/assets/screenshot161.png)



