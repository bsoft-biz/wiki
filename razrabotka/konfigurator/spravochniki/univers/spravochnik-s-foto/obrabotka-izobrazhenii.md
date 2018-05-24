# Обработка изображений

  
Обработка изображений можно посмотреть по [ссылке](http://www.veel.ru/articles/subd-oracle/obrabotka-izobrazhenij-ob-ekt-ordimage). 

Официальная документация по использованию ORDImage доступна [по ссылке](https://docs.oracle.com/cd/E11882_01/appdev.112/e10776/ch_imgref.htm#AIVUG80485)

ORDImage object type поддерживает хранение, управление, манипуляции с изображениями.

Атрибуты определены в файле ordispec.sql:

-------------------

source              ORDSource,

height              INTEGER,

width               INTEGER,

contentLength       INTEGER,

fileFormat          VARCHAR2\(4000\),

contentFormat       VARCHAR2\(4000\),

compressionFormat   VARCHAR2\(4000\),

mimeType            VARCHAR2\(4000\),

source: the source of the stored image data. - источник данных

height: the height of the image in pixels. - высота

width: the width of the image in pixels. - ширина

contentLength: the size of the image file on disk, in bytes. - размер файла на диске

fileFormat: the file type or format in which the image data is stored \(TIFF, JFIF, and so on\). - формат файла

contentFormat: the type of image \(monochrome and so on\). - тип файла\(черно-белый и т.д.\)

compressionFormat: the compression algorithm used on the image data. - алгоритм сжатия, использ. для изображения

mimeType: the MIME type information.

Все параметры можно менять с помощью определенных методов, описанных в оф. инструкции.

Изменение размера объекта Blob.

```sql
declare
cursor curs is 
select cod from tms_univ_photo where photo is not null; 
oimg ORDImage;
oimg_100 ORDImage := ORDImage.init();
img blob;
img_100 blob;
v_emp number := 101;
begin
for rec in curs loop
begin
-- получение исходного изображения
select photo into img from tms_univ_photo where cod=rec.cod;
-- создание на основе исходного изображения объекта ORDImage
oimg := ORDSYS.ORDImage(img);
-- выборка записи, в которую предполагается записать копию изображения
-- запись должна быть выбрана в режиме FOR UPDATE
select photo_small into img_100 from tms_univ_photo where cod=rec.cod for update;
-- создание объекта ORDImage, связанного с полем назначения
oimg_100 := ORDSYS.ORDImage(img_100);
-- масштабирование изображения до размеров 100x100 с сохранением пропорций
oimg.processCopy('maxScale=250 250', oimg_100);
update tms_univ_photo set
photo_small = oimg_100.getContent()
where cod=rec.cod;
exception when others then
say(rec.cod||sqlerrm);
end;
end loop; 
end;
```

