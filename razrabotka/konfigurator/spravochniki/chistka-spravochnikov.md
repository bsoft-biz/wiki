# Чистка справочников

### Чистка Tms\_Univers.

```sql
delete vslrprm_calcd
delete tms_munc
alter trigger TMS_UNIVERS_DONT_DELETE disable; 
alter trigger TRG_CHK_SECUR_TMS_ORG_ACCOUNTS disable;
alter trigger TRG_CHK_SECUR_TMS_MPT disable;
select * from Tms_univers
where tip in ('O','F','M','P') and gr1 not in ('Cont','BANK','BNK'); 
delete
from Tms_univers
where tip in ('O','F','M','P') and gr1 not in ('Cont','BANK','BNK');
select * from Tms_univers
where tip = 'T' and gr1 in ('AV','LGOT','M','TIP','121','1234', 
'5331','612','621','7223','SUP','912','COST');
delete
from Tms_univers
where tip = 'T' and gr1 in ('AV','LGOT','M','TIP','121','1234',
'5331','612','621','7223','SUP','912','COST');
alter trigger TMS_UNIVERS_DONT_DELETE enable;
alter trigger TRG_CHK_SECUR_TMS_ORG_ACCOUNTS enable;
alter trigger TRG_CHK_SECUR_TMS_MPT enable;
```

###  Чистка tms\_univers\_uniqk.

```sql
select count (*) from tms_univers_uniqk
where cod not in(select cod from tms_univers)
select * from vms_univers where cod=4211
select * from tms_univers_uniqk
where cod not in(select cod from tms_univers)
delete from  tms_univers_uniqk
where cod not in(select cod from tms_univers)
```



