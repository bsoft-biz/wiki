# Через контексты

Политика на запрет/разрешение редактирования справочников syss \(PY\_SYSS\).

По умолчанию политика не влияет на доступ к справочнику.

Правила для предоставления доступа к изменению справочников по типам реализованы в функции secure\_cm.secure\_syss \(сх. UN4PUBLIC\).

Для разрешения/запрета доступа на редактирование нужно в RunSql на пользователе или на группе пользователей добавить строку с опр. условиями в контексты PERMITED\_SYSS\_TIP или RESTRICTED\_SYSS\_TIP.

Если заполнен контекст PERMITED\_SYSS\_TIP, то применится его правило, иначе если заполнен контекст RESTRICTED\_SYSS\_TIP, то применится правило not\(RESTRICTED\_SYSS\_TIP\).

Примеры runSql для запрета редактирования:

В RunSQL

envun4.EnvSetValue\('restricted\_syss\_tip','0 = 0'\); 

envun4.EnvSetValue\('restricted\_syss\_tip','tip in \(''R''\) and cod in \(502,18,61\)'\);  
envun4.EnvSetValue\('restricted\_syss\_tip','tip in \(''S''\) and cod in \(14\)'\);

Примеры runSql для доступа пользователей к редактированию:

В RunSQL

envun4.EnvSetValue\('PERMITED\_SYSS\_TIP','0 = 0'\); 

envun4.EnvSetValue\('PERMITED\_SYSS\_TIP','tip in \(''R''\) and cod in \(502,18,61\)'\);  
envun4.EnvSetValue\('PERMITED\_SYSS\_TIP','tip in \(''S''\) and cod in \(14\)'\);

