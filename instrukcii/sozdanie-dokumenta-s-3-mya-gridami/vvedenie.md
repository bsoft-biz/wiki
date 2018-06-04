# Введение

В качестве примера возьмем вымышленный объект Кафе-бар "_Veine_". Наш документ будет состоять из трех гридов и шапки. В шапке будет выбираться Кафе-бар "_Veine_" и отдел снабжения. В первом гриде будут находится наименования блюд. Во втором гриде - наименования продуктов для приготовления блюд. В третьем гриде - наименования продуктов для замены.

Любой объект в среде СУБД Oracle должен носить название. Ниже приведена расшифровка названий, которые будут использоваться при создании Таблиц \(Tables\), Видов \(Views\), Индексов \(Indexes\), Последовательности \(Sequences\) и Триггеров \(Triggers\).

![](../../.gitbook/assets/bez-imeni-3.png)

![](../../.gitbook/assets/bez-imeni-1.png)

![](../../.gitbook/assets/bez-imeni-2.png)

![](../../.gitbook/assets/indeks.png)

![](../../.gitbook/assets/posledovatelnost.png)

![](../../.gitbook/assets/trigger.png)

 Прежде чем создать любой документ, необходимо представить как он будет выглядеть в готовом виде, определить сколько в нём будет колонок, какой их тип, где будет первичный и внешние ключи, какие колонки будут со значением "_Not Null_" и т.д.

**Grid № 1**:

●     Колонка _NRDOC_ является первичным ключом и связана внешним ключом с _TMDB\_DOCS_ с колонкой _COD_. \(В таблице _TMDB\_DOCS_ одна запись приравнивается к одному документу.\)

●     Колонка NRDOC1 так же является первичным ключом.

●     Колонка Дата \(DATA\) предназначена для записывания даты.

●     Колонка Код\(DISH\) связана внешним ключом со справочником _TMS\_UNIVERS_ \(с колонкой COD\).

●     Колонка Наименование блюд \(CLCDISHT\) предназначена для вставки текста из справочника _TMS\_UNIVERS_.

●     Колонки Передано \(CANT1\) Возвращено \(CANT2\) и Итого кол-во \(CANT3\) предназначены для численного заполнения.

**Grid № 2**

●     Колонки _NRDOC_,  _NRDOC1_ и _NRDOC2_ являются первичными ключами.

●     Колонки _NRDOC_, _NRDOC1_ связаны внешним ключом с таблицей YVEINE\_TMDB\_INTAKE\_LIST\_A \(Колонки _NRDOC_, _NRDOC1_\) \[Grid 1\].

●     Колонка Код \(_PRODUCT_\) связана внешним ключом со справочником _TMS\_UNIVERS_ \(с колонкой _COD_\).

●     Колонка Наименование продуктов \(_CLCPRODUCTT_\) предназначена для вставки текста из справочника _TMS\_UNIVERS_.

●     Колонки Норма \(_CANT1_\), Цена \(_PRET1_\) и Сумма \(_SUMA1_\) предназначены для числовых значений.

**Grid № 3**

●     Колонки _NRDOC_, _NRDOC1_, _NRDOC2_ и _NRDOC3_ являются первичными ключами.

●     Колонки _NRDOC_, _NRDOC1_ и _NRDOC2_ связаны внешним ключом с таблицей YVEINE\_TMDB\_INTAKE\_LIST\_B \(Колонки _NRDOC_, _NRDOC1_ и _NRDOC2_\) \[Grid 2\].

●     Колонка Код \(PRODUCT\) связана внешним ключом со справочником _TMS\_UNIVERS_ \(с колонкой _COD_\).

●     Колонка Наименование продуктов для замены \(_CLCPRODUCTT_\) предназначена для вставки текста из справочника _TMS\_UNIVERS_.

●     Колонка Количество \(_CANT1_\) предназначена для числовых значений.

![](../../.gitbook/assets/dokument.png)

**Используемое программное обеспечение:**

ОС Windows 8.1 Build 9431

Oracle VM VirtualBox  4.2.18 r88780

Toad for Oracle 11.6

Oracle 10g 10.2.0.3

Universal Accounting Build 4.1.5.52

##  **Глава 1 Создание таблицы**

###  **1.1 Добавление колонок и создание внешних ключей**

 Для создания таблицы необходимо с помощью программы _Toad_ подключиться к рабочей схеме. Для этого заполним необходимые поля и нажмем

![](../../.gitbook/assets/connect.png)

 для подключения.

![](../../.gitbook/assets/screenshot001.png)

 Перейдем в **Schema Browser** с помощью кнопки

![](../../.gitbook/assets/schema-browser.png)

![](../../.gitbook/assets/screenshot002.png)

 Далее нажимаем на кнопку

![](../../.gitbook/assets/create-new-node.png)

 для создания таблицы.

![](../../.gitbook/assets/screenshot003.png)

 Напротив

