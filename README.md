![Project-logo](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/Project-logo.png)
#### [EN](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/README.md) | [UA](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/README-UA.md) This material is also available in Ukrainian.   
---  
<div align="center">  
    
## Coffee sales analysis<br>(Tableau Public)   
  
</div>  
  
## Project description  
    
The project is dedicated to developing interactive analytical dashboards in **Tableau** based on transactional data of a coffee bean sales company in three international markets (USA, Ireland, UK).
***Project goal*** is to transform raw order data into clear business insights for management that allow to assess sales efficiency, analyze customer behavior, product portfolio profitability structure and identify key time trends.  
  
## Basic dashboard functionality  
  
The project is divided into two logical blocks of analytics:  
  
### 1. Dashboard #1: Customer and Product Analysis  
  
- **Geographical Sales Matrix:** Detailed table of distribution of the number of orders, revenue, net profit and coffee volume (in kg) by country, roast type and coffee variety.  
- **Top Customers Analysis by Year:** Dynamic table of the best customers with the ability to adjust their number using the `Top N Customers` parameter.  
- **Interactive Treemap:** Visualization of the customer base, where the user can independently choose the ranking metric (Sales, Profit, Number of orders, Weight) via the `Select Measure` parameter.  
- **Order Distribution (Box-Plot):** Analysis of the dispersion of the weight of orders by each country to identify consumer anomalies and the median check.  
  
### 2. Dashboard #2: Time Series and KPI Trend Analysis  
  
- **Profitability and ARPPU:** Quarterly dynamics of net profit, combined with the ARPPU (Average Revenue Per Paying User) metric on a single axis (Dual Axis) with the construction of trend lines to predict business scaling.  
- **Monthly Profit KPI Card:** Bar chart with automatic color coding by margin level (Green: >10.5%, Yellow: 9.5%–10.5%, Red: <9.5%).  
- **Moving Average of Sales (Moving Average):** Zonal chart of monthly revenue, superimposed on a 12-month moving average line to smooth seasonality and assess the global trend.  
- **MoM (Month-over-Month) Analysis:** Monthly dynamics of sales growth or decline compared to the previous month with color highlighting of growth/decline zones.  
  
---   
  
## Technology stack and tools  
  
- **Data source:** Excel (`Raw_Data.xlsx`) — 3 relational tables (`orders`, `customers`, `products`).  
- **Data modeling:** Tableau Logical relationships (**Relationships / Data model**) by keys `Customer ID` and `Product ID` to prevent duplication of rows (Data Duplication).  
- **Visualization tool:** Tableau Desktop / Tableau Public.  
- **Calculations (Calculated Fields):** Complex aggregated and logical indicators have been implemented (`Profit Margin`, `ARPPU`, `Moving Average`, `CASE/IF-THEN` logic for parameters).  
  
---  
  
## Project implementation  
  
- Loaded data from Raw_Data.xlsx to Tableau Public and created a data model.  
  
  ![Data model](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_3.png)  
  
- The necessary calculation fields have been created.  
  
   ![Calculation fields](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_4.png)  
     
- An analytical table of sales by country has been formed, grouped by roasting type and coffee variety, indicators of the number of orders, sales volume, profit, and total mass of coffee sold.  
    
   ![Sales table](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_5.png)  
  
-  Customer analysis by number of orders, sales level, profit, total mass of coffee sold by year  
  
   ![Sales table](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_7.png)
  
 - An additional calculation field 'Measure for Treemap' has been created for further use with the customer segmentation parameter

  ![Top customers by sales level](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_8.png)  
   
 - Created a 'Select Measure' parameter to allow the user to choose the TOP customer segmentation criterion  

   ![Select Measure](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_9.png)  
   
 - A sheet has been created with the calculation of TOP customers by the selected measure

   ![Top customers by measure](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_10.png) 

 - A sheet has been created with an analysis of the distribution of orders from different countries by the amount of coffee sold in kg.

  ![Distribution of orders by country](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_11.png)  

  - A summary dashboard with coffee sales analysis and customer segmentation was created

  ![Sales and customer analysisy](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_12.png)  

