# Инструкция по прыжкам

###  **Прыжки из документа**

 Открываем дизайн первого грида

![](../.gitbook/assets/s7.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%281%29.png)

```sql
DblClick=goto                      
TargetType=doc.print           
NrDoc=_NRDOC                
TargetSection=6:5:PRINTDOC_AKTRAZDELKI           
GotoNextRecord=1   
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%2810%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%284%29.png)

![](../.gitbook/assets/d1.png)

 После двойного клика по любой строке колонки CANT2 \(Возвращено\) построится печатная форма данного документа.

![](../.gitbook/assets/d2.png)

 После закрытия построенной печатной формы произошел переход на другую строку \(GotoNextRecord\).

![](../.gitbook/assets/d3.png)

 После двойного клика мыши построится печатная форма с другими данными \(\_NRDOC\).

![](../.gitbook/assets/d4.png)

 После закрытия построенной печатной формы произошел переход на другую строку \(GotoNextRecord\).

![](../.gitbook/assets/d5.png)

 После двойного клика мыши построится печатная форма с другими данными \(\_NRDOC\).

![](../.gitbook/assets/d6.png)

 После закрытия построенной печатной формы произошел переход на другую строку \(GotoNextRecord\).

![](../.gitbook/assets/d7.png)

 После двойного клика мыши построится печатная форма с другими данными \(\_NRDOC\).

![](../.gitbook/assets/d8.png)

 Открываем дизайн первого грида

![](../.gitbook/assets/gr21a-2%20%282%29.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%2810%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=doc.action
Action_ID=4
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%2812%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%283%29.png)

![](../.gitbook/assets/d9.png)

 После двойного клика мыши на любой строке поля CANT3 \(возвращено\) выполнится действие с ID=4.

![](../.gitbook/assets/d10.png)

 В данном случае это

![](../.gitbook/assets/zapolnit-na-osnovanii-spisaniya-gp.png)

![](../.gitbook/assets/d11.png)

 Открываем дизайн первого грида

![](../.gitbook/assets/gr21a-2-1.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%287%29.png)

```sql
DblClick=goto
TargetType=form
TargetSection=CURS
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%2814%29.png)

 и нажимаем 

![](../.gitbook/assets/ok-design%20%289%29.png)

![](../.gitbook/assets/d12.png)

 В результате двойного клика мыши по полю CANT3 \(Возвращено\), откроется форма

![](../.gitbook/assets/valyutnye-kursy.png)

![](../.gitbook/assets/d13.png)

 Открываем дизайн первого грида

![](../.gitbook/assets/gr21a-2.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%288%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=cartela
TargetSection=ATTR_ORD_ADD
nrdoc=_nrdoc
MainTA=1
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%2813%29.png)

 и нажимаем 

![](../.gitbook/assets/ok-design%20%287%29.png)

![](../.gitbook/assets/d14.png)

 В результате двойного клика мыши по полю CANT3 \(Возвращено\), открывается карточка.

![](../.gitbook/assets/d15.png)

 Открываем дизайн первого грида

![](../.gitbook/assets/gr21a-2%20%281%29.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%286%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=report
TargetSection=1:0:RG113
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%286%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%288%29.png)

![](../.gitbook/assets/d16.png)

 В результате двойного клика мыши по полю CANT3 \(Возвращено\), строится отчет.

![](../.gitbook/assets/d17.png)

 Имя секции можно посмотреть в конфигураторе, нажав кнопку

![](../.gitbook/assets/node-properties%20%281%29.png)

 Имя секции для данного отчёта

![](../.gitbook/assets/rg113.png)

![](../.gitbook/assets/d18.png)

###  **Прыжки из форм.**

 Открываем любую форму, например

![](../.gitbook/assets/valyutnye-kursy%20%284%29.png)

![](../.gitbook/assets/f1.png)

 Выделяем любое поле.

![](../.gitbook/assets/f2.png)

 Открываем дизайн грида с помощью горячих клавиш Alt+D и нажимаем

![](../.gitbook/assets/bloknot.png)

![](../.gitbook/assets/f3.png)

 Записываем:

