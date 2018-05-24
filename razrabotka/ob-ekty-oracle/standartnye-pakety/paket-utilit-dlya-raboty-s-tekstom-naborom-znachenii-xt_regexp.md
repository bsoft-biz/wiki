# Пакет утилит для работы с текстом, набором значений xt\_regexp

  
Ссылка на источник:

Пакет - [https://github.com/xtender/XT\_REGEXP](https://github.com/xtender/XT_REGEXP)

Описание пакета - [описание пакета на вики GitHub](https://github.com/xtender/XT_REGEXP/wiki/%D0%9A%D1%80%D0%B0%D1%82%D0%BA%D0%BE%D0%B5-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5)

## Краткое описание {#H41A44043044243A43E43543E43F43844143043D438435}

Function list:

```sql
function split_simple(p_str in varchar2,p_delim in varchar2)
return varchar2_table pipelined;
```

 Simple split string by delimiter as substring without regular expression.

```sql
function split(pStr varchar2,pDelimRegexp varchar2,pMaxCount number default 0)
return varchar2_table;
```

Function splits string by substrings matched for regular explression.

Example:

```sql
select * from table(
xt_regexp.split('Please, make me happy!','(?<=,)\s')
);
```

 Another example:

```sql
select * from table(
xt_regexp.split('Please, make me happy!','\s',3)
);
```

```sql
function matches(pStr varchar2,pPattern varchar2,
pCANON_EQ number default 0,
pCASE_INSENSITIVE number default 0,
pCOMMENTS         number default 0,
pDOTALL          number default 0,
pMULTILINE        number default 0,
pUNICODE_CAS     number default 0,
pUNIX_LINES      number default 0
)
return boolean;
```



Function return true, if input string matches regular explression. First parameter-string for testing, second - regular expression, others - modifiers for regular expression:

* CANON\_EQ - canonical equal;
* CASE\_INSENSITIVE - case insensitive;
* COMMENTS - ignore comments starts with \#;
* DOTALL - dot symbol in regexp includes string delimiter\(/n,/r/n\) \(default-not\);
* LITERAL - template is not regular expression;
* MULTILINE - multiline mode;
* UNICODE\_CASE - case for unicode;
* UNIX\_LINES - string deliniter is /n

```sql
function get_matches(
pStr varchar2,
pPattern varchar2,
pMaxCount number default 0,
pCANON_EQ number default 0,
pCASE_INSENSITIVE number default 0,
pCOMMENTS         number default 0,
pDOTALL          number default 0,
pMULTILINE        number default 0,
pUNICODE_CAS     number default 0,
pUNIX_LINES      number default 0)
return varchar2_table;
```

Function returns collection of matched strings. Params like previous function, excepts pMaxCount - max count strings, if not set or equal 0 returns all.

Example:

```sql
select * from table(
xt_regexp.get_matches('Please, make me happy!','\S*m\S*')
);
```

```sql
function join_matches(
pStr varchar2,
pPattern varchar2,
pDelim varchar2 default ';',
pCANON_EQ number default 0,
pCASE_INSENSITIVE number default 0,
pCOMMENTS         number default 0,
pDOTALL          number default 0,
pMULTILINE        number default 0,
pUNICODE_CAS     number default 0,
pUNIX_LINES      number default 0)
return varchar2;
```

 Function like get\_matches, but returns joined collection with delimiter.

```sql
function replace_all(pStr varchar2,pPattern varchar2,pReplacement varchar2)
return varchar2
```

Function replaces matched substring with third param.

Example - add "Scott!!!!" after comma with "Please":

```sql
select xt_regexp.replace_all('Please, make me happy!',
'(?<=Please)(,)','$1 Scott!!!!') from dual;
```

 Result: **Please, Scott!!!! make me happy!**

```sql
function replace_first(pStr varchar2,pPattern varchar2,pReplacement varchar2)
return varchar2
```

 Function line previous but replaces just first occurence.

