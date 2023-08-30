# Соревнование по структуризации чеков ОФД

## Описание проекта

Данные чеков ОФД содержат детальную информацию о тратах клиентов. Они помогают улучшать качество моделей кредитного скоринга и склонности к банковским продуктам, а также улучшать пользовательский опыт за счет структуризации трат клиентов в мобильном приложении. Однако работа с этим источником затрудняется его неструктурированностью: вся информация о купленном товаре лежит в одной строке произвольного формата.

В предположении что каждая чековая позиция описывает какой-либо товар, наименование этого товара, а также его бренд, являются главной информацией, которую можно извлечь из чека. По итогу задача структуризации этих данных ограничивается выделением и нормализацией брендов и товаров.

## Инструменты:

`Python==3.9.16`
`Pandas==1.5.3`
`sklearn==1.2.2`
`gensim==4.3.0`
`pytorch_lightning==2.0.3`
`seqeval==1.2.2`
`torch==2.0.1+cu118`

## Описание данных:

- text — текст комментария
- toxic — целевая переменная (токсичен комментарий или нет)

## Краткое описание проведённой работы:
<i> 
Текст очищен от посторонних символом , проведена лематизация , 2 разные токенизации (встроенная в keras и Tfidf) и удалены стоп-слова .Убран дисбаланс классов, Построены модели на основе Keras и Catboost (c cross validation)</i>

## Выводы
<i>В процессе экспериментов с различными архитектурами моделей были проведены тщательные исследования, направленные на выбор оптимального решения. В конечном итоге, была определена лучшая архитектура, которая продемонстрировала наилучшую производительность в классификации комментариев на позитивные и негативные. 

В целом, результаты экспериментов и выбор оптимальной модели свидетельствуют о том, что проект успешно решает задачу автоматической модерации и будет способствовать повышению качества взаимодействия пользователей с описаниями товаров в интернет-магазине «Викишоп».</i>

## Рекомендации
<i>Используйте данные, собранные в процессе работы системы модерации, для анализа трендов в токсичности, популярных слов и выражений. Это может помочь в дальнейшем улучшении модели.
</i>

---

#### Если проект не открывается или вы хотите посмотреть со всеми интерактивными ячейками(plotly,ydata-profiling), его можно открыть по ссылке: <a href='https://nbviewer.org/github/verydirtyhands/toxic_comments/blob/main/p12f.ipynb'>Токсичные комментарии в интернет-магазине «Викишоп»</a>
