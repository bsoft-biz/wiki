# функция UN$SLD.MAKE

## функция UN$SLD.MAKE

 Фильтры для процедуры \(указывая их мы получаем таблицу в которой есть все  необходимые данные\) 

```sql
/* Filter examples:
A CONT  - '21 !214 521.1 522.(1,2)' - счет
B CONT1 - '1,2,3' or '1 2 3' - субсчет
C SC    \   - аналитика 
D DEP   -- '1,2,3' or '!1,2,3' - центр затрат
E SC1   / - субконто
F NRDOC - '1,2,3' or '1 2 3' 
G STRSC - 'abc' or ''abc'' or 'abc,def' or ''abc','def''
H NRCM - '1,2,3' or '1 2 3'
I DATA - '01.01.2006' or '01.01.2006,01.02.2006' or ''01.01.2006','01.02.2006''
J AP
K DIV
0 <Show Zero Records>
1 CANT
2 PRICE
3 VAL
4 GAAP
5 CANT1
*/
```

```sql
PROCEDURE MAKE(pData DATE:=NULL,sTableName VARCHAR2:=NULL
,pFilt VARCHAR2:=NULL,pCont VARCHAR2:=NULL,pCont1 VARCHAR2:=NULL
,pSc VARCHAR2:=NULL,pDep VARCHAR2:=NULL,pSc1 VARCHAR2:=NULL
,pNrDoc VARCHAR2:=NULL,pStrSc VARCHAR2:=NULL,pNrCM VARCHAR2:=NULL
,pAn_Data VARCHAR2:=NULL
,pDestTable VARCHAR2:=NULL -- Table for insert data (instead of XSLD)
,pCantsCoef VARCHAR2:=NULL
,pTableFilter VARCHAR2:=NULL -- Additional filter om TMDB_CM (dt side)
--,pSmart BOOLEAN:=NULL -- Empty pFilt is equal to '*'
,pOldMethod BOOLEAN:=NULL -- Don't use TXSLD
,pRegister BOOLEAN:=NULL -- Don't use pData+23/24
,pCalcOne BOOLEAN:=NULL -- Calculate one number for CALC_SOLD
,pValuta VARCHAR2:=NULL -- Valuta for CALC_SOLD
,pUseTime BOOLEAN:=NULL -- Use TMDB_DOCS_ADD.SOLD_TIME
,pTestMode BOOLEAN:=NULL -- Calculate the difference between real and TXSLD
);
```



