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

- [🔥 Комплексные ETL проекты](#комплексные-etl-проекты)
  - [🎮 Steam Scraper](#steam-scraper)
- [📈 Небольшие проекты](#небольшие-проекты)
  - [📊 Дэшборд - ключевые показатели эффективности производства нефтехимического холдинга](#дэшборд---ключевые-показатели-эффективности-производства-нефтехимического-холдинга)
- [🎓 Обо мне](#обо-мне)
- [🛠️ Навыки](#навыки)
- [💼 Опыт работы](#опыт-работы)
- [📬 Контакты](#контакты)

---
<br>

## 🔥 Комплексные ETL проекты

### 🎮 Steam Scraper

---

#### 🎯 Цель проекта
Автоматизация поиска наиболее выгодных сделок на торговых площадках market-csgo, buff и c5game.

---

#### 🔍 Проблемы и решения
- **Ограничения площадок**: Площадки защищены от скрапинга; Buff требует авторизации; Предметов более 40000.
- **Ограниченные ресурсы**: Сервер с 1 GB памяти требует оптимизации кода, снижения количества I/O операций и эффективного управления памятью.
- **Анализ данных**: Волатильность цен и большое количество экстремальных значений, искажающих картину, требуют учета статистики продаж и уровня спроса.

---

#### 🔧 Реализация
1. Формируется список потенциальных сделок на основе разницы цен между площадками.
2. Для каждого предмета из списка собирается история продаж (цены и даты).
3. Рекомендации ранжируются по формуле, учитывающей прибыль, достоверность данных и потенциальную скорость продажи.

---

#### 🛠️ Технологии
- **Язык**: Python  
- **База данных**: PostgreSQL  
- **Инфраструктура**: AWS, автоматизация BASH, тестирование и отладка среды - Docker  
- **Визуализация**: Metabase  

---

#### 📊 Ссылка на дашборд
Доступен с 08:00 до 20:00 CET:  
[Дашборд Metabase](http://47.129.223.184:3000/public/dashboard/1a51169a-8c3c-4d9e-8ee7-a508fb3f7539?date=2024-12-10)

---
| **Функция**         | **Описание**                                                                 | **Технологии**                             
|---------------------------|------------------------------------------------------------------------------|--------------------------------------|
| [**Сбор данных**](https://github.com/sazhiromru/scraper/blob/main/README.md#scraping-section)           | Сбор данных с трех веб-сайтов и сохранение в формате CSV.                   | Python, Selenium, Beautiful Soup, Pandas, re |
| [**Обработка данных**](https://github.com/sazhiromru/scraper/blob/main/README.md#wrangling-section)      | Очистка, анализ данных, нахождение выгодных сделок, сбор истории продаж для 150 URL, формирование итогового списка рекомендаций. | Pandas, NumPy, Selenium, Beautiful Soup, re |   
| [**SQL**](https://github.com/sazhiromru/scraper/blob/main/README.md#SQL-section)                   | Создание базы данных, подключение через bastion-сервер, сохранение данных с использованием psycopg2, периодическая очистка устаревших записей. | PostgreSQL, AWS, Python, psycopg2 |
| [**AWS**](https://github.com/sazhiromru/scraper/blob/main/README.md#AWS-section)                   | Настройка инфраструктуры: создание VPC, EC2, RDS PostgreSQL, S3, CloudWatch, IAM, интеграция компонентов. | VPC, EC2, S3, CloudWatch, IAM  |
| [**Docker**](https://github.com/sazhiromru/scraper/blob/main/README.md#Docker-section)                | Создание контейнера для запуска Google Chrome на EC2.                       | Docker                               |
| [**Bash**](https://github.com/sazhiromru/scraper/blob/main/README.md#bash-section)                  | Автоматизация процессов на EC2 с помощью Bash-скриптов.                     | Bash                                |
| [**Metabase**](https://github.com/sazhiromru/scraper/blob/main/README.md#Metabase-section)               | Подключение к базе данных через bastion-сервер, создание интерактивного дашборда. | Metabase                            |

---
<br>

## 📈 Небольшие проекты

---

### 📊 Дэшборд - ключевые показатели эффективности производства нефтехимического холдинга

---

(Добавьте описание проекта здесь)

---
<br>

## 🎓 Обо мне

- 🎓 **Выпускник MBA РАНХиГС**
- 💼 **Опыт в управлении цепочками поставок, бизнес- и дата-аналитике** в крупнейшей нефтехимической компании России.
- 🏢 **11 лет опыта работы в индустрии**
- 📊 **Увлечен превращением данных в полезные инсайты** и поддержкой принятия бизнес-решений.

---
<br>

## 🛠️ Навыки

### 👨‍💻 Программирование и скрипты
- **Python (Pandas, NumPy, Matplotlib, Seaborn, Selenium, BeautifulSoup, re )**
- **SQL**

### 📊 Инструменты визуализации данных
- **Power BI**
- **Metabase**

### 🗄️ Базы данных
- **PostgreSQL**
- **MySQL**
- **ClickHouse**

### ☁️ Облако и другие технологии
- **AWS Cloud Practitioner**
- **Jupyter Notebooks**

---
<br>

## 💼 Опыт работы

- **Бизнес-аналитик** в крупнейшей нефтехимической компании России  
  - 🗓️ **Период**: 7 лет (2017–2024)  
  - 📊 **Задачи**: Анализ данных, автоматизация бизнес-процессов, внедрение ETL-пайплайнов для повышения эффективности производства.  

- **Аналитик данных**  
  - 🗓️ **Период**: 4 года (2013–2017)  
  - 📈 **Задачи**: Разработка инструментов визуализации, создание отчетности для топ-менеджмента, работа с большими данными.  

- **Стажировка в Германии**  
  - 🗓️ **Период**: 6 месяцев  
  - 🌍 **Описание**: Участие в международном проекте по цифровизации цепочек поставок.
 
  <br>

  ## 📬 Контакты

<p align="left">
  <a href="https://t.me/ваш_телеграм" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>
  <a href="https://linkedin.com/in/ваш_профиль" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
</p>
