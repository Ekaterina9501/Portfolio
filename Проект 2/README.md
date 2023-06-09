# Изучение статистики продаж продуктов питания мобильного приложения
Сотрудниками компании был проведен A/A/B-эксперимент на тему смены шрифтов во всём приложении. Пользователей разбили на 3 группы: 2 контрольные со старыми шрифтами и одну экспериментальную — с новыми. Статус проекта (Завершен)
## Данные
В наличии были следующие данные о посещениях сайта:
* название события
* уникальный идентификатор пользователя
* время события
* номер эксперимента
## Задача
На основе данных использования мобильного приложения для продажи продуктов питания проанализировать воронку продаж, а также оценить результаты A/A/B-тестирования 

## Используемые библиотеки
*A/B-тестирование  
Python  
Pandas  
Matplotlib  
Seaborn  
событийная аналитика  
продуктовые метрики  
Plotly  
проверка статистических гипотез  
визуализация данных*
## Выводы
Была изучена воронка продаж данного приложения со всеми процессами и шагами пользователей, их количеством. Было обнаружено, что 1.53% пользователей после установки приложения не попали на главный экран. Скорее всего у некоторых пользователей после скачивания приложение не запускается, поэтому стоит рассмотреть данную проблему и обратиться к разработчикам за поиском причины. Самое популярное событие - показ главного экрана, а самое непопулярное - показ экрана руководства. Также этап Tutorial(экран руководства) не является популярным этапом (840 повторов/ 11.15% пользователей) и не влияет на то, дойдет ли пользователь до финальной покупки или нет. Важным замечанием была потеря большого количества пользователей на 2ом шаге воронки - OffersScreenAppear, то есть данное событие совершает только 61% пользователей от общего количества пользователей совершивших предыдущее событие. Стоит также обратить внимание на данный этап и проработать приложение для поднятия процента перехода, что следовательно даст большую вероятность перехода к покупке того или инного товара. 

Для проверки результатов А/А/В теста провели проверку равенства долей по всем трем группам на каждом эпате воронки. Было принято решение провести проверку между 246 и 247 (А/А) группами, чтобы проверить корректность всех механизмов и расчётов. Далее провести сравнение каждой контрольной группы с эксперементальной и, в заключении, сравнить объединунную группу А(246 + 247) с экспериментальной. По проведенному тестированиям между А/А, А/В и АА/В группами можно сделать вывод, что при уровне значимости alpha = 0.05, нулевая гипотеза не отвергается ни при каких тестах. Доли во всех выборках равны. Различий между контрольными группами и тестовой нет. Следовательно А/В тест можно остановить и текст на сайте менять не нужно.
