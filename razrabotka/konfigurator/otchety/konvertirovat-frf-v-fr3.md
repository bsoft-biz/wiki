# Конвертировать frf в fr3

  
В конфигураторе нужно выставить VersionFR = 4 

\[ZZZ\]

VersionFR=4

.type.VersionFR=Integer

и изменить имя шаблона на fr3 в Template.

Шаблон конвертировать через утилиту [Project1.exe](https://github.com/bsoft-biz/wiki/blob/master/src/Project1.exe)

В Project1 открываешь шаблон frf  и сохраняешь в fr3. \( сохраняет практически все компоненты\).

Датасеты нужно проставить уже через клиент.  В главном меню наверху назначить Мастер, детэйл \(в Data\).

Сначала построить пустой отчёт с этим шаблоном, потом через окно откладки зайти в дизайн, потом проставить поля в компонентах.

после конвертации в fr3

1\) Передавать параметры даты как  datebegin datefinal вместо datastart и dataend

2\) Значения параметров filt передавать через

begin

процедура \(:filt1\);

end;

/\*

filt1=edit\_fmAGRO\_filt1

\*/

3\) Не поддерживает передачу параметров из конфигуратора, т.е. не видит значения :ini\_параметр \(надо явно указывать в процедуре значение\)

4\) В fr3 нельзя в поле писать \[IF\(\[SubDtl."RULAJDT"\]=0, 'X', \[SubDtl."RULAJDT"\]\)\] 

надо создавать обработчик события OnBeforePrint и в нем уже прописывать условия.

Например:

procedure Memo55OnBeforePrint\(Sender: TfrxComponent\);

begin

if Memo55.Text='0' then 

 Memo55.Text := 'X'; 

end;

5\) нужно по другому прописывать суммы

было \[SUM\(\[Master."SUMADT"\]\)\]

стало \[SUM\(&lt;Master."SUMADT"&gt;,MasterData1\)\]

6\) когда используют fast report, то поле filt1 не передает значения null, а передает 0

