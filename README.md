# US Superstore Business Analytics Dashboard (Excel)

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
- **Period:** 2014–2017  
- **Size:** 10,001 rows × 21 fields (after cleaning)  
- **Main fields:** `Order Date`, `Ship Date`, `Ship Mode`, `Customer`, `Segment`, `Region`, `Category`, `Sub-category`, `Sales`, `Quantity`, `Discount`, `Profit`  

**Data preparation (Power Query):**
- Promoted headers, formatted data types  
- Removed invalid/missing values (4 rows)  
- Removed duplicates (7 rows)  
- Loaded cleaned dataset for dashboard creation
<img width="317" height="511" alt="image" src="https://github.com/user-attachments/assets/c7ad2908-8e19-493a-b4a8-1e5114043cec" />

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
<img width="1575" height="711" alt="image" src="https://github.com/user-attachments/assets/8e3c5df4-6df6-42af-9914-859695b5a919" />

---

## 6. Key Insights
### Business Performance Analysis & Recommendations (2017 vs 2016)

### 1. Overall KPIs
- **Sales (2017):** 733,215.3  
- **Sales (2016):** 609,205.6  
- **Sales Growth:** +20.36%  
- **Profit (2017):** 93,439.3  
- **Profit (2016):** 81,795.2  
- **Profit Growth:** +14.24%  

**Insight:**  
2017 was a successful year with strong sales and profit growth. However, the profit growth rate (+14.24%) lagged behind sales growth (+20.36%), indicating potential margin pressure.

**Recommendation:**  
Focus on cost control and pricing optimization to ensure profit growth keeps pace with sales growth.

---

### 2. Subcategory Performance

#### Overall Top 10 Subcategories
- **Total Sales 2017:** 642,486 (+20.4% vs 2016)
- Strong performers:  
  - Appliances (+64.8%)  
  - Binders (+46.5%)  
  - Accessories (+43.1%)  
  - Phones, Chairs, Storage, Copiers (double-digit growth)  
- Weak performers:  
  - Tables (+0.1%)  
  - Machines (-22.1%)  

**Recommendation:**  
- Increase investment in **high-growth subcategories** (Appliances, Binders, Accessories).  
- Reassess strategy for **Machines** and **Tables**, focusing on product positioning, pricing, or potential product refresh.

---

#### Furniture
- **Total Sales 2017:** 215,387 (+8.3%)  
- Strong growth: Bookcases (+14.3%), Chairs (+13.9%)  
- Weak growth: Furnishings (+3.7%), Tables (+0.1%)  

**Recommendation:**  
- Maintain growth in **Chairs** and **Bookcases** with targeted promotions.  
- Review marketing and pricing strategy for **Tables**, as growth has stalled despite being top 5 in sales.

---

#### Office Supplies
- **Total Sales 2017:** 246,097 (+33.8%)  
- Strong growth: Appliances (+64.8%), Art (+48.7%), Binders (+46.5%), Paper, Labels  
- Decline: Envelopes (-28.6%), Fasteners (-10.7%)  

**Recommendation:**  
- Focus expansion on **Appliances, Art, and Binders**.  
- Investigate demand shifts for **Envelopes and Fasteners** (digitalization, product relevance) and decide whether to phase out or reposition.

---

#### Technology
- **Total Sales 2017:** 271,731 (+20.0%)  
- Strong growth: Accessories (+43.1%), Phones (+33.4%), Copiers (+26.8%)  
- Decline: Machines (-22.1%)  

**Recommendation:**  
- Capitalize on strong demand for **Phones and Accessories** with bundled sales and promotions.  
- Conduct a deep dive into **Machines**’s decline to assess whether it is structural (market shrinkage) or competitive (pricing, product features).

---

### 3. City-Level Performance

#### Overall Top 10 Cities
- **Total Sales 2017:** 339,408 (+27.5%)  
- Top growth: Seattle (+252.7%), Columbus (+84.8%), New York City (+58.6%)  
- Decline: Lafayette (-69.5%), Detroit (-42.7%), Los Angeles (-13.3%), Houston (-1.4%)  

**Recommendation:**  
- Double down on **Seattle, Columbus, and NYC** with stronger sales coverage.  
- Diagnose causes of decline in **Detroit and Lafayette** — may require local pricing adjustments or channel strategy changes.

---

#### Furniture by City
- **Total Sales 2017:** 97,810 (+6.7%)  
- Top growth: Chicago (+99.4%), Philadelphia (+151.9%), Seattle (+139.5%)  
- Decline: Springfield (-76.7%), San Diego (-53.9%), Houston (-36.1%)  

**Recommendation:**  
- Scale efforts in **Philadelphia and Seattle** as they show explosive growth.  
- Reduce exposure or redesign product mix in declining cities.

---