```sql
DblClick=goto
TargetType=document
nrdoc=5645
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%281%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%282%29.png)

![](../.gitbook/assets/f4.png)

 В результате двойного клика мыши на любой строке поля COD1 \(Код1\) происходит переход в документ с Nrdoc=

![](../.gitbook/assets/5645%20%281%29.png)

![](../.gitbook/assets/f5.png)

 Добавляем свойство

![](../.gitbook/assets/gotodocumentediting.png)

 для пользователя или группы пользователей. Это свойство открывает документ на редактирование после перехода на него по двойному клику. Сохраняем изменения в текущей транзакции с помощью галочки

![](../.gitbook/assets/commit%20%281%29.png)

![](../.gitbook/assets/f6.png)

 В программе нажимаем горячую клавишу F5 для обновления настроек. В появившемся окне нажимаем

![](../.gitbook/assets/yes%20%283%29.png)

![](../.gitbook/assets/f7.png)

 Далее выйдет окно об успешном обновлении настроек. Нажимаем

![](../.gitbook/assets/ok-design%20%285%29.png)

![](../.gitbook/assets/f8.png)

 Переходим на открытую вкладку

![](../.gitbook/assets/valyutnye-kursy%20%283%29.png)

 Дважды кликнем левой кнопкой мыши на любой строке поля COD1 \(Код1\).

![](../.gitbook/assets/f9.png)

 В результате происходит переход в открытый документ с Nrdoc=

![](../.gitbook/assets/5645%20%282%29.png)

![](../.gitbook/assets/f10.png)

 Переходим на открытую вкладку

![](../.gitbook/assets/valyutnye-kursy%20%285%29.png)

 Открываем дизайн грида с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%289%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=document
nrdoc=5645
ReturnType=Form
ReturnSection=CURS
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%2811%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%281%29.png)

![](../.gitbook/assets/f11.png)

 В результате двойного клика мыши происходит переход в открытый документ с Nrdoc=

![](../.gitbook/assets/5645.png)

 но после нажатия на

![](../.gitbook/assets/sokhranit%20%285%29.png)

 или

![](../.gitbook/assets/otmena.png)

 или

![](../.gitbook/assets/vx.png)

 \(или горячих клавиш Ctrl+~ или Ctrl+-\)

![](../.gitbook/assets/f12.png)

 происходит возвращение в форму с именем секции

![](../.gitbook/assets/curs.png)

 \(откуда происходил переход в документ\).

![](../.gitbook/assets/f13.png)

 Имя секции можно посмотреть в конфигураторе, нажав кнопку

![](../.gitbook/assets/node-properties%20%283%29.png)

 при выделенной форме. В данном случае имя секции

![](../.gitbook/assets/curs%20%281%29.png)

![](../.gitbook/assets/f14.png)

 Открываем форму

![](../.gitbook/assets/12.1-rabota-s-tsd.png)

 Далее открываем дизайн грида с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%282%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=form.print
TargetSection=0:0:PRINTFORM:SCALESEXP
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%282%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%286%29.png)

![](../.gitbook/assets/f15.png)

 В результате двойного клика мыши на строке в поле STRIH1\_CODPRODUCER \(Штрихкод\) происходит построение печатной формы.

![](../.gitbook/assets/f16.png)

 Имя секции печатной формы можно посмотреть в конфигураторе, нажав кнопку

![](../.gitbook/assets/node-properties%20%284%29.png)

 В данном случае это 

![](../.gitbook/assets/printform.png)

![](../.gitbook/assets/f17.png)

 У данной формы только одна печатная форма, которая и была построена ранее.

![](../.gitbook/assets/f18.png)

 Переходим на открытую вкладку

![](../.gitbook/assets/valyutnye-kursy%20%281%29.png)

 Далее открываем дизайн грида с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%285%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=doc.new
TargetSysFID=1400
TargetJournal=MATERIALE
```

 Сохраняем изменения с помощью 

![](../.gitbook/assets/save-on-exit%20%283%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%2810%29.png)

![](../.gitbook/assets/f19.png)

 В результате двойного клика мыши происходит создание нового документа с SysFID=

![](../.gitbook/assets/1400.png)

![](../.gitbook/assets/f20.png)

 Открываем конфигуратор, выбираем документ, у которого будут дочерние документы. Добавляем свойство

![](../.gitbook/assets/childdocs.png)

 где 10-это DB ID дочернего документа. Так же можно добавить свойство

![](../.gitbook/assets/childcancelonerror.png)

 если в процессе создания дочернего документа возникает ошибка, то вставка в tmdb\_docs отменяется. Сохраняем изменения в текущей транзакции с помощью галочки

![](../.gitbook/assets/commit.png)

![](../.gitbook/assets/ch1.png)

 В программе нажимаем горячую клавишу F5 для обновления настроек. В появившемся окне нажимаем кнопку

![](../.gitbook/assets/yes.png)

![](../.gitbook/assets/confirm.png)

 Далее выйдет окно о успешном обновлении настроек, нажимаем кнопку

![](../.gitbook/assets/ok-design%20%2811%29.png)

![](../.gitbook/assets/uma.md.png)

 Открываем форму

![](../.gitbook/assets/valyutnye-kursy%20%282%29.png)

 Выделяем любую строчку в любой колонке.

![](../.gitbook/assets/ch2.png)

 Далее открываем дизайн грида с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%284%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=doc.child
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit.png)

 и нажимаем

![](../.gitbook/assets/ok-design.png)

![](../.gitbook/assets/ch3.png)

