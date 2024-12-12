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
  - [🎮 Steam Scraper](#steam-scraper)
- [📈 Небольшие проекты](#small)
  - [📊 Дэшборд - ключевые показатели эффективности производства нефтехимического холдинга](#dashboard-production)
- [🎓 Обо мне](#about-section)
- [🛠️ Навыки](#skills-section)
- [💼 Опыт работы](#experience-section)
- [📬 Контакты](#contacts-section)

---
<br>

<a id="ETL"></a>
## 🔥 Комплексные ETL проекты
---
<a id="steam-scraper"></a>
### 🎮 Steam Scraper

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
    <img src="https://raw.githubusercontent.com/sazhiromru/images/main/DB1.PNG" alt="Внешний вид дэшборда" width="30%" />
    <img src="https://raw.githubusercontent.com/sazhiromru/images/main/db2.PNG" alt="Внешний вид дэшборда" width="30%" />
    <img src="https://raw.githubusercontent.com/sazhiromru/images/main/db3.PNG" alt="Внешний вид дэшборда" width="30%" />
</div>






---
<br>

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
- - **Grafana**

### 🗄️ Базы данных
- **PostgreSQL**
- **MySQL**
- **ClickHouse**

### ☁️ Облако и другие технологии
- **AWS Cloud Practitioner**
- **Docker**
- **Airflow**

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
