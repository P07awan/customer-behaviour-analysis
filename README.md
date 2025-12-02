# Customer Behaviour Analysis — End-to-End Project (MySQL + Python + Power BI)

This project provides a complete **Customer Behaviour Analytics Pipeline** using:

* **MySQL** — for database storage and SQL-based insights
* **Python** — for data cleaning, preprocessing, and deeper analytics
* **Power BI** — for interactive dashboards & business reporting

---

## 🚀 Project Overview

The goal of this project is to analyze customer behaviour, extract insights, and visualize the results in a professional BI dashboard. The workflow includes:

1. Importing and cleaning raw customer data using Python.
2. Storing the cleaned dataset into **MySQL database**.
3. Running analytical SQL queries (Q1–Q10) to answer business questions.
4. Building a **Power BI Dashboard** using MySQL connectivity.
5. Preparing insights and visualizations to understand trends.

---

## 📂 Project Structure

```
Customer-Behaviour-Analysis/
│
├── data/
│   ├── raw_data.csv
│   ├── cleaned_data.csv
│
├── sql/
│   ├── customer_analysis_queries.sql
│
├── powerbi/
│   ├── dashboard.pbix
│
├── python/
│   ├── cleaning_notebook.ipynb
│   ├── eda_notebook.ipynb
│
└── README.md (you are here)
```

---

## 🗂️ Dataset Description

The dataset contains:

* Customer demographics (age, gender, region, age group)
* Purchase behaviour (amount, product, category)
* Discount usage
* Previous purchase count
* Shipping preferences
* Review ratings
* Subscription information

---

## 🧹 Python Data Cleaning

Python was used for:

* Handling missing values
* Renaming inconsistent columns
* Converting data types
* Adding derived fields (age groups, loyalty segmentation)
* Exporting cleaned dataset to MySQL

Key steps:

```python
df.columns = df.columns.str.lower().str.replace(' ', '_')
df.to_sql("customer", engine, if_exists="replace", index=False)
```

Detailed cleaning available in: `python/cleaning_notebook.ipynb`.

---

## 🐬 MySQL Database Setup

Database Name:

```
customer_behaviour
```

Table:

```
customer
```

### 🔑 MySQL Default Credentials

* Username: **root**
* Password: (your MySQL password)
* Host: `localhost`
* Port: `3306`

---

## 📊 SQL Analysis (Q1–Q10)

All SQL business questions are included in:

```
sql/customer_analysis_queries.sql
```

Key insights include:

* Revenue by gender
* Discount efficiency
* Top-performing products
* Loyal vs returning customers
* Subscription influence on spending
* Category-wise top items
* Age-group revenue contribution

---

## 📈 Power BI Dashboard

The Power BI dashboard includes:

* **KPI Cards** (Total Revenue, Avg Purchase, Discounts)
* **Gender-wise revenue pie chart**
* **Subscription revenue comparison**
* **Top products bar chart**
* **Customer segmentation donut chart**
* **Category-level drilldowns**

Connection settings:

* Data Source: **MySQL Database**
* Server: `localhost`
* Database: `customer_behaviour`
* Authentication: Username & Password

**Note:** MySQL Connector/ODBC must be installed for Power BI integration.

---

## 📌 Key Business Insights

* Subscribed customers spend **significantly more** on average.
* Most discount users still fall below the average purchase threshold.
* A few products contribute to the **majority of sales**.
* Loyal customers (10+ purchases) drive **high repeat revenue**.
* Standard shipping dominates purchases compared to express.
* Age group 25–35 generates the highest revenue.

---

## 🛠️ Tools & Technologies

* **Python** (Pandas, SQLAlchemy, Matplotlib)
* **MySQL 8.x**
* **Power BI Desktop**
* **ODBC & MySQL Connector**

---

**Developer:** Pawan Kushwaha

---
