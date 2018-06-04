# Инструкция по фокусам

Для того чтобы при открытии документа был сфокусирован какой-либо Control, необходимо в конфигураторе добавить свойство FocusControl и его название \(тип свойства по умолчанию String\). Сохраняем изменения с помощью галочки

![](../.gitbook/assets/commit%20%288%29.png)

 "Commit".

![](../.gitbook/assets/1%20%282%29.png)

 В программе нажимаем горячую клавишу F5 для обновления настроек. В появившемся окне нажимаем кнопку

![](../.gitbook/assets/yes.png)

![](../.gitbook/assets/confirm%20%281%29.png)

 Далее выйдет окно о успешном обновлении настроек, нажимаем кнопку

![](../.gitbook/assets/ok%20%2810%29.png)

![](../.gitbook/assets/uma.md%20%282%29.png)

 После открытия документа на редактирование, фокус находится на Control'e `UnDBEdit1`.

![](../.gitbook/assets/4%20%283%29.png)

 Для того, чтобы при открытии документа на редактирование фокусировался другой Control, изменим его название в конфигураторе на другое.

![](../.gitbook/assets/5%20%283%29.png)

 При сохранении, обновлении настроек и открытии документа, фокусируется на Control `UnDBEdit2`.

![](../.gitbook/assets/6%20%282%29.png)

 Для того, чтобы при открытии документа на редактирование фокусировался третий Control, изменим его название в конфигураторе.

![](../.gitbook/assets/7.png)

 При сохранении, обновлении настроек и открытии документа, фокусируется на Control `UnDBEdit3`.

![](../.gitbook/assets/8%20%281%29.png)

 Для перехода в дизайн Header'a нажимаем на ролик мыши или с зажатым Ctrl нажимаем правой кнопкой мыши и в появившемся списке выбираем

![](../.gitbook/assets/design.png)

 Здесь можно посмотреть имена объектов Control, которые уже созданы.

![](../.gitbook/assets/19%20%281%29.png)

 Для того, чтобы при открытии документа на редактирование фокусировался Control `DBMemo1`, запишем его название в конфигураторе.

![](../.gitbook/assets/20%20%282%29.png)

 При сохранении, обновлении настроек и открытии документа, фокусируется Control `DBMemo1`.

![](../.gitbook/assets/21.png)

Для того, чтобы при открытии документа на редактирование фокусировался Control `DBCheckBox1`, запишем его название в конфигураторе.

![](../.gitbook/assets/22%20%282%29.png)

 При сохранении, обновлении настроек и открытии документа, фокусируется Control `DBCheckBox1`.

![](../.gitbook/assets/23%20%283%29.png)

Так же можно фокусироваться на грид. Документ, выбранный в качестве примера, имеет 3  грида. Соответственно `gr21a` это первый грид. 

![](../.gitbook/assets/9%20%283%29.png)

 В документе при нажатии на каждом гриде горячих клавиш Alt+D сверху можно посмотреть

![](../.gitbook/assets/s7%20%281%29.png)

![](../.gitbook/assets/14%20%281%29.png)

 Для второго грида это соответственно

![](../.gitbook/assets/s8.png)

![](../.gitbook/assets/16%20%282%29.png)

 А для третьего

![](../.gitbook/assets/s9.png)

![](../.gitbook/assets/18.png)

 При записи свойства 

![](../.gitbook/assets/focuscontrol1.png)

 сохранении изменений с помощью

![](../.gitbook/assets/commit.png)

 и обновлении настроек, фокусируется первый грид:

![](../.gitbook/assets/10%20%282%29.png)

 При записи свойства

![](../.gitbook/assets/focuscontrol2.png)

 сохранении изменений с помощью

![](../.gitbook/assets/commit%20%286%29.png)

 и обновлении настроек, фокусируется второй грид:

![](../.gitbook/assets/11%20%281%29.png)

 При записи свойства

![](../.gitbook/assets/focuscontrol3.png)

 сохранении изменений с помощью

![](../.gitbook/assets/commit%20%282%29.png)

 и обновлении настроек, фокусируется третий грид:

![](../.gitbook/assets/12.png)

Список объектов Control, имена которых можно записывать в свойстве FocusControl в конфигураторе:

![](../.gitbook/assets/24%20%282%29.png)

| **Имя Control’a:** | **Свойство в конфигураторе:** | **Внешний вид:** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Edit1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO1.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C1.png?raw=true) |
| DBEdit1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO2.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C2.png?raw=true) |
| UnDBEdit1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO3.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C3.png?raw=true) |
| UnScList1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO4.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C4.png?raw=true) |
| CheckBox1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO5.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C5.png?raw=true) |
| DBCheckBox1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO6.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C6.png?raw=true) |
| DateEdit1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO7.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C7.png?raw=true) |
| DBDateEdit1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO8.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C8.png?raw=true) |
| DateTimeEdit1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO9.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C9.png?raw=true) |
| DBDateTimeEdit1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO10.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C10.png?raw=true) |
| RadioGroup1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO11.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C11.png?raw=true) |
| DBRaditGroup1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO12.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C12.png?raw=true) |
| Memo1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO13.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C13.png?raw=true) |
| DBMemo1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO14.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C14.png?raw=true) |
| Button1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO16.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C15.png?raw=true) |
| DBImage1 | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO15.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C16.png?raw=true) |
| DBImage1 \(с картинкой\) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/CO15.png?raw=true) | ![](https://github.com/prbsoft/wiki/blob/master/src/focus/C17.png?raw=true) |

