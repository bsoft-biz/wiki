# Параметры выпадающих справочников

Эти все свойства указываются в Alt+D для нужного поля в “блокнотике” ![N](https://github.com/prbsoft/wiki/blob/master/src/Блокнот.png?raw=true)\(то есть нажать кнопку слева от надписи "Dropdown list setup and other field properties"\).

| **Имя свойства** | **Описание** | **Пример** |
| :--- | :---: | :--- |
| .DefValue | Задает значение по умолчанию у данного поля | .DefValue=… |
| TextFilter | Когда, стоя на любой ячейке столбца, начнем набирать текст, будет сразу появляться окошко для установки фильтра \(которое обычно вызывается по Ctrl+F\) | TextFilter=1 |
| CheckMark | + галка ReadOnly +\(по желанию, шрифт Windings2 жирный зеленый 14\)=&gt; Двойной клик левой кнопкой мыши ставит в ячейку галку/указанную цифру/букву/и т.п. | CheckMark=1 |
| Origin | Чтобы список выпадал сразу при получении фокуса. Cod - название числового поля. Не работает вместе со SpeedSearch=1 | Origin=cod |
| AutoPostEdit |  | AutoPostEdit=1 |
| SavePos | Сохранять предыдущую позицию справочника при его повторном открытии. Для запоминания справочником последней выбранной позиции в свойстве Params должны быть указаны следующие свойства: SavePos, SavePosKeys, SavePosName | SavePos=1 |
| SavePosKeys | Ключевые поля \(по умолчанию - ListFields\) | SavePosKeys=DTDEP,DTSC |
| SavePosName | Уникальное имя \(по умолчанию - DesignName\) | SavePosName=Contracte |
| StartField | Поле, которое подсвечивается \(по умолчанию справочник\) | StratField="gos\_nom\_short" |
| StartField | Это поле грида будет получать фокус каждый раз при добавлении новой строки | StartField=1 |
| AutoDropDown | При переходе на поле не отрывать автоматически выпадающий справочник | AutoDropDown=0 |
| COPYFIELD | Заполнение поля документа из справочника при выборе позиции в справочнике. Можно воспользоваться свойством COPYFIELD, при этом указывается поле для заполнения и поле со значением, например:COPYFIELD2=EXPEDITOR\_SC=agentзначит, что поле документа _\*\*_EXPEDITOR\_SC будет заполняться значением поля agent справочника при выборе позиции из справочника. | TIP=UCOPYFIELD1=     CLCEXPEDITOR\_SCT=                         agentNameCOPYFIELD2=     EXPEDITOR\_SC=                agentCOPYFIELD3=                PRPARC\_SERIA= SERIA\_FPFIELD\_COD=  DTDEPU\_FILTER\_TIP= \*O\*E\*Firms1 |
| DesignName | Имя дизайна для сохранения в метаданных. При использовании нескольких выпадающих справочников типа SQL в одном гриде появляется глюк, при котором настройки \(дизайн нрида\) одного справочника влияют \(отображаются\) в другом. Эти настройки сохраняются под одним именем. Чтобы этого избежать нужно явно задать имя дизайна, которое будет использоваться для этого поля. | spr\_auto |

{% hint style="info" %}
_Подсказки:_

Если в выпадающем списке не работает Enter и Esc, то надо открыть дизайн с LShift и в Grid изменить Keyb.mode на 1
{% endhint %}

[Настройка документа для ввода данных сканером штрих-кодов](https://bsoft.gitbook.io/wiki/razrabotka/obekty-una/gridy/nastroika-dokumenta-dlya-vvoda-dannykh-skanerom-shtrikh-kodov)

