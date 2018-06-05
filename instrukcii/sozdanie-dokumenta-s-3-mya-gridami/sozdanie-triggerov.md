# Создание триггеров

##  **5 Создание триггеров**

 Для использования последовательности создадим для каждой таблицы триггер. Для этого перейдем в списке на вкладку _Triggers_.

![](../../.gitbook/assets/screenshot200.png)

 Нажимаем на кнопку

![](../../.gitbook/assets/create-trigger.png)

 для создания нового триггера. В данном случае это `YVEINE_TMDB_INTAKE_LIST_A_TRG` \(см. Введение\).

![](../../.gitbook/assets/screenshot201.png)

 Напротив

![](../../.gitbook/assets/trigger-name%20%281%29.png)

 записываем имя триггера, в данном случае это `YVEINE_TMDB_INTAKE_LIST_A_TRG`. С помощью кнопки

![](../../.gitbook/assets/mnogotochie%20%289%29.png)

 выбираем таблицу, для которой создаётся данный триггер. В данном случае это таблица `YVEINE_TMDB_INTAKE_LIST_A` и нажимаем

![](../../.gitbook/assets/ok7%20%284%29.png)

![](../../.gitbook/assets/screenshot202.png)

 Ставим галочку напротив _`Insert`_ ``\(триггер будет действовать до \(_`Before`_\) добавления \(_`Insert`_\)\).

![](../../.gitbook/assets/screenshot203.png)

 Далее переходим на вкладку

![](../../.gitbook/assets/body.png)

 Здесь зеленой стрелкой отмечен комментарий, а синей PL/SQL блок \[Если новая колонка _`NRDOC1`_ с нулевым значением, тогда Выбирается последовательность следующего значения из виртуальной таблицы _`DUAL`_\]. Работа этого триггера будет давать колонке _`NRDOC1`_ уникальное значение при добавлении новой записи исходя из последовательности\(_`Sequence`_\).

![](../../.gitbook/assets/screenshot204.png)

 После нажатия на кнопку

![](../../.gitbook/assets/ok6%20%285%29.png)

 триггер будет создан.

![](../../.gitbook/assets/screenshot205.png)

 Для появления только что созданного триггера для первой таблицы нажмем кнопку

![](../../.gitbook/assets/refresh-all%20%281%29.png)

 "**Refresh all objects**".

![](../../.gitbook/assets/screenshot206.png)

 В результате чего в списке _Triggers_ появился созданный триггер `YVEINE_TMDB_INTAKE_LIST_A_TRG`. На вкладке

![](../../.gitbook/assets/sourse2.png)

  находится PL/SQL блок.

![](../../.gitbook/assets/screenshot207.png)

 На вкладке

![](../../.gitbook/assets/columns%20%284%29.png)

 выбранная строка для которой создан триггер.

![](../../.gitbook/assets/screenshot208.png)

 Вкладка

![](../../.gitbook/assets/errors.png)

 показывает ошибки.

![](../../.gitbook/assets/screenshot209.png)

 Приступим к созданию второго триггера. Для этого нажмем на

![](../../.gitbook/assets/create-new-node-3%20%281%29.png)

![](../../.gitbook/assets/screenshot210.png)

 Напротив

![](../../.gitbook/assets/trigger-name.png)

 запишем имя второго триггера. В данном случае это `YVEINE_TMDB_INTAKE_LIST_B` \(см. Введение\). С помощью кнопки

![](../../.gitbook/assets/mnogotochie%20%287%29.png)

выбираем таблицу, для которой создаётся данный триггер. Это таблица `YVEINE_TMDB_INTAKE_LIST_B`.

Ставим галочку напротив _`Insert`_. В этом случае триггер будет работать \(_`Before Insert`_\) До Добавления записи.

![](../../.gitbook/assets/screenshot211.png)

 Переходим на вкладку 

![](../../.gitbook/assets/body%20%281%29.png)

 и записываем PL/SQL блок, аналогичный первому триггеру. В данном случае колонка _`NRDOC2`_.

![](../../.gitbook/assets/screenshot212.png)

 После чего нажимаем

![](../../.gitbook/assets/ok6%20%281%29.png)

![](../../.gitbook/assets/screenshot213.png)

 Для появления нового триггера в списке нажмём

![](../../.gitbook/assets/refresh-all%20%285%29.png)

 "**Refresh all objects**".

![](../../.gitbook/assets/screenshot214.png)

 В списке находим второй триггер YVEINE\_TMDB\_INTAKE\_LIST\_B\_TRG. На вкладке

![](../../.gitbook/assets/sourse2%20%281%29.png)

  находится PL/SQL блок.

![](../../.gitbook/assets/screenshot215.png)

 Теперь создадим третий триггер. Для этого нажмем на

![](../../.gitbook/assets/create-trigger%20%281%29.png)

![](../../.gitbook/assets/screenshot216.png)

 Напротив

![](../../.gitbook/assets/trigger-name%20%282%29.png)

 записываем имя третьего триггера `YVEINE_TMDB_INTAKE_LIST_C_TRG` \(см. Введение\). С помощью кнопки

![](../../.gitbook/assets/mnogotochie%20%286%29.png)

 выбираем таблицу для создаваемого триггера. В данном случае это `YVEINE_TMDB_INTAKE_LIST_C` и нажимаем

![](../../.gitbook/assets/ok7%20%283%29.png)

![](../../.gitbook/assets/screenshot217.png)

 Далее переходим на вкладку

![](../../.gitbook/assets/body%20%282%29.png)

 и записываем PL/SQL блок аналогичный двум предыдущим триггерам. В данном случае колонка _`NRDOC3`_.

![](../../.gitbook/assets/screenshot218.png)

 Для завершения редактирования нажимаем

![](../../.gitbook/assets/ok6%20%282%29.png)

![](../../.gitbook/assets/screenshot219.png)

 Для появления нового триггера в списке нажмём

![](../../.gitbook/assets/refresh-all%20%287%29.png)

 "**Refresh all objects**".

![](../../.gitbook/assets/screenshot221.png)

 Триггер `YVEINE_TMDB_INTAKE_LIST_A_TRG` предназначен для колонки _`NRDOC1`_.

![](../../.gitbook/assets/screenshot222.png)

 Триггер `YVEINE_TMDB_INTAKE_LIST_B_TRG` предназначен для колонки _`NRDOC2`_.

![](../../.gitbook/assets/screenshot223.png)

 Триггер `YVEINE_TMDB_INTAKE_LIST_C_TRG` предназначен для колонки _`NRDOC3`_.

![](../../.gitbook/assets/screenshot224.png)

 Для завершения текущей транзакции с сохранением нажмем 

![](../../.gitbook/assets/commit3%20%284%29.png)

 **“Commit”**.

![](../../.gitbook/assets/screenshot225.png)



