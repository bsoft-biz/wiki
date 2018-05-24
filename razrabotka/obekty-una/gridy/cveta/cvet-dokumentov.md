# Цвет документов

**Актуальная версия триггера.**

```sql
CREATE OR REPLACE TRIGGER TRG_DOCS_COLOR 
before insert or update ON TMDB_DOCS
for each row
WHEN (
(new.at1 is null or upper(sys_context('envun4','docs_alt_color_enabled')) = 'TRUE')
and sys_context('envun4','dont_fire_trigger') is null
)
begin
begin
select '-' into :new.doccolor from vmdb_docs_add
where cod = :new.cod and recalc_nrdoc is not null and :new.at1 is null;
exception when no_data_found then
-- alt_color используется для задания цвета документа в тех случаях, когда это невозможно
-- сделать изменением самого поля doccolor. например, при сохранении документа в программе
-- производится update tmdb_docs с установкой doccolor в значение, считанное программой при
-- входе в документ, поэтому изменение поля docolor, произведённое при открытом в режиме
-- редактирования документе, теряется.
select alt_color into :new.doccolor from vmdb_docs_add
where cod = :new.cod
and alt_color is not null
and upper(sys_context('envun4','docs_alt_color_enabled')) = 'TRUE';
end;
exception when no_data_found then
begin
select '' into :new.doccolor from vmdb_cmi 
where nrdoc = :new.cod and rownum = 1 and :new.at1 is null;
exception when no_data_found then
if :new.at1 is null then
:new.doccolor := '`';
end if;
end;
end;
/
```

 **Установить Контекст**

```sql
sys_context('envun4','docs_alt_color_enabled') = true
```

**Процедуры для работы с цветом**

set\_doc\_color

clear\_doc\_color

Цвета для документа определяются с помощью **функции**:

pkg\_docs\_util.decode\_color

