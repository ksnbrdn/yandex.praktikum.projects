# Определение наиболее выгодного региона нефтедобычи
Было проведено исследование, чтобы спрогнозировать регион, где добыча нефти принесёт наибольшую прибыль. Надо было проанализировать возможную прибыль и риски техникой Bootstrap с разделением каждого предсказанного значения прибыли по регионам на 1000 выборок. Далее оставить лишь те регионы, в которых вероятность убытков меньше 2.5%. Среди них выбирать регион с наибольшей средней прибылью.  
В ходе работы была выполнена предобработка данных.  
Признаки 'id' удалили, это идентификаторы скважины - не несут ценности для обучения будущей модели. Пропусков и явных дупликатов не нашлось. Все данные выглядят корректно. Нет явно выбивающихся значений. Выявили высокую зависимость показателей объёма запасов нефти от признака f2 для 1 и 3 региона. В регионе 2 мы видим прямую и линейную зависимость целевого показателя 'product' от f2.  
Разобили данные на обучающую и валидационную выборки в соотношении 75:25. Обучили модель и выполнили предсказания на валидационной выборке при помощи линейной регрессии.  
В 1 и 3 регионе средние значение объема в месторождении примерно одинаковые, при этом модели имеют большую погрешность. В 2 регионе средние запасы нефти в месторождениях ниже больше чем в 2 раза, но и погрешность модели значительно ниже.  
Определили, что среднее количество запасов сырья по всем трём регионам недостаточное даже для безубыточной разработки новой скважины.  
Применили технологию bootstrap. По результатам полученных данных мы определили доверительный интревал получения прибыли в 95%, ограничив вероятность убытка величиной менее 2,5%. И на основе этих данных смогли выбрать более перспективный регион для разработки 200 скважин.  
Т.о., мы можем порекоммендовать для дальнейшей разработки регион 2: процент вероятности убытка в данном регионе составит - 0.9% и средняя прибыль выше чем в остальных регионах - 511.36 млн.руб.     

## Использованы библиотеки и методы:
- pandas
- numpy
- scipy
- sklearn
