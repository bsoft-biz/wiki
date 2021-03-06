# Журналы

Объекты Журналы служат для фильтрации Пользователем таблицы документов по участкам. Доступные журналы отображаются в меню \[Registre\] приложения Universal Accounting. Структура списка журналов соответствует структуре дерева объектов типа Журналы в Администраторе. Объект типа Журнал содержит описание фильтров для типов документов, принадлежащих соответствующему журналу.

| **Имя свойства** | **Тип** | **Описание** | **Значение для примера** |
| :--- | :---: | :--- | :--- |
|  |  | **Основные свойства:** |  |
| Active | Boolean | Если значение `False`, объект игнорируется | `True` |
| Caption | String | Подпись для журнала в меню \[Registre\] | 0.1 Материалы |
| DLL ID | Integer | Идентификационный номер DLL | 0 |
| DLL Journal Name | String | Идентификационный номер журнала в DLL | Marfuri |
| DocTypesDefault | Integer | Тип документов по умолчанию \(при insert автоматически создается этот `sysfid`\) | 1602 |
| DocTypesFilter | Memo | Фильтр типов документов, образующих журнал \(Строится условие по `ID`\) | `ID=1602` |
| SqlFilter | Memo | Фильтр типов документов образующих журнал \(Строится условие по `SysFID`\) | `sysfid =1602` |
|  |  | **Дополнительные свойства:** |  |
| NodeType | String | Если меню журналы отображается в виде тулбара \(см свойство TBJournals\), тогда полезно в этом меню вывести ссылки на формы и отчеты. Объект, на который ссылаются указывается в  свойстве NodeTypeSection. | Forms Reports |
| NodeTypeSection | String | Имя секции объекта, на который ссылается пункт меню журналы со свойством NodeType. | F\_CONFIRMARE\_O |
| Hint | String | Подсказка | 02.Подтверждение |
| DisableInsert | Boolean | Запретить добавление документов в журнале | `true` |
| LinkMenu | String | При выполнении программы в этом пункте меню добавляется список из секций, указанных в свойстве  ToolBarFormSections \(если значение Forms\). | Forms |
| DisableChild | Boolean | Задокументировать свойства | `true` |
| ShortCut | String | +Ctrl+Alt | 5 |
| Dynamic | Boolean | Найти и задокументировать свойства: \(должны быть на DEV\) | `false` |
| `ORDER BY` | `String` | Упорядочить строки в журнале | список полей для сортировки |
| SQLBody | Memo | Произвольный запрос в журнале \(в запросе должны быть обязательно все поля из докс, а потом уже дополнительные поля\). Это свойство SQLBody нужно, если в vmdb\_docs не хватает полей для журнала и нужно объединить ее с другой вьюхой и вытащить доп. поля в журнал. | `select *  from (select a.*,  b.доп. поля from vmdb_docs a left join ДОП. ТАБЛИЦА b on a.cod=r.nrdoc where sysfid in (список sysfid) )` |
|  |  | **Прочие свойства:** |  |
| Caption | String | Наряду с журналами создаем такой псевдожурнал | Rapoarte |
| NodeType | String | Отчеты будут кнопкой рядом с журналами | Reports |

