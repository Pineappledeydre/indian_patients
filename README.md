# Обзор проекта

Данный проект направлен на прогнозирование заболеваний печени на основе медицинских данных. Используются различные алгоритмы машинного обучения для классификации людей как имеющих заболевание печени или нет, на основе нескольких медицинских признаков. Целью является создание эффективной предсказательной модели, которая может помочь медицинским специалистам в диагностике заболеваний печени.

## Требования

Для запуска проекта необходимо установить следующие библиотеки Python:

- **pandas**: Для работы с данными и анализа.
- **numpy**: Для численных вычислений.
- **matplotlib**: Для визуализации данных.
- **seaborn**: Для улучшенной визуализации.
- **scikit-learn**: Для алгоритмов машинного обучения и инструментов.
- **imbalanced-learn**: Для работы с несбалансированными данными (SMOTE для увеличения выборки).
- **xgboost**: Для градиентного бустинга.

Для установки всех необходимых зависимостей проекта вы можете использовать файл `requirements.txt`. Для этого выполните следующую команду:

```bash
pip install -r requirements.txt
```

## Данные

В проекте используется набор данных, содержащий медицинские признаки, такие как:

- Возраст
- Пол
- Уровень билирубина
- Уровень альбумина
- Уровень щелочной фосфатазы
- Уровень SGOT (АСТ)
- Уровень SGPT (АЛТ)
- Уровень общего белка
- Протромбиновое время
- и другие...

Целевая переменная — наличие заболевания печени (бинарная классификация: 0 — нет заболевания, 1 — есть заболевание печени).

## Шаги для запуска проекта

1. **Загрузка данных:** Загрузите набор данных о заболеваниях печени с помощью pandas и ознакомьтесь с ним.

    ```python
    import pandas as pd
    df = pd.read_csv('liver_disease.csv')
    ```

2. **Предобработка данных:** Для корректной работы модели важно провести обработку данных (удаление пропусков, нормализация, балансировка данных и т.д.).

3. **Обучение моделей:** В проекте использовались различные модели машинного обучения, такие как:

   - DecisionTreeClassifier
   - RandomForestClassifier
   - XGBClassifier
   - KNeighborsClassifier
   - MLPClassifier

4. **Оценка модели:** Модели были оценены на тестовых данных. Результаты классификации для каждой модели представлены с использованием следующих метрик:

   - **Точность (Accuracy):** Доля правильных предсказаний.
   - **Полнота (Recall):** Способность модели правильно выявлять случаи заболевания печени.
   - **Точность (Precision):** Способность модели правильно классифицировать положительные случаи.
   - **F1-оценка:** Баланс между точностью и полнотой.
   - **ROC-AUC:** Площадь под кривой ROC.

5. **Настройка гиперпараметров:** Для улучшения качества моделей был применен поиск по сетке (GridSearchCV) и случайный поиск (RandomizedSearchCV) для оптимизации гиперпараметров.

## Заключение

Проект продемонстрировал возможности машинного обучения для предсказания заболеваний печени. Было протестировано несколько моделей, и результаты показали, что ансамблевые методы, такие как случайный лес и XGBoost, превосходят отдельные классификаторы по точности и другим метрикам.

## Перспективы

Будущие улучшения могут включать:

- Сбор большего количества медицинских данных для улучшения обобщающих способностей моделей.
- Использование более сложных моделей, таких как нейронные сети.
- Применение более продвинутых методов обработки несбалансированных данных.

## Как запустить

1. Клонируйте репозиторий:

    ```bash
    git clone <your_repository_link>
    cd <your_project_directory>
    ```

2. Установите зависимости:

    ```bash
    pip install -r requirements.txt
    ```

3. Запустите Jupyter Notebook или Python-скрипт для анализа данных и обучения моделей:

    ```bash
    jupyter notebook
    ```
