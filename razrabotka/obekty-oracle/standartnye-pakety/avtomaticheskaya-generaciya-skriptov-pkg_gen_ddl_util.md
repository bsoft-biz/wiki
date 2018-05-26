# Автоматическая генерация скриптов pkg\_gen\_ddl\_util

Пакет для генерации скриптов DDl - pkg\_gen\_ddl\_util есть на схеме box и в [svn](https://bsoft.biz/svn/una/utils/pkg_gen_ddl_util.pkb)

В пакете есть функция для генерации скрипта простого триггера\(с использованием переменной типа %rowtype\) на вьюху.

Пример использования функции из пакета:

```sql
begin
say(pkg_gen_ddl_util.get_view_trigger('YPMR_VSLRPRM_MROT','YPMR_tSLRPRM_MROT'));
end;
```



