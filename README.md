# Supplier Insights

## Introduction
![](https://github.com/FadilatBraimah/Supplier-Insights/blob/5fc49011a9aea8649682cb948bfd8f53bfc0eb77/Supplierinsight.jpg) 
Enterprise Manufacturers Ltd, a leading manufacturing company, sources raw materials from various suppliers for production and maintenance. The company faced significant challenges due to the absence of a centralized procurement system, leading to difficulties in assessing supplier performance. To address these issues, data from multiple plants was consolidated to analyze supplier quality and identify performance bottlenecks. The dataset, "Supplier Insight Data," provided valuable information, including materials, defects, vendors, and downtime caused by defective materials. This documentation outlines how I tackled the project, deriving meaningful insights and actionable recommendations.

## Problem Statement
Enterprise Manufacturers Ltd was struggling with supplier management due to a lack of a centralized system. This led to difficulties in assessing supplier's performance, making it hard to identify which vendors were providing quality materials and which were not. The absence of standardized processes meant that different plants worked with different vendors, creating inconsistencies and inefficiencies. There was no clear way to trace the root causes of defects or the downtime resulting from defective materials. These challenges significantly impacted operational efficiency and made it difficult for the company to make data-driven decisions about supplier performance. To address these issues, the management team needed a clear understanding of supplier quality across all plants.

## Objectives
This project aimed to:
- Find out Which vendors/plants are causing the greatest defect quantity.
- Which vendors/plants are causing the greatest downtime?
- Is there a particular combination of material and vendor that performs poorly?
- Is there a particular combination of Vendor and plant that performs poorly?
- How does the same vendor and material perform across different plants?

## Tools Used
To achieve these goals, I used:
- Power BI: Used for visualizing the data.
- Power Query: To clean and prepare the data for analysis.
- DAX (Data Analysis Expressions): Used for calculations and measures for deeper insights. In this project, I wrote so advanced DAX formulas and learnt the use of parameters.

## Data Transformation and Modeling
I started by cleaning the data to remove duplicates and fix missing values. Then, I organized the data into a star schema. 
The schema centralizes a fact table surrounded by dimension tables to optimize data queries and visualizations. The fact table called the "Supplier Fact" table, holds the core metrics such as total defect quantity and total downtime minutes, as well as foreign keys linking to dimension tables. The dimension tables include Defect, Type Defect, Category, Vendor, Plant Location, Material Type, and Date. These tables were linked together with clear relationships to make analysis easier. I also created measures like total defect and total downtime. The downtime in minutes column was converted to hours as most organisations calculate their downtime in hours, which provided useful metrics for understanding trends and performance.
![](https://github.com/FadilatBraimah/Supplier-Insights/blob/5fc49011a9aea8649682cb948bfd8f53bfc0eb77/Datamodel.png)

## Creating a Date Table
I created a Date Table using DAX, ensuring it contained all necessary fields like months, quarters and days to allow seamless time-based filtering and comparisons, making the analysis more robust and insightful
![](https://github.com/FadilatBraimah/Supplier-Insights/blob/5fc49011a9aea8649682cb948bfd8f53bfc0eb77/Date.jpg)

## Data Visualization
This project contained five (5) pages of analysis dashboards excluding the landing page. Here are insights from some of the pages.
### Overview
![](https://github.com/FadilatBraimah/Supplier-Insights/blob/5fc49011a9aea8649682cb948bfd8f53bfc0eb77/Overviewvisual.jpg)
At the top, key performance indicators (KPIs) such as total defects, downtime hours, and a parameter which calculates the downtime cost per hour are displayed alongside their month-over-month and year-over-year changes, showing performance trends. 
- The total defect quantity is 2.60 billion, with a month-over-month increase of 4.25% and a year-over-year increase of 123.32%, this signifies a significant rise in defects. The total downtime hours amount to 215,810, reflecting a 4.39% increase from the previous month and a 123.45% increase from last year. Downtime cost per hour is $2.16 million, which has also increased by similar percentages. These metrics indicate an upward trend in operational challenges requiring immediate intervention.
- The monthly trend compares defect quantities for 2018 and 2019. In 2019, there was a noticeable increase in defects between July and October, which could indicate seasonal production issues or inefficiencies during these months.

## Vendor
![](https://github.com/FadilatBraimah/Supplier-Insights/blob/5fc49011a9aea8649682cb948bfd8f53bfc0eb77/vendor.jpg) 
- The vendor with the highest defect quantity is Yombu, contributing 15 million defects, followed closely by Avamm. The chart is sorted in descending order, making it easy to identify the top vendors contributing to defects. These high defect quantities highlight areas requiring immediate attention for quality improvement.
- The High-Risk Vendors scatter plot shows vendors with the highest defect quantities and a significant impact on downtime. The vendors clustered in the upper-right corner are responsible for the largest defects and downtime, indicating critical risks to operations.
- The Medium-Risk Vendors scatter plot represents vendors with moderate defect quantities and impact. These vendors show a balance between performance and risk, but they still require monitoring to ensure quality.
- The Low-Risk Vendors scatter plot features vendors with minimal defects and downtime. Vendors in this group exemplify strong performance and reliability.

## Insights 
- Vendors like Avamm and Yombu are the largest contributors to defects, with over 15 million defects each, making them the top priority for quality checks.
- Plants like Hingham and Charles City report the highest downtime, with over 99 million hours each, suggesting these facilities may require operational improvements or better maintenance strategies.
- The Mechanical category accounts for the largest defects, totalling 820.83 million, followed by Logistics and Packaging. This breakdown provides insight into which processes need the most attention.

## Recommendations 


VIEW THE INTERACTIVE DASHBOARD HERE!!! ![Dashbord](https://app.powerbi.com/view?r=eyJrIjoiMzAyZDQ1ZTAtOTJjYi00ZmYxLWFhYTMtNmVhYjdjMmJhNDg4IiwidCI6IjgyMTFmMzM1LWI0YWUtNGQ3NS04ODdkLTdkZGM4ZTJlZDRhYiJ9)

*_THANK YOU FOR READING!!!!!_* 🥰
![](https://github.com/FadilatBraimah/Supplier-Insights/blob/5fc49011a9aea8649682cb948bfd8f53bfc0eb77/thankyounote.jpeg)
