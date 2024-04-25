## This project demonstrates the creation of a project powertbi dashboard of Ecommerce Sales  data 
## It covers data extraction from a SQL database, data processing and DAX queries, dashboard design, and sharing ## insights. The project aims to provide real-time insights into credit card operations, enabling stakeholders to ## monitor and analyze performance efficiently.  

- Devlope Comprehensive yearly dashborad provides real time weekly insight  insights 
- insight into key performance matrix and trend 
- Enable to stasck honder to moniter and analyze credit card operation effectively  

# Requirements : 

Ecommerce Sales Dashboard

Problem Statement

Import data through Ms SQL server

Connect powerbi in MS SQL Server

#Data Cleaning

#Data Processing

#Data modelling

#Time Intelligence function

#Data Visualization

#Creating Dashboard

# Creating Insight

Create KPI ytd sales . profit, Quantity sold , profit margin

Find year and year growth for each kpl & show ytd sparkline for each measure

Find ytd sales performance for each state

Top 5 and bottom 5 product by sales

Sales by region to know worst and best and worst performing region all over country

Ytd SALES by shipping type to get best shipping type percentage


## 1. Project objective
## 2. Data from SQL
## 3. Data processing & DAX
## 4. Dashboard & insights
## 5. Export & share project

### Project Objective

- To develop a Pizza Sales card Yearly  dashboard that
provides real-time insights into key
performance metrics and trends,
enabling stakeholders to monitor
and analyze Ecommerce data wrt date time 

### step. 1 import dta from sql   

### step.2 load data tables from sql 

### step. 3 Data processing and DAX queries   

 Dax Query 
 ### calender 
- Month = FORMAT(calender[Date],"mmmm") 
- Month number = MONTH(calender[Date])
- Year = YEAR(calender[Date]) 

### Ecommerce data 
- Profit background Color = IF([YOY Profit]>0, "green", "red" )
- Profit Icon = var positive_icon = UNICHAR(9650)
            var negative_icon = UNICHAR(9660)
            var result = IF([YOY Profit]>0,positive_icon,negative_icon)
            return result 


- Profit Icon Color = IF([YOY Profit]>0 ,"green" ,"red")  
- Profit Margin = SUM(ecommerce_data[profit_per_order])/SUM(ecommerce_data[sales_per_order]) 

- Profit Margin background Color = IF([YOY Profit Margin]>0, "green", "red" )

- Profit Margin Icon = var positive_icon = UNICHAR(9650)
            var negative_icon = UNICHAR(9660)
            var result = IF([YOY Profit Margin]>0,positive_icon,negative_icon)
            return result 


- PYTD Profit = CALCULATE(SUM(ecommerce_data[profit_per_order]),DATESYTD(SAMEPERIODLASTYEAR(calender[Date])))

- PYTD Profit Margin = CALCULATE((ecommerce_data[Profit Margin]),DATESYTD(SAMEPERIODLASTYEAR(calender[Date]))) 


- PYTD Quantity = CALCULATE(SUM(ecommerce_data[order_quantity]),DATESYTD(SAMEPERIODLASTYEAR(calender[Date]))) 

- PYTD Sales = CALCULATE(SUM(ecommerce_data[sales_per_order]),DATESYTD(SAMEPERIODLASTYEAR(calender[Date])))  

- Quantity background Color = IF([YOY Quantity]>0 ,"green" ,"red") 

- Quantity Icon = var positive_icon = UNICHAR(9650)
            var negative_icon = UNICHAR(9660)
            var result = IF([YOY Quantity]>0,positive_icon,negative_icon)
            return result




## year to date sales is 11.53 M
## year to date Profit is 1.34 M
## year to date Profit Margin 11.58 % 
## year to date Quantity  107.2 % 

- •  West area have most sales 32.23 % 
- • Standard class have more Most shipping Class 60.56 % 



 



## This project demonstrates the creation of a comprehensive credit card dashboard using Power BI. It covers data extraction from a SQL database, data processing and DAX queries, dashboard design, and sharing insights. The project aims to provide real-time insights 