#### Office Supplies by City
- **Total Sales 2017:** 105,216 (+22.7%)  
- Top growth: Seattle (+178.4%), Springfield, Philadelphia, Columbus (>90%)  
- Decline: Detroit (-82.9%), NYC (+0.7% flat growth)  

**Recommendation:**  
- Explore why **NYC** is stagnant despite being the top sales contributor.  
- Consider shifting inventory from **Detroit** to higher-performing cities.

---

#### Technology by City
- **Total Sales 2017:** 142,183 (+33.9%)  
- Top growth: Newark (+643.7%), Seattle (+490.9%), NYC (+202.1%), Columbus (+174.3%), SF (+97.2%)  
- Decline: Lafayette (-97.1%), San Diego (-88.3%), Philadelphia, Chicago, LA  

**Recommendation:**  
- Treat **Newark and Seattle** as breakthrough markets with untapped potential.  
- Investigate **San Diego and Lafayette**’s collapse to avoid further losses.

---

### 4. Segment Performance

#### Consumer
- **Total Sales 2017:** 287,389 (+12.2%)  
- Strong growth: Appliances (+101.8%), Phones (+54.5%), Copiers, Binders (>45%)  
- Decline: Machines (-88.8%), Storage (-11.7%), Accessories (-2.2%)  

**Recommendation:**  
- Strengthen focus on **Phones and Appliances**.  
- Address **Machines** collapse — likely due to technology substitution or outdated offerings.

---

#### Corporate
- **Total Sales 2017:** 214,098 (+16.3%)  
- Strong growth: Binders (+161.2%), Appliances (+117.4%), Accessories (+90.4%), Storage (+51.9%), Machines (+63.4%)  
- Decline: Tables (-46.4%), Copiers (-56.9%), Chairs (-17.6%)  

**Recommendation:**  
- Push **Binders, Appliances, Accessories** with B2B campaigns.  
- Reconsider strategy for **Tables and Copiers**, which are underperforming in corporate use cases.

---

#### Home Office
- **Total Sales 2017:** 150,456 (+60.9%)  
- Strong growth: Copiers (+234.5%), Tables (+200.2%), Accessories (+123.4%), Machines (+131.0%), Chairs/Furnishings (>65%)  
- Decline: Binders (-29.9%)  

**Recommendation:**  
- Expand aggressively in **Home Office** segment, leveraging remote work trends.  
- Limit investment in **Binders**, which show clear decline in home use.

---

### 5. Profit by State
- Top profit: California (76,381.4), New York (74,038.5), Washington (33,402.7), Michigan (24,463.2)  
- Heavy losses: Texas (-25,729.4), Ohio (-16,971.4), Pennsylvania (-15,560.0), Illinois (-12,607.9)  
- Mid-sized states like Indiana, Virginia, Georgia, Kentucky show strong profitability.  

**Recommendation:**  
- Protect profits in **CA, NY, WA, MI** with sustained investment.  
- Audit cost structure and sales strategy in **TX, OH, PA, IL** to stop losses.  
- Replicate successful strategies from **Indiana, Virginia, and Georgia** in similar markets.

---

### 6. Seasonality Analysis
- Sales consistently **peak in Q4 (Nov–Dec)**.  
- Drop in **Oct 2017** requires investigation.  
- Overall sales trend upward year-over-year.  

**Recommendation:**  
- Maximize marketing efforts in **Q4**.  
- Investigate October decline (competitor promotion, supply chain, or pricing issue).  

---

### 7. State-Level Sales Concentration
- **Highest Sales:** California (457,688), New York (310,876) — dominant markets.  
- **Lowest Sales:** Idaho (305), South Dakota, Nebraska, Iowa, Kansas (300–650).  

**Recommendation:**  
- Prioritize **CA and NY** for major revenue growth.  
- Consider whether to scale back in extremely low-performing states, or adopt low-cost digital strategies to test potential.

---

### Final Recommendations
1. **Focus expansion** on high-growth subcategories (Appliances, Phones, Binders, Accessories).  
2. **Fix underperformers** like Machines, Tables, Envelopes, and Copiers through repositioning or rationalization.  
3. **Double down** on breakout cities (Seattle, Newark, Philadelphia) and scale back in collapsing markets (Detroit, Lafayette, San Diego).  
4. **Leverage seasonality** with strong Q4 campaigns to capture holiday demand.  
5. **Rebalance state strategy**: protect profits in CA/NY, stop losses in TX/OH/PA/IL, and replicate success in mid-sized states.  
6. **Segment-specific targeting**:  
   - Consumer → push Phones & Appliances.  
   - Corporate → push Binders & Accessories.  
   - Home Office → push Copiers, Tables, and Accessories.  

**Overall:**  
The company achieved robust growth in 2017 but with uneven performance across products, cities, and states. Strategic focus should be on consolidating high-growth areas, fixing loss-making regions, and maximizing seasonal opportunities.

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
