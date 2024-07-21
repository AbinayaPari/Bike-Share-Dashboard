# Bike-Share-Dashboard

### Project Overview
The aim of this project was to develop a SQL and Power BI dashboard to analyze and visualize hourly revenue, profit trends, and rider demographics, providing actionable insights for optimizing business performance and driving revenue growth

### Data Source
Bike Shares Data: A secondary dataset containing bike shares from the years 2020 and 2021, along with demographic details of customers, was used.

### Tools
- MySQL- Querying and Managing Dataset [Download Here](https://dev.mysql.com)
- PowerBI-Data Visulaization[Download Here](https://www.microsoft.com)
### Data Cleaning and Data Managing
SQL was used for querying and managing the dataset, enabling efficient extraction, filtering, and aggregation of relevant data for further analysis and visualization in Power BI.
```sqlwith cte as(
select * from bike_share_yr_0
union all
select* from bike_share_yr_1)

select 
dteday,
season,
a.yr,
weekday,
hr,
rider_type,
riders,
price,
COGS,
riders*price as revenue,
riders*price -COGS as profit
from cte a
left join cost_table b
on a.yr=b.yr;
```

### Data Visualization
Power BI was used for creating interactive visualizations and dashboards, allowing for intuitive analysis and presentation of the data to uncover insights and trends.##
### Results and Findings
The dashboard revealed peak earnings midday and early evening, especially between 10 and 15 hours, with Wednesday and Friday showing notably higher sales. With a profit margin of 0.45 and around 3 million riders, the project, completed ahead of the deadline, provided actionable insights, leading to a projected revenue increase.


