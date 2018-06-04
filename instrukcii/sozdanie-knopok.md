# Создание кнопок

 Для установки кнопок используется универсальный документ

![](../.gitbook/assets/dll-id-and-docname.png)

 Для перехода в дизайн Header'a нажимаем на ролик мыши или с зажатым Ctrl нажимаем правой кнопкой мыши и в появившемся списке выбираем

![](../.gitbook/assets/design%20%282%29.png)

![](../.gitbook/assets/dizain.png)

 В дизайне сверху открываем список с помощью

![](../.gitbook/assets/treugolnik.png)

 и выбираем

![](../.gitbook/assets/button.png)

![](../.gitbook/assets/spisok.png)

 Для создания выбранного Control'a нажимаем

![](../.gitbook/assets/list.png)

![](../.gitbook/assets/5.png)

 Вторым способом считается клик правой кнопкой мыши на свободном месте и выбор

![](../.gitbook/assets/button%20%281%29.png)

 из списка:

![](../.gitbook/assets/2-i-sposob.png)

 С помощью зажатой левой клавиши мыши перемещаем control

![](../.gitbook/assets/button1.png)

 в нужное место.

### **Кнопка Cartela**

![](../.gitbook/assets/cartela%20%281%29.png)

 В свойстве

![](../.gitbook/assets/caption%20%282%29.png)

 записываем имя кнопки, в данном случае "Cartela":

![](../.gitbook/assets/spisok-cartela.png)

 Чтобы открыть карточку \(cartela\) при нажатии кнопки и передать в нее параметр \(nrdoc\), необходимо в свойстве

![](../.gitbook/assets/params%20%284%29.png)

 нажать

![](../.gitbook/assets/mnogotochie%20%284%29.png)

 и в открывшемся окне записать:

```sql
TargetType=cartela
TargetSection=ATTR_ORD_ADD
nrdoc=_nrdoc
MainTA=1
```

![](../.gitbook/assets/7%20%281%29.png)

аким образом, мы определяем, что по кнопке открывается карточка, имя секции которой = ATTR\_ORD\_ADD. Передаем в форму параметр nrdoc=\_nrdoc, значение которого берется из запроса для панели, на которой расположена кнопка. После чего нажимаем

![](../.gitbook/assets/galochka%20%282%29.png)

для завершения редактирования.

Сохраняем изменения с помощью галочки

![](../.gitbook/assets/save-on-exit%20%287%29.png)

 и нажимаем

![](../.gitbook/assets/ok%20%2815%29.png)

 При нажатии на кнопку

![](../.gitbook/assets/cartela.png)

 выйдет окно с карточкой:

![](../.gitbook/assets/kartochka.png)

### **Кнопка Form** {#H41A43D43E43F43A430-1}

![](../.gitbook/assets/form.png)

 В свойстве

![](../.gitbook/assets/caption.png)

 записываем имя кнопки, в данном случае "Form".

![](../.gitbook/assets/spisok-form.png)

 Чтобы открыть форму по нажатию кнопки, необходимо в свойстве

![](../.gitbook/assets/params%20%283%29.png)

 кнопки нажать

![](../.gitbook/assets/mnogotochie%20%281%29.png)

 и в открывшемся окне прописать:

```sql
TargetType=form
TargetSection=CURS
```

![](../.gitbook/assets/forma.png)

 Мы указываем, что по нажатию кнопки открывается форма с именем секции = CURS

 После чего нажимаем

![](../.gitbook/assets/galochka%20%284%29.png)

 для завершения редактирования. Сохраняем изменения с помощью галочки

![](../.gitbook/assets/save-on-exit%20%284%29.png)

 и нажимаем

![](../.gitbook/assets/ok%20%2813%29.png)

_Подсказка:_

В конфигураторе при выделенной форме нажав кнопку

![](../.gitbook/assets/node-properties%20%286%29.png)

 в свойстве

![](../.gitbook/assets/section%20%282%29.png)

 можно посмотреть имя секции:

![](../.gitbook/assets/kurs.png)

 При нажатии на кнопку

![](../.gitbook/assets/form%20%281%29.png)

 откроется форма с курсами:

![](../.gitbook/assets/3.png)

### **Кнопка Action** {#H41A43D43E43F43A430-2}

![](../.gitbook/assets/action.png)

 В свойстве

![](../.gitbook/assets/caption%20%285%29.png)

 записываем имя кнопки, в данном случае "Action"

![](../.gitbook/assets/spisok-action.png)

 Чтобы выполнить действие при нажатии кнопки, необходимо в свойстве

![](../.gitbook/assets/params%20%281%29.png)

 кнопки нажать

![](../.gitbook/assets/mnogotochie%20%2810%29.png)

 и в открывшемся окне прописать:

