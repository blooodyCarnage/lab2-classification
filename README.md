# Лабораторная работа №2 — Классификация. Нейронные сети
Выполнил студент: Марченко А.Е. АП-326
## Описание

Исследование методов классификации данных с использованием Scikit-Learn и TensorFlow/Keras.

**Датасет:** Breast Cancer Wisconsin (Diagnostic), доступный через Scikit-Learn.

Набор данных содержит 569 наблюдений, 30 числовых признаков и два класса опухолей.

## Разбиение данных

- Обучающая выборка — 60% (341 наблюдение).
- Валидационная выборка — 20% (114 наблюдений).
- Тестовая выборка — 20% (114 наблюдений).

## Реализованные методы

- Naive Bayes (GaussianNB, MultinomialNB, ComplementNB, BernoulliNB)
- Decision Tree
- Linear Discriminant Analysis
- Support Vector Machines
- k-Nearest Neighbors
- Нейронная сеть TensorFlow/Keras

Проведён подбор гиперпараметров и сравнительный анализ по Accuracy, Precision, Recall, F1-score и ROC-AUC.

## Лучшие результаты

| Модель | Accuracy | F1-score | ROC-AUC |
|---|---:|---:|---:|
| TensorFlow NN | 0.9912 | 0.9880 | 0.9980 |
| SVM | 0.9825 | 0.9756 | 0.9947 |
| LDA | 0.9737 | 0.9630 | 0.9924 |

## Используемые технологии

Python 3.13, NumPy, Pandas, Scikit-Learn, Matplotlib, Seaborn, TensorFlow/Keras, TensorBoard, Jupyter Notebook.

## Запуск проекта

Создать виртуальное окружение:

```powershell
py -3.13 -m venv .venv
```

Установить зависимости:

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Открыть `lab2.ipynb` в VS Code, выбрать Python из `.venv` и выполнить ячейки последовательно.

Для просмотра результатов обучения в TensorBoard после запуска экспериментов:

```powershell
.\.venv\Scripts\tensorboard.exe --logdir logs\tensorboard
```

Открыть `http://localhost:6006`.

## Структура проекта

- `lab2.ipynb` — исходный код и результаты экспериментов.
- `figures/` — графики и визуализации.
- `results/` — результаты экспериментов 
- `requirements.txt` — зависимости проекта.