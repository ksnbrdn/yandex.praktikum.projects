# Рекомендация тарифов
Оператор мобильной связи выяснил: многие клиенты пользуются архивными тарифами. Они хотят построить систему, способную проанализировать поведение клиентов и предложить пользователям новый тариф: «Смарт» или «Ультра». В распоряжении данные о поведении клиентов, которые уже перешли на эти тарифы.  
Нужно построить модель для задачи классификации, которая выберет подходящий тариф.   
Требуется построить модель с максимально большим значением accuracy. Для проекта надо довести долю правильных ответов по крайней мере до 0.75, а также проверить accuracy на тестовой выборке.  
Каждый объект в наборе данных — это информация о поведении одного пользователя за месяц.       
Были исследованы модели Decision Tree Classifier, RandomForestClassifier и Logistic Regression. Наилучший результат Accuracy - 0.81 - показала модель RandomForestClassifier с гиперпараметрами n_estimators равным - 34 и max_depth равным 10.  
Модель RandomForestClassifier с наилучшими гиперапараметрами была проверена на тестовой выборке и показала результат Accuracy - 0.89.  
Модель RandomForestClassifier была проверена на вменяемость. Для проверки использовалась модель DummyClassifier, которая показала результат Accuracy - 0.68. Наша модель RandomForestClassifier адекватна и эффективна.  

## Использованы библиотеки и методы:
- pandas
- numpy
- seaborn
- sklearn
- tqdm
