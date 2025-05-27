# 📊 Sales Data Analysis | Power BI Dashboard

## 📌 Project Overview
This Power BI project delivers a comprehensive analysis of ElectroHub's sales data, uncovering key patterns in product sales, profit margins, discount behavior, and customer order trends. The dashboard is crafted to empower business users with actionable insights through interactive, slicer-driven analytics.

## 🎯 Dashboard Features

### 📌 Overview Tab:

   📈 Sales Trends Analysis (Line Chart): Daily, Monthly, Quarterly, and Annually.
    
   📊 Profit vs. Net Sales Relationship (Scatter Plot)
    
   🏷️ Average Discount Analysis by Promotion Categories (Bar Chart)
    
   🛒 Total Number of Orders (Card Visual)
    
   🌎 Sales by Cities (Map Visual)

### 📌 Top/Bottom 5 Analysis Tab:
   
   🥇 Top 5 and Bottom 5 Products by Sales, Profit, Quantity Sold (dedicated tab)

### 📌 Comparison Tab:
    
   📊 Without DAX:
    Two slicers with stacked bar charts comparing Sales, Profit, Quantity Sold for different periods.
    
   📊 With DAX:
    Created two Date tables (one active, one inactive) and used USERELATIONSHIP in a measure to enable dual-period comparison on demand:

    Sample DAX Query:
    
    Sum of Net Sales = CALCULATE(SUM('Fact Table'[Net Sales]), ALL('Date Table 1'[Date]),USERELATIONSHIP('Date Table 2'[Date], 'Fact Table'[Date (dd/mm/yyyy)]))
    
### 📌 Detailed Order-wise Metrics:

#### 📋 Table Visual showing Sales, Profit, Discount, Net Sales, and all remaining order fields.

#### Interactive Product, Date, Customer ID, Promotion Category slicers.

#### Custom DAX measure (Sum of Net Sales) acts as a dynamic filter controller:
      
  * Ensures slicers affect visuals only when related data exists.
      
  * Seamless interactivity across fields.
   

## 📦 Dataset Details

   Store Data Dataset which consists of 4 Tables (Customer, Product, Promotion details and Order Details (Fact Table)).
 
## 🛠️ Tools & Techniques

* Power BI Desktop

* Power Query Editor: Data cleaning, new column creation, and pre-model transformations

* DAX Measures: KPIs, period comparisons, dynamic filtering

* USERELATIONSHIP-based dynamic relationship management

* Structured Data Modeling with multiple Date tables and relationship strategies

* Slicer-driven interactive filtering

* Clean multi-tab report layout

## 📸 Dashboard Preview

Top/Bottom 5 Analysis Tab:

![image](https://github.com/user-attachments/assets/f38c269f-d497-4882-b202-59fb3302e30e)

Overview Tab:

![image](https://github.com/user-attachments/assets/624d41f7-4bdb-4070-a43c-7f2cbaecee44)

Comparison Tab without DAX:

![image](https://github.com/user-attachments/assets/7677b90b-12ee-4a0a-9564-d8a991b91869)

Comparison Tab with DAX:

![image](https://github.com/user-attachments/assets/848d2700-9a21-46cf-b41f-f450b8731995)

Detailed Order-wise Metrics:

![image](https://github.com/user-attachments/assets/2409f5eb-b6dd-403e-bffb-4f176110beba)

## 🔗 Live Dashboard
[Check it out on NovyPro (add link after upload)]

## ✅ How to Use

* Download the .pbix file.

* Open with Power BI Desktop (2023 May or newer).

* Use slicers and visuals for real-time interactive analysis.

## 📝 Technical Highlights

* Multi-tabbed modular report design

* Advanced USERELATIONSHIP DAX implementation for dual-period comparisons

* Dynamic slicer-based filtering using DAX-driven filter measures

* Data cleaning, transformation, and derived columns in Power Query

* Seamless interactivity between Table Visuals and slicers for granular analysis

* Geographical mapping and KPI cards for business metrics
