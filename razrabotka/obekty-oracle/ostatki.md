# Остатки

```sql
BEGIN 
SYS.DBMS_JOB.REMOVE(4);
COMMIT;
END;
/
```

```sql
DECLARE
X NUMBER;
BEGIN
SYS.DBMS_JOB.SUBMIT
( job       => X 
,what      => 'pkg_sld_util.rebuild_sld_actual(p_raise => false);'
,next_date => to_date('14.02.2011 03:00:00','dd/mm/yyyy hh24:mi:ss')
,interval  => 'trunc(sysdate) + 1 + 3/24'
,no_parse  => FALSE
);
SYS.DBMS_OUTPUT.PUT_LINE('Job Number is: ' || to_char);
COMMIT;
END;
/
```

lifo

`un$lifo_strsc.autorun;`

```sql
v_date date := pkg_docs_util.doc_date(p_nrdoc);
```

DatePrefix

не только префикс даты, но и для SC и Dep

Для того чтобы, makesld игнорировало зарегистр сальдо на день запроса, можно воспользоваться след конструкций:

```sql
if trunc(un$sld.get_datastart(pDatastart)) = pDatastart and pCB1=0 then
v_register := true;
end if;
un$sld.make(pDatastart-nvl(pCB1,0),pFilt=>'AC1',
pCont=>NVL(pParameter1,'2171'),pDep=>pFilt1,
pRegister=>v_register,pOldMethod=>v_register);
```

если дата совпадает с датой регистрирования сальдо, то pRegister=&gt;true \(документ регистрации сальдо не попадает\),pOldMethod=&gt;true \(актуальное сальдо не используется, т.е. считаем с начала \(или предидущей даты регистрации\)\)

--------------------------------------------

Актуальное сальдо:

\* Каждый день джоб считает остатки в самой подробной аналитике и инсертит и в tsld или txld \(предварительно ее почистив\)

\* На cm есть тригер, который инсертит  в `tsld` или `txld` каждую проводку по dt с+ по ct с -

\* `un$sld_make` при расчете сальдо смотрит в `tsld` или `txld` и определяет используется ли актуальное сальдо

\* если используется актуально сальдо, то в txsld находится сальдо на "дату актуальности" \(дату последней проводки - как бы 31.12.3000\)- "актуальное сальдо"

\* при расчете остатка на произвольную дату - dsold мы от актуального  сальдо вычитаем обороты за период между этой датой и "датой актуальности"

```sql
select suma from tsld или txsld
unioun all
select -suma from CM
where data between dsold and 31.12.3000
```

Зарегистрированные остатки - при вводе остатков в документы

\* эти документы идут датой дату+23/24

\* проводки помечабтся и их нет в vmdb\_cmr \(но при расчете остатков они попадают из tmdb\_cm\) и тригер не срабатывает что нет кор счета

\* вводится строка в tmdb\_dsld с датой = дате документа

\* при расчете остатков если дата &lt; даты регистрации остатков актуальное сальдо не используется

\* при расчете остатков проводки берутся начиная с даты последней регистрации остатков \(`un$sld.get_datastart`\) = `max(tmdb_dsld.dataend)`, кот меньше dsold + 23/24 - таким образом документов регистрации остатков может быть несколько

остатки на время

\* при расчете остатков на определенное время use\_time документы на дату конца/начала \(в зависимости от того используется ли актуальное сальдо\) периода фильтруются по времени, указанном в `tmdb_docs_add.doc_time`

```sql
/*
SQL Execute: BEGIN
UN$G_RG1P12.ClearAll;
UN$G_RG1P12.SetFlags(:AFlags,:BFlags,:CFlags);
UN$G_RG1P12.SetCond(:DateB,:DateE,:Cont,:Cont1,:Sc,:Sc1,:Dep,
:xCont,:xCont1,:xSc,:xSc1,:xDep,:NrDoc,:NrCm,:Data,:StrSc,
:xNrDoc,:xNrCm,:xData,:xStrSc,:SysFId,:UserId,:Valuta,:Docs);
END;
dFinal:=TO_DATE('31.12.3000','dd.mm.yyyy');
if bUseFinal and not pUseTime
cFiltCM:='DATA BETWEEN '||DateToStr(dBegin)||' AND '||DateToStr(dFinal)||LF;
dSold DATE:=NVL(pData,SYSDATE);
dBegin:=TRUNC(dSold)+1;
dFinal:=TO_DATE('31.12.3000','dd.mm.yyyy');
',(SELECT CASE WHEN AP IN (''A'',''P'') THEN AP ELSE ''N'' END FROM TMS_PDC'||
' WHERE CONT=A.DT AND CONT1=0 AND ROWNUM=1)AP'||LF end||
'FROM('||LF||
' SELECT CONT DT,CONT1 DT1,SC DTSC,DEP DTDEP,SC1 DTSC1'||
',NRDOC DTNRDOC,STRSC DTSTRSC,NRCM DTNRCM,DIV DTDIV,DATA DTDATA'||
',VALUTA VALUTADT,SUMA,CANT,SUMAVAL SUMAVALDT,SUMAGAAP,CANT1 DTCANT1'||LF||
' FROM TXSLD'||LF||
')A WHERE 1=1'||LF||cFilter||
'UNION ALL'||LF||
'SELECT DT,DT1,DTSC,DTDEP,DTSC1,DTNRDOC,DTSTRSC,DTNRCM,DTDIV,DTDATA'||
',VALUTADT,-SUMA,-CANT,-SUMAVALDT,-SUMAGAAP,-DTCANT1'||
case when bUseAP then
',(SELECT CASE WHEN AP IN (''A'',''P'') THEN AP ELSE ''N'' END FROM TMS_PDC'||
' WHERE CONT=A.DT AND CONT1=0 AND ROWNUM=1)AP'||LF end||
' FROM TMDB_CM A'||
' WHERE '||cFiltCM;
busetime    
dBegin:=TRUNC(dSold)+1;
if busefinal = false
cFiltCM:='DATA BETWEEN '||DateToStr(dBegin)||' AND '||DateToStr(dFinal)||LF;
dSold DATE:=NVL(pData,SYSDATE);
dBegin:=TRUNC(dSold);
dFinal:=TO_DATE('31.12.3000','dd.mm.yyyy');
cSource:='SELECT '||v_hint||' DT,DT1,DTSC,DTDEP,DTSC1,DTNRDOC,
DTSTRSC,DTNRCM,DTDIV,DTDATA'||
',VALUTADT,SUMA,CANT,SUMAVALDT,SUMAGAAP,DTCANT1'||LF||
case when bUseAP then
',(SELECT CASE WHEN AP IN (''A'',''P'') THEN AP ELSE ''N'' END FROM TMS_PDC'||
' WHERE CONT=A.DT AND CONT1=0 AND ROWNUM=1)AP'||LF end||
' FROM TMDB_CM A'||LF||
' WHERE '||cFiltCM;
new vers use final=false
dFinal:=TRUNC(dSold);
*/
```

