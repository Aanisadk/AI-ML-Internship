## 🛒 E-Commerce Customer Behavior & Delivery Analytics

### *Unit Economics, Logistics Bottlenecks & Discount Elasticity*

**Python • NumPy • Pandas • Matplotlib**

---

## 📌 About the Project

This project is an **E-Commerce Customer Behavior & Delivery Analytics** project developed as part of an academic data analytics practicum.

The project focuses on analyzing e-commerce transaction data to understand **customer behavior, revenue performance, delivery efficiency, discounting patterns, return behavior, and customer satisfaction**.

The complete workflow was performed using **Python in Google Colab**, starting from raw data inspection and cleaning and continuing through numerical analysis, business analytics, customer segmentation, and data visualization.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Clean and prepare raw e-commerce transaction data
* Identify and remove duplicate records
* Handle missing values appropriately
* Standardize categorical data
* Perform numerical operations using NumPy
* Calculate delivery delays and fulfillment status
* Identify high-value orders using percentile analysis
* Calculate net realized revenue after discounts
* Analyze category-wise business performance
* Analyze regional fulfillment problems
* Study customer satisfaction and delivery performance
* Perform rule-based customer segmentation
* Create professional visualizations using Matplotlib
* Generate meaningful business insights from the data

---

## 🧰 Tools & Technologies

| Tool / Technology   | Purpose                                    |
| ------------------- | ------------------------------------------ |
| 🐍 **Python**       | Main programming language                  |
| 🔢 **NumPy**        | Numerical operations and vectorized logic  |
| 🐼 **Pandas**       | Data cleaning, transformation and analysis |
| 📊 **Matplotlib**   | Data visualization                         |
| ☁️ **Google Colab** | Development and execution environment      |

---

## 📂 Project Files

| File                                                                        | Description                                                      |
| --------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| 📄 [Assignment PDF](ecommerce_customer_behavior_and_delivery_analytics.pdf) | Assignment question and project brief provided for the practicum |
| 📊 [Dataset](e-commarce.csv)                                                | E-commerce dataset used for the analysis                         |
| 📓 [Google Colab](e_commarce.ipynb)                                     | Complete Python / Google Colab notebook containing the analysis  |


## 📄 Assignment

The assignment brief provided for this project is included in the repository.

**Assignment File:**

[Assignment PDF](ecommerce_customer_behavior_and_delivery_analytics.pdf)

It contains the complete problem statement, dataset requirements, analytical tasks, visualization requirements, grading criteria, and submission guidelines.

---

# 🧹 Data Cleaning & Preprocessing

The raw e-commerce dataset was first inspected and cleaned using **Pandas**.

The following preprocessing steps were performed:

### 1. Data Loading & Validation

The dataset was loaded using Pandas and checked for:

* Dataset dimensions
* Column data types
* Missing values

### 2. Duplicate Detection & Removal

Duplicate records were identified using the **Order ID** as the primary transaction identifier.

Redundant duplicate records were removed while keeping the first occurrence.

### 3. Payment Method Standardization

The `Payment_Method` column was cleaned by:

* Removing unnecessary whitespace
* Standardizing text casing
* Converting `upi` into `UPI`

This ensured consistent categorical values.

### 4. Missing Order Value Handling

Missing values in `Order_Value` were filled using **category-wise median imputation**.

This approach helps preserve the spending characteristics of individual product categories and is more suitable for skewed order-value data.

### 5. Customer Rating Handling

Missing customer ratings were handled using the **mode** of the rating column.

The mode was selected because customer ratings represent discrete values on a rating scale.

---

# 🔢 NumPy Operations

NumPy was used to perform efficient **vectorized numerical operations** without unnecessary row-wise loops.

### Delivery Delay

A new `Delivery_Delay` feature was created by comparing:

**Actual Delivery Days − Estimated Delivery Days**

This allowed orders to be classified according to their fulfillment performance.

### Fulfillment Status

Orders were categorized into:

* **Early**
* **On-Time**
* **Minor Delay**
* **Severe Delay**

The classification was performed using NumPy's `np.select()` with vectorized conditions.

### High-Value Order Detection

The **95th percentile** of `Order_Value` was calculated using NumPy.

Orders exceeding this threshold were identified as **High-Value Orders**.

### Net Revenue

Net realized revenue was calculated after considering the applied discount.

This provides a better representation of the actual revenue generated from each transaction.

---

# 📊 Business Analytics

The cleaned dataset was further analyzed using **Pandas groupby, aggregation, pivot tables, and vectorized conditions**.

### Category Performance

