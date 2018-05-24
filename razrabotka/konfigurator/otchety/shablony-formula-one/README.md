# Шаблоны Formula One

[  
Page Break](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/Page+Break) \(переход на новую страницу\)

[F1PageHeader и Footer](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/F1PageHeader+%D0%B8+Footer)

[Колонтитулы](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9A%D0%BE%D0%BB%D0%BE%D0%BD%D1%82%D0%B8%D1%82%D1%83%D0%BB%D1%8B)

[Опции в шаблонах Formula One](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%9E%D0%BF%D1%86%D0%B8%D0%B8+%D0%B2+%D1%88%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD%D0%B0%D1%85+Formula+One)

[Формат ячеек Formula One](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A4%D0%BE%D1%80%D0%BC%D0%B0%D1%82+%D1%8F%D1%87%D0%B5%D0%B5%D0%BA+Formula+One)

[Цвет отдельных ячеек](http://wiki.bsoft.biz/xwiki/bin/view/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%A6%D0%B2%D0%B5%D1%82+%D0%BE%D1%82%D0%B4%D0%B5%D0%BB%D1%8C%D0%BD%D1%8B%D1%85+%D1%8F%D1%87%D0%B5%D0%B5%D0%BA)

Параметры/управляющие конструкции находятся в первых трех столбцах. Примеры:

params setrowheightauto off

params supressblanklines off

params usecellcolor on

params userowcolor off

title

detail1

groupF \_clcpos\_codt

summary

params JoinFields

Полезности:

Конкатенация строк: =\_codU&" - "&\_Denumirea

ReturnRefresh=1  =&gt; если в печатной форме настроен прыжок из нее в какой-то, например, документ, а после выхода из документа нам надо снова венуться в уже прорефрешенную печатную форму, из которой все и начиналось, то в шаблоне печатной формы, наряду с настройками прыжка \(см."help по прыжкам.doc"\), нужно добавить это свойство.

если в 3й колонке для groupH пишется pagebreak nogeader, тогда эта строка будет всегда начинаться с нового листа/страницы

Если в каких-то строках есть title page, то на каждой новой странице эти строки будут печататься

если получается вставить картинку, то надо при сохранении выбрать другой тип formula one \(поэкспериментировать\)

usewhen\(part=4\) usewhen\(tip=1\)   если сочетание условий, может фтв тоже работает

  title        general

 summary

 grouph

  groupf

detail1

detail2        names

titlespec1

tip

PIVOT

\_

//  Не найдено ни '\_', ни '\[', ни ссылки на ячейку

params      

nocopyformat OFF

SETROWHEIGHTAUTO\) ON

SETCOLWIDTHAUTO\)

SUPRESSBLANKLINES\)

NOCOPYROWFORMAT\)

PRESERVESYSCOLS\)

USEROWCOLOR\)

USEROWCOLOR\)

SMARTDATE\)

JOINVALUES\) Объединение повторяющейся аналитики

JOINENFORCED\) Принудительное объединение

JOINFIELDS\) Список полей аналитики

SHOWZEROVALUES\) Отображение значений "0"

usewhen

usewith

//  AParams содержит имя поля и \(необязательно\) его значение, отделенное

//  разделителем, обозначающим тип условия: равенство или неравенство.

//  Разделители ',' '=' и '==' обозначают условие на равенство,

//  разделители '!' '!=' и '&lt;&gt;' обозначают условие на неравенство.

//  Если ни один из перечисленных разделителей не найден в строке AParams,

//  вся строка считается именем поля, а условие - условием на равенство 1.

//  В любом случае поле и его значение считаются ЦЕЛОЧИСЛЕННЫМИ \(ftInteger\)

//---------------------------------------------------------------------------

"//  Функция находит в оставшейся части строки выражения типа ссылки на ячейку

//  Поддерживается относительная и абсолютная адресация \(A1, B$2, $C4, $D$6\)

//  Поддерживаются интервалы типа C2:E8 \(как две разные ссылки\)

//  ""Бесконечные"" интервалы \(типа C:E, 3:5\) ПОКА не поддерживаются

//  nPos1 и nPos2 - позиции найденных слов \(после них нет смысла искать\)

//---------------------------------------------------------------------------

static int \_\_fastcall FindRef\(AnsiString& AText, int APos, int APos1, int APos2\)

"

