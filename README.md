# 📊 **Analysis of Product Profitability**

## 📝 **Project Overview**  
This project analyzes the profitability of products across various categories and geographies over multiple years. By leveraging a dataset of online sales transactions, it provides insights into **sales trends, customer segmentation, and product performance** to guide strategic business decisions.

---

## 📂 **Dataset Overview**  
The dataset contains information on online sales transactions, capturing various metrics such as:  
- **Product Description**  
- **Unit Price & Quantity**  
- **Discounts**  
- **Shipping Costs**  
- **Order Dates & Geographical Data**  

**Objective**: To calculate and analyze the **Total Sales** and **Profitability** for each product and provide year-wise and category-wise breakdowns of performance.

---

## 🚀 **Key Features & Analysis**

### 1. **Sales Trends by Year**  
Analyzed monthly sales trends across multiple years (2020–2024) to identify patterns and seasonality.  
Example output for 2024:  
```
January: $627,778.90  
February: $602,332.22  
...  
December: $640,246.05  
```

### 2. **Product Performance by Category**  
Sales performance of different product categories across years (e.g., Accessories, Apparel, Electronics).  
Example:  
- **2024 Sales by Category**  
  - Accessories: $1.58M  
  - Electronics: $1.52M  

### 3. **Geographical Sales Analysis**  
Identified country-wise sales trends across regions like the United States, France, and Germany.  
Example:  
- **2024**  
  - United States: $642,257.21  
  - Germany: $702,298.76  

### 4. **Customer Segmentation**  
Segmentation of customers based on total spending to identify high-value and low-value customers, helping businesses focus on priority segments.

---

## 🛠 **Technologies Used**
- **Python**: Data manipulation and analysis  
  - Libraries: `pandas`, `matplotlib`, `numpy`  
- **Jupyter Notebook**: Interactive analysis and visualization  

---

## 📊 **Code Overview**

### **Data Preparation**
```python
import pandas as pd

# Load dataset
df_osd = pd.read_csv('online_sales_dataset.csv')
df_osd['InvoiceDate'] = pd.to_datetime(df_osd['InvoiceDate'])
df_osd['Year'] = df_osd['InvoiceDate'].dt.year
```

### **Sales Trend Analysis**
```python
for year, data in data_by_year.items():
    monthly_sales = data.resample('M', on='InvoiceDate')['TotalSales'].sum()
    print(f"Monthly Sales for {year}:")
    print(monthly_sales)
```

### **Category & Geographical Analysis**
```python
# Product performance by category
for year, data in data_by_year.items():
    category_sales = data.groupby('Category')['TotalSales'].sum()
    print(f"Sales by Category for {year}:")
    category_sales.plot(kind='bar', title=f'Sales by Category in {year}')
```

---

## 📬 **Contact**  
For any questions or feedback, feel free to reach out.  
