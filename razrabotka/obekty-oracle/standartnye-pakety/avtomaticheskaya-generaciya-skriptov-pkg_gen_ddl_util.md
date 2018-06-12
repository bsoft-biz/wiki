# Автоматическая генерация скриптов pkg\_gen\_ddl\_util

Пакет для генерации скриптов DDl - `pkg_gen_ddl_util` есть на схеме `box` и в `svn`

В пакете есть функция для генерации скрипта простого триггера\(с использованием переменной типа %rowtype\) на вьюху.

Пример использования функции из пакета:

```sql
begin
say(pkg_gen_ddl_util.get_view_trigger('YPMR_VSLRPRM_MROT','YPMR_tSLRPRM_MROT'));
end;
```



