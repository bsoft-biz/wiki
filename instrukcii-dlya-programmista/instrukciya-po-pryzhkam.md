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

![](../.gitbook/assets/bloknot%20%2812%29.png)

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

![](../.gitbook/assets/bloknot%20%288%29.png)

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

![](../.gitbook/assets/bloknot%20%289%29.png)

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

![](../.gitbook/assets/bloknot%20%287%29.png)

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

![](../.gitbook/assets/node-properties%20%282%29.png)

 Имя секции для данного отчёта

![](../.gitbook/assets/rg113%20%281%29.png)

![](../.gitbook/assets/d18.png)

###  **Прыжки из форм.**

 Открываем любую форму, например

![](../.gitbook/assets/valyutnye-kursy%20%285%29.png)

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

![](../.gitbook/assets/commit%20%285%29.png)

![](../.gitbook/assets/f6.png)

 В программе нажимаем горячую клавишу F5 для обновления настроек. В появившемся окне нажимаем

![](../.gitbook/assets/yes%20%288%29.png)

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

![](../.gitbook/assets/valyutnye-kursy%20%286%29.png)

 Открываем дизайн грида с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%2811%29.png)

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

![](../.gitbook/assets/node-properties%20%284%29.png)

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

![](../.gitbook/assets/node-properties%20%285%29.png)

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

![](../.gitbook/assets/1400%20%281%29.png)

![](../.gitbook/assets/f20.png)

 Открываем конфигуратор, выбираем документ, у которого будут дочерние документы. Добавляем свойство

![](../.gitbook/assets/childdocs.png)

 где 10-это DB ID дочернего документа. Так же можно добавить свойство

![](../.gitbook/assets/childcancelonerror%20%281%29.png)

 если в процессе создания дочернего документа возникает ошибка, то вставка в tmdb\_docs отменяется. Сохраняем изменения в текущей транзакции с помощью галочки

![](../.gitbook/assets/commit%20%283%29.png)

![](../.gitbook/assets/ch1.png)

 В программе нажимаем горячую клавишу F5 для обновления настроек. В появившемся окне нажимаем кнопку

![](../.gitbook/assets/yes%20%285%29.png)

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

 Дважды кликнув на любой строке поля COD1 \(Код1\), выйдет окно о создании документа на основании. Нажимаем кнопку

![](../.gitbook/assets/yes%20%282%29.png)

![](../.gitbook/assets/ch4.png)

 В следующем окне выбираем дату документа, после чего нажимаем кнопку

![](../.gitbook/assets/ok-child-docs.png)

![](../.gitbook/assets/ch5.png)

 Переходим на вкладку

![](../.gitbook/assets/zhurnal-operacii%20%283%29.png)

  где находится уже созданный дочерний документ.

![](../.gitbook/assets/ch6.png)

 Можно добавить свойство

![](../.gitbook/assets/createchildsilent%20%283%29.png)

 в результате при создании дочернего документа не будет вопроса о создании документа на основании. Сохраняем изменения в текущей транзакции с помощью галочки

![](../.gitbook/assets/commit%20%2811%29.png)

