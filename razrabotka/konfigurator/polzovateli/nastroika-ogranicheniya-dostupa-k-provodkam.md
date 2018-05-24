# Настройка ограничения доступа к проводкам

Для начала нужно проверить, чтобы на схеме не было гранта, который отменяет все POLICY. Он выглядит так:

```sql
GRANT EXEMPT ACCESS POLICY TO <название_схемы>
```

Необходимо отменить этот грант:

```sql
REVOKE EXEMPT ACCESS POLICY FROM <название_схемы>
```

Далее необходимо учесть то, что контексты, в пакете **UN4PUBLIC.SECURE\_CM** создаются в другом пространстве имен, т.е. не в ENVUN4, а в **UN$SECURE**.

Таким образом, нужно смотреть контексты с другим параметром namespace:

**не так:**

```sql
select SYS_CONTEXT ('ENVUN4' , 'PERMITED_CONTS_DT') from dual
```

**а так:**

```sql
select SYS_CONTEXT ('un$secure' , 'PERMITED_CONTS_DT') from dual
select SYS_CONTEXT ('un$secure' , 'PERMITED_CONTS_CT') from dual
```

По умолчанию POLICY на tmdb\_cm созданы без столбцов, т.е. без:

```sql
,sec_relevant_cols     => 'CTSTRSC,CTNRDOC,CTSC1,CTDEP,CTSC'
,sec_relevant_cols_opt => dbms_rls.all_rows
```

Поэтому если оставить их без изменения, то после наложения ограничения **Secure\_Cm.restricted\_conts\('531'\)** нельзя будет увидеть никакие данные по этому счету. Но если пересоздать эти POLICY \(**единоразово**\), то пользователю будут доступны только суммы без разреза по вышеуказанным полям/аналитикам.

**Пересоздание POLICY для скрытия по столбцам:**

```sql
begin
 SECURE_CM.create_policies_CM;
end;
```

**Задание ограничения в конфигураторе в InitSQL или в RunSQL:**

```sql
Secure_Cm.restricted_conts('531');
```

-----

Если прописывать ограничение в InitSQL то необходимо не забыть добавить переменную привязки **:res:=1;** дабы избежать ошибки:

UN4PUBLIC.UN$USERPARAMS line 1324  
ORA-01006: переменной привязки не существует

```sql
begin
 Secure_Cm.restricted_conts('531');
 :res:=1;
end;
```



