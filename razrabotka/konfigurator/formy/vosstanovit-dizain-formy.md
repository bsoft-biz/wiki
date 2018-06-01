# Восстановить дизайн формы

  
Дизайн форм хранится в таблице a$lob.

После обновления конфигуратора не подгружается дизайн некоторых форм. Это может происходить потому что в поле lob\_name имя дизайна содержит корень Sal1.

В таком случае в новом клиенте при первом обращении к форме дизайн не подгружается и в таблице a$lob создаются новые строки с пустым дизайном и корнем S1c.

Чтобы восстановить дизайн формы, нужно до первого обращения к форме выполнить update:

update a$lob set  lob\_name = replace\(lob\_name,'fmFSal1','fmFS1c'\) where obj\_id=1780

где 1780 - это nr ord формы.
