Woodgrove Ads – Microsoft Advertising Sales Executive Dashboard
Role being mimicked
Sales Operations Data Analyst – Microsoft Advertising.
​

As the Sales Operations Data Analyst, you own an executive‑ready sales dashboard for Woodgrove Ads, pulling and shaping data from multiple sources and turning a complex sales pipeline into clear, usable insights for leaders.

Business scenario
Woodgrove Ads sells Microsoft Advertising inventory (Search, Display, Video) to enterprise customers. Stakeholders:

VP Sales, Advertising – needs high‑level revenue and pipeline KPIs by quarter.

Regional Sales Directors – need performance by region, manager, and rep.

Marketing Lead – cares about campaign performance and ROAS by product/account.
​

The dashboard is designed as a one‑screen executive overview with the ability to slice by region, manager, rep, and industry.

Business goals
Track booked revenue and open pipeline versus quarterly targets.

Identify which ad products, regions, managers, and accounts drive growth.

Monitor pipeline health (coverage, win rate, cycle length, deal size).

Surface large, at‑risk opportunities so leaders can intervene early.

Core questions the dashboard answers
Are we on track to hit quarterly revenue targets overall and by region?

Which regions, managers, reps, industries, and accounts are over‑ or under‑performing?

How healthy is the pipeline (coverage, win rate, average sales cycle, average deal size)?

Where are the biggest risks in the pipeline (large, overdue, still‑open deals)?

Users and key views
Executives (VP Sales, C‑level):

Top KPI strip: Average Sales Cycle, Average Deal Size, Win Rate, Total Revenue, Total Pipeline.

Revenue vs Target gauge (by current filter context).

Regional Sales Directors and Managers:

Revenue by Account (Top N), Revenue by Industry.

Revenue and Win Rate by Rep.

Pipeline by Stage (Qualified/Proposal/Negotiation).

Marketing / Product:

Ability to slice all views by Industry (proxy for product/segment) and Region to see which combinations perform best.
​

All visuals respond to slicers for Region, Manager, Rep, Industry, and (optionally) Quarter.

Tech stack
Data generation: Python script to generate synthetic opportunities, revenue, and pipeline data.

Storage: CSV files following a simple star schema (dimensions for Date, Account, Rep, Region, Industry; facts for Opportunities and Revenue).

BI: Power BI Desktop

Power Query for data cleaning and typing (e.g., converting CloseDate to Date).

Data model with relationships between Date, Account, Rep, Industry, and fact tables.

DAX measures for Total Revenue, Total Pipeline, Win Rate, Average Sales Cycle, Average Deal Size, and Target‑based KPIs.

Dashboard contents (current version)
KPI cards:

Average Sales Cycle, Average Deal Size, Win Rate, Total Revenue, Total Pipeline.

Visuals:

Revenue and Win Rate by Rep.

Total Revenue by Account (Top N).

Total Revenue by Industry.

Revenue Target vs Total Revenue gauge.

Total Pipeline by Stage donut/bar chart.

Filters/Slicers:

Region, Manager, Rep, Industry (and optional Date/Quarter).

## Power BI Dashboard

This project includes a Power BI dashboard for executive insights and sales performance analysis. The dashboard visualizes:
- Average Sales Cycle
- Average Deal Size
- Win Rate
- Total Revenue
- Total Pipeline
- Revenue and Win Rate by Sales Rep
- Revenue by Account and Industry
- Pipeline by Stage
- Revenue Target vs. Actual

You can find the Power BI dashboard file here:
- [powerbi/Woodgrove Data Power Bi.pbip](powerbi/Woodgrove%20Data%20Power%20Bi.pbip)

![Power BI Dashboard Overview](docs/powerbi_dashboard_overview.png)