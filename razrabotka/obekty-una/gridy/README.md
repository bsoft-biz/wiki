# Гриды

[Параметры выпадающих справочников Alt+D](https://bsoft.gitbook.io/wiki/razrabotka/obekty-una/gridy/parametry-vypadayushikh-spravochnikov)

[Цвета](https://bsoft.gitbook.io/wiki/razrabotka/obekty-una/gridy/cveta)

Форматы представления и редактирования данных \([Display Format Edit mask](https://bsoft.gitbook.io/wiki/razrabotka/obekty-una/gridy/display-format-edit-mask)\)

[Настройка документа для ввода данных сканером штрих-кодов](https://bsoft.gitbook.io/wiki/razrabotka/obekty-una/gridy/nastroika-dokumenta-dlya-vvoda-dannykh-skanerom-shtrikh-kodov)

[Настройка SagiProperties](https://bsoft.gitbook.io/wiki/razrabotka/obekty-una/gridy/nastroika-sagiproperties)

Считать и отображать итог  в шапке, при вводе данных в гриде .

В гриде делается update таблицы шапки , а в гриде выставляется св-во по умолчанию + SagiMasterRefresh

{% hint style="info" %}
**Подсказка:**

-в гридах форм можно задать формат полей типа дата и/или время. Для этого соответствующие поля запроса надо назвать с соответствующим окончанием: \_date =&gt; дата; \_time =&gt; время; \_datetime =&gt; датавремя \(например: select  sysdate as datas\_datetime from dual =&gt; будет визуально показываться и дата и время\)

-в универсальной настраиваемой форме, где в верхней панели есть datab, dataf, sc. Чтобы в запросе для выпадающего списка в поле sc ссылаться на значения datab,dataf: datab=edit\_fmFS1c\_dtb

-если в универсальной настраиваемой форме при выборе sc появляются данные в мастере и не появляются в детаиле, надо убрать в Alt+D детаила галку "Рефрешить мастер"
{% endhint %}



