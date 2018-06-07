# Модальные формы

  
Модальная форма - это форма которая открывается в отдельном окне.

`Свойства:`

| **Название свойства** | **Тип** | **Описание**  | **Значение для примера**  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `Modal` | `Boolean` | будет ли форма модальной | `true` |
| `Modal_OK` | `Boolean` | наличие в форме кнопки ок на форме | `true` |
| `Modal_OK_SQL` | `Memo` | `pl/sql`, который выполняется при нажатии кнопки Ок на форме | `begin envun4.envsetvalue ('FILTER_JOURNAL','1');                        if sys_context('envun4','SMENA')        is null then -- смена           msg('Укажите смену!');  end if;  if sys_context('envun4','KLADOVSCIK') is null then                       msg('Укажите кладовщика!');      end if;end;` |
| `Modal_RefreshDataCurent` | `Boolean` | будет ли обновлена текущая дата, журнал документов, период для отчетов  | `true` |
| `Modal_RefreshDocs` | `Boolean` |  | `true` |
| `Modal_RefreshReportPeriod` | `Boolean` |  | `true` |
| `PanelAllowExit` | `Boolean` | Выход по `Ok`. Если `false`, то при редактировании панели пока не нажать `Post` нельзя закрыть модальную форму  | `true` |
|  |  | **Размеры формы \(если не указать, то открывается на весь экран\)** |  |
| `Modal_SizeX` | `Integer` |  | `420` |
| `Modal_SizeY` | `Integer` |  | `350` |