![](../.gitbook/assets/ch7.png)

 После обновления настроек, дважды кликнув на любой строке поля COD1 \(Код1\) выйдет сразу окно с настройкой даты документа \(окно о создании документа на основании игнорируется с помощью свойства

![](../.gitbook/assets/createchildsilent%20%282%29.png)

 Нажимаем кнопку

![](../.gitbook/assets/ok-child-docs%20%281%29.png)

![](../.gitbook/assets/ch8.png)

 Переходим на вкладку

![](../.gitbook/assets/zhurnal-operacii%20%282%29.png)

 где находится уже созданный дочерний документ.

![](../.gitbook/assets/ch9.png)

###  **Прыжки из отчётов.**

 В конфигураторе открываем любой журнал и добавляем свойство 

![](../.gitbook/assets/showreportsection%20%281%29.png)

 Сохраняем изменения в текущей транзакции с помощью галочки

![](../.gitbook/assets/commit%20%284%29.png)

 В программе обновляем настройки с помощью горячей клавиши F5.

![](../.gitbook/assets/r1.png)

 При открытии журнала, в котором добавлено свойство

![](../.gitbook/assets/showreportsection.png)

![](../.gitbook/assets/r2.png)

 строится отчёт.

![](../.gitbook/assets/r3.png)

 Имя секции отчетов можно посмотреть нажав

![](../.gitbook/assets/node-properties.png)

 при выделенном отчёте. В данном случае имя секции отчёта

![](../.gitbook/assets/rg113.png)

![](../.gitbook/assets/r4.png)

 Открываем шаблон отчёта и добавляем в колонку A слово "title", в колонке F записываем:

```sql
[RepJump]
TargetType=form
TargetSection=CURS
```

 Сохраняем изменения с помощью кнопки

![](../.gitbook/assets/save%20%283%29.png)

![](../.gitbook/assets/r5.png)

 Нажимаем кнопку

![](../.gitbook/assets/postroit.png)

 для построения отчёта.

![](../.gitbook/assets/r6.png)

 В шаблоне отчёта в первых трёх колонках \(A, B и C\) задаются параметры. В построенном отчёте будут видны колонки начиная с D \(D, E, F, G, H, I и т.д.\)

![](../.gitbook/assets/r7.png)

 То есть в построенном отчёте колонка A=D, B=E, C=F, D=G, E=H и т.д. При двойном клике мыши по полю С

![](../.gitbook/assets/r8.png)

 произойдёт переход в форму.

![](../.gitbook/assets/r9.png)

 Выделяем ячейку с написанным ранее текстом и нажимаем правой кнопкой мыши, в появившемся списке выбираем

![](../.gitbook/assets/format-cells.png)

![](../.gitbook/assets/r10.png)

 В открывшемся окне переходим на вкладку

![](../.gitbook/assets/patterns.png)

 выбираем например

![](../.gitbook/assets/krasnyi.png)

 в поле 

![](../.gitbook/assets/fil-color.png)

 и

![](../.gitbook/assets/krasnyi2.png)

 в поле

![](../.gitbook/assets/fil-pattern.png)

 Образец выбранного цвета можно посмотреть ниже поля

![](../.gitbook/assets/sample.png)

 Далее нажимаем кнопку 

![](../.gitbook/assets/ok%20%287%29.png)

![](../.gitbook/assets/r11.png)

 В результате выбранная ячейка стала красной, сохраняем изменения с помощью кнопки

![](../.gitbook/assets/save%20%285%29.png)

![](../.gitbook/assets/r12.png)

 Отчёт можно построить заново, либо в открытом отчёте нажать кнопку

![](../.gitbook/assets/obnovlenie%20%284%29.png)

 для обновления отчёта. В результате ячейка колонки С \(в шаблоне F\) стала красной. При двойном клике мыши по-прежнему произойдёт переход в форму

![](../.gitbook/assets/valyutnye-kursy%20%284%29.png)

![](../.gitbook/assets/r13.png)

 Открываем шаблон отчёта и \(в колонке A остаётся слово "title"\) в колонке F записываем:

```sql
[RepJump]
TargetType=document
nrdoc=5648
```

 Сохраняем изменения с помощью кнопки

![](../.gitbook/assets/save.png)

![](../.gitbook/assets/r14.png)

 Отчёт можно построить заново, либо в открытом отчёте нажать кнопку

![](../.gitbook/assets/obnovlenie.png)

 для обновления отчёта. Дважды кликнем левой кнопкой мыши на ячейке в колонке C \(в шаблоне F\).

![](../.gitbook/assets/r15.png)

 В результате происходит переход в открытый документ с Nrdoc=

![](../.gitbook/assets/5648.png)

 Документ открыт для редактирования с помощью свойства

![](../.gitbook/assets/gotodocumentediting%20%281%29.png)

 которое находится в конфигураторе у данного пользователя \(если установить значение свойства в false, документ открыт на редактирование не будет, но переход на него по DblClick будет произведён\).

![](../.gitbook/assets/r16.png)

 Открываем шаблон отчёта и \(в колонке A остаётся слово "title"\) в колонке F записываем:

```sql
[RepJump]
TargetType=report
TargetSection=100:0:RPT:SLR_RG12
```

 Сохраняем изменения с помощью кнопки

![](../.gitbook/assets/save%20%286%29.png)

![](../.gitbook/assets/r17.png)

 Отчёт можно построить заново, либо в открытом отчёте нажать кнопку

![](../.gitbook/assets/obnovlenie%20%282%29.png)

 для обновления отчёта. В результате двойного клика левой кнопкой мыши

![](../.gitbook/assets/r18.png)

 произойдёт построение другого отчёта.

![](../.gitbook/assets/r19.png)

 Открываем шаблон отчёта и \(в колонке A остаётся слово "title"\) в колонке F записываем:

```sql
[RepJump]
TargetType=doc.new
TargetSysFID=1400
TargetJournal=MATERIALE
```

 Сохраняем изменения с помощью кнопки 

![](../.gitbook/assets/save%20%284%29.png)

![](../.gitbook/assets/r20.png)

 Отчёт можно построить заново, либо в открытом отчёте нажать кнопку

![](../.gitbook/assets/obnovlenie%20%283%29.png)

 для обновления отчёта. В результате двойного клика левой кнопкой мыши

![](../.gitbook/assets/r21.png)

 произойдёт создание нового документа с SysFID=

![](../.gitbook/assets/1400.png)

![](../.gitbook/assets/r22.png)

 Имя секции журнала можно посмотреть в конфигураторе с помощью кнопки

![](../.gitbook/assets/node-properties%20%287%29.png)

 выделив нужный журнал. В данном случае имя секции журнала 

![](../.gitbook/assets/materiale.png)

![](../.gitbook/assets/r23.png)

 Открываем конфигуратор, выбираем документ, у которого будут дочерние документы. Добавляем свойство

![](../.gitbook/assets/childdocs%20%281%29.png)

 где 10-это DB ID дочернего документа. Так же можно добавить свойство

![](../.gitbook/assets/childcancelonerror.png)

 если в процессе создания дочернего документа возникает ошибка, то вставка в tmdb\_docs отменяется. Сохраняем изменения в текущей транзакции с помощью галочки

![](../.gitbook/assets/commit%20%281%29.png)

![](../.gitbook/assets/ch1%20%281%29.png)

 В программе нажимаем горячую клавишу F5 для обновления настроек. В появившемся окне нажимаем кнопку

![](../.gitbook/assets/yes%20%283%29.png)

![](../.gitbook/assets/confirm%20%282%29.png)

 Далее выйдет окно о успешном обновлении настроек, нажимаем кнопку

![](../.gitbook/assets/ok%20%285%29.png)

![](../.gitbook/assets/uma.md%20%283%29.png)

 Открываем шаблон отчёта и \(в колонке A остаётся слово "title"\) в колонке F записываем:

```sql
[RepJump]
TargetType=doc.child
```

 Сохраняем изменения с помощью кнопки

![](../.gitbook/assets/save%20%281%29.png)

![](../.gitbook/assets/r24.png)

 Отчёт можно построить заново, либо в открытом отчёте нажать кнопку

![](../.gitbook/assets/obnovlenie%20%281%29.png)

 для обновления отчёта. В результате двойного клика левой кнопкой мыши выйдет окно о создании документа на основании. Нажимаем кнопку

![](../.gitbook/assets/yes%20%281%29.png)

![](../.gitbook/assets/r25.png)

 В следующем окне настраиваем дату документа, после чего нажимаем кнопку

![](../.gitbook/assets/ok-child-docs%20%282%29.png)

![](../.gitbook/assets/r26.png)

 Переходим на вкладку

![](../.gitbook/assets/zhurnal-operacii%20%281%29.png)

 где находится только что созданный дочерний документ.

![](../.gitbook/assets/r27%20%281%29.png)

 Можно добавить свойство

![](../.gitbook/assets/createchildsilent.png)

 в результате при создании дочернего документа не будет вопроса о создании документа на основании. Сохраняем изменения в текущей транзакции с помощью галочки

![](../.gitbook/assets/commit%20%289%29.png)

![](../.gitbook/assets/ch7%20%281%29.png)

 После обновления настроек, отчёт можно построить заново, либо в открытом отчёте нажать кнопку

![](../.gitbook/assets/obnovlenie%20%285%29.png)

 для обновления отчёта. В результате двойного клика левой кнопкой мыши выйдет сразу окно с настройкой даты документа \(окно о создании документа на основании игнорируется с помощью свойства

![](../.gitbook/assets/createchildsilent%20%281%29.png)

 Нажимаем кнопку

![](../.gitbook/assets/ok-child-docs%20%283%29.png)

![](../.gitbook/assets/r26%20%281%29.png)

 Переходим на вкладку

![](../.gitbook/assets/zhurnal-operacii.png)

 где находится только что созданный дочерний документ.

![](../.gitbook/assets/r27.png)

###  **Примечание**

 Если в шапку \(Header\) документа добавить кнопку \(Button1\) и в свойстве Params написать:

 `TargetType=doc.child`

![](../.gitbook/assets/pr1.png)

 То при нажатии на неё выйдет окно о завершении операции редактирования документа. Это происходит по причине того, что документ находится в открытой незавершённой транзакции, которую необходимо завершить с сохранением \(Commit\), либо с отменой \(Rollback\). Таким образом создание дочернего документа является невозможным.

![](../.gitbook/assets/pr2.png)

 Если добавить в дизайн колонки CANT в

![](../.gitbook/assets/bloknot%20%2810%29.png)

```sql
DblClick=goto
TargetType=doc.child
```

![](../.gitbook/assets/pr3.png)

 При двойном клике в документе по строке поля Количество \(CANT\), выйдет то же сообщение о завершении редактирования документа.

![](../.gitbook/assets/pr4.png)

 Если в шапку \(Header\) документа добавить кнопку \(Button1\) и в свойстве Params написать:

```sql
TargetType=doc.new
TargetSysFID=1400
TargetJournal=MATERIALE
```

![](../.gitbook/assets/pr5.png)

 При создании нового документа с кнопки Новый документ происходит то же самое, что и при создании документа на основании. То есть создание нового документа с кнопки становится невозможным.

![](../.gitbook/assets/pr6.png)

 Если добавить в дизайн колонки CANT в

![](../.gitbook/assets/bloknot%20%286%29.png)

```sql
DblClick=goto
TargetType=doc.new
TargetSysFID=1400
TargetJournal=MATERIALE
```

![](../.gitbook/assets/pr7.png)

 При двойном клике в документе по строке поля Количество \(CANT\), выйдет то же сообщение о завершении редактирования документа.

![](../.gitbook/assets/pr8.png)

 Таким образом создать новый или дочерний документы по DblClick или кнопки \(Button\) из открытого документа нельзя.

