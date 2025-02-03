# **Sales Performance Analysis**  

## 📘 Overview  
This **Sales Performance Analysis** project aims to create a **dashboard** that helps clients **analyze sales performance**. The dashboard provides insights into **monthly trends (MOM%), yearly trends (YOY%), best-selling products, and customer-preferred promotions**.  

## 🎯 Objective  
The objective of this project is to:  
- **Track overall sales performance** using key metrics.  
- **Analyze trends** to determine whether sales are improving or declining.  
- **Identify top-selling products and customer preferences for promotions**.  
- **Support business decision-making** with data-driven insights.  

---

## 📊 Key Metrics  

- **Total Revenue**: Overall revenue, adjustable by filters.  
- **Month-over-Month Growth (MOM%)**: Measures percentage change in revenue compared to the previous month.  
- **Year-over-Year Growth (YOY%)**: Compares revenue from the same period in the previous year.  
- **Basket Size**: Average number of items per transaction.  
- **Ticket Size**: Average revenue per transaction.  
- **Overall Sales Trend**: Monitors revenue patterns over time.

- ## 🛠️ Storyboard
-   ### Overview Dashboard Analysis
  ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Analyst/Sales_Performance_Analysis/StoryboardSale%20performance%20Overview.png)
 
This dashboard is a mockup designed to provide a quick and comprehensive overview for stakeholders. It summarizes key metrics, allowing users to quickly understand the current state of the data. The following aspects are highlighted:

- **Total Sales**: Displays the overall sales performance, both including and excluding VAT.
- **User Statistics**: Provides the total number of users, active users, new users, and unique buyers.
- **Store Statistics**: Shows the total number of stores contributing to the sales.
- **Conversion Insights**: Tracks active users, conversions, and drop-off rates over time to understand trends in customer engagement.
- **Average Time per Order**: Highlights the efficiency of customer interactions in terms of time.
- **Conversion Rate**: Displays the percentage of active users who successfully converted into buyers.

The dashboard visualizes trends, such as comparing active users against conversions and drop-offs, and calculates the conversion rate percentage. This enables quick decision-making and a clear understanding of how user activity impacts overall sales performance.
-   ### Order Performance Analysis
  ![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Analyst/Sales_Performance_Analysis/Storyboard%20Order%20Performance.png)
This dashboard focuses on analyzing order performance to provide actionable insights into customer behavior and sales patterns. Key aspects include:

- **Order Trends**: Displays the total number of orders made over time, segmented by successful and canceled reservations.
- **Traffic Analysis**: Identifies peak order times during the day and highlights which hours experience the highest traffic and order volume.
- **Order Creation Time**: Shows the distribution of orders by creation time to pinpoint when most customers place their orders.
- **Popular Products**: Identifies top-selling products within each order to understand customer preferences.

These insights enable better decision-making for upselling strategies and planning effective promotional campaigns to maximize sales during high-traffic periods.

-   ### Cohort Analysis Dashboard
![ชื่อรูปภาพ](https://github.com/thanaphongK37/Data-Science-and-Data-Analyst-Project/blob/main/Data_Analyst/Sales_Performance_Analysis/Storyboard%20Cohort%20Rate.png)

This dashboard evaluates customer retention over a 30-day period to understand engagement trends and loyalty. Key features include:

- **Daily Retention Rates**: Tracks the percentage of users who return on subsequent days after their initial visit or purchase.
- **Initial Customer Count**: Displays the number of users on Day 1 (100%) for each cohort group based on the starting date.
- **Behavior Analysis**: Provides insights into the percentage of users retained on specific days (e.g., Day 2, Day 7, Day 30) to identify drop-off points.
- **Customer Loyalty**: Assesses whether the products or services meet customer needs by determining how many return after their initial interaction.

This analysis helps in identifying patterns of customer behavior, improving product offerings, and crafting strategies to increase retention rates.


---

## 🗄️ Data Sources  
This project utilizes two main datasets:  
1. **Customer Profile Data**: Contains demographic and behavioral attributes.  
2. **Transaction History**: Records of past purchases, including product details, prices, and timestamps.  

---

## 🔧 Technologies Used  

- **SQL (Databricks)**: Data extraction and transformation.  
- **Apache Superset**: Interactive dashboard creation for data visualization.  

---

## 📌 Current Status  
✅ Dashboard is implemented and actively used for sales performance monitoring.  
🔄 Continuous improvements based on stakeholder feedback.  
📈 Potential enhancements include deeper customer segmentation and predictive sales analytics.  
