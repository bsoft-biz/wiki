# Настройка прав

Чтобы разрешить пользователю удаление из универс:  
un4public.envun4.EnvSetValue\('univers\_allow\_del', 1\);

Чтобы полностью запретить вставку в универс:  
 un4public.envun4.EnvSetValue\('univ\_ins\_deny', 1\);

## XUNIVLOCK {#HXUNIVLOCK}

На таблице TMS\_UNIVERS есть триггер, который проверяет права текущего пользователя на модификацию того раздела справочника, к которому относится изменяемая запись.

Триггер называется TMS\_UNIVERS\_TRLOCK, он использует процедуру UNIVLOCK\_CHECKTIP для проверки прав доступа.

На таблицах TMS\_AFX, TMS\_MPT, TMS\_MUNC, TMS\_ORG и еще на нескольких, связанных с TMS\_UNIVERS каскадным удалением, тоже стоят триггера, проверяющие те же права. Эти триггера используют процедуру  UNIVLOCK\_CHECKCOD, которая по коду вычисляет значения TIP и GR1 и вызывает для них процедуру UNIVLOCK\_CHECKTIP. Так сделано потому, что в этих таблицах наизвестны значения TIP и GR1, приходится делать проверку

в два действия.

Суть проверки сводится к оценке двух факторов:

1. Запрещен ли данный раздел справочника?

2. Если да, то нет ли у пользователя особых прав?

Запрещение модификации реализовано следующим образом.

Есть таблица TMS\_UNIVLOCK, в ней - три поля:

TIP VARCHAR2\(1\)

GR1 VARCHAR2\(5\)

PERSON VARCHAR2\(50\)

Каждая запись этой таблицы объявляет запрет на изменение какой-то части справочника Univers - на пару значений TIP и GR1 или на весь TIP \(если GR1 пуст\).

Поле PERSON служит для указания сотрудника, ответственного за изменения этого раздела справочника.

На этой таблице есть триггер TMS\_UNIVLOCK\_TR, позволяющий вносить в нее изменения только пользователю с правами администратора. Для запрета модификации какого-то раздела справочника надо внести новую запись в эту таблицу.

Особые права пользователей реализованы следующим образом.

Есть временная таблица XUNIVUNLOCK, в ней - пять полей:

TIP VARCHAR2\(1\)

GR1 VARCHAR2\(5\)

I NUMBER\(1\)

U NUMBER\(1\)

D NUMBER\(1\)

Эта таблица при каждом соединении вначале пуста, но процедура инициализации рабочего окружения пользователя может вносить сюда какие-то записи. Каждая запись означает права пользователя на внесение изменений в соответствующий раздел справочника, несмотря на общий запрет модификации. Пользователь, которому нужно дать такие права, должен в своей секции Администратора иметь свойство RunSQL, в котором будет примерно такие строки:

BEGIN   
INSERT INTO VUNIVUNLOCK \(TIP,GR1\) VALUES \('O','R'\);   
END;   
В этом примере пользователю даются права на **любую** работу со списком сотрудников \(включая их карточки\).

BEGIN  
 INSERT INTO VUNIVUNLOCK \(TIP,GR1\) VALUES \('O','R',0,1,0\);   
END;  
В этом примере пользователь получает право вносить изменения, но не может добавлять либо удалять сотрудников.

Важно заметить, что вставка выполняется не в таблицу XUNIVUNLOCK, а во вьюшку VUNIVUNLOCK. 

Эта вьюшка при вставке исключает дублирование записей, это важно при повторном выполнении RunSQL во время обновления настроек \(F5\)  
  
Для разрешения/запрета пользователю выполнения определённых операций, необходимо явно указать это цифровым значением   
1-разрешить   
любое другое - запретить   
null или отсутствие параметра считается разрешением
