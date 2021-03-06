### Задание

Необходимо решить задачу распознавания рукописных цифр (датасет MNIST).
Задача решается в рамках платформы онлайн-конкурсов по машинному обучению Kaggle. [Ссылка на задание](https://www.kaggle.com/c/digit-recognizer).

##### 1. Провести предподготовку данных
В задаче каждая фотография рукописной цифры задана в виде строки из 784 (28x28) значений градации серого для каждого пикселя.
Градация от 0 до 255 (0 - белый, 255 - черный). 
Необходимо отнормировать значения для каждой картинки и получить train и validation датасеты. 

##### 2. Обучить логистическую регрессиию на scikit-learn
Здесь нужно получить модель логистической регресии и вычислить точность предсказания на валидационном датасете.
Точность должна быть ~91%.

##### 3. Создать модель многослойной нейронной сети в keras 
Используя библиотеку для глубокого обучения keras.io необходимо создать нейронную сеть из нескольких слоев.
Изучить возможности библиотеки, уметь отвечать на вопросы про Dense слои, методы активации, размерности входных/выходных матриц, метод compile и fit.
Провести сравнение с логистической регрессией.

##### 4. Построить графики обучения и сделать несколько архитектурных вариаций сети
Собрать историю обучения сети (см. выход функции fit) и построить график обучения (уменьшения loss на каждой итерации).
Сделать несколько вариаций архитектуры сети

##### 5. Провести эксперименты со своими рукописными цифрами
В любом графическом редакторе нарисовать набор из 10-20 цифр необходимого размера (28х28), сохранить в папке.
Реализовать функцию, которая считывает все файлы из папки и преобразует в вектор.
Прогнать нарисованные цифры через полученную на предыдущем этапе лучшую нейронную сеть и подсчитать % ошибок.

###### * Студент, получивший максимальное место на kaggle среди участников из своей группы получает автомат за весь курс.

_Базовый пример реализации приведен в ноутбуке example._