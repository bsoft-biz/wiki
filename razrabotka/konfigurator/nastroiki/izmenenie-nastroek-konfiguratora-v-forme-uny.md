# Изменение настроек конфигуратора в форме Уны

Есть вьюха `vms_settings`, которую можно использовать для редактирования настроек в виде грида!

Редактировать можно только поле "Значение\(value\)".

Пример формы для редактирования настроек ЗП есть на `box`:

Формы - Администрирование - Настройки по зарплате.

В гриде настроен только апдейт для поля "Значение".Пример запроса для отображения в виде грида настроек по зарплате:

```sql
select * 
from vms_settings
where (lower(section) = 'slr')
order by gr, name
```

