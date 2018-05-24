# Цвет отдельных ячеек

в шаблон:

params usecellcolor    on

\(есть еще свойство:

params userowcolor off\)

и для нужной ячейки помимо, например, поля cant, вывести и bgcolor\_cant

:SQLMaster:='select ... cant1, 16777215 bgcolor\_cant1

from ...'

