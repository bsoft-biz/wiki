# Через контексты

Политика на запрет/разрешение редактирования справочников syss \(`PY_SYSS`\).

По умолчанию политика не влияет на доступ к справочнику.

Правила для предоставления доступа к изменению справочников по типам реализованы в функции `secure_cm.secure_syss` \(сх. `UN4PUBLIC`\).

Для разрешения/запрета доступа на редактирование нужно в RunSql на пользователе или на группе пользователей добавить строку с опр. условиями в контексты `PERMITED_SYSS_TIP` или `RESTRICTED_SYSS_TIP`.

Если заполнен контекст `PERMITED_SYSS_TIP`, то применится его правило, иначе если заполнен контекст `RESTRICTED_SYSS_TIP`, то применится правило not\(`RESTRICTED_SYSS_TIP`\).

Примеры runSql для запрета редактирования:

В RunSQL

```sql
envun4.EnvSetValue('restricted_syss_tip','0 = 0'); 
envun4.EnvSetValue('restricted_syss_tip','tip in (''R'') and cod in (502,18,61)');
envun4.EnvSetValue('restricted_syss_tip','tip in (''S'') and cod in (14)');
```

Примеры runSql для доступа пользователей к редактированию:

В RunSQL

```sql
envun4.EnvSetValue('PERMITED_SYSS_TIP','0 = 0'); 
envun4.EnvSetValue('PERMITED_SYSS_TIP','tip in (''R'') and cod in (502,18,61)');
envun4.EnvSetValue('PERMITED_SYSS_TIP','tip in (''S'') and cod in (14)');
```



