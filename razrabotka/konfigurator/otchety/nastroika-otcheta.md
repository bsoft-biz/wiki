# Настройка отчета

  
**title** - выводится информация из SqlHeader

**title \| Page**    - на каждой странице

**title \| General**    - только на ПЕРВОЙ странице

**detail1** - выводится информация из SqlMaster

**summary** - подвал, для итога :  \_\_поле

**params \| JoinFields \| поле группировки \(без \_ \)**   - группировка по полю, без повторений, т.е. пишется один раз значение поля группировки

**groupF \| \_поле группировки \| PageBreak** - переход на новую страницу

**title \| Page**    - на каждой странице

**Все настраиваемые параметры страницы применяются после закрытия формы отчета в клиенте.**

Свойство **TXTFixedPreview=true** - отображает отчет в текстовом виде \(н-р: заявка\)

## Создание отчета с шаблоном типа \*.fr3 {#H42143E43743443043D43843543E44244743544243044144843043143B43E43D43E43C44243843F4302A.fr3}

Ссылка на пример отчета \(файл находится в папке Настройка отчета\):

Для отчетов с шаблоном **\*.fr3** необходимым свойством является:

**VersionFR=4**

Чтобы настроить **DataSet** шаблона нужно создать ПФ в документе с таким же SQL и шаблоном \(в пф должно быть свойство **VersionFR=4**\) и при печати этой ПФ нажать кнопку шаблон. Там можно настроить **DataSet** и поля отчета.

Свойство шаблона, которое отвечает за количество столбцов отчета:

**Columns=2**

Чтобы указать **DataSet** - пункт меню **Report - Data**.

Переменные в шаблоне должны иметь тот же **DataSet**, который был выбран для шаблона.

