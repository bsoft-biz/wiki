# Цвет отдельных ячеек

в шаблон:

params usecellcolor    on

\(есть еще свойство:

params userowcolor off\)

и для нужной ячейки помимо, например, поля cant, вывести и bgcolor\_cant

```sql
:SQLMaster:='select ... cant1, 16777215 bgcolor_cant1
from ...'
```