![](../../.gitbook/assets/table-name.png)

 записываем название таблицы. В данном случае это `YVEINE_TMDB_INTAKE_LIST_A` \(см. Введение\).

![](../../.gitbook/assets/screenshot004.png)

 С помощью кнопки

![](../../.gitbook/assets/add-col.png)

 добавляем колонки.

![](../../.gitbook/assets/screenshot005.png)

 Добавляем колонку _`NRDOC`_ ``с `Data Type` _`NUMBER`_ и точностью \(`Precision`\) 10. Ставим галочки ниже _`PK`_ `(Primary Key)` и _`Not Null`_.

![](../../.gitbook/assets/screenshot006.png)

 Далее добавляем колонку _`NRDOC1`_ ``с точно такими же параметрами. Колонка _`NRDOC1`_как и _`NRDOC`_является первичным ключом\(_`PK`_\) и с ненулевым значением.

![](../../.gitbook/assets/screenshot007.png)

 Добавляем поле _`ID`_с числовым типом данных\(_`NUMBER`_\) и точностью \(`Precision`\) 10.

![](../../.gitbook/assets/screenshot008.png)

 Далее добавляем колонку _`DATA`_с типом данных _`DATE`_.

![](../../.gitbook/assets/screenshot009.png)

 Колонка _`DISH`_\(Блюдо\) имеет такой же тип данных и точность как и колонка _`ID`_.

![](../../.gitbook/assets/screenshot010.png)

 И последними добавляем колонки _`CANT1`_

![](../../.gitbook/assets/screenshot011.png)

 _`CANT2`_и

![](../../.gitbook/assets/screenshot012.png)

_`CANT3`_с одинаковыми типом данных и точностью.

Далее нажимаем на вкладку

![](../../.gitbook/assets/constraints.png)

![](../../.gitbook/assets/screenshot013.png)

 Здесь уже есть первичный ключ\(_PK_\) который представлен двумя колонками. Нажимаем на 

![](../../.gitbook/assets/add-constraint.png)

![](../../.gitbook/assets/screenshot014.png)

 В появившемся окне выбираем внешний ключ \(_`Foreign Key`_\) и нажимаем

![](../../.gitbook/assets/ok2%20%282%29.png)

![](../../.gitbook/assets/screenshot015.png)

 На левой стороне показаны все колонки таблицы, на правой стороне выбранные колонки. Выбор можно осуществлять посредством двойного клика левой клавиши мыши \(ЛКМ\) или с помощью знаков

![](../../.gitbook/assets/bolshe.png)

![](../../.gitbook/assets/menshe.png)

![](../../.gitbook/assets/bolshe-2.png)

![](../../.gitbook/assets/menshe-2.png)

 Выбираем поле _`NRDOC`_.

![](../../.gitbook/assets/screenshot016.png)

 Далее переходим на вкладку 

![](../../.gitbook/assets/referenced-table.png)

 и из списка выбираем таблицу _`TMDB_DOCS`_.

![](../../.gitbook/assets/screenshot017.png)

 В левой части находятся поля таблицы _`TMDB_DOCS`_. Выбираем поле _`COD`_. Ограничениям \(_`Constraints`_\) необходимо давать имя. Кнопка

![](../../.gitbook/assets/suggest.png)

 предложит имя по умолчанию. Но можно написать и свой вариант.

![](../../.gitbook/assets/screenshot018.png)

 Далее переходим на вкладку

![](../../.gitbook/assets/options.png)

 и ставим галочки напротив _`On Delete Cascade`_ \(для каскадного удаления\) и _`Deferrable-Initially Deferred`_. \(чтобы Constraint проверялись только на **`Commit'e`**\)

![](../../.gitbook/assets/screenshot019.png)

 Далее нажимаем на ,выбираем внешний ключ \(_`Foreign Key`_\) и нажимаем

![](../../.gitbook/assets/ok2%20%283%29.png)

![](../../.gitbook/assets/screenshot020.png)

 Выбираем колонку _DISH_ \(Блюдо\) и переходим на вкладку

![](../../.gitbook/assets/referenced-table%20%281%29.png)

![](../../.gitbook/assets/screenshot021.png)

 Выбираем из списка справочник _`TMS_UNIVERS`_.

![](../../.gitbook/assets/screenshot022.png)

 И выбираем колонку _`COD`_. После чего даём ограничению имя либо произвольно, либо с помощью кнопки

![](../../.gitbook/assets/suggest%20%281%29.png)

![](../../.gitbook/assets/screenshot023.png)

 После выполненных действий нажимаем кнопку

![](../../.gitbook/assets/ok2%20%284%29.png)

![](../../.gitbook/assets/screenshot024.png)

 Для того чтобы таблица появилась в списке нажимаем на

![](../../.gitbook/assets/refresh-all.png)

  "**Refresh all objects**".

![](../../.gitbook/assets/screenshot025.png)

 После чего в поиске вводим название и находим созданную таблицу.

![](../../.gitbook/assets/screenshot026.png)