Product categories were compared based on:

* Total Net Revenue
* Average Discount Offered
* Return Rate

The categories were ranked according to their total net revenue.

### Regional Fulfillment Analysis

The percentage of **Severe Delay** orders was calculated for each city tier.

This helps identify regions experiencing greater logistics and fulfillment problems.

### Customer Sentiment Analysis

A pivot table was created to compare **average Customer Rating** across different fulfillment statuses and product categories.

This helps examine the relationship between delivery performance and customer satisfaction.

### Customer Segmentation

Transactions were divided into three business-oriented segments:

🔴 **High-Risk Transaction**
High discount combined with a returned order.

🟢 **Loyal & Satisfied**
Higher-value orders from customers with strong ratings and no return.

🔵 **Standard Order**
All remaining transactions.

The segmentation was performed using **rule-based vectorized conditions**, without machine learning.

---

# 📈 Visual Analytics

The final stage of the project focused on **visual analytics and communicative storytelling using Matplotlib**.

The visualizations were designed with clear titles, labeled axes, appropriate units, contrasting colors, and subtle gridlines.

### 📊 Commercial Contribution

A bar chart was created to compare **Total Net Revenue by Product Category**, with categories arranged in descending order of revenue.

### 🚚 Fulfillment Distribution

A histogram was created to show the distribution of **Actual Delivery Days**, together with a benchmark line representing the average estimated delivery time.

### 💸 Discount & Return Analysis

A scatter plot was created to study the relationship between:

* **Discount Percentage**
* **Order Value**
* **Return Status**

Returned and non-returned orders were represented using different colors.

### ⭐ Logistics Impact on Customer Sentiment

Average customer ratings were compared across different fulfillment statuses to visualize the potential impact of delivery delays on customer satisfaction.

---

# 📋 Project Workflow

```text
Raw Dataset
     ↓
Data Inspection
     ↓
Data Cleaning
     ↓
Missing Value Handling
     ↓
Duplicate Removal
     ↓
Data Standardization
     ↓
NumPy Vectorized Analysis
     ↓
Business Analytics
     ↓
Customer Segmentation
     ↓
Matplotlib Visualization
     ↓
Business Insights
```

---

# 📚 Skills Demonstrated

This project demonstrates practical knowledge of:

* Python
* NumPy
* Pandas
* Data Cleaning
* Data Preprocessing
* Missing Value Imputation
* Duplicate Detection
* Vectorized Operations
* Statistical Analysis
* Percentile Analysis
* GroupBy & Aggregation
* Pivot Tables
* Rule-Based Segmentation
* Business Analytics
* Data Visualization
* Matplotlib
* Data Storytelling

---

# 💡 Key Analytical Areas

The project provides an analytical view of:

**💰 Revenue Performance**
Understanding which product categories contribute most to net revenue.

**🚚 Delivery Performance**
Identifying early deliveries, on-time orders, minor delays, and severe delays.

**🔄 Return Behavior**
Understanding return patterns and identifying potentially high-risk transactions.

**💸 Discount Behavior**
Analyzing the relationship between discounts, order value, and returns.

**⭐ Customer Satisfaction**
Studying customer ratings in relation to fulfillment performance.

**🌍 Regional Logistics**
Identifying city tiers experiencing higher fulfillment friction.

---

# 📓 Notebook

The complete implementation is available in the Jupyter Notebook:

[Google Colab](e_commarce.ipynb)

The notebook contains the complete workflow from **data loading and cleaning to analysis and visualization**.

---

# 📊 Dataset

The dataset used for this project is available in:

[Dataset](e-commarce.csv)

It contains the e-commerce transaction records used throughout the analysis.

---

# 📝 Assignment Reference

The original academic assignment and project brief are included as:

📄 [Assignment PDF](ecommerce_customer_behavior_and_delivery_analytics.pdf)

---

# 🎓 Academic Project

**Project Type:** Foundational Data Analytics Practicum
**Domain:** E-Commerce Analytics
**Primary Focus:** Customer Behavior, Delivery Analytics, Unit Economics & Discount Analysis
**Core Technologies:** Python, NumPy, Pandas, Matplotlib

---

## ⭐ Conclusion

This project demonstrates a complete **data analytics workflow** using Python, starting from raw e-commerce transaction data and progressing through data cleaning, numerical analysis, business analytics, customer segmentation, and visual storytelling.

The project combines **technical data analysis with business-focused interpretation** to understand revenue, logistics, discounts, returns, and customer satisfaction.

---

### 🚀 Built with Python • NumPy • Pandas • Matplotlib
