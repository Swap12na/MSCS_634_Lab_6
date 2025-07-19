# Lab 6: Association Rule Mining with Apriori and FP-Growth

**Course:** MSCS 634 – Data Mining  
**Student Name:** Vishnu Mallam  
**Lab Title:** Association Rule Mining with Apriori and FP-Growth  

## 1. Project Overview
This lab focuses on uncovering meaningful associations from a real-world retail transaction dataset using two widely-used algorithms: **Apriori** and **FP-Growth**. The goal is to identify **frequent itemsets** and generate **association rules** that reveal customer purchasing behavior. These insights support business functions such as:

- Marketing and cross-selling
- Inventory optimization
- Recommendation engines

---

## 2. Dataset Description
**Dataset Name:** Online Retail  
**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+Retail)  

**Key Features:**

- Transactions recorded between 01/12/2010 and 09/12/2011
- Retailer based in the UK
- Contains fields like: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

**Preprocessing Steps:**

- Removed rows with missing `CustomerID`
- Filtered data for transactions from the **United Kingdom**
- Excluded canceled invoices (InvoiceNo starting with 'C') and rows with negative quantities
- Transformed the data into a **basket matrix** for Market Basket Analysis

---

## 3. Tools and Libraries Used

- Python (Jupyter Notebook)
- `pandas` – data manipulation
- `mlxtend` – for Apriori, FP-Growth, and association rule mining
- `matplotlib`, `seaborn` – data visualization
- `openpyxl` – Excel file loading

---

## 4. Methodology

### Step 1: Data Preparation
- Cleaned dataset and filtered for relevant transactions
- Created a transaction-item matrix (one-hot encoded)

### Step 2: Exploratory Data Analysis
- Visualized the **top 10 most sold items** using bar plots

### Step 3: Frequent Itemset Mining
- Applied **Apriori** algorithm with `min_support = 0.02`
- Applied **FP-Growth** algorithm with `min_support = 0.02`
- Compared performance (speed and memory)

### Step 4: Association Rule Generation
- Used `min_confidence = 0.5`
- Evaluated rules based on **support**, **confidence**, and **lift**
- Plotted **lift vs confidence** for interpretation

---

## 5. Key Results

- **Most frequent item:** `WHITE HANGING HEART T-LIGHT HOLDER`
- Discovered strong associations among decorative home products
- FP-Growth outperformed Apriori in both **speed** and **memory**
- High lift values (> 2) indicated strong bundling opportunities

---

## 6. Business Applications

- Product bundling and recommendations
- Layout and navigation optimization (in-store or online)
- Demand forecasting and stock management
- Targeted promotions using basket analysis

---

## 7. Performance Comparison

| Metric         | Apriori     | FP-Growth  |
|----------------|-------------|------------|
| Speed          | Slower      | Faster     |
| Memory Usage   | Higher      | Lower      |
| Scalability    | Limited     | High       |

---

