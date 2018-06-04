# Создание вида

##  **2 Создание вида**

###  **2.1 Создание вида \(вариант № 1\)**

 Так как напрямую с таблицами не работают, создадим вид \(_View_\). Для этого перейдем в список _Views_ и нажмем на

![](../../.gitbook/assets/create-new-node2.png)

 для создания нового вида \(_View_\).

![](../../.gitbook/assets/screenshot309.png)

 Напротив

![](../../.gitbook/assets/view-name%20%282%29.png)

 записываем имя вида \(_View_\). На вкладке 

![](../../.gitbook/assets/source%20%282%29.png)

 пишем скрипт, который выберет все колонки из таблицы `YVEINE_TMDB_INTAKE_LIST_A`. После чего нажимаем

![](../../.gitbook/assets/ok5%20%281%29.png)

![](../../.gitbook/assets/screenshot310.png)

 Для создания второго вида\(_View_\) нажимаем

![](../../.gitbook/assets/create-new-node2%20%281%29.png)

 и напротив

![](../../.gitbook/assets/view-name.png)

 пишем имя. На вкладке 

![](../../.gitbook/assets/source.png)

 записываем скрипт, который выберет все колонки из таблицы YVEINE\_TMDB\_INTAKE\_LIST\_B и нажмем

![](../../.gitbook/assets/ok5%20%282%29.png)

![](../../.gitbook/assets/screenshot311.png)

 Для создания третьего вида делаем тоже самое, что и на предыдущих шагах. Нажимаем 

![](../../.gitbook/assets/create-new-node2%20%282%29.png)

 Напротив

![](../../.gitbook/assets/view-name%20%281%29.png)

 записываем имя третьего вида\(_View_\). На вкладке 

![](../../.gitbook/assets/source%20%281%29.png)

 записываем скрипт на выборку всех колонок из таблицы `YVEINE_TMDB_INTAKE_LIST_С` и нажимаем

![](../../.gitbook/assets/ok5.png)

![](../../.gitbook/assets/screenshot312%20%281%29.png)

 Для появления созданных видов \(_Views_\) нажимаем

![](../../.gitbook/assets/refresh-all%20%283%29.png)

 "**Refresh all objects**". Для завершения транзакции с сохранением нажимаем

![](../../.gitbook/assets/commit3%20%282%29.png)

 **“Commit”**.

![](../../.gitbook/assets/screenshot313.png)

###  **2.2 Создание вида \(вариант № 2\)**

 Для более быстрого создания вида \(_View_\) перейдем в редактор, для этого нажмем на

![](../../.gitbook/assets/editor%20%281%29.png)

![](../../.gitbook/assets/screenshot072.png)

 Напишем скрипт создания вида \(_`CREATE VIEW`_\) и выберем все колонки \(_`SELECT *`_\) из таблицы \(`FROM YVEINE_TMDB_INTAKE_LIST_A`\). Для его запуска используем горячие клавиши **Ctrl+Enter**.

![](../../.gitbook/assets/screenshot073.png)

 Напишем скрипт создания вида \(_`CREATE VIEW`_\) и выберем все колонки \(_`SELECT *`_\) из таблицы \(`FROM YVEINE_TMDB_INTAKE_LIST_B`\). Для его запуска используем горячие клавиши **Ctrl+Enter**.

![](../../.gitbook/assets/screenshot074.png)

 Напишем скрипт создания вида \(_`CREATE VIEW`_\) и выберем все колонки \(_`SELECT *`_\) из таблицы \(`FROM YVEINE_TMDB_INTAKE_LIST_C`\). Для его запуска используем горячие клавиши **Ctrl+Enter**.

![](../../.gitbook/assets/screenshot075.png)

 После чего откроем _Views_.

![](../../.gitbook/assets/screenshot076.png)

 C помощью поиска найдем созданные виды \(_Views_\).

![](../../.gitbook/assets/screenshot077.png)

###  **2.3 Добавление дополнительных колонок в вид**

 Тип данных у всех колонок\(кроме _`DATA`_\) "`Data Type`" _`NUMBER(10)`_, а это значит, что данные из справочников будут в виде цифрового кода, так как колонка _`COD`_в справочнике _`TMS_UNIVERS`_ имеет такой же тип данных _`NUMBER(10)`_. Именно поэтому необходимо создать новые колонки, в которых будет другой тип данных. Для этого переходим на вкладку

![](../../.gitbook/assets/script.png)

 и копируем его в редактор с помощью

![](../../.gitbook/assets/edit%20%282%29.png)

![](../../.gitbook/assets/screenshot078.png)

Добавляем вычисляемую \(_`CLC`_\) текстовую \(_`T`_\) колонку _`CLCDISHT`_ и записываем к ней подзапрос \(`SELECT DENUMIREA FROM TMS_UNIVERS WHERE COD = A.DISH`\).

Для выполнения скрипта используем горячие клавиши **Ctrl+Enter**.

![](../../.gitbook/assets/screenshot079.png)

 В результате чего появится дополнительная колонка _`CLCDISHT`_.

![](../../.gitbook/assets/screenshot080.png)

 Для второго вида\(_View_\) делаем идентичное действие. Переходим на вкладку

![](../../.gitbook/assets/script%20%281%29.png)

 и копируем скрипт в редактор с помощью

![](../../.gitbook/assets/edit%20%281%29.png)

![](../../.gitbook/assets/screenshot081.png)

Добавляем вычисляемую \(_`CLC`_\) текстовую \(_`T`_\) колонку _`CLCPRODUCTT`_. Записываем подзапрос \(`SELECT DENUMIREA FROM TMS_UNIVERS WHERE COD = A.PRODUCT`\)

Для выполнения запроса используем горячие клавиши **Ctrl+Enter**.

![](../../.gitbook/assets/screenshot085%20%281%29.png)

 В результате чего появится дополнительная колонка _`CLCPRODUCTT`_.

![](../../.gitbook/assets/screenshot083.png)

 Тоже самое выполняем и для третьего вида\(_View_\). Переходим на вкладку и копируем его в редактор с помощью кнопки

![](../../.gitbook/assets/edit.png)

![](../../.gitbook/assets/screenshot084.png)

Добавляем вычисляемую \(_`CLC`_\) текстовую \(_`T`_\) колонку _`CLCPRODUCTT`_. Записываем подзапрос \(`SELECT DENUMIREA FROM TMS_UNIVERS WHERE COD = A.PRODUCT`\)

Для выполнения запроса используем горячие клавиши **Ctrl+Enter**.

![](../../.gitbook/assets/screenshot085.png)

 В результате чего появится дополнительная колонка _`CLCPRODUCTT`_. После проведенных действий сохраняем изменения в текущей транзакции с помощью

![](../../.gitbook/assets/commit3.png)

  “**Commit”**.

![](../../.gitbook/assets/screenshot086.png)



