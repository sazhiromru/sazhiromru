<h1 align="center">Привет, я <a href="https://github.com/sazhiromru">Романов Георгий</a> 👋</h1>

<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaGJuc2J1YjExMm9jdDF4bGhkaGF3ZGg0bXkyYzRvdDQ3c25qYXk3biZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4k9BkIfSbgr2LTRB8P/giphy.gif" width="180"/>
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExdnFxY2hibGhhZHRoZGpoeTZocnhneWxjM2h0ZXFjNXVxYmQzd3k3OSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/ySeD2PB1OfMSKFEheH/giphy.gif" width="180"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Инженер%20данных-FFD43B?style=for-the-badge&logo=python&logoColor=blue" alt="Бейдж Аналитика данных">
  <img src="https://img.shields.io/badge/Бизнес%20аналитик-323330?style=for-the-badge&logo=soundcharts&logoColor=white" alt="Бейдж Бизнес-аналитика">
</p>
<br></br>

<div align="center">
  <h1>🔥 Комплексные ETL проекты</h1>
</div>

---

## 🎮 Steam Scraper
---
### 🎯 Цель проекта
Автоматизация поиска наиболее выгодных сделок на торговых площадках market-csgo, buff и c5game.

---

### 🔍 Проблемы и решения
- **Ограничения площадок**: Площадки защищены от скрапинга; Buff требует авторизации; Предметов более 40000 
- **Ограниченные ресурсы**: Сервер с 1 GB памяти требует оптимизации кода, снижения количества I/O операций и эффективного управления памятью.  
- **Анализ данных**: Волатильность цен и большое количество экстремальных значений, искажающих картину, требуют учета статистики продаж и уровня спроса.

---

### 🔧 Реализация
1. Формируется список потенциальных сделок на основе разницы цен между площадками.  
2. Для каждого предмета из списка собирается история продаж (цены и даты).  
3. Рекомендации ранжируются по формуле, учитывающей прибыль, достоверность данных и потенциальную скорость продажи.

---

### 🛠️ Технологии
- **Язык**: Python  
- **База данных**: PostgreSQL  
- **Инфраструктура**: AWS, автоматизация BASH, тестирование и отладка среды - Docker 
- **Визуализация**: Metabase  

---

### 📊 Ссылка на дашборд
Доступен с 08:00 до 20:00 CET:  
[Дашборд Metabase](http://47.129.223.184:3000/public/dashboard/1a51169a-8c3c-4d9e-8ee7-a508fb3f7539?date=2024-12-10)



| **Функция**         | **Описание**                                                                 | **Технологии**                             
|---------------------------|------------------------------------------------------------------------------|--------------------------------------|
| **Сбор данных**           | Сбор данных с трех веб-сайтов и сохранение в формате CSV.                   | Python, Selenium, Beautiful Soup, Pandas, re |
| **Обработка данных**      | Очистка, анализ данных, нахождение выгодных сделок, сбор истории продаж для 150 URL, формирование итогового списка рекомендаций. | Pandas, NumPy, Selenium, Beautiful Soup, re |   
| **SQL**                   | Создание базы данных, подключение через bastion-сервер, сохранение данных с использованием psycopg2, периодическая очистка устаревших записей. | PostgreSQL, AWS, Python, psycopg2 |
| **AWS**                   | Настройка инфраструктуры: создание VPC, EC2, RDS PostgreSQL, S3, CloudWatch, IAM, интеграция компонентов. | VPC, EC2, S3, CloudWatch, IAM  |
| **Docker**                | Создание контейнера для запуска Google Chrome на EC2.                       | Docker                               |
| **Bash**                  | Автоматизация процессов на EC2 с помощью Bash-скриптов.                     | Bash                                |
| **Metabase**              | Подключение к базе данных через bastion-сервер, создание интерактивного дашборда. | Metabase                            |


(https://github.com/sazhiromru/scraper/blob/main/README.md#Metabase)



## 🎓 About Me

- 🎓 **RANEPA MBA Graduate**
- 💼 **Experienced in Supply Chain Management, Business Analysis, and Data Analysis** for the largest petrochemical company in Russia.
- 🏢 **11 years of industry experience**
- 📊 **Passionate about turning data into actionable insights** and driving business decisions.
- 
## 🛠️ Technical Skills

### 👨‍💻 Programming & Scripting
- **Python (Pandas, NumPy, Matplotlib, Seaborn, Selenium, BeautifulSoup, re )**
- **SQL**

### 📊 Data Vizualization Tools
- **Power BI**
- **Metabase**

### 🗄️ Databases
- **PostgreSQL**
- **MySQL**
- - **ClickHouse**

### ☁️ Cloud & Others
- **AWS Cloud Practitioner**
- **Jupyter Notebooks**

---



