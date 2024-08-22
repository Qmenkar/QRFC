# QRFC
Ration Food Calculator / Рiking Кation Сalculator / Spreadsheet

## Описание:

Калькулятор походного рациона питания

Калькулятор позволяет создать рацион питания на N дней для X участников.
Основное назначение - организация походного рациона.

## Основные возможности:
Использование базы знаний на странице "Продуктовая таблица".
Гибкие возможности для организации рациона по дням.
Масштабирование количества дней, продуктов, участников.
Выбор единицы расчётов (гр/кг).
Расчёт закупки в итоговой таблице.
Таблица для расчёта дополнительных продуктов и резервов.
Автоматическая проверка ошибок в расчётах.
Расчёт закупки продуктов.
Калькуляция взаиморасчётов. 
Подробная статистика по итоговой массе и калорийности.
Применение мультипликаторов для каждого из дней и итоговых таблиц.

Видео-инструкция на youtube: https://youtu.be/qH6leCVlpCo
Заметка: текущий рацион типа K2v6 в калькуляторе предназначен только для ознакомления.

## Инструкция по редактированию рациона питания:

1. Определить количество участников для рациона в "Количество участников (множитель):" 
Дополнительно можно указать предельно допустимое количество жиров и углеводов. Это не повлияет на состав рациона, только на информирование по балансу БЖУ по дням.

2. Любой день кроме первого и завершающего можно скопировать/удалить выше или ниже любого другого дня.
Для наглядности лучше делать это вместе со строкой-разделителем (пустая строка между днями).

3. Подобным образом можно добавлять/удалять/копировать строки с продуктами в каждый из дней.
Можно копировать и дополнять дни продуктами вручную или из "великой продуктовой таблицы" простым копированием нужной строки.
Для каждого дня можно добавить мультипликатор, который повторяет рацион этого дня на указанное значение.

4. В итоговую таблицу* нужно добавить все продуты из рациона по дням.
т.е. все названия продуктов из дневных рационов должны быть в итоговой таблице. Названия должны совпадать (по этому текстовому шаблону происходит поиск и суммирование продуктов).

5. Таблица с резервными и дополнительными продуктами заполняется вручную.
В этой таблице удобно располагать сверхнормативные, экспериментальные или резервные продукты. А так же продукты с неопределенным периодом употребления (по настроению или необходимости). Для таблиц так же можно добавить множитель, на который будет масштабировано всё содержание итоговых таблиц. Так же есть возможность отобразить итоговые суммы рациона в граммах или килограммах.

6. Дополнительно, можно посчитать группы для закупки товаров. 
Группы считаются по идентификатору (id, по "умолчанию от 1 до 6). id заполняются в столбце итоговой таблицы. Это нужно для балансировки закупки и подсчёта массы продуктов для каждого из участников.
В таблице закупки можно посчитать затраты каждого из участников закупки.

Остальные расчёты происходят автоматически.

* В ячейках таблиц есть примечания по заполнению и методике расчёта.
** При ручной правке дневных рационов стоит уделить внимание диапазонам охвата в ячейках утро/день/вечер (охват может "уплыть")
*** Во избежание ошибок при подготовке рациона желательно работать с копией исходного файла.
**** Дополнительные примечания в ячейках первого и завершающего дней.

## Примечания

1. В рационе используются автоматические проверки корректности заполнения.
1.1 Проверки веса и количества продуктов в дневных рационах и в итоговой таблице.
> Если возникла ошибка при проверке следует проверить охват диапазона в столбце "Вес, гр. * X чел" итоговой таблицы.
> Если возникла ошибка при проверке следует проверить охват диапазона в столбцах "итого" (по дням, обычно первый и последний дни).
> Не забывать добавление продуктов из дневных рационов (которые разбиты по дням). 
> Название продукта должно соответствовать названию в итоговой таблице (по названию идёт поиск). 
> Добавлять строки в итоговые таблицы желательно ниже первой и выше последней. При произвольном добавлении желательно выполнить проверку формул, работающих по диапазонам таблицы (это наглядно отобразится в ячейке "проверка таблиц" и "алгоритм-2" как "ошибка").
> В итоговых таблицах следует избегать дублирования записей (это приведет к ошибке) и отобразиться в ячейках проверки таблиц.
1.2 Проверка калорийности по дням.
> Наиболее вероятная причина ошибки: "кривой" диапазон охвата области для ячеек кк утро/день/вечер в одном из дней.

2. Ячейки белого цвета заполняются руками. 
Остальные ячейки считаются автоматически. Основные цвета ячеек перечислены в "легенде". Цвета не важны для расчётов и нужны только для наглядности.

3. Список продуктов хранится на вкладке "Продуктовая таблица". Дополнить рацион можно простым копированием строк из этой таблицы.

4. Надо понимать что ряд продуктов может носить универсальный характер. Например, "крупа мультизлаковая" может быть набором самых разных круп. Или шоколад - может быть как обычным шоколадом, так и конфетами, батончиками и т.п.

5. В примере этого рациона, продукты повторяются с определённой чётностью, например "4". Кроме первого и последнего дней. Например, рацион для дней 2,3,4,5 = 6,7,8,9 = 9,10,11,12 и т.д. Таким образом достигается умеренное разнообразие продуктов питания.
