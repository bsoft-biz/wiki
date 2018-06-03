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

![](../.gitbook/assets/save-on-exit%20%287%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%282%29.png)

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

![](../.gitbook/assets/bloknot%20%286%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=doc.action
Action_ID=4
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%288%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%281%29.png)

![](../.gitbook/assets/d9.png)

 После двойного клика мыши на любой строке поля CANT3 \(возвращено\) выполнится действие с ID=4.

![](../.gitbook/assets/d10.png)

 В данном случае это

![](../.gitbook/assets/zapolnit-na-osnovanii-spisaniya-gp.png)

![](../.gitbook/assets/d11.png)

 Открываем дизайн первого грида

![](../.gitbook/assets/gr21a-2-1.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%284%29.png)

```sql
DblClick=goto
TargetType=form
TargetSection=CURS
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%2810%29.png)

 и нажимаем 

![](../.gitbook/assets/ok-design%20%285%29.png)

![](../.gitbook/assets/d12.png)

 В результате двойного клика мыши по полю CANT3 \(Возвращено\), откроется форма

![](../.gitbook/assets/valyutnye-kursy.png)

![](../.gitbook/assets/d13.png)

 Открываем дизайн первого грида

![](../.gitbook/assets/gr21a-2.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%285%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=cartela
TargetSection=ATTR_ORD_ADD
nrdoc=_nrdoc
MainTA=1
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%289%29.png)

 и нажимаем 

![](../.gitbook/assets/ok-design%20%283%29.png)

![](../.gitbook/assets/d14.png)

 В результате двойного клика мыши по полю CANT3 \(Возвращено\), открывается карточка.

![](../.gitbook/assets/d15.png)

 Открываем дизайн первого грида

![](../.gitbook/assets/gr21a-2%20%281%29.png)

 с помощью горячих клавиш Alt+D, нажимаем

![](../.gitbook/assets/bloknot%20%283%29.png)

 и записываем:

```sql
DblClick=goto
TargetType=report
TargetSection=1:0:RG113
```

 Сохраняем изменения с помощью

![](../.gitbook/assets/save-on-exit%20%283%29.png)

 и нажимаем

![](../.gitbook/assets/ok-design%20%284%29.png)

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

![](../.gitbook/assets/valyutnye-kursy%20%281%29.png)

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

![](../.gitbook/assets/save-on-exit.png)

 и нажимаем

![](../.gitbook/assets/ok-design.png)

![](../.gitbook/assets/f4.png)



