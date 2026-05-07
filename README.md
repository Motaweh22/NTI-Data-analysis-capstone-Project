# 📊 Sales Report Dashboard – End-to-End Data Analytics Project

## 📌 Project Overview

This project presents an end-to-end **Data Analytics and Business Intelligence solution** built using **Python** and **Microsoft Power BI** to analyze supermarket transactional data across multiple branches.

The project starts with raw data cleaning and preprocessing in Python, followed by KPI development, business analysis, and interactive dashboard creation in Power BI.

The main goal was to transform raw transactional data into actionable business insights through data quality improvement, feature engineering, KPI analysis, and dashboard reporting.

The project focuses on:

- Sales performance monitoring
- Product line analysis
- Branch performance comparison
- Customer behavior analysis
- Payment method trends
- Business decision support
- Promotion effectiveness analysis

---

## 🎯 Business Objectives

The main objectives of this project are:

- Monitor overall sales performance.
- Evaluate promotion effectiveness.
- Identify top-performing branches.
- Analyze product profitability.
- Understand customer purchasing behavior.
- Compare customer segments.
- Track sales trends over time.
- Support strategic business decisions using data.

---

## 🛠 Tools & Technologies

### Data Processing

- Python
- Pandas
- NumPy
- Jupyter Notebook

### Business Intelligence

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Data Modeling

---

## 📊 Dataset Information

This project uses the **Supermarket Sales Dataset** containing transactional sales data from three supermarket branches.

### Dataset Summary

- **Total Records:** 1,006 transactions
- **Unique Invoices:** 1,000
- **Features:** 16 columns
- **Branches:** 3
- **Product Lines:** 6
- **Payment Methods:** 3
- **Time Period:** January 2019 – March 2019

### Main Features

- Invoice ID
- Branch
- Customer Type
- Gender
- Product Line
- Unit Price
- Quantity
- Tax (5%)
- Total Sales
- Date
- Time
- Payment Method
- Rating

---

## 🧹 Data Cleaning & Preprocessing

Data cleaning and preprocessing were performed using **Python**, **Pandas**, and **NumPy** before importing the dataset into Power BI.

The objective was to improve data quality, resolve inconsistencies, enrich the dataset, and prepare it for KPI analysis and dashboard reporting.

### Data Quality Issues Resolved

#### NULL Values

- **Tax 5%:** 9 missing rows were filled using:

```python
Tax = Total - (Unit Price × Quantity)
```

- **Total:** 3 missing rows were calculated using:

```python
Total = (Unit Price × Quantity) + Tax
```

#### Currency Symbols

- Removed `'USD'` from **5 records** in `UnitPrice`
- Converted the column from string to numeric format

#### Customer Type

- Standardized **27 invalid entries** by replacing them with:

`Normal`

#### Time Formatting

- Standardized time values into:

`HH:MM:SS AM/PM`

Example:

`08:30 PM → 08:30:00 PM`

#### Data Types

- Converted `UnitPrice` from **object → float**

#### Duplicate Records

- Removed **6 duplicate rows**

#### Outlier Handling

##### Quantity

- Corrected negative quantities:

`-8, -7, -1 → 8, 7, 1`

##### Rating

- Fixed abnormal rating:

`97 → 9.7`

##### Tax & Total

- Reviewed high-value outliers
- Confirmed they were valid business transactions and retained them

---

## 🆕 Feature Engineering

Additional business features were created to support deeper analysis.

### New Features

#### branch_city

A derived feature mapping each branch to its corresponding city:

- A → Yangon
- B → Mandalay
- C → Naypyitaw

This enabled:

- Geographic sales analysis
- Branch comparison
- Regional customer behavior analysis

---

## 🗂 Data Modeling

A semantic model was built in Power BI to support analytical reporting and KPI calculations.

### Modeling Tasks

- Optimized column data types
- Built date hierarchy
- Created calculated columns
- Created reusable DAX measures
- Structured dimensions for branch, product, customer, and time analysis

---

## 📌 Key Performance Indicators (KPIs)

The dashboard tracks the following business KPIs:

### Sales KPIs

- **Total Sales**
- **Sales Without Tax**
- **Average Transaction Value**
- **Monthly Sales Growth**

### Customer KPIs

- **Customer Count**
- **Member vs Normal Customers**
- **Gender Distribution**

### Product KPIs

- **Top Product Line**
- **Total Quantity Sold**
- **Product Contribution %**

### Branch KPIs

- **Top Performing Branch**
- **Branch Contribution %**
- **Average Branch Rating**

### Operational KPIs

- **Average Customer Rating**
- **Payment Method Distribution**
- **Peak Sales Period**
- **Promotion Effectiveness**

---

## 📂 Dashboard Pages

# 1️⃣ Executive Overview

### Key Insights

- Overall business performance
- Sales trend monitoring
- Product contribution analysis
- Branch comparison

<img width="1429" alt="Executive Dashboard" src="https://github.com/user-attachments/assets/167cd29f-6d39-44d4-823d-3a7a9868b75f" />

---

# 2️⃣ Product Analysis

### Key Insights

- Identify top-selling product lines
- Compare product contribution
- Analyze product quantities
- Track monthly product performance

<img width="1413" alt="Product Dashboard" src="https://github.com/user-attachments/assets/9d2d976d-66a4-40be-950e-98e1cc240c07" />

---

# 3️⃣ Branch Analysis

### Key Insights

- Compare branch performance
- Identify strongest branch
- Analyze branch ratings
- Understand payment preferences

<img width="1443" alt="Branch Dashboard" src="https://github.com/user-attachments/assets/0822dc85-c234-4982-b3c3-59019affabb3" />

---

# 4️⃣ Customer Analysis

### Key Insights

- Gender distribution
- Customer type comparison
- Product preferences
- Monthly customer behavior

<img width="1405" alt="Customer Dashboard" src="https://github.com/user-attachments/assets/e29ef948-ab2f-4913-a463-8178687528fd" />

---

## 🧮 DAX Measures

```DAX
Total Sales = SUM(Sales[Total])

Sales Without Tax = SUM(Sales[cogs])

Customer Count = DISTINCTCOUNT(Sales[Invoice ID])

Average Rating = AVERAGE(Sales[Rating])

Top Branch =
CALCULATE(
    [Total Sales],
    TOPN(1, VALUES(Sales[Branch]), [Total Sales])
)
```

---

## 💡 Key Business Insights

Based on dashboard analysis:

- **Naypyitaw** generated the highest total sales.
- **Food and Beverages** was the best-performing product line.
- **Member customers** generated higher revenue than normal customers.
- **E-wallet** was the most preferred payment method.
- Customer satisfaction averaged around **7 / 10**.
- Sales activity peaked during **March 2019**.

---

## 🚀 Business Impact

This dashboard helps stakeholders:

- Identify profitable products.
- Optimize branch performance.
- Improve customer targeting.
- Monitor operational KPIs.
- Support strategic planning.
- Discover growth opportunities.

---

## 📁 Repository Structure

```bash
supermarket-sales-analysis/
│── README.md
│── Capstone.pbix
│── Supermarket_Sales.csv
│── Cleaned_Supermarket_Sales.csv
│── DataCleaningV4.ipynb
```
---

⭐ If you found this project useful, feel free to star this repository.
