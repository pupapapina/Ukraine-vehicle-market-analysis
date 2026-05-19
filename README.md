# Ukraine-vehicle-market-analysis
Comprehensive analysis of the Ukrainian car market (2024) using open government Big Data. This project showcases a full Data Analyst workflow: exploratory data analysis (Python/Pandas), relational database design (PostgreSQL), and interactive Power BI dashboards for business insights.

# 🚗 Ukraine Vehicle Market Analysis (2024)

## 📌 About the Project

This project represents a comprehensive analysis of the Ukrainian automotive market based on open government data. The project's goal is to demonstrate the full workflow of a Data Analyst / BI Developer: from raw data inspection (Big Data) and designing a relational database to building interactive dashboards and generating business insights.

## 🗄 Data Source

The primary data source was a large dataset in `.csv` format obtained from the Unified State Web Portal of Open Data (Diia.Open Data portal / Ministry of Internal Affairs of Ukraine). The dataset contains a detailed description of all vehicle registration operations conducted in the service centers of the Ministry of Internal Affairs during 2024, including vehicle characteristics.

## 🛠 Technology Stack

* **Databases:** PostgreSQL (DBeaver)
* **Data Analysis and Processing:** Python (Jupyter Notebook / Anaconda Navigator, Pandas)
* **Visualization and Modeling:** Microsoft Power BI (DAX, Power Query)

## ⚙️ Project Execution Stages (Workflow)

### 1. Data Quality Assessment

Before building the architecture, an Exploratory Data Analysis (EDA) was performed. The Anaconda Navigator (Python) tool was used for this.

* **Result:** The analysis showed that the government data is valid and well-structured. Additional Data Cleaning or complex transformation of the dataset was not required.
* 📄 *The file containing the data quality check code is attached in this repository.*

### 2. Relational Database Design (PostgreSQL)

To efficiently work with the "Big Data" array and quickly connect to the BI system, the raw CSV file was loaded into a local PostgreSQL DBMS. A small relational model was designed, consisting of two main tables:

* `vehicles` — the main fact table containing millions of records detailing registration operations, dates, and technical characteristics of vehicles.
* `koatuu_mapped_final` — a dimension table (lookup) storing KOATUU codes with corresponding names of regions and cities. This ensured proper geographical classification and data normalization.

### 3. Data Modeling in Power BI

The database was connected to Microsoft Power BI. For a deeper and more isolated analysis of imports, an additional (third) table was created directly within the Power BI environment (using Power Query/DAX).

* It exclusively contains vehicles that were imported to Ukraine from abroad for the first time (both brand new and used imported ones). This allowed for a detailed study of the import segment and the identification of anomalous demand spikes.

### 4. Visualization and Business Insights Generation

Based on the prepared data model, a multi-level interactive dashboard was developed, revealing:

* A general portrait of the car market (market leaders, fuel preferences, car age).
* Specifics of commercial transport (B2B segment).
* Trends in the new car market (electrification, transition to hybrids).
* Analysis of the seasonality of registration operations in the Ministry of Internal Affairs.
* 📄 *A detailed description of the analytical conclusions and business recommendations can be found in the `Ukraine Vehicle Registration Analysis 2024.pdf/docx` file in this repository.*

## 📂 Repository Structure

* `/data_quality` — Jupyter Notebook with raw data quality checks.
* `/power_bi` — link to power bi project, if there is any problems with this file write me david.bogdanov.2004@gmail.com
* `/docs` — PDF document with a detailed analytical report and business recommendations.


# Ukraine-vehicle-market-analysis

Комплексний аналіз авторинку України (2024) на основі відкритих державних великих даних (Big Data). Цей проєкт демонструє повний цикл роботи аналітика даних (Data Analyst): розвідувальний аналіз даних (Python/Pandas), проєктування реляційної бази даних (PostgreSQL) та інтерактивні дашборди Power BI для генерації бізнес-інсайтів.

