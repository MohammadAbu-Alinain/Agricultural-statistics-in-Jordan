# 🌾 Jordan Agriculture Statistics Dashboard (2008–2018)

## 📌 Overview

This Power BI dashboard visualizes statistical insights from the **Jordanian Ministry of Agriculture** over the period **2008 to 2018**. The data was sourced from a **PDF report** provided by the ministry and covers key metrics related to agricultural land use, production, climate, loans, exports, and farmer demographics.

The project showcases how public sector agricultural data can be transformed into an insightful, interactive dashboard using Power BI, Power Query, and DAX.

---

## 🗂️ Data Source

- 📄 **Source Document**: Official PDF report from the **Jordanian Ministry of Agriculture**
- 🗓️ **Years Covered**: 2008–2018
- 📥 **Ingested Using**: Power BI’s built-in **PDF connector**
- ✅ **Cleaned with**: Power Query Editor

---

## 🧹 Data Cleaning & Transformation (Power Query)

The imported PDF tables were not clean and required significant processing:
- Removed irrelevant rows (headers/footers) and repeated titles
- Standardized column names across years
- Converted data types (text → numbers, dates)
- Transposed irregular tables into normalized fact tables
- Created dimension tables for:
  - Crops
  - Years
  - Governorates
  - Loan categories
  - Water sources
- Implemented filters to correct data split across multiple pages

---

## 🧮 DAX Measures and Calculations

The dashboard relies heavily on DAX for dynamic analysis. Key measures include:
- `Total Area Cultivated` = SUM of dunums across crop categories
- `Average Rainfall (mm)` = AVERAGE per region/year
- `Total Loans Issued` = SUM of loan amounts by sector
- `Loan Distribution %` = PERCENTAGE OF TOTAL per loan type
- `Production Efficiency` = Production volume per dunum

Time-intelligent DAX functions like `DATEADD`, `CALCULATE`, and `YTD` were used to enable trend comparisons across years.

---

## 📊 Dashboard Structure

The Power BI report consists of **multiple pages**, each dedicated to a specific data theme. Every page contains **interactive charts, slicers, and KPIs** designed for deep analytical exploration.

### 📄 Page 1: National Overview
- **KPIs**: Total agricultural area, average rainfall, total production, total loans
- **Charts**:
  - Line chart showing crop production trends over time
  - Bar chart comparing governorate-level agricultural activity
  - Card visuals with year slicer for high-level statistics

### 🧑‍🌾 Page 2: Farmer Demographics
- **Charts**:
  - Pie chart: Gender distribution of landowners
  - Bar chart: Land distribution by ownership type
  - Tree map: Farmers categorized by region

### 🌦️ Page 3: Climate & Rainfall
- **Charts**:
  - Area chart of yearly rainfall per region
  - Column chart comparing rain-fed vs irrigated land
  - Slicer to select rainfall stations

### 🪴 Page 4: Crop Production
- **Charts**:
  - Multi-line chart: Crop category production over time
  - Matrix: Crop type × Year with production values
  - Slicers: Crop name, governorate

### 💸 Page 5: Agricultural Loans
- **Charts**:
  - Donut chart showing loan distribution by type
  - Bar chart for yearly loan totals
  - Map (if location data exists): Regional loan volume

### 📦 Page 6: Imports and Exports
- **Charts**:
  - Line chart: Export and import trends
  - Bar chart: Most exported agricultural products
  - Table: Year-by-year trade comparison

Every visual is responsive to user interaction via slicers (year, category, region, crop), and updates instantly for comparative insights.

---

## 🛠️ Technologies Used

- Power BI Desktop (.pbix)
- Power Query M Language
- DAX (Data Analysis Expressions)
- PDF Connector
- Ministry of Agriculture Report (PDF)

---

## 🚀 How to Use

1. Open the file `(احصائيات الزراعة في الاردن (2008 - 2018.pbix)` in **Power BI Desktop**
2. Ensure access to the original PDF (if you want to refresh the source)
3. Explore interactive visuals and filters
4. Use page navigation at the bottom to move between dashboard sections
5. Customize DAX or Power Query steps for deeper or modified analysis

---

## 📌 Business and Academic Applications

- Policy analysis and decision support in the agricultural sector
- Research on trends in Jordanian agricultural production
- Climate impact assessment
- Market analysis and loan distribution monitoring

---

## 📢 Credits

Data courtesy of:
**Ministry of Agriculture - Jordan**  
Prepared and visualized by: [Mohammad Abu Al-inain]

---
