### Задание

Необходимо решить задачу предсказания обнаружения присутствия людей в помещении.
Задача решается в рамках платформы онлайн-конкурсов по машинному обучению TrainMyData. [Ссылка на задание](https://trainmydata.com/c/occupancy_detection)

##### 1. Провести предподготовку данных
(Обязательно) Здесь можно использовать отличный туториал, предоставляемый [на сайте](https://trainmydata.com/c/occupancy_detection/discussions/page/2533274790395907).
При защите нужно уметь отвечать на все вопросы, связанные с кодом.

Результатом выполнения этого пункта является блок ячеек или скрипт предобработки данных

##### 2. Обучить модель из sklearn
Следующим шагом необходимо обучить модель логистической регрессии.
Для этого нужно использовать класс [LogisticRegression](http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html) из sklearn.

Получить предсказания модели на валидационной части выборки.
Оценить результат по метрике [Accuracy](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html).

##### 3. Реализовать логистическую регрессию самостоятельно
На этом шаге необходимо реализовать модель логистической регрессии, используя python самостоятельно.
Для начала можно реализовать не векторный вариант. То есть при обучении все параметры обновлять в цикле.
Этот пункт можно пропустить и переходить сразу к векторному виду, но ТОЛЬКО, если вы понимаете, как делать.

##### 4. Реализовать логистическую регрессию в векторном виде
Преобразовать код из пункта 3 в векторный формат. То есть обновление всех параметров должно происходить одновременно без циклов.
Проверить, что ваш результат совпадает с результатом модели из scikit-learn.

###### * Студент, получивший максимальное место на MLBootCamp среди участников из своей группы получает автомат за весь курс.
