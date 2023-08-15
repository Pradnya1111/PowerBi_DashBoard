# PowerBi_DashBoard
Maven Market PowerBi Dashboard <br>
Created Dashboard using Power BI with Maven Market dataset.<br>
Maven Market Dashboard:
![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/ff87ab9b-4bc9-4fe1-9281-22daca829154)


Maven Market Has the Following Dataset:
1) Customers
2) Products
3) Regions
4) Return Data
5) Stores
6) Transaction Data<br>

# Cleaning and Preparing Data:
In this phase, confirmed all data types are accurate, we have created new columns based on existing data such as in Customer Table we have added new column named "full_name" merging first_name and last_name, separated by space, added new column "birth_year" extracting the year from birthdate column and formated as text, created conditional column named "has_children"  which equals "N" if total childrens are 0, otherwise "Y". 
In Products table we used statistical tool to return the number of distinct product brands, followed by distinct product names. Added calculated column to get discounted price which equals to 90% of original retail price (formated as fixed decimal number and rounded to 2 digits), Replaced the null values with zeros.
In Stores Table we made sure that headers have been promoted. Added calculated column named full_address by merging store city, state and country comma and space separated. Also added calculated column named "area_code" by extracting the characters before dash in phone.
In Calendar table added following columns start of week, start of month, name of day, quater of year, name of month, year.
For Transactions Data, we added new folder on desktop  containing both files and in powerbi we combined the files and removed the source column.<br>

![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/e3b2bf93-4d02-4472-9f00-dbd31af17488)<br>

# Building Relationships:
 Created one-to-many relationship between Data(Fact) and Dimentions(Lookup) tables, Data going through only "Downstream"
 
![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/edb9aed8-6c27-421d-b09a-7b187bd188ea)<br>

# DAX Measures:
In Data view, we have added the following calculated columns:<br>

![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/7ec6e0d2-611f-45f6-b114-041f1d7be6f1)<br>

# Visualizing Data:
Inserted the Matrix visual to show Total Transactions, Total Profit, Total Margin and Return Rate by Product Brand(Top N filter to show top 30 product brands by total transcations sorting  descending). Added KPI cards to show Total Transactions with start of month as trend axis and last month transaction as target goal, created two more copies for Total Profit and Total Returns(low is good).<br>
Added Map visual to show Total Transaction by store city, added selection controls menu in formatting pane to show Select All, also added Slicer.<br>
Added Treemap visual to break down Total Transactions by store country.
Added Gauge Chart to show Total Revenue against Revenue Target(Added visual level Top N filter to show latest start of month).








