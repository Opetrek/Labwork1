# Тема лабораторной работы "Создание системы для автоматической диагностики технических неисправностей на основе данных технического обслуживания"

Данный проект посвящен созданию системы для автоматической диагностики технических неисправностей на основе данных технического обслуживания.
В качестве исходных данных используется датасет с соревнования Kaggle [Machine Predictive Maintenance Classification](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification). 

## Используемые Библиотеки и Зависимости

- Python 3.x
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn

## Инструкции по запуску

 Зайти в Kaggle по ссылке ниже.

 [![Colab](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://www.kaggle.com/code/gtrrf2310/fork-of-pred-mach-main-analysis?scriptVersionId=158592354)

 Если по какой-то причине ссылка не работает, в соревновании [Kaggle](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification) в разделе Code мой файл есть в открытом доступе. 
 Имя файла "Fork of Pred-mach-main analysis".

## Цель лабораторной работы

Цель этой лабораторной работы - разработать систему, которая бы прогнозировала технические неисправности на основе данных тех.обслуживания.
Для обучения были взяты данные с конкурса Kaggle.


## Методы и модели, реализованные в коде

Проект включает в себя реализацию нескольких методов и моделей для решения задачи предиктивного обслуживания и диагностики технических неисправностей. В ходе анализа данных и построения моделей мы использовали следующие методы:

1. **Логистическая Регрессия:**
   - Метод линейной классификации, который может быть использован для предсказания бинарных результатов.

2. **Метод Опорных Векторов (SVM):**
   - Мощный метод для классификации, регрессии и детекции выбросов, основанный на поиске оптимальной гиперплоскости разделения между классами.

3. **Дерево Решений и Случайный Лес:**
   - Дерево решений используется для создания структуры решений на основе признаков.
   - Случайный лес - ансамбль деревьев решений, обученных на различных подмножествах данных.

Каждая из этих моделей имеет свои уникальные преимущества и может быть эффективной в определенных сценариях предиктивного обслуживания. 

## Основа Решения

Работа проводилась над таблицей, содержащая следующие данные

![Пример результата модели](https://github.com/Opetrek/Labwork1/blob/main/%D0%A2%D0%B0%D0%B1%D0%BB.%D0%BD%D0%B5%D0%B8%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BD%D0%BE%D1%81%D1%82%D0%B5%D0%B9.png)

В ходе исследования данных и построения моделей для автоматической диагностики технических неисправностей, наши основные шаги включали:

1. **Изучение и предобработка данных:**
   - Анализ и визуализация основных характеристик датасета.
   - Обработка пропущенных значений и удаление лишних признаков.
   - Преобразование данных, включая конвертацию температур из Кельвинов в Цельсии.

2. **Визуальный анализ данных:**
   - Использование графиков и диаграмм для выявления зависимостей между признаками.
   - Рассмотрение распределения и корреляции данных для лучшего понимания взаимосвязей.

3. **Выбор и подготовка моделей:**
   - Реализация различных моделей, таких как логистическая регрессия, метод опорных векторов, дерево решений и случайный лес.
   - Кодирование категориальных признаков и масштабирование данных при необходимости.

4. **Оценка и сравнение моделей:**
   - Оценка моделей на тестовом наборе данных.
   - Сравнение метрик эффективности, таких как точность и матрица ошибок.

В ходе анализа мы также столкнулись с некоторыми данными, которые не имели особого смысла или требовали дополнительного контекста. В таких случаях, мы принимали решение исключить неполные или неинформативные данные.


## Результаты и Выводы

В ходе работы с данными были выявлены некоторые закономерности, как возникновение определенной технической неисправности в зависимости от скорость вращения(Rotation Speed) и крутящего момента(Torque).

![Пример результата модели](https://github.com/Opetrek/Labwork1/blob/main/%D0%9B%D0%B0%D0%B1.%D1%80%D0%B0%D0%B11%20-%20%D0%B7%D0%B0%D0%BA%D0%BE%D0%BD%D0%BE%D0%BC%D0%B5%D1%80%D0%BD%D0%BE%D1%81%D1%82%D1%8C.png)

Данные технических сбоев

![Пример результата модели](https://github.com/Opetrek/Labwork1/blob/main/%D0%9B%D0%B0%D0%B1.%D1%80%D0%B0%D0%B11%20-%20%D1%82%D0%B8%D0%BF%20%D0%BD%D0%B5%D0%B8%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BD%D0%BE%D1%81%D1%82%D0%B5%D0%B9%20%D1%81%D0%BF%D0%B8%D1%81%D0%BE%D0%BA.png)

были преобразованы из текстового типа в численный для удобства обучения модели

![Пример результата модели](https://github.com/Opetrek/Labwork1/blob/main/%D0%9B%D0%B0%D0%B1.%D1%80%D0%B0%D0%B11%20-%20%D1%82%D0%B8%D0%BF%20%D0%BD%D0%B5%D0%B8%D1%81%D0%BF%D1%80%D0%B0%D0%B2%D0%BD%D0%BE%D1%81%D1%82%D0%B5%D0%B9%20%D0%B3%D0%B8%D1%81%D1%82.png)

и затем использованы в качестве критерия, по которому нужно было сделать прогнозирование на основе данных тех. обслуживания. 

Предварительно данные были разделены на обучающую(train) и тестовую(test) части для обучения прогнозирования.
Использовав различные типы обучения на основе данных: LogisticRegression, DecisionTreeClassifier, Random Forest Classifier и SVM , была обучена модель для прогнозирования тех.неисправностей. 

![Пример результата модели](https://github.com/Opetrek/Labwork1/blob/main/%D0%A0%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82%20%D0%BD%D0%B5%D0%B8%D1%81%D0%BF%D1%80%D0%B0%D0%B2..png)

Применив предобученную модель на данных, техническая неисправность в изначальных данных часто совпадает с той тех.неисправностью, которая определяется предобученной моделью.


