# Абстрактный документ

```sql
[ABSTRACTDOCS]
.objType=1
.objSubType=-1
.Caption=Abstract
.Type=DOCUMENTSGR
.MISS.eng..Caption=Abstract
.MISS.rom..Caption=Abstract
.MISS.rus..Caption=Abstract
[COMMONACTIONS]
.objType=1
.objSubType=0
.Caption=Common actions
.document=
.MISS.eng..Caption=Common actions
.MISS.rom..Caption=Common actions
.MISS.rus..Caption=Common actions
Abstract=true
.type.Abstract=Boolean
.ListValue.Abstract=true,false
.Parent=ABSTRACTDOCS
[COMMONACTIONBOTTOM]
.objType=1
.objSubType=2
.Caption=Блокировка документа
.MISS.eng..Caption=Блокировка документа
.MISS.rom..Caption=Блокировка документа
.MISS.rus..Caption=Блокировка документа
AbstractListSysFID_1=1602,1604
.type.AbstractListSysFID_1=String
.Hint.AbstractListSysFID_1=Spisok SYSFID (filter)
ActionType=1
.type.ActionType=String
ID=1
.type.ID=Int
SQL1=.MEMO.COMMONACTIONBOTTOM.SQL1
.type.SQL1=Memo
TextForUser=Заблокировать документ!
.type.TextForUser=String
.Parent=COMMONACTIONS
[.MEMO.COMMONACTIONBOTTOM.SQL1]
begin
 block_doc(:nrdoc);
end;
```