**Друга частина проекту**  
    
 - Created a sheet with visualization of Profitability and ARPPU, used line graphs. Provided interim conclusions  
  
   ![Quarterly profit and ARPPU](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_13.png) 
   
 - Created a sheet with visualization of profitability by month and automatic color coding by margin level  
   
   ![Monthly profit and profitability](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_15.png)  
    
 - A sheet has been created with a chart of monthly sales over a period and a line chart that calculates the average annual sales level (average monthly value over the last 12 months)  
    
   ![Monthly sales](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_16.png)  
  
 - A sheet was created showing the monthly dynamics of sales growth/decline compared to the previous month with color highlighting of growth/decline zones  
  
   ![Monthly Sales Change](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_17.png)  
  
 - Summary dashboard created - Analysis of profit and sales dynamics (Dashboard  2: Profit and Sales Dynamics Analysis)  
  
   ![Profit and Sales Dynamics Analysis](https://github.com/isachenko-andrii/Coffee-Sales-Analysis/blob/main/img/csa_18.png)  
      
## Key findings    
  
***Strengths of the business***  
  
- **Stable margin:** for 3.5 years, the margin has been maintained at around 10%, which indicates disciplined pricing and cost control.  
- **Broad customer base:** 913 unique customers without excessive dependence on one buyer — healthy risk distribution.  
- **Growth in 2021:** +13.6% sales and +22.3% orders — the business demonstrates the ability to grow.  
- **Good product mix:** 4 coffee varieties × 3 roasts × 4 sizes = 48 items, which allows you to satisfy different tastes.  
  
***Weaknesses and risks***  
  
- **Over-reliance on the US (79% of revenue):** any deterioration in the US market critically affects the entire business.  
- **Loyalty program is not effective:** loyalty cards do not encourage customers to spend more ($47 vs $51).  
- **Low margin Robusta (6%):** although it gives 20% of sales, it contributes less to profit compared to weight.  
- **Slowdown in 2022:** sales pace in 2022 is lower than previous years, the reason needs to be investigated.  
  
***Undiscovered potential***  
  
- **Liberica is undersold:** highest margin (13%), but only 3rd in volume — there is an opportunity to increase sales through marketing.  
- **Ireland and the UK are underdeveloped:** 21% share for the two countries with a similar margin with the US — potential for geographical diversification.  
- **Large packs (2.5 kg):** generate 53% of revenue, but are not the subject of active promotion — it is worth increasing focus.  
  
## Strategic recommendations  
  
<table align="center">
<thead>
<tr>
<th> Priority </th>
<th> Recommendation </th>
<th> Expected effect </th>
</tr>
</thead>
<tbody>
<tr>
<td> 🔴Critical </td>
<td>
Investigate the reason for the decline in 2022: compare monthly sales with 2021, identify lost customers or a decrease in the average check.
</td>
<td>
Stop the decline, restore growth.
</td>
</tr>
<tr>
<td> 🔴Critical </td>
<td>
Review the loyalty program: add real incentives (discounts for 2.5 kg packaging, volume bonuses) so that cards stimulate higher spending.
</td>
<td>
Increase ARPPU of loyal customers by 10%+
</td>
</tr>
<tr>
<td> 🟡Important </td>
<td>
Increase marketing budget for Liberica: conduct campaigns about unique taste and premiumness, position as a top product.
</td>
<td>
Increase Liberica share from 27% to 33%+
</td>
</tr>
<tr>
<td> 🟡Important </td>
<td>
Develop a strategy for entering the UK market: find local distributors, launch targeted campaigns.
</td>
<td>
Increase UK share from 6% to 10-12%
</td>
</tr>
<tr>
<td> 🟢Opportunity </td>
<td>
Launch large package program: discounts/bonuses when ordering 2.5 kg, package offers for regular customers.
</td>
<td>
Increase average order volume.
</td>
</tr>
<tr>
<td> 🟢Opportunity </td>
<td>
Reduce or review Robusta: with a margin of 6% vs 13% Liberica - it is worth analyzing profitability and possible repositioning.
</td>
<td>
Improve overall margin by 0.5-1%.
</td>
</tr>
<tr>
<td> 🟢Opportunity </td>
<td>
Introduce autumn seasonal marketing (Sep-Nov): sales naturally increase in autumn - it is worth reinforcing this trend with promotions and new positions.
</td>
<td>
Strengthen the peak season by 15-20%.
</td>
</tr>
</tbody>
</table>
  
## Result  
  
Coffee business shows stable performance with ~10% margin for 3.5 years and growth in 2021. However, there are two key challenges: slowdown in 2022 and excessive concentration in the US market.  
  
**Top priority** — investigate the reasons for the 2022 downturn and reform the loyalty program. Mid-term opportunity — aggressively promote Liberica as a premium product with the best margin, as well as develop the Irish and UK markets to diversify geographical risk.  
  
**Key recommendation** — Focus on quality over quantity: promote Liberica and large packages (2.5 kg) — this is a combination that gives maximum revenue with minimal effort. At the same time, fix the loyalty program so that it really retains customers and stimulates average check growth.  
  
## Project structure  
  
**Coffee-Sales-Analysis**/ — project catalog  
├── data/ — project data  
├── doc/ — technical specifications  
├── img/ — saved charts and dashboards  
├── twbx/ — project files  
├── LICENSE — MIT License  
├── project-logo.png — project cover  
├── README-UA.md — project description in Ukrainian   
└── README.md — project description in English  
  
## How to view a project  
  
1. Download the project file `Coffee Sales Analysis.twbx` from this repository.  
2. Open it with the free [Tableau Reader](https://www.tableau.com/products/reader) or Tableau Desktop.  
3. The project is also published on Tableau Public: [Coffee Sales Analysis](https://surl.li/fhpoop)  
  
## Contacts  
  
**Author:** [Andrii Isachenko](https://isachenko-andrii.github.io)  
**Position:** Junior Data Analyst  
**LinkedIn:** [Andrii Isachenko](https://www.linkedin.com/in/isachenko-andrii/)  
**Email:** andrii.isachenko@gmail.com  
  
## Acknowledgements  
  
- Thanks to the course [Data Analyst/GoIT](https://goit.global/ua/courses/data-analytics/), which was part of the work on this project.  
  
---  
  
**Project Status:** Completed.  
  
**License:** MIT License.  
