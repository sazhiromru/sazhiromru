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
Сбор, обработка и анализа данных с площадок market-csgo, buff163 и c5game.
Цель - создание 

### 🔍 Проблемы и подходы к их решению
Площадки защищены от скрапинга и алгоритмизации действий.  

Buff требует авторизацию.  

Проект работает на вычислительной мощности в 1 GB, что критически мало для Google Chrome, требует оптимизации кода, управление памятью и снижения количества I/O операций.

Так же, вследствии волантильности цен и большого количества аутлайнеров, при создании рекомендаций необходимо учитывать не только разницу цен, но и статистику продаж и уровень спроса.
Упрощенно, реализован следующий алгоритм:
1) По разнице цен между площадками формируется лист потенциальных сделок.
2) Для каждого предмета из этого листа формируются отдельные ссылки, по ним извлекаются история продаж с ценами и датами.
3) Итоговый лист рекомендаций ранжируется по особой формуле, которая учитывает разницу цен(потеницильную прибыль), достоверность данных (сравнение с ценами предыдущих сделок) и скорость продажи (частота сделок)

Проект написан на Python, БД - PostgreSQL, сервер AWS, автоматизация BASH, визуализирован в Metabase.
Доступен по ссылке c 08 до 20 CET TIME: 
http://47.129.223.184:3000/public/dashboard/1a51169a-8c3c-4d9e-8ee7-a508fb3f7539?date=2024-12-10



| **Этап/Функция**         | **Описание**                                                       | **Технологии**              | **Ссылка**                |
|---------------------------|--------------------------------------------------------------------|-----------------------------|---------------------------|
| **Сбор данных (Скрапинг)** | Сбор данных с трех веб-сайтов, сохранение в формате CSV.          | Python, Selenium            | [Код для скрапинга](#)    |
| **Обработка данных**      | Очистка, преобразование данных, вычисление новых столбцов.        | Pandas, NumPy               | [Код обработки](#)        |
| **Загрузка в базу данных**| Сохранение обработанных данных в SQL-базу данных.                 | SQL, SQLite, Python         | [Код загрузки](#)         |
| **Визуализация данных**   | Создание интерактивного дашборда с использованием Power BI.       | Power BI, SQL               | [Дашборд Power BI](#)     |





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



