# Логирование работы процедур и функций

  
Логирование работы процедур и функций \(`un$process_log.log`\)

Пример логирования работы процедуры `gds_gr_incl_exp();`

```sql
procedure process_export 
is
v_mutex varchar2(128);
v_res int;
v_nrdoc number(10); 
begin
-- Проверка, не запущена ли уже процедура в другой сессии
v_mutex := pkg_docs_util.create_mutex(cv_process_name);
dbms_application_info.set_module('pkg_sales','process_export');
un$process_log.log(cv_process_id,'Processing started','I');
--  
--un$userparams.loadglobalworkperiod;
/*    if not v_registered then

      envun4.envsetvalue('PARAM_NRSETLEVELACCESS','1');

      pkg_auto_docs.register_user;

      pkg_auto_docs.init_policy_filter;

      v_registered := true;

     un$process_log.log(cv_process_id,'Register user');    end if;*/
```

```sql
begin
un$process_log.log(cv_process_id,
'Экспорт справочника входимостей товаров в группы начат');
gds_gr_incl_exp();
un$process_log.log(cv_process_id,
'Экспорт справочника входимостей товаров в группы окончен');
exception when others then
un$process_log.log_exception(cv_process_id);
end;   
```

```sql
v_res := dbms_lock.release(v_mutex);
un$process_log.log(cv_process_id,'Processing finished','I');  
exception when others then
if v_mutex is not null then
v_res := dbms_lock.release(v_mutex);
end if;
un$process_log.log_exception(cv_process_id);
end;
```



