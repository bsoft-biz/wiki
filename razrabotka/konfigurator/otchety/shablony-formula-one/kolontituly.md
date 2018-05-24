# Колонтитулы

Настройка колонтитулов отчетов и печатных форм в FormulaOne

Колонтитулы могут быть заданы для конкретного отчета или печатной формы,

и могут быть заданы для всей схемы \(в секции настроек \[General\]\).

Свойство на уровне секции отчета/печатной формы имеет приоритет,

пустое свойство на этом уровне выключает глобальную настройку.

Свойство "F1PageHeader" задает текст верхнего колонтитула,

свойство "F1PageFooter" задает текст нижнего колонтитула.

Колонтитулы могу содержать текст и специальные коды формата.

Эти коды позволяют задать горизонтальное выравнивание текста

\(по левому краю, по правому краю или по центру строки\),

а также вставить какую-то специальную информацию - см. список.

Коды выравнивания \(&L, &C, и &R\) должны указываться до кодов шрифта

\(таких, как &B для жирного шрифта и &I для курсива\). Коды для вставки

информации рабочего листа \(например, номер страницы\) указываются в конце.

Если коды формата указываются в неправильном порядке, часть из них могут

быть проигнорированы. Коды формата отделяются друг от друга пробелами.

По умолчанию колонтитулы выравниваются по центру строки - если не указаны

коды &L или &R.

Код формата Описание

&L          Left-aligns the characters that follow.

&C          Centers the characters that follow.

&R          Right-aligns the characters that follow.

&B          Use a bold font.

&I          Use an italic font.

&U          Underline the header.

&S          Strikeout the header.

&O          Ignored.

&H          Ignored.

&"fontname" Use the specified font.

&nn         Use the specified font size \(must be a two digit number\).

&D          Prints the current date.

&T          Prints the current time.

&F          Prints the workbook name.

&A          Prints the worksheet name.

&P          Prints the page number.

&P+number  Prints the page number plus number.

&P-number  Prints the page number minus number.

&&          Prints an ampersand.

&N          Prints the total number of pages in the document.

Universal Accounting Format Codes

&X          User name

&Y          Global filter text

Пример колонтитула:  
Лист &P из &N

