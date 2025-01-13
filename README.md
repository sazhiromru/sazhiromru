<h1 align="center">Привет, я <a href="https://github.com/sazhiromru">Романов Георгий</a> 👋</h1>

<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaGJuc2J1YjExMm9jdDF4bGhkaGF3ZGg0bXkyYzRvdDQ3c25qYXk3biZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4k9BkIfSbgr2LTRB8P/giphy.gif" width="180"/>
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdnFxY2hibGhhZHRoZGpoeTZocnhneWxjM2h0ZXFjNXVxYmQzd3k3OSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/ySeD2PB1OfMSKFEheH/giphy.gif" width="180"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Инженер%20данных-FFD43B?style=for-the-badge&logo=python&logoColor=blue" alt="Бейдж Инженера данных">
  <img src="https://img.shields.io/badge/Бизнес%20аналитик-323330?style=for-the-badge&logo=soundcharts&logoColor=white" alt="Бейдж Бизнес-аналитика">
</p>

---

## 📋 Содержание

- [🔥 Комплексные ETL проекты](#etl)
  - [💰 Betting analyzer (*Python: BeautifulSoup, Selenium, Pandas, NumPy → GoogleCloud  → Airflow, Redis → Kafka → ClickHouse → Grafana)*](#betting)
  - [🎮 Steam Scraper (*Python: BeautifulSoup, Selenium, Pandas, NumPy → AWS → PostgreSQL → Metabase)*](#steam-scraper)
- [📈 Небольшие проекты](#small)
  - [📊 Дэшборд - ключевые показатели эффективности производства нефтехимического холдинга (*SQL - PowerBI*)](#dashboard-production)
  - [🏆 Kaggle competition - Child Mind - (*Python:Pandas, SNS, matplotlib, LGBM*)](#kaggle)
- [🎓 Обо мне](#about-section)
- [🛠️ Навыки](#skills-section)
- [💼 Опыт работы](#experience-section)
- [📬 Контакты](#contacts-section)

---
<br>

<a id="ETL"></a>
## 🔥 Комплексные ETL проекты
---
<a id="betting"></a>
### 💰 Betting analyzer

---
![Диаграмма проекта](https://raw.githubusercontent.com/sazhiromru/images/refs/heads/main/mermaid-diagram-2025-01-08-082426.svg)

---
#### 🎯 Цель проекта
Система синхронно сопоставляет лайв-коэффиценты на трех крупнейших букмекерских сайтах и анализирует лучшие ставки. 



#### 🔍 Проблемы и решения
- **Ограничения площадок**: Площадки защищены от скрапинга и автоматизированных действий. Есть авторизация. 
- **Ограниченные ресурсы**: Сервер с 1 GB памяти требует оптимизации кода, снижения количества I/O операций и эффективного управления памятью.
- **Анализ данных**: Данные должны сниматься синхронно, что требует наличие координатора и системы работы с ошибками/задержками. 


#### 🔧 Реализация
1. Формируется список потенциальных сделок на основе разницы цен между площадками.
2. Для каждого предмета из списка собирается история продаж (цены и даты).
3. Рекомендации ранжируются по формуле, учитывающей прибыль, достоверность данных и потенциальную скорость продажи.


#### 🛠️ Технологии
- **Язык**: Python  
- **База данных**: PostgreSQL  
- **Инфраструктура**: AWS, автоматизация BASH, тестирование и отладка среды - Docker  
- **Визуализация**: Metabase  


#### 📊 Ссылка на дашборд
Доступен с 08:00 до 20:00 CET:  
[Дашборд Grafana](Скоро тут появится ссылка)  

  


| **Функция**         | **Описание**                                                                 | **Технологии**                             
|---------------------------|------------------------------------------------------------------------------|--------------------------------------|
| [**Сбор данных**](https://github.com/sazhiromru/scraper/blob/main/README.md#scraping-section)           | Сбор данных с трех веб-сайтов и сохранение в формате CSV.                   | Python, Selenium, Beautiful Soup, Pandas, re |
| [**Обработка данных**](https://github.com/sazhiromru/scraper/blob/main/README.md#wrangling-section)      | Очистка и анализ данных, нахождение выгодных сделок, проверка истории продаж для 150 лучших предметов, верификация данных, формирование итогового списка рекомендаций. Удаление устаревших файлов | Pandas, NumPy, Selenium, Beautiful Soup, re |   
| [**SQL**](https://github.com/sazhiromru/scraper/blob/main/README.md#SQL-section)                   | Создание базы данных, подключение через bastion-сервер, сохранение данных с использованием psycopg2, периодическая очистка устаревших записей. | PostgreSQL, AWS, Python, psycopg2 |
| [**AWS**](https://github.com/sazhiromru/scraper/blob/main/README.md#AWS-section)                   | Настройка инфраструктуры: создание VPC, EC2, RDS PostgreSQL, S3, CloudWatch, IAM, интеграция компонентов, настройка security group. | VPC, EC2, S3, CloudWatch, IAM  |
| [**Docker**](https://github.com/sazhiromru/scraper/blob/main/README.md#Docker-section)                | Создание контейнера для запуска Google Chrome на EC2.                       | Docker                               |
| [**Bash**](https://github.com/sazhiromru/scraper/blob/main/README.md#bash-section)                  | Автоматизация процессов на EC2 с помощью Bash-скриптов.                     | Bash                                |
| [**Metabase**](https://github.com/sazhiromru/scraper/blob/main/README.md#Metabase-section)               | Подключение к базе данных через bastion-сервер, создание интерактивного дашборда. | Metabase                            |

---
<br>
<a id="steam-scraper"></a>
### 🎮 Steam Scraper

---
![Диаграмма проекта](https://raw.githubusercontent.com/sazhiromru/images/969a0f40bed959fac421447a24223250edea6b76/steam-diagram.svg)

---
#### 🎯 Цель проекта
Автоматизация поиска наиболее выгодных сделок на торговых площадках market-csgo, buff и c5game.  
Система собирает все предложения о покупке и продаже предметов с трех сайтов, и находит лучшие сделки.



#### 🔍 Проблемы и решения
- **Ограничения площадок**: Площадки защищены от скрапинга; Buff требует авторизации; Предметов более 40000.
- **Ограниченные ресурсы**: Сервер с 1 GB памяти требует оптимизации кода, снижения количества I/O операций и эффективного управления памятью.
- **Анализ данных**: Волатильность цен и большое количество экстремальных значений, искажающих картину, требуют учета статистики продаж и уровня спроса.


#### 🔧 Реализация
1. Формируется список потенциальных сделок на основе разницы цен между площадками.
2. Для каждого предмета из списка собирается история продаж (цены и даты).
3. Рекомендации ранжируются по формуле, учитывающей прибыль, достоверность данных и потенциальную скорость продажи.


#### 🛠️ Технологии
- **Язык**: Python  
- **База данных**: PostgreSQL  
- **Инфраструктура**: AWS, автоматизация BASH, тестирование и отладка среды - Docker  
- **Визуализация**: Metabase  


#### 📊 Ссылка на дашборд
Доступен с 08:00 до 20:00 CET:  
[Дашборд Metabase](http://47.129.223.184:3000/public/dashboard/1a51169a-8c3c-4d9e-8ee7-a508fb3f7539?date=2024-12-10)  

  


| **Функция**         | **Описание**                                                                 | **Технологии**                             
|---------------------------|------------------------------------------------------------------------------|--------------------------------------|
| [**Сбор данных**](https://github.com/sazhiromru/scraper/blob/main/README.md#scraping-section)           | Сбор данных с трех веб-сайтов и сохранение в формате CSV.                   | Python, Selenium, Beautiful Soup, Pandas, re |
| [**Обработка данных**](https://github.com/sazhiromru/scraper/blob/main/README.md#wrangling-section)      | Очистка и анализ данных, нахождение выгодных сделок, проверка истории продаж для 150 лучших предметов, верификация данных, формирование итогового списка рекомендаций. Удаление устаревших файлов | Pandas, NumPy, Selenium, Beautiful Soup, re |   
| [**SQL**](https://github.com/sazhiromru/scraper/blob/main/README.md#SQL-section)                   | Создание базы данных, подключение через bastion-сервер, сохранение данных с использованием psycopg2, периодическая очистка устаревших записей. | PostgreSQL, AWS, Python, psycopg2 |
| [**AWS**](https://github.com/sazhiromru/scraper/blob/main/README.md#AWS-section)                   | Настройка инфраструктуры: создание VPC, EC2, RDS PostgreSQL, S3, CloudWatch, IAM, интеграция компонентов, настройка security group. | VPC, EC2, S3, CloudWatch, IAM  |
| [**Docker**](https://github.com/sazhiromru/scraper/blob/main/README.md#Docker-section)                | Создание контейнера для запуска Google Chrome на EC2.                       | Docker                               |
| [**Bash**](https://github.com/sazhiromru/scraper/blob/main/README.md#bash-section)                  | Автоматизация процессов на EC2 с помощью Bash-скриптов.                     | Bash                                |
| [**Metabase**](https://github.com/sazhiromru/scraper/blob/main/README.md#Metabase-section)               | Подключение к базе данных через bastion-сервер, создание интерактивного дашборда. | Metabase                            |

---
<br>

<a id="small"></a>
## 📈 Небольшие проекты

---

<a id="dashboard-production"></a>
### 📊 Дэшборд - ключевые показатели эффективности производства нефтехимического холдинга

#### 📊 Описание дэшборда

Данный дэшборд объединяет данные из трех источников:

1. **Факт производства** — выгрузка из SAP.
2. **Изначальный план** — данные на первое число месяца.
3. **Обновленный план** — данные на текущую дату.

Для шести заводов планы сохраняются в шести отдельных Excel-файлах, а факт производства из SAP сохраняется в седьмом файле.

#### Функционал Дэшборда

**Текущая дата**
- **Отображение фактических показателей производства.**
- **Разница**: рассчитывается как `План - Факт` и отображается на графике.

 **Конец месяца**
- **Суммарный факт**: отображает данные с 1-го числа до текущей даты.
- **Обновленный план**: включает данные на оставшуюся часть месяца.
- **Разница до конца месяца**: показывает изменения в плане, сделанные в течение месяца.

#### Преимущества
Этот дэшборд позволяет:
1. **Мониторить фактические показатели производства.**
2. **Оперативно анализировать обновленные прогнозы** ключевых марок продукции на конец месяца.
3. **Выявлять отклонения от изначального плана** и анализировать их причины.


<div align="center">
    <img src="https://raw.githubusercontent.com/sazhiromru/images/main/DB1.PNG" alt="Внешний вид дэшборда" width="100%" />
    <img src="https://raw.githubusercontent.com/sazhiromru/images/main/db2.PNG" alt="Внешний вид дэшборда" width="100%" />
    <img src="https://raw.githubusercontent.com/sazhiromru/images/main/db3.PNG" alt="Внешний вид дэшборда" width="100%" />
</div>  

<a id="kaggle"></a>
### 🏆 Kaggle competition - Child Mind - Pandas, SNS, matplotlib, LGBM 

**Задача**: Предсказать, у каких детей и подростков может быть проблемное использование интернета.

**Данные**: Анонимные опросные данные с демографической, психологической и поведенческой информацией, позволяющие понять связь между различными факторами и склонностью к проблемному интернет-поведению.  

**Супер простое описание**:  
Есть данные по 4 тысячам детей по их успеваемости, оценкам по физкультуре, весу/росту, успехах в различных спортивных метриках, BMI и так далее. Для примерно девятиста детей есть так же данные акселерометра, что совсем бесполезно на мой взгляд (данные есть по 29% детей, для тестового датасета вообще 2 из 30 - 6%). По этим характеристикам надо предсказать уровень SII - оценка того, насколько ребенок зависим от интернета и насколько он негативно влияет на его жизнь.  

**Идея**  
Аналитики пытаются предсказать sii - целевую категорийную величина. Я попытаюсь предсказать PCIAT-TOTAL - результат прохождения опросника, на основании которого присуждается sii. Он не дискретен, работает по следующей формуле:
1. От 0 до 20 быллов - 0 категория зависимости
2. От 21 до 40 - 1 категория зависимости и.т.д
   Т.к эта величина не дискретная, в отличие от sii, прогноз теоретически должен быть точнее

**Результат**  
Data scientist в ближайшее время из меня не выйдет. Результат - 0.38, при диапазоне в первой тысяче до 0.4 до 0.5.
Ссылка на блокнот Kaggle: https://www.kaggle.com/code/georgiiromanov/child-mind-final
<details>
  <summary><strong>📜 Код Kaggle</strong></summary>

```python
  
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import LabelEncoder
import numpy as np 
import pandas as pd 
import os
from sklearn.impute import KNNImputer 

count = 0
for dirname, _, filenames in os.walk('/kaggle/input'):
    for filename in filenames:
        print(os.path.join(dirname, filename))
        count +=1
        if count >= 15:
            break
    if count >= 15:
        break
        
data_train = pd.read_csv(r'/kaggle/input/child-mind-institute-problematic-internet-use/train.csv')
data_test = pd.read_csv('/kaggle/input/child-mind-institute-problematic-internet-use/test.csv')
data_train.head()

# убираем нулевые значения искомой метрики, строим график распределения по значениям


filtered_data = data_train[data_train['sii'].notna()].reset_index()

sns.countplot(data = filtered_data, x = 'sii')

plt.title('Распределение Sii')
plt.xlabel('Значение Sii')
plt.ylabel('Количество')
plt.show()

# распределение по полу и возрасту
sns.countplot(data = filtered_data, x = 'Basic_Demos-Age', hue = 'Basic_Demos-Sex' )

plt.title('Age/Sex распределение')
plt.xlabel('количетсво')
plt.legend(['мужской','женский'], title = 'Пол')
plt.show()

# еще распределие, со стакнутыми колонками
pivot_table = filtered_data.pivot_table(index = 'Basic_Demos-Age', columns = 'Basic_Demos-Sex', aggfunc = 'size',fill_value = 0)
pivot_table.head()

pivot_table.plot(kind = 'bar', stacked = True)
plt.title('Еще распредение для наглядности')
plt.legend(['мужской', 'женский'], title ='пол')
plt.tight_layout()
plt.show()

#Убираем колонки, которых нет в тестовом дата сете, кроме целевой
columns_to_drop = [col for col in data_train.columns if col not in data_test.columns]
print(columns_to_drop)
columns_to_drop.remove('PCIAT-PCIAT_Total')
filtered_data.drop(columns = columns_to_drop, inplace = True)

# строим график, где смотрим распределение по нулевым значениям оставшихся колонок. здесь в итоге выбираем целевые 35%
graph = filtered_data.isnull().sum().apply(lambda x: x/len(filtered_data['PCIAT-PCIAT_Total'])*100).sort_values(ascending = False)
graph.plot(kind = 'barh', figsize = (20,30))
plt.gca().yaxis.set_tick_params(labelsize=18, pad=5)
plt.tight_layout()
plt.gca().grid()
ticks = [x*5 for x in range(1,21)]
plt.gca().xaxis.set_ticks(ticks)

# удаляем столбцы с более 35% NaN
indexes_to_delete = graph.index[graph > 35].tolist()
filtered_data.drop(columns = indexes_to_delete, inplace = True)

# так же убираем ID т к решили не использовать данные акселерометра
columns_to_drop_2 = ['index','id']
filtered_data.drop(columns = columns_to_drop_2, inplace = True)

# преобразуем категорийные столбцы в числовые. В основном это времена года когда проводились тесты
column_to_label = filtered_data.select_dtypes(include = 'object').columns

labeled_data = filtered_data.copy()
label_coder = LabelEncoder()
for col in column_to_label:
    labeled_data[f'{col}'] = label_coder.fit_transform(labeled_data[f'{col}'])

# строим матрицу в sns, анализируем на глаз, выбираем число 70%, убираем колонки с большей кореляцией(в основном это различные показатели массы и состава тела)
matrix = labeled_data.corr()
plt.figure(figsize=(40, 40))
sns.heatmap(matrix, annot=True, cmap='coolwarm', linewidths=0.5, fmt='.2f', vmin=-1, vmax=1)

limit = 0.7

drop_columns_3 = set()
for i in range(len(matrix.columns)):
    for j in range(i):
        if abs(matrix.iloc[i, j]) > limit:
            col = matrix.columns[i]
            drop_columns_3.add(col)

drop_columns_3.discard('PCIAT-PCIAT_Total')

cleaned_data = labeled_data.drop(columns=drop_columns_3)



imputers = {}
imputed_dataset = {}

imputers = KNNImputer(n_neighbors=17)
    
imputed_dataset = pd.DataFrame(
    imputers.fit_transform(cleaned_data), 
    columns=cleaned_data.columns)

#Создаем модель, подбираем значения
    
from sklearn.model_selection import train_test_split, RandomizedSearchCV
from sklearn.metrics import mean_squared_error
import lightgbm as lgb
import pandas as pd
import numpy as np

SEED = 42

# Ensure imputed_dataset is defined
# imputed_dataset = ...

X = imputed_dataset.drop(columns=['PCIAT-PCIAT_Total'])  # your target column name
y = imputed_dataset['PCIAT-PCIAT_Total']

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=SEED)
'''
# Parameter grid (potentially smaller)
param_grid = {
    'learning_rate': [0.01, 0.03, 0.05, 0.1],
    'max_depth': [6, 8, 10, 12, 14],
    'num_leaves': [500],
    'min_data_in_leaf': [5, 10, 20, 50],
    'feature_fraction': [0.6, 0.8, 1.0],
    'bagging_fraction': [0.6, 0.8, 0.9],
    'bagging_freq': [1, 3, 5],
    'lambda_l1': [4.735462555910575],
    'lambda_l2': [4.735028557007343e-06],
}

model = lgb.LGBMRegressor(random_state=42, verbose=-1)

search = RandomizedSearchCV(
    estimator=model,
    param_distributions=param_grid,
    n_iter=3000,
    scoring='neg_mean_squared_error',
    cv=5,
    random_state=42,
    verbose=1
)

search.fit(X_train, y_train)
print("Best Parameters:", search.best_params_)
print(f"Best RMSE: {(-search.best_score_)**0.5:.4f}")
# Parameter grid (potentially smaller)
param_grid = {
    'learning_rate': [0.05],  
    'max_depth': [4, 6],
    'num_leaves': [200, 300, 400, 500],
    'min_data_in_leaf': [10],  
    'feature_fraction': [0.4, 0.5, 0.6],
    'bagging_fraction': [0.9],
    'bagging_freq': [3],  
    'lambda_l1': [1, 2, 3, 4, 4.735462555910575],
    'lambda_l2': [3e-05, 3e-04, 4.735028557007343e-06],
}


model = lgb.LGBMRegressor(random_state=42, verbose=-1)

search = RandomizedSearchCV(
    estimator=model,
    param_distributions=param_grid,
    n_iter=10,
    scoring='neg_mean_squared_error',
    cv=5,
    random_state=42,
    verbose=1
)

search.fit(X_train, y_train)
print("Best Parameters:", search.best_params_)
print(f"Best RMSE: {(-search.best_score_)**0.5:.4f}")
best_model = search.best_estimator_
columns_final = list(imputed_dataset.columns)
columns_final.remove('PCIAT-PCIAT_Total')
X_test = data_test[columns_final]

# Select columns with object (categorical) data type
column_to_label_2 = X_test.select_dtypes(include='object').columns

# Transform categorical columns using label_coder
for col in column_to_label_2:
    X_test.loc[:, col] = label_coder.fit_transform(X_test[col])

X_final_test = pd.DataFrame(
    imputers.fit_transform(X_test), 
    columns=X_test.columns)

y_pred = best_model.predict(X_final_test)
X_final_test['PCIAT_TOTAL'] = y_pred
X_final_test['sii'] = np.where(X_final_test['PCIAT_TOTAL']<21,0,
                              np.where(X_final_test['PCIAT_TOTAL']<31,1,2))
X_final_test['id'] = data_test['id']
X_final_test[['id','sii']].to_csv('submission.csv', index=False,na_rep='null')

```

</details>
<br></br>

<a id="about-section"></a>
## 💼 Опыт работы и достижения

- 🏢 **11 лет опыта работы в нефтехимической отрасли**  
  - Управление цепочками поставок, бизнес- и дата-аналитика в одной из крупнейших нефтехимических компаний России.  

- 🎓 **Выпускник MBA РАНХиГС**  
  - Программа аккредитована **AMBA** и **AACSB**.  

- 🌍 **Стажировка в Deutsche Management Akademie Niedersachsen, Германия**  
  - С практической стажировкой в компании Hansa-Flex.  

- 📊 **IELTS 8.0** (уровень английского: C1)  

- 📜 **IBM Data Engineer Professional Certificate**  

- ☁️ **AWS Certified Cloud Practitioner**


---
<br>

<a id="skills-section"></a>
## 🛠️ Навыки

### 👨‍💻 Программирование и скрипты
- **Python (Pandas, NumPy, Matplotlib, SKlearn, Seaborn, Selenium, BeautifulSoup, re )**
- **SQL**

### 📊 Инструменты визуализации данных
- **Power BI**
- **Metabase**
- **Grafana**

### 🗄️ Базы данных
- **PostgreSQL**
- **MySQL**
- **ClickHouse**

### ☁️ Облако и другие технологии
- **AWS Cloud Practitioner**
- **Docker**
- **Airflow**
- **Kafka**
- **Redis**

---
<br>

<a id="experience-section"></a>
## 💼 Опыт работы

### СИБУР, Москва  
**Бизнес-аналитик** (2021–2023)  
- Разработка аналитических отчетов для управления цепями поставок и базовых полимеров.  
- Анализ товарных потоков, эффективности продаж и хранения.  
- Управление рисками переполнения складов, контроль логистических ограничений.

**Главный эксперт, управление цепями поставок** (2017–2021)  
- Разработал полуавтоматическую систему расчета материальных потоков (SAP, SQL, Power Query) для 21 склада с оборотом более 1 млн тонн продукции в месяц.  
- Руководил запуском производства диоктилтерефталата в Перми, включая управление сырьевыми ресурсами и планирование распределения продукции.  
- Оптимизировал уровень запасов и ежедневное планирование отгрузок для ПЭТ-заводов.

**Начальник службы эксплуатации** (2012–2017)  
- Руководил ремонтом и обслуживанием магистральных продуктопроводов.  
- Управлял командой из 100+ сотрудников, обеспечивал соответствие нормативным требованиям.  
- Продвинулся с позиции слесаря до начальника отдела.  

**Ключевые достижения**:  
- Участвовал в разработке системы управления цепями поставок для запуска крупнейшего завода полимеров в России (ЗСНХ).  
- Внёс вклад в проектирование архитектуры баз данных и систем управления спросом и операциями.  

 
  <br>

<a id="contacts-section"></a>
  ## 📬 Контакты

<p align="left">
  <a href="https://t.me/poi8lkj" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>
  <a href="https://linkedin.com/in/ваш_профиль" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
</p>
