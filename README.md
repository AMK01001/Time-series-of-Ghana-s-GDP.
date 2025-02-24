# Проект: Временные ряды ВВП Ганы


## Оглавение
[1. Описание проекта](https://github.com/AMK01001/Time-series-of-Ghana-s-GDP.?tab=readme-ov-file#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

[2. Какой кейс решаем?](https://github.com/AMK01001/Time-series-of-Ghana-s-GDP.?tab=readme-ov-file#%D0%BA%D0%B0%D0%BA%D0%BE%D0%B9-%D0%BA%D0%B5%D0%B9%D1%81-%D1%80%D0%B5%D1%88%D0%B0%D0%B5%D0%BC)

[3. Результаты](https://github.com/AMK01001/Time-series-of-Ghana-s-GDP.?tab=readme-ov-file#%D1%80%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82%D1%8B)

## Описание проекта 

Работы с временными рядами ВВП Ганы

Цель данного проекта заключается в проведении всестороннего анализа временных рядов ВВП Ганы для выявления ключевых экономических тенденций, создания прогнозных моделей и принятия обоснованных решений для развития экономики.
:arrow up:[к оглавлению]https://github.com/AMK01001/Time-series-of-Ghana-s-GDP.?tab=readme-ov-file#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%B5%D0%BD%D0%B8%D0%B5()

## Какой кейс решаем?

### *ИССЛЕДОВАНИЕ ДАННЫХ*

Работать с данными по ВВП Ганы.


**КРИТЕРИИ ОЦЕНИВАНИЯ**:

Задачи проекта:

- Прочитайте исходный файл с данными. Визуализируйте исходный временной ряд, сделайте первичные выводы о присутствии компонент тренда и сезонности в ряде.

*Отложите последние три года из датасета как тестовую выборку для оценки результатов предсказания.*

- Постройте график скользящего среднего, проанализируйте результат. Для построения MA используйте метод rolling(), который принимает в качестве параметра размер окна. Используйте среднее как функцию для сглаживания. Ширину окна подберите самостоятельно.

*Пример: train_df.spx.rolling(window=2).mean().*

*Визуализируйте исходный временной ряд и построенный с помощью скользящего среднего прогноз, сравните графики между собой и сделайте выводы.*

- С помощью теста Дики-Фуллера оцените стационарность временного ряда и примите решение о выборе модели ARMA/ARIMA.

*Примечание. Если ваш ряд является нестационарным, дифференцируйте его до тех пор, пока он не станет таковым. Количество дифференцирований, необходимых для сведения ряда к стационарному, будет вашим параметром d для модели ARIMA.*

*Параметры p и q выберите по коррелограммам ACF и PACF.*

*Примечание. Помните, что параметры p и q для ARMA/ARIMA определяются из коррелограмм стационарного ряда. То есть, если ваш изначальный временной ряд не являлся стационарным, то коррелограммы строятся для разностей того порядка, которые являются стационарными*.

*Постройте модель ARMA/ARIMA для прогнозирования поведения временного ряда.*

*Также постройте несколько моделей с параметрами, ближайшими к найденным p и q, и сравните коэффициент AIC (или подберите наилучшие параметры с помощью пакета pmdarima).*

- Постройте модель с наилучшими параметрами и выполните предсказание для отложенной тестовой выборки (последние три года).

- Отобразите результат графически — постройте графики истинного и предсказанного поведения временного ряда, а также 95%-ый доверительный интервал для прогноза.

- Сделайте выводы по полученным результатам.

**Знакомства с данными**

### Датасет состоит из двух столбцов:

- year 

- GDP (current US$)


**Требования к оформлению ноутбука-решения**

- Оформите решение в Jupyter Notebook. После выполнения задания не забудьте сохранить результат в корректном формате .IPYNB.
- Возьмите за основу ноутбук-шаблон: не следует менять последовательность действий и уже заполненные ячейки (если прямо не указано иного). Вам необходимо только дополнить 
предложенный файл.
- Выполняйте каждое задание в отдельной ячейке, выделенной под него (в шаблоне они помечены как «ваш код здесь»). Не создавайте множество дополнительных ячеек — они делают 
ноутбук перегруженным и трудночитаемым.
- В решении должен быть использован только уже пройденный материал, кроме тех случаев, когда на использование дополнительного материала будет указано отдельно. 
Также в кейсе вам будет предложено творческое задание (доработка модели с использованием дополнительных инструментов). В нём вы сможете использовать любой доступный материал. 
Это будет указано в задании явным образом.
- Код должен быть читабельным и понятным: имена переменных и функций должны отражать их сущность, приветствуется отсутствие многострочных конструкций и условий. 
Любую задачу можно решить множеством вариантов: постарайтесь найти самый красивый и лаконичный. 
- Оформите код по стандартам PEP-8. Вы можете освежить в памяти требования стандарта в соответствующем руководстве. Также вы можете воспользоваться одним из онлайн-ресурсов, 
который проверяет код на соответствие стандартам (однако он зачастую бывает слишком строг).
- Все визуализации необходимо выполнять в соответствии с требованиями, которые вы изучали ранее. Все диаграммы и графики должны иметь содержательные названия и подписи осей.
 Помните, что любой человек должен без труда и дополнительных вопросов понять, что изображено на визуализации только по имеющейся на ней информации.
- Оформите выводы к графикам в формате Markdown под самим графиком в отдельной ячейке (в шаблоне они помечены как «ваши выводы здесь»). Если вы хотите красиво оформить 
текстовые вставки, можно воспользоваться следующим ресурсом.

**Что практикуем**
работу с данными и оформление отчетов с помощью средств python

## Результаты
Ноутбук с выполненными заданиями и выводами(https://github.com/AMK01001/Time-series-of-Ghana-s-GDP./blob/main/%D0%92%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5%20%D1%80%D1%8F%D0%B4%D1%8B.%20%D0%A7%D0%B0%D1%81%D1%82%D1%8C%20II.ipynb)

:arrow up:[к оглавлению]https://github.com/AMK01001/Time-series-of-Ghana-s-GDP.?tab=readme-ov-file#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%B5%D0%BD%D0%B8%D0%B5()
