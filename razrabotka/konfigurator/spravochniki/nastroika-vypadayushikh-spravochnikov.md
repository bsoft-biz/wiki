# Настройка выпадающих справочников

Чтобы **заполнять поля документа из справочника при выборе позиции в справочнике**, можно воспользоваться свойством **COPYFIELD**, при этом указывается поле для заполнения и поле со значением, например:

**COPYFIELD2=EXPEDITOR\_SC=agent**

значит, что поле документа **EXPEDITOR\_SC** будет заполняться значением поля **agent** справочника при выборе позиции из справочника.

Пример кода справочника:

TIP=U

COPYFIELD1=CLCEXPEDITOR\_SCT=agentName

COPYFIELD2=EXPEDITOR\_SC=agent

COPYFIELD3=PRPARC\_SERIA=SERIA\_FP

COPYFIELD4=PRPARC\_NR=NUMAR\_FP

COPYFIELD5=PRPARC\_DATA=DATA\_FP

COPYFIELD6=INTREPAUTO\_UNIV\_SC=INTREPAUTO\_UNIV\_SC

COPYFIELD7=CLCINTREPAUTO\_SCT=CLCINTREPAUTOT

COPYFIELD8=SOFER\_SYSS=SOFER

COPYFIELD9=SOFER=CLCSOFERT

COPYFIELD10=AUTOMOBIL\_SYSS=AUTOMOBIL

COPYFIELD11=AUTOMOBIL=CLCAUTOMOBILT

COPYFIELD12=PRICELIST\_ID=CODPRICE

COPYFIELD13=PRICELIST\_GRP=CODGRP

COPYFIELD14=CLCPRICEGRPT=CLCPRICEGRPT

FIELD\_COD=DTDEP

U\_FILTER\_TIP=\*O\*E\*Firms1

AutoDropDown=0 - при переходе на поле не отрывать автоматически выпадающий справочник

### Типы выпадающих справочников в экшенах:

Для выпадающего **календаря**:

/\*

.text.p\_datastart=Дата начала:

.type.p\_datastart=**DateX**

\*/

**Текстовое** поле для даты:

/\*

.text.p\_datastart=Дата начала:

.type.p\_datastart=**DateX**

\*/

