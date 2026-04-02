# car-sales-dashboard-powerbi
Power BI dashboard on 23,906 car sales records ($671M revenue) —  YTD/MTD KPIs, YoY growth, 6-page report with Sankey, Chord,  Map &amp; Drill-through across 6 data sources.


# 🚗 Car Sales Dashboard | Power BI Project

## About This Project

This is the most technically involved Power BI project 
I've built so far. It wasn't just about making charts — 
the data itself came from 6 different sources that had 
to be connected and modeled before any visualization 
could happen. The actual analysis part came after 
getting the data integration right.

The dataset covers 23,906 car sales transactions across 
2022–2023, spanning 30 companies, 7 dealer regions 
and $671.5 million in total sales.

---

## Data Sources Used

This is what made this project different from most 
Power BI projects. The data wasn't sitting in one 
clean CSV — it came from:

- **Excel files** — main sales data (Car Sales.xlsx) 
  with customer, company, model and pricing info
- **SQL Server export** — dealer names, dealer numbers 
  and regional mapping (Car_sql.xlsx)
- **Access Database** — Car_access.accdb with 
  supplementary car attributes
- **XML File** — Car_DV.xml for additional data points
- **Separate Excel** — Car.xlsx with engine, 
  transmission, color and body style details
- **Power BI Dataset** — combined model 
  after integration

All 6 sources were merged in Power Query using 
Car_id as the common key across tables. Getting 
the relationships right in the data model before 
writing a single DAX measure took the most time.

---

## Report Pages — 6 Total

**OverView**
The main landing page. Shows YTD Total Sales, 
YTD Avg Price and YTD Cars Sold as KPI cards 
with MTD comparison and YoY growth indicators. 
Also has a weekly area chart for sales trend, 
a Sankey diagram, Chord diagram, map visual 
and donut chart — all with 4 slicers for 
dynamic filtering.

**Total Sales Per Company**
Table showing YTD Total Sales broken down by 
each of the 30 companies, alongside a treemap 
for visual market share comparison. Chevrolet 
($47.6M) and Ford ($47.2M) lead very closely — 
the gap between them is less than $500K.

**Total Sales**
Detailed table view of all sales records with 
granular filtering capability. Useful for 
drilling into specific transactions.

**Company Sales**
Clustered bar chart and funnel chart comparing 
company performance side by side. The funnel 
view is particularly useful for seeing where 
the drop-off in volume happens as you go from 
top to bottom companies.

**Sales By Regions**
Map visual plotting sales by dealer region — 
Austin leads with 4,135 transactions, followed 
by Janesville (3,821) and Scottsdale (3,433). 
Bubble size represents YTD total sales volume.

**Drill_Drow (Drill Down)**
Column chart and a Line & Clustered Column 
combo chart for period-level drill down — 
weekly, monthly and yearly granularity. 
This page is specifically for time-based 
trend analysis.

---

## Key Metrics & DAX Measures Built

- **YTD Total Sales** — year-to-date revenue sum
- **YTD Avg Price** — year-to-date average car price
- **YTD Cars Sold** — year-to-date unit count
- **MTD KPI** — month-to-date equivalent of above
- **YoY Sales Growth** — percentage growth vs same 
  period prior year
- **YoY Avg Price Growth** — price trend year on year
- **YoY Cars Sold Growth** — unit volume trend
- **Sales Differences** — delta between periods 
  shown as KPI indicator cards
- **Sales Dif Colour** — conditional color formatting 
  on difference cards (green/red based on positive 
  or negative movement)
- **Max Point on Area Chart** — used to highlight 
  the peak week on the weekly trend chart
- **Cars Sold Colour / Avg Price Color** — 
  dynamic color logic for KPI formatting

---

## Key Findings From the Data

**$671.5M in total sales across 23,906 transactions**
Average price per car was $28,090 — which is 
reasonable for a mix of SUVs, Sedans, Hatchbacks 
and Passengers.

**SUVs dominate body style**
6,374 SUVs vs 6,128 Hatchbacks — almost equal. 
Sedans (4,488) and Passengers (3,945) are 
significantly behind. Hardtop is the least 
common at 2,971.

**Auto vs Manual is almost exactly split**
12,571 Auto vs 11,335 Manual — much closer 
than you'd expect. This comes through clearly 
in the Sankey diagram.

**Pale White is far and away the most popular color**
11,256 Pale White sales vs 7,857 Black and 
4,793 Red. The color-to-body-style relationship 
is what the Chord diagram visualizes.

**Chevrolet and Ford are neck and neck**
Only $423K difference in total sales between 
the top 2 companies across a 2-year period — 
on $47M+ each. Very competitive at the top.

---

## Custom Visuals Used

- **Sankey Diagram** — flow from Body Style 
  to Engine Type showing sales volume at each path
- **Chord Diagram** — connections between Body Style 
  and Color showing relationship with price
- **Network Navigator** — imported but used 
  for relationship mapping

---

## Tools Used

- **Power BI Desktop** — full data model, 
  DAX measures, all 6 report pages, custom visuals
- **Power Query (M language)** — data cleaning, 
  merging 6 sources, type casting, normalization
- **Excel** — source data files
- **Microsoft Access** — Car_access.accdb 
  as one of the data sources
- **XML** — Car_DV.xml as additional data source

---

## Files in This Repo

- `carsales - Power BI Desktop.pbix` — main Power BI file
- `Car Sales.xlsx` — primary dataset (23,906 rows, 16 cols)
- `Car.xlsx` — car attributes (engine, color, body style)
- `Car_sql.xlsx` — dealer and region data
- `Car_access.accdb` — Access database source
- `Car_DV.xml` — XML data source


  ## Photos

  <img width="1225" height="688" alt="image" src="https://github.com/user-attachments/assets/1c192c86-4c2c-489f-8f39-c81d10fe0303" />

  <img width="1224" height="688" alt="image" src="https://github.com/user-attachments/assets/1c056620-2fc5-4709-af1c-9affe40364df" />

  <img width="1219" height="687" alt="image" src="https://github.com/user-attachments/assets/aad7e814-53f9-4fa6-9ac3-fa3479f52d07" />

  <img width="1221" height="688" alt="image" src="https://github.com/user-attachments/assets/28b9a0f7-8575-44bb-847f-d77dfc1ee796" />

  <img width="1234" height="699" alt="image" src="https://github.com/user-attachments/assets/112c3c59-74dd-42cd-9ae5-d4af61422720" />

  <img width="1236" height="694" alt="image" src="https://github.com/user-attachments/assets/8ebc314e-ef42-4bbe-bde1-4fc31fd08863" />


## Conclusion 

This project leveraged Power BI's robust visualization capabilities to provide a comprehensive analysis of car sales data. By integrating multiple data sources and utilizing a variety of advanced visualization techniques, we were able to uncover valuable insights that can inform decision-making in the automotive industry. The interactive and dynamic nature of the dashboards allows users to explore the data in depth, providing a powerful tool for market analysis, forecasting, and strategic planning.