```sql
TargetType=doc.action
action_id=1
```

![](../.gitbook/assets/deistvie.png)

 Мы указываем, что по нажатию кнопки выполняется действие, которое имеет id=1

 После чего нажимаем

![](../.gitbook/assets/galochka%20%281%29.png)

 для завершения редактирования. Сохраняем изменения с помощью галочки

![](../.gitbook/assets/save-on-exit%20%285%29.png)

 и нажимаем

![](../.gitbook/assets/ok%20%281%29.png)

 В данном случае у документа первое и единственное действие это:

![](../.gitbook/assets/generirovanie-bukh.provodok.png)

 Именно это действие будет выполнено после нажатия кнопки

![](../.gitbook/assets/action%20%281%29.png)

 На вкладке

![](../.gitbook/assets/bukh.provodki.png)

 показано выполненное действие:

![](../.gitbook/assets/4%20%282%29.png)

 Документ с проводками после сохранения примет вид:

![](../.gitbook/assets/dokument-s-provodkami.png)

### Кнопка Print {#H41A43D43E43F43A430-3}

![](../.gitbook/assets/print%20%281%29.png)

 В свойстве

![](../.gitbook/assets/caption%20%281%29.png)

 записываем имя кнопки, в данном случае "Print".

![](../.gitbook/assets/spisok-print.png)

 Чтобы открыть печатную форму при нажатии кнопки, необходимо в свойстве

![](../.gitbook/assets/params%20%282%29.png)

 кнопки  нажать

![](../.gitbook/assets/mnogotochie%20%289%29.png)

 и в открывшемся окне прописать:

```sql
TargetType=doc.print
TargetSection=2:0:ABSTRACT PRINT DOCUMENT (D):1:0:0:8
```

![](../.gitbook/assets/pechat.png)

 Мы указываем, что при нажатии кнопки построится печатная форма с именем секции =2:0:ABSTRACT PRINT DOCUMENT \(D\):1:0:0:8

 После чего нажимаем

![](../.gitbook/assets/galochka%20%283%29.png)

 для завершения редактирования. Сохраняем изменения с помощью галочки

![](../.gitbook/assets/save-on-exit%20%288%29.png)

 и нажимаем

![](../.gitbook/assets/ok%20%284%29.png)

 В данном случае построится 

![](../.gitbook/assets/nakladnaya.png)

 имя секции которой можно посмотреть нажав в конфигураторе при выделенной печатной форме

![](../.gitbook/assets/node-properties%20%281%29.png)

 и в открывшемся окне напротив

![](../.gitbook/assets/section%20%281%29.png)

![](../.gitbook/assets/okno-2.png)

 При нажатии на кнопку

![](../.gitbook/assets/print.png)

  построится печатная форма:

![](../.gitbook/assets/pechatnaya-forma.png)

### Кнопка Report {#H41A43D43E43F43A430-4}

![](../.gitbook/assets/report%20%281%29.png)

 В свойстве

![](../.gitbook/assets/caption%20%284%29.png)

 записываем имя кнопки, в данном случае "Report".

![](../.gitbook/assets/spisok-report.png)

 Чтобы открыть отчёт при нажатии кнопки, необходимо в свойстве

![](../.gitbook/assets/params.png)

 кнопки нажать

![](../.gitbook/assets/mnogotochie%20%283%29.png)

 и в открывшемся окне прописать:

```sql
TargetType=report
TargetSection=1:0:RG113
```

![](../.gitbook/assets/report-params.png)

Мы указываем, что при нажатии кнопки построится отчёт с именем секции

=`1:0:RG113`

 После чего нажимаем

![](../.gitbook/assets/galochka.png)

 для завершения редактирования. Сохраняем изменения с помощью галочки 

![](../.gitbook/assets/save-on-exit%20%289%29.png)

 и нажимаем

![](../.gitbook/assets/ok.png)

 Имя секции отчёта можно посмотреть нажав в конфигураторе при выделенной печатной форме

![](../.gitbook/assets/node-properties%20%283%29.png)

 и в открывшемся окне напротив

![](../.gitbook/assets/section.png)

![](../.gitbook/assets/universalnyi-otchyot.png)

 При нажатии на кнопку

![](../.gitbook/assets/report.png)

 построится отчёт:

![](../.gitbook/assets/otchet.png)

 Вид кнопок в шапке \(Header\) документа:

![](../.gitbook/assets/header-2.png)

 Подсказка:

В дизайне Header'a в свойстве

![](../.gitbook/assets/caption%20%283%29.png)

 можно задать любое имя для кнопки. Имена Action, Cartela, Form, Print и Report  выбраны в качестве примера.

