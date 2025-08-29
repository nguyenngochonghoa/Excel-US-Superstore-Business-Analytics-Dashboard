# US-Superstore-Business-Analytics-Dashboard (Excel)

## 📌 Introduction  
This project presents an **interactive Excel dashboard** analyzing sales and profit trends for the **US Superstore dataset (2014–2017)**.  

👉 **Goal**: Transform raw transactional data into actionable insights using descriptive analytics and interactive dashboards.  
The analysis provides visibility into **year-over-year performance, category & city trends, customer segments, and state-level insights** to support better business decision-making.  

---

## 🎯 Why This Project?  
In the fast-growing retail industry, data-driven decisions are essential for sustainable growth.  
This project was built to:  

- **Practice Descriptive Analytics** → transforming raw transactional data into business insights.  
- **Develop Excel BI skills** → using Pivot Tables, Slicers, and VBA for automation.  
- **Understand retail business dynamics** → exploring how product categories, regions, and customer segments contribute to revenue and profit.  
- **Communicate findings visually** → designing an interactive dashboard that answers key business questions at a glance.  

By bridging **data analysis** and **business decision-making**, this project showcases the value of analytics in driving strategic actions.  

--

## 📊 Dataset  
- **Source**: [Kaggle – US Superstore](https://www.kaggle.com/datasets/juhi1994/superstore?resource=download)  
- **Period**: 2014–2017  
- **Size**: 10,001 rows × 21 fields (after cleaning)  
- **Main fields**: Order Date, Ship Date, Ship Mode, Customer, Segment, Region, Category, Sub-category, Sales, Quantity, Discount, Profit  

**Data Cleaning (Power Query)**  
- Promoted headers & set proper data types  
- Removed 4 invalid rows & 7 duplicates  
- Final dataset loaded into Excel for dashboard creation  

---

## ❓ Business Questions  
The dashboard was designed to answer:  
- Sales & Profit for the latest year vs previous year  
- YoY Growth (%) for Sales & Profit  
- Sales by Sub-category and City (2016 vs 2017)  
- Profit distribution across States  
- Monthly Sales trends (2014–2017)  
- Top 10 & Bottom 10 States by lifetime Sales  

---

## 🛠️ Techniques Applied  
- Pivot Tables & Pivot Charts  
- Slicers & Filters (Category, Segment, Ship Mode)  
- Custom Formulas & Conditional Formatting  
- VBA Macro `CreatePPT`: auto-export dashboard views to PowerPoint  

---

## 📈 Dashboard Features  
- **KPI Cards** → Sales & Profit (latest year vs PY), YoY Growth  
- **Filters** → Category, Segment, Ship Mode  
- **Breakdowns** → Sales by Sub-category & City (2016 vs 2017)  
- **Visuals** → Profit by State (map), Monthly Sales by Year, Top/Bottom 10 States  

---

## 🔎 Key Insights  
- **2017 Sales**: 733K (+20.4% YoY)  
- **2017 Profit**: 93K (+14.2% YoY)  
- **Category Trends** → High growth in Appliances (+64.8%) & Accessories (+43.1%), but Machines (–22.1%) declined.  
- **Regional Trends** → Seattle (+252.7%) & Newark (+643.7%) surged, while Lafayette (–69.5%) & San Diego (–88.3%) fell.  
- **Seasonality** → Strong Q4 peaks each year, especially Nov–Dec.  
- **State Performance** → California & New York dominate, while smaller states contribute minimally.  

---

## ⚠️ Limitations  
- Data limited to **2014–2017 (historical only)**  
- Profit map aggregates all years (not by year)  
- Dashboard built in **Excel only**  
- **Descriptive Analytics** only (no forecasting/prescriptive models yet)  

---

## 🚀 Future Development  
- Add **forecasting models** (Prophet, ARIMA)  
- Integrate **real-time data refresh**  
- Expand to **Customer Segmentation (RFM/CLV)**  
- Deploy in **Power BI/Tableau** for scalability & interactivity  

---

## ▶️ How to Run  
1. Download repo files and open `US_Superstore_Dashboard.xlsm`  
2. Enable Macros for VBA functionality  
3. Use slicers (Category, Segment, Ship Mode) to interact  
4. Click **Create PPT** button to auto-export dashboard slides  

---
