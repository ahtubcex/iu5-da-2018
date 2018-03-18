### Задание

Необходимо решить задачу предсказания стоимости дома в зависимости от его характеристик.
Задача решается в рамках платформы онлайн-конкурсов по машинному обучению Kaggle. [Ссылка на задание](https://www.kaggle.com/c/house-prices-advanced-regression-techniques).

##### 1. Провести предподготовку данных
(Обязательно) Необходимо перевести категориальные фичи в числовые, отмасштабировать показатели для лучшей обучаемости модели при необходимости (можно провести эксперименты, как это будет влиять на результаты модели).
Построить графики по распределнию площадей домой и распределнию цен.
Для реализации этой части использовать библиотеки pandas и matplotlib и seaborn.

Необходимо оценить предоставляемые данные, на свое усмотрение предположить несколько возможных зависимостей между признаками и предсказываемыми значениями, проверить гипотезы, построив необходимые графики.

По возможности можно определить, какие признаки являются незначимыми или их доля мала, и объединить такие признаки с другими.

Создать несколько собственных фич на основе своих эвристик и оценить, влияют ли они на качество модели.

Результатом выполнения этого пункта является блок ячеек или скрипт предобработки данных

##### 2. Разделить данные
В этом пункте необходимо поделить данные на обучающую и валидационную выборку.
Для этого можно использовать [train_test_split](http://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html).
Делить можно в соотношениях 70-90 / 30-10 % соответственно.

##### 3. Обучить модель из sklearn
Следующим шагом необходимо обучить модель линейной регрессии.
Для этого нужно использовать класс [LinearRegression](http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html) из sklearn.

Получить предсказания модели на валидационной части выборки.
Оценить результат по метрике [Mean Absolute Error](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error) (MAE) и по метрике, используемой для оценки результатов этого конкурса на [kaggle](https://www.kaggle.com/wiki/RootMeanSquaredLogarithmicError).

##### 4. Реализовать линейную регрессию
На этом шаге необходимо реализовать модель линейной регрессии, используя python самостоятельно.
Для этого изначально можно попробовать написать алгоритм для одного обучаемого параметра, а затем написать реализацию общего случая, используя сначала циклы, а затем векторные вычисления из библиотеку numpy.
Если есть полное понимание, как нужно реализовать алгоритм для множества обучаемых параметров с использованием векторизации вычислений - можно сразу делать так, главное на защите уметь объяснить.

##### 5. Эксперименты с моделью
На этом шаге вы уже имеете базовую модель, которая делает предсказания.
Необходимо прогнать модель на тестовой выборке и отправить решение на kaggle.
После этого можно улучшать свой результат, экспериментируя с подготовкой данных и параметрами модели.
Рекомендуется смотреть т.н. kernel'ы на kaggle - раздел, где участники соревнований выкладывают код со своими идеями и реализациями. Это может быть очень полезно, как для обучения, так и для реализации новых идей.

###### * Студент, получивший максимальное место на kaggle среди участников из своей группы получает автомат за весь курс.

_Базовый пример реализации приведен в ноутбуке example._

##### Заметки
* При прогоне модели из example, где нет нормировок и используются всего 3 фичи, был получен результат в mae ~ 57к и rmsle ~ 0.409.
* При использовании почти всех фич из выборки mae сократилось до 24к, а rmsle до 0.29
* При замене NaN в фичах можно подставлять наиболее частое значение по фиче из выборки
* Использование всех фич без разбора иногда ухудшает результат
* При переводе качественных фич в цифровые значения и нормализации непрерывных величин удобно написать небольшую функцию и применить ее для всех фич.