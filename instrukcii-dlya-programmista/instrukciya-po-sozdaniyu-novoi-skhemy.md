# Инструкция по созданию новой схемы

**Инструкция по созданию новой схемы**

Данная инструкция описывает этапы создания новой \(пустой\) схемы программы ”Universal Accounting”, путем экспорта имеющейся рабочей схемы. После завершения всех этапов данной инструкции создается схема идентичная рабочей схеме, но с незаполненными журналами документов. При этом в новой схеме полностью сохраняется структура, настройки и содержание справочников, форм, отчетов и печатных форм документов.

**Содержание:**

1. Предварительные настройки.
2. Экспорт рабочей схемы.
3. Импорт новой схемы.
4. Проверка отличий.

### **1. Предварительные настройки.**

1.1 Подключиться посредством удаленного помощника \(командная строка : mstsc \) к серверу, на котором находится необходимая схема.

1.2 Запустить программу un4Versions.exe. Приложение находится в папке GOOD на локальном диске \(интерфейс приложения un4Versions.exe – рис.1\).

1.3 Посредством приложения un4Versions.exe подключиться к нужному серверу с правами супервизора. Для этого необходимо выполнить следующие действия :

 1.3.1 Выбрать вкладку "Настройки"

![](../.gitbook/assets/1%20%281%29.png)

 или пункт меню "Настройки подключения"

![](../.gitbook/assets/2%20%281%29.png)

 1.3.2 В поле "сервер или ..." ввести имя сервера

![](../.gitbook/assets/3%20%282%29.png)

 1.3.3 Если пароль на подключение к схеме с правами супервизора SYS/SYS, нажать кнопку "Подключиться" 

![](../.gitbook/assets/4%20%284%29.png)

 Если пароль другой, нажать "Подключиться с вводом пароля"

![](../.gitbook/assets/5%20%281%29.png)

 и ввести необходимый пароль.

### **2. Экспорт рабочей схемы.**

Необходимо сделать экспорт имеющейся схемы с фильтром на данные. Для этого необходимо выполнить следующие шаги:

 2.1 Выбрать вкладку "DataPump"

![](../.gitbook/assets/6%20%283%29.png)

 или пункт меню "Экспорт/импорт схемы"

![](../.gitbook/assets/7%20%282%29.png)

 2.2 Во внутренних вкладках выбрать вкладку "Действия"

![](../.gitbook/assets/8.png)

 2.3 Ввести или выбрать из списка поле "Схема-источник"

![](../.gitbook/assets/9%20%282%29.png)

 Это поле содержит название рабочей схемы, которую мы экспортируем.

 2.4 Ввести или выбрать из списка поле "Oracle Directory"

![](../.gitbook/assets/10.png)

 Если оставить поле пустым, то по умолчанию берется директория оракла DATA\_PUMP\_DIR.

 2.5 При необходимости откорректировать поле "Файл экспорта"

![](../.gitbook/assets/11%20%283%29.png)

 \(по умолчанию - совпадает с именем схемы-источника\)

 2.6 Нажать кнопку "Скомпилировать ист."

![\(&#x43D;&#x435;&#x43E;&#x431;&#x44F;&#x437;&#x430;&#x442;&#x435;&#x43B;&#x44C;&#x43D;&#x43E;\)](../.gitbook/assets/12%20%283%29.png)

 2.7 Нажать кнопку "Создать таблицу объектов"

![](../.gitbook/assets/13%20%281%29.png)

 2.8 Выбрать вкладку "Фильтр на таблицы"

![](../.gitbook/assets/14%20%282%29.png)

 2.9 Нажать кнопку "Заполнить главные"

![](../.gitbook/assets/15%20%282%29.png)

 \(в нижней части окна\)

 2.10 Просмотреть и, если не установлен, поставить фильтр: галка "Контроль вручную"

![](../.gitbook/assets/16%20%283%29.png)

  \(рис.2\).

2.11 Снова вернуться на вкладку "Действия"

2.12 Нажать кнопку "Экспорт по фильтру"

![](../.gitbook/assets/17%20%282%29.png)

 При этом появится окно сообщений

![](../.gitbook/assets/18%20%281%29.png)

 Следует дождаться успешного завершения процесса экспорта.

![](../.gitbook/assets/19.png)

### **3. Импорт новой схемы.**

Необходимо сделать импорт полученного файла в новую схему. Для этого необходимо выполнить следующие шаги:

3.1 Подключиться к серверу импорта \(туда, где будет стоять база\). Если он на другом сервере – см. пункт 1.3.

3.2 Если необходимо - снова заполнить поле "Схема-источник"

![](../.gitbook/assets/20%20%281%29.png)

\(поле обязательно должно быть заполнено при импорте!\). Здесь указывается имя схемы, которая экспортировалась \(без документов\) для создания новой схемы.

3.3 В поле "Новая схема" ввести название \(по умолчанию имя схемы-источника\)

![](../.gitbook/assets/21%20%282%29.png)

 3.4 Нажать кнопку "Импорт всей схемы"

![](../.gitbook/assets/22%20%281%29.png)

 При этом появится окно сообщений

![](../.gitbook/assets/23%20%282%29.png)

 Следует дождаться успешного завершения процесса

![](../.gitbook/assets/24.png)

 Как правило, процесс импорта завершается с ошибками. Ошибки можно посмотреть нажав кнопку

![](../.gitbook/assets/25.png)

 3.5 Обязательно нажать кнопку "Скомпилировать ист." 

![](../.gitbook/assets/26.png)

### **4. Проверка отличий.**

Необходимо проверить в наличии и состоянии объектов. Для этого необходимо выполнить следующие действия :

1. Выбрать вкладку "Сравнение объектов"

![](../.gitbook/assets/27.png)

 2. Установить фильтр \(галку\) "Контроль вручную"

![](../.gitbook/assets/28%20%281%29.png)

 \(рис.3\).

3. Необходимо добиться, чтобы количество невалидных объектов было минимальным.

![&#x420;&#x438;&#x441;&#x443;&#x43D;&#x43E;&#x43A; 1](../.gitbook/assets/29.png)

![&#x420;&#x438;&#x441;&#x443;&#x43D;&#x43E;&#x43A; 2](../.gitbook/assets/30.png)

![&#x420;&#x438;&#x441;&#x443;&#x43D;&#x43E;&#x43A; 3](../.gitbook/assets/31%20%281%29.png)