# 🚗 Аналіз ринку транспортних засобів України (2024)

## 📌 Про проєкт

Цей проєкт являє собою комплексний аналіз ринку автомобілів України на основі відкритих державних даних. Мета проєкту — продемонструвати повний цикл роботи аналітика даних (Data Analyst / BI Developer): від перевірки сирих даних (Big Data) та проєктування реляційної бази даних до побудови інтерактивних дашбордів та генерації бізнес-інсайтів.

## 🗄 Джерело даних

Основним джерелом даних став великий набір даних у форматі `.csv`, отриманий з Єдиного державного вебпорталу відкритих даних (портал Дія.Відкриті дані / МВС України). Набір даних містить детальний опис усіх реєстраційних операцій з транспортними засобами, проведених у сервісних центрах МВС протягом 2024 року, включно з характеристиками автомобілів.

## 🛠 Технологічний стек

* **Бази даних:** PostgreSQL (DBeaver)
* **Аналіз та обробка даних:** Python (Jupyter Notebook / Anaconda Navigator, Pandas)
* **Візуалізація та моделювання:** Microsoft Power BI (DAX, Power Query)

## ⚙️ Етапи виконання проєкту (Workflow)

### 1. Перевірка якості даних (Data Quality Assessment)

Перед побудовою архітектури був проведений розвідувальний аналіз даних (EDA). Для цього використовувався інструмент Anaconda Navigator (Python).

* **Результат:** Аналіз показав, що державні дані є валідними та добре структурованими. Додаткове очищення даних (Data Cleaning) або складна трансформація набору даних не знадобилися.
* 📄 *Файл із кодом перевірки якості даних прикріплений у цьому репозиторії.*

### 2. Проєктування реляційної бази даних (PostgreSQL)

Для ефективної роботи з масивом "Big Data" та швидкого підключення до BI-системи, сирий CSV-файл був завантажений у локальну СКБД PostgreSQL. Було спроєктовано невелику реляційну модель, що складається з двох основних таблиць:

* `vehicles` — основна таблиця фактів, що містить мільйони записів з деталізацією реєстраційних операцій, дат та технічних характеристик транспортних засобів.
* `koatuu_mapped_final` — таблиця вимірів (довідник), у якій зберігаються коди КОАТУУ з відповідними назвами областей та міст. Це забезпечило правильну географічну класифікацію та нормалізацію даних.

### 3. Моделювання даних у Power BI

База даних була підключена до Microsoft Power BI. Для глибшого та більш ізольованого аналізу імпорту, безпосередньо в середовищі Power BI (за допомогою Power Query/DAX) була створена додаткова (третя) таблиця.

* Вона містить виключно ті транспортні засоби, які були вперше ввезені в Україну з-за кордону (як абсолютно нові, так і вживані імпортовані). Це дозволило детально дослідити сегмент імпорту та виявити аномальні сплески попиту.

### 4. Візуалізація та генерація бізнес-інсайтів

На основі підготовленої моделі даних був розроблений багаторівневий інтерактивний дашборд, який розкриває:

* Загальний портрет авторинку (лідери ринку, паливні вподобання, вік авто).
* Специфіку комерційного транспорту (B2B сегмент).
* Тренди на ринку нових авто (електрифікація, перехід на гібриди).
* Аналіз сезонності реєстраційних операцій у МВС.
* 📄 *Детальний опис аналітичних висновків та бізнес-рекомендацій можна знайти у файлі `Аналіз реєстрацій авто 2024.pdf/docx` у цьому репозиторії.*

## 📂 Структура репозиторію

* `/data_quality` — Jupyter Notebook з перевіркою якості сирих даних.
* `/power_bi` — посилання на проєкт Power BI. Якщо виникнуть проблеми з цим файлом, напишіть мені: david.bogdanov.2004@gmail.com
* `/docs` — PDF-документ з детальним аналітичним звітом та бізнес-рекомендаціями.
