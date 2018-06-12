# Весовая

## Форма проходной ЖД/Авто

```sql
[ZZZ]
-- если несколько весовых
ARM=2
.type.ARM=String
--
Active=true
.type.Active=Boolean
--
Caption=04. Весовая Ж/Д
.type.Caption=String
.MISS.rom.Caption=04. Cintar intrare pt cale ferata
.MISS.rus.Caption=04. Весовая Ж/Д
-- Тип
DLL FormName=PROHODNAIA_SOARE
.type.DLL FormName=String
.MISS.eng.DLL FormName=PROHODNAIA_SOARE
.MISS.rom.DLL FormName=PROHODNAIA_SOARE
.MISS.rus.DLL FormName=PROHODNAIA_SOARE
--
DLL ID=8200
.type.DLL ID=Integer
-- поставить true чтобы приходили только картинки по нажатию взвесить
DisableRealTimePreview=true
.type.DisableRealTimePreview=Boolean
--
SagiEditQuery=true
.type.SagiEditQuery=Boolean
-- true новый драйвер, false - старый
UseAlexComScales=true
.type.UseAlexComScales=Boolean
-- Для отображения фото и видео
UseCamera=true
.type.UseCamera=Boolean
-- путь к unVideoCatch.exe на локальной машине
VideoCatchPath=D:\Video\unVideoCatch.exe
.type.VideoCatchPath=String
-- для ЖД весов невозможно дождаться чтобы на весах был 0 - там вагон за вагоном, 
--а на авто удобно чтобы машина съехала, весы стабилизировались на 0 а потом заехала новая
UseZeroWeight=true
.type._UseZeroWeight=Boolean
-- фильтр для спр-ка поставщиков
clcdep_postavt_gr1=E,I
.type.clcdep_postavt_gr1=String
clcdep_postavt_tip=O
.type.clcdep_postavt_tip=String
--
CloseImmediateVideoCatch=true
.type.CloseImmediateVideoCatch=Boolean
.Hint.CloseImmediateVideoCatch=если true закрывается unVideaCatch после получения фото
```

## unvideocatch

Для работы videoCatch нужно прописывать в ini две камеры

ini для unvideocatch

RealTime для NetDVR значения 0 или 1

0 - не отоброжается видео в UnVideoCatch но передаются фото через Handle в другом окне

1 - отображается видео в UnVideoCatch

