# 🏬 US Superstore Business Analytics Dashboard (Excel)

## 🎯 Why This Project?  
In the fast-growing retail industry, data-driven decisions are essential for sustainable growth.  
This project was built to:  

- **Practice Descriptive Analytics** → transforming raw transactional data into business insights.  
- **Develop Excel BI skills** → using Pivot Tables, Slicers, and VBA for automation.  
- **Understand retail business dynamics** → exploring how product categories, regions, and customer segments contribute to revenue and profit.  
- **Communicate findings visually** → designing an interactive dashboard that answers key business questions at a glance.  

By bridging **data analysis** and **business decision-making**, this project showcases the value of analytics in driving strategic actions.  

---

## 1. Introduction
This project presents an **interactive Excel dashboard** analyzing sales and profit trends for the **US Superstore dataset (2014–2017)**.  
The dashboard helps answer key business questions such as:
- Year-over-year growth in Sales and Profit  
- Performance by Category, Sub-category, City, and State  
- Regional differences and top/bottom performing states  
- Monthly sales trends across multiple years  

👉 **Goal:** Transform raw transactional data into **actionable insights** through interactive visualization and KPIs for business decision-making.

---

## 2. Dataset
- **Source:** Kaggle – US Superstore  
- **Period:** 2014–2017  
- **Size:** 10,001 rows × 21 fields (after cleaning)  
- **Main fields:** `Order Date`, `Ship Date`, `Ship Mode`, `Customer`, `Segment`, `Region`, `Category`, `Sub-category`, `Sales`, `Quantity`, `Discount`, `Profit`  

**Data preparation (Power Query):**
- Promoted headers, formatted data types  
- Removed invalid/missing values (4 rows)  
- Removed duplicates (7 rows)  
- Loaded cleaned dataset for dashboard creation  

---

## 3. Business Questions
The dashboard was designed to answer:
1. Total Sales and Profit for the latest year vs. previous year  
2. Growth rates compared to prior year  
3. Sales breakdown by Sub-category (2016 vs 2017)  
4. Sales breakdown by City (2016 vs 2017)  
5. Profit distribution by State  
6. Sales trends across 12 months per year  
7. Top 10 and Bottom 10 States by lifetime Sales  

---

## 4. Techniques Applied
- Pivot Tables & Pivot Charts for KPIs and breakdowns  
- Slicers & Filters (Category, Segment, Ship Mode)  
- Custom Formulas  
  - Growth rate:  
    ```excel
    =IF(AND(ISNUMBER(C16),ISNUMBER(D16)),C16/D16-1,"")
    ```
  - Conditional formatting: `[Blue]0.0%▲;[Red](0.0)%`  
  - Dynamic Top 10:  
    ```excel
    {=SWITCH(G62,1,SORT(A63:B110,2,-1,FALSE),2,SORT(A63:B110,2,1,FALSE))}
    ```
- Interactive design (wireframe-based layout with KPI cards and tables)  
- VBA Automation (`CreatePPT` macro):  
  - Exports filtered dashboard views to PowerPoint  
  - Dynamic slide titles and automated screenshot embedding  

---

## 5. Dashboard Features
- **KPI Cards:** Sales & Profit (latest year vs. last year), Growth vs PY  
- **Interactive Filters:** Category, Segment, Ship Mode  
- **Breakdowns:** Sales by Sub-category & City (2016 vs 2017)  
- **Maps & Trends:**  
  - Profit by State (2014–2017 aggregated)  
  - Monthly sales trends by year  
  - Top 10 & Bottom 10 States (all-time sales)  

---

## 6. Key Insights
### Overall Performance
- **2017 Sales:** 733,215.3 vs 2016: 609,205.6 → **+20.36% growth**  
- **2017 Profit:** 93,439.3 vs 2016: 81,795.2 → **+14.24% growth**  
- Sales growth outpaced profit growth → possible margin pressure.  

### Category & Sub-Category Trends
- 2017 Sales: **642,486 (+20.4% YoY)**  
- High growth: Appliances (+64.8%), Binders (+46.5%), Accessories (+43.1%)  
- Weak: Tables (+0.1%), Machines (–22.1%)  

### Regional & City-Level
- 2017 City Sales: **339,408 (+27.5% YoY)**  
- High growth cities: Seattle (+252.7%), Columbus (+84.8%), NYC (+58.6%)  
- Declines: Lafayette (–69.5%), Detroit (–42.7%), LA (–13.3%)  

### Customer Segments
- **Consumer:** +20.4% YoY, strong in Appliances & Binders  
- **Corporate:** +12.2% YoY, Appliances (+101.8%), Phones (+54.5%)  
- **Home Office:** +16.3% YoY, Binders (+161.2%), Appliances (+117.4%)  

⚠️ Risk: Machines, Tables, Copiers show consistent decline.  

### Seasonality
- Sales peak in **Q4 (Nov–Dec)** every year  
- Slight dip in **Oct 2017** → possible promo timing issue  

### State-Level
- **Highest Sales (all-time):** California (457,688), New York (310,876)  
- **Lowest Sales:** Idaho, South Dakota, Nebraska (<1,000)  
- Indicates market concentration → prioritize strong states.  

---

## 7. Limitations
- Dataset covers only 2014–2017 (no real-time updates).  
- Profit by State map aggregates all years (not yearly).  
- Excel only → limited scalability (no Power BI/Tableau).  
- Descriptive analysis only (no predictive/prescriptive modeling).  

---

## 8. Future Development
- Forecasting models (Prophet, ARIMA) to predict future sales  
- Real-time data refresh integration  
- Customer segmentation (RFM, CLV) for targeted marketing  
- Migrate to Power BI/Tableau for richer interactivity  

---

## 9. How to Run
1. Download the repo files  
2. Open `US_Superstore_Dashboard.xlsm`  
3. Enable macros for VBA functionality  
4. Use slicers to filter by Category, Segment, or Ship Mode  
5. Press **Create PPT** button to auto-export dashboard slides  

---
