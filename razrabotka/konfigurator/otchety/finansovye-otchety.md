# Финансовые отчеты

**1\) На форме “Финансовые отчеты” в верхнем гриде добавляем название нашего шаблона \(инструкции\), его псевдоним и указываем полный путь к шаблоны отчета.**

2\) Во втором гриде формируем список полей для отчета: сначала указывается

SID - имя поля

COLNO - не обязательное поле \( номер поля\)   \(?\)

CALCTYPE :

BE - остаток на конец

BS - остаток на начало

RDT - обороты по дебиту

RCT - обороты по кредиту

T - вычисляемое поле

ACC - откуда брать данные для расчета \(можно указать счет, список счетов, сами поля\)

ACC1 - субсчет

SC -аналитика

DEP - центр затрат

SC1 - субконто

2\) в конфигураторе необходимо установить свойства:

SQLAllInOne -PKG\_FIN\_RP.forma2\_2\(:datastart,:sqlmaster,:sqlheader\);

RpID - название шаблона из формы фин. от.

Report ID - 23   \(?\)

