# 📊 Sales Report Dashboard – Power BI Project

## 📌 Project Overview

This project presents an interactive **Sales Analytics Dashboard** built using **Microsoft Power BI** to analyze supermarket sales performance across multiple branches.

The dashboard transforms raw transactional data into actionable business insights through **data cleaning, transformation, modeling, DAX calculations, and interactive visual analytics**.

The project focuses on:

- Sales performance monitoring
- Product line analysis
- Branch performance comparison
- Customer behavior analysis
- Payment method trends
- Business decision support

---

## 🎯 Business Objectives

The main objectives of this project are:

- Monitor overall sales performance.
- Identify top-performing branches.
- Analyze product profitability.
- Understand customer purchasing behavior.
- Compare customer segments.
- Track sales trends over time.
- Support strategic business decisions using data.

---

## 🛠 Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Data Modeling
- Excel / CSV
- Business Intelligence

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

## 🧹 Data Cleaning & Transformation

Data preprocessing and transformation were performed using **Power Query** and **DAX**.

### Data Cleaning

- Checked for duplicate invoice records
- Handled missing values
- Validated numeric columns
- Corrected inconsistent formatting
- Standardized categorical values
- Verified transaction integrity

### Feature Engineering

Additional calculated measures were created for:

- Total Sales
- Sales Without Tax
- Customer Count
- Average Rating
- Top Branch
- Top Product Line
- Monthly Sales Trends

---

## 🗂 Data Modeling

A relational data model was created inside Power BI to optimize performance and enable accurate business analysis.

### Modeling Tasks

- Defined relationships between tables
- Optimized column data types
- Created calculated columns
- Built reusable DAX measures
- Designed date hierarchy

> Add your Power BI model screenshot here.

```html
<img src="YOUR_MODEL_SCREENSHOT_LINK" />
```

---

## 📌 Key Performance Indicators (KPIs)

The dashboard tracks the following business KPIs:

### Sales KPIs

- **Total Sales:** Overall revenue generated across all branches.
- **Sales Without Tax:** Net sales excluding tax.
- **Average Transaction Value:** Average revenue per transaction.
- **Monthly Sales Growth:** Month-over-month sales performance.

### Customer KPIs

- **Customer Count:** Total unique customer transactions.
- **Member vs Normal Customers:** Customer segmentation analysis.
- **Gender Distribution:** Purchase behavior by gender.

### Product KPIs

- **Top Product Line:** Highest revenue-generating product category.
- **Total Quantity Sold:** Number of products sold.
- **Product Contribution %:** Share of each product line in total sales.

### Branch KPIs

- **Top Performing Branch:** Branch with highest revenue.
- **Branch Contribution %:** Revenue contribution by branch.
- **Average Branch Rating:** Customer satisfaction by branch.

### Operational KPIs

- **Average Customer Rating**
- **Payment Method Distribution**
- **Peak Sales Period**

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
Sales-Report-PowerBI/
│── README.md
│── Capstone.pbix
│── Supermarket_Sales.csv
```

---

## 🔮 Future Improvements

Possible future enhancements:

- Sales forecasting using machine learning
- Customer segmentation clustering
- Profit margin analysis
- Inventory optimization dashboard
- Real-time data integration

---

## 👤 Author

**Motawea Nagi**  
Business Intelligence Analyst | Data Analytics | Machine Learning | Power BI

GitHub: *(Add your GitHub profile link)*  
LinkedIn: *(Add your LinkedIn profile link)*

---

⭐ If you found this project useful, feel free to star this repository.
