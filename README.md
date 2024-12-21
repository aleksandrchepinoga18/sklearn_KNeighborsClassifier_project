# sklearn_KNeighborsClassifier_project

Набор данных получен в результате переписи населения 1994 года и содержит информацию о некотором количестве людей, проживающих в США. Задача состоит в том, чтобы предсказать, зарабатывает человек более $50к в год или нет. Список признаков:

**Age**: Возраст человека.
**Workclass**: Статус занятости.
**fnlwgt**: Это количество людей, которое, по мнению переписи, представляет запись.
**Education**: Высший уровень образования, достигнутый человеком.
**Education-num**: Высший уровень образования, достигнутый человеком в числовой форме.
**Marital-status**: Семейное положение человека.
**Occupation**: Общий род занятий человека.
**Relationship**: Представляет то, кем этот человек является по отношению к другим (перекликается с признаком marital-status).
**Race**: Раса.
**Sex**: Пол.
**Capital-gain**: Прирост капитала.
**Capital-loss**: Убыток капитала.
**Hours-per-week**: Число рабочих часов в неделю.
**Native-country**: Страна происхождения.
**The label**: Отклик — зарабатывает больше $50к или меньше.

### **Библиотеки**

1. **`pandas`**:
   - Для работы с данными в виде таблиц (DataFrame).
   - Методы: `pd.read_csv`, `df.drop`, `df.select_dtypes`, `df.head`, `df.describe`.

2. **`numpy`**:
   - Для работы с массивами и числовыми операциями.
   - Методы: `np.arange`, `np.cumsum`, `np.array`.

3. **`matplotlib.pyplot`**:
   - Для визуализации данных.
   - Методы: `plt.plot`, `plt.scatter`, `plt.xlabel`, `plt.ylabel`, `plt.title`, `plt.grid`, `plt.show`.

4. **`seaborn`** (опционально):
   - Для более сложной визуализации данных.

5. **`sklearn` (scikit-learn)**:
   - Основная библиотека для машинного обучения.
   - Методы:
     - **Предобработка**:
       - `StandardScaler`: стандартизация данных.
       - `MinMaxScaler`: масштабирование данных в диапазон [0, 1].
       - `OneHotEncoder`: кодирование категориальных признаков.
     - **Разделение данных**:
       - `train_test_split`: разделение данных на обучающую и тестовую выборки.
     - **Модели**:
       - `KNeighborsClassifier`: k-ближайших соседей.
       - `RandomForestClassifier`: случайный лес.
     - **Методы поиска параметров**:
       - `GridSearchCV`: поиск оптимальных параметров с использованием перебора.
       - `RandomizedSearchCV`: случайный поиск оптимальных параметров.
     - **Методы уменьшения размерности**:
       - `PCA`: метод главных компонент.
     - **Метрики**:
       - `f1_score`: оценка F1-score.
       - `classification_report`: отчет о классификации.

6. **`xgboost`**:
   - Библиотека для градиентного бустинга.
   - Методы: `xgb.DMatrix`, `xgb.train`.

7. **`lightgbm`**:
   - Библиотека для градиентного бустинга (эффективнее XGBoost).
   - Методы: `lgb.Dataset`, `lgb.train`, `lgb.LGBMClassifier`.

8. **`scipy.stats`**:
   - Для генерации случайных значений в `RandomizedSearchCV`.
   - Методы: `randint`, `uniform`.

9. **`mpl_toolkits.mplot3d`**:
   - Для построения 3D-графиков.
   - Методы: `Axes3D`, `ax.scatter`, `ax.view_init`.

---

### **Методы и техники**

1. **Предобработка данных**:
   - Удаление пропусков.
   - Заполнение пропусков модой.
   - One-hot кодирование категориальных признаков.
   - Стандартизация и масштабирование данных (`StandardScaler`, `MinMaxScaler`).

2. **Разделение данных**:
   - Разделение на обучающую и тестовую выборки (`train_test_split`).

3. **Уменьшение размерности**:
   - Метод главных компонент (PCA).

4. **Модели машинного обучения**:
   - k-ближайших соседей (k-NN).
   - Случайный лес (Random Forest).
   - Градиентный бустинг:
     - XGBoost.
     - LightGBM.

5. **Подбор гиперпараметров**:
   - GridSearchCV.
   - RandomizedSearchCV.

6. **Оценка моделей**:
   - F1-score.
   - Classification report.

7. **Визуализация**:
   - Графики объясненной дисперсии (PCA).
   - 2D и 3D графики распределения данных.
