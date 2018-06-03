# Нумерация документов

 Как видно из поля № док-та нумерация не происходит.

![](../.gitbook/assets/do2.png)

 Переходим в конфигуратор и находим Action для нумерации

![](../.gitbook/assets/prisvoenie.png)

![](../.gitbook/assets/n2.png)

 Копируем данный Action с помощью:

![](../.gitbook/assets/copy-node.png)

![](../.gitbook/assets/n3.png)

 Получаем сообщение о завершении экспорта одного узла:

![](../.gitbook/assets/copy-nodes%20%281%29.png)

 Далее нажимаем

![](../.gitbook/assets/ok%20%2814%29.png)

 Вставляем как подузел  в Document Actions требуемого документа в помощью:

![](../.gitbook/assets/paste-new-subnode.png)

![](../.gitbook/assets/n5.png)

 Получаем сообщение о завершении импорта одного узла:

![](../.gitbook/assets/copy-nodes.png)

 Выделяем свойство

![](../.gitbook/assets/sql.png)

 и нажимаем

![](../.gitbook/assets/edit-property.png)

для открытия окна редактирования \(либо двойным кликом левой кнопкой мыши\). В открывшемся окне указываем пакет Un$vp$util и через точку \(!\) процедуру alt\_seq

И в скобках передаём номер документа через двоеточие \(!\) \(:nrdoc,'10'\)

![](../.gitbook/assets/editing-property-sql1.png)

 Далее нажимаем

![](../.gitbook/assets/ok-konfiguratora.png)

 Переходим к свойствам для автовыполнения действия \(Action\). Для этого находим свойства EAutoGFCOrder и EAutoGFCRun. Включаем Multiselect, нажав кнопку

![](../.gitbook/assets/multiselect.png)

 Далее копируем два свойства для автовыполнения действия \(Action\) с помощью кнопки 

![](../.gitbook/assets/vstavit.png)

 или с помощью горячих клавиш Ctrl+C.

![](../.gitbook/assets/n8.png)

 Вставляем свойства с помощью кнопки

![](../.gitbook/assets/vstavit%20%281%29.png)

 или с помощью горячих клавиш Ctrl+V.

 Таким образом в свойстве EAutoGFCOrder указывается ID действия \(Action\), которое должно выполниться при сохранении документа. Свойство EAutoGFCRun включает автовыполнение действий \(Action\) при сохранении документа.

![](../.gitbook/assets/svoistva.png)

 Сохраняем изменения  с помощью

![](../.gitbook/assets/commit%20%283%29.png)

 \(Commit\). Для вступления изменений в силу в программе нажимаем горячую клавишу F5 для обновления настроек:

![](../.gitbook/assets/confirm%20%281%29.png)

 В открывшемся окне нажимаем

![](../.gitbook/assets/yes%20%282%29.png)

 Получаем сообщение об успешном обновлении настроек:

![](../.gitbook/assets/uma.md%20%281%29.png)

 После чего нажимаем

![](../.gitbook/assets/ok%20%289%29.png)

 Создадим новый документ с помощью кнопки

![](../.gitbook/assets/novyi.png)

 Далее сохраняем документ с помощью кнопки

![](../.gitbook/assets/sokhranit%20%283%29.png)

![](../.gitbook/assets/n13.png)

 В результате чего в поле № док-та автоматически установилась цифра 1.

![](../.gitbook/assets/do1.png)

 При создании и сохранении других документов, происходит автоматическая нумерация.

![](../.gitbook/assets/dok-ta.png)

