# Вывод штрих-кодов в печатной форме

  
1\) Установить шрифты. [шрифты для штрихкодов.rar](http://wiki.bsoft.biz/xwiki/bin/download/%D0%A0%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0/%D0%92%D1%8B%D0%B2%D0%BE%D0%B4+%D1%88%D1%82%D1%80%D0%B8%D1%85-%D0%BA%D0%BE%D0%B4%D0%BE%D0%B2+%D0%B2+%D0%BF%D0%B5%D1%87%D0%B0%D1%82%D0%BD%D0%BE%D0%B9+%D1%84%D0%BE%D1%80%D0%BC%D0%B5/%D1%88%D1%80%D0%B8%D1%84%D1%82%D1%8B%20%D0%B4%D0%BB%D1%8F%20%D1%88%D1%82%D1%80%D0%B8%D1%85%D0%BA%D0%BE%D0%B4%D0%BE%D0%B2.rar)

2\) В печатной форме для ячейки устанавливаем шрифт, например EAN-13 HalfHeight 

3\) В запросе необходимо преобразовать наше значение, используя функцию : un$bcod.MakeEAN13,

например: un$bcod.MakeEAN13\(nrdoc\)
