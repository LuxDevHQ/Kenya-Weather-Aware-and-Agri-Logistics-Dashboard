### **Capstone Project:** Kenya Weather Aware E-Commerce and Agri-Logistics Dashboard.

---
## 1. Background / Problem Statement  
A Kenya-based e-commerce and produce-delivery startup operates in multiple cities (Nairobi, Mombasa, Kisumu, Eldoret, Nakuru). The company delivers goods ranging from electronics to fresh farm produce. 

The **operations team** has noticed that **weather conditions** especially rainfall and wind significantly impact delivery times, cancellations, and even supply availability. For agricultural produce, weather also affects planting and harvesting windows, which in turn influences stock levels and delivery demand.  

Currently, the company lacks a **centralized analytics system** to: 

- Monitor and forecast weather conditions for each city.  
- Predict operational risks to deliveries.  
- Offer simple, data-driven planting/harvest advisories for suppliers.  
- Integrate sales, customer, and product data into one interactive dashboard.  

 >> At the end the student should design and implement an **end-to-end data analytics solution** that automatically collects, processes, and visualizes both **operational data** (orders, deliveries, customers) and **environmental data** (weather forecasts).  

The solution should help the company:  
- Identify days and locations with **high delivery risk** due to adverse weather.  
- Recommend adjustments to **delivery schedules and routing**.  
- Provide simple **agricultural advisories** to suppliers based on weather forecasts.  
- Track sales, top products, and customer trends alongside weather impact.  
---

## 3. Objectives  
1. **Data Acquisition**  
   - Pull product data from a public e-commerce API of your choice. 
   - Pull customer and order data from a mock API, [fakerapi.it/fake-data-download](https://fakerapi.it/fake-data-download).  
   - Pull 5-day/3-hour weather forecast data for each target city (Nairobi, Mombasa, Kisumu, Eldoret, Nakuru) from **OpenWeather API**. 

2. **Data Processing & Storage.**  
   - Clean and merge datasets into a relational model (e.g., products, customers, orders, weather), please use PostgreSQL DB.  
   - Create derived metrics: daily rainfall (mm), rain risk flag, wind risk flag, delivery SLA performance, crop planting windows.  

3. **Data Automation.**  
   - Use a workflow orchestrator (e.g., Airflow) to schedule daily data collection and updates.  

4. **Analytics and Insights.**  
   - Measure the impact of weather on delivery performance.  
   - Identify risky delivery days in advance.  
   - Generate basic crop planting recommendations per city/region.  

5. **Visualization**  
   - Create a Power BI dashboard with:  
     - **Delivery Risk Map** of Kenya (by city).  
     - Weather vs. delivery SLA trend analysis.  
     - Top products and sales performance.  
     - Agricultural advisory panel (simple Yes/No planting windows).  

---

## 4. Project Deliverables:
 
1. **Project Report** detailing:  
   - Data sources and their role in the analysis.  
   - Data model (ER diagram).  
   - Data pipeline design (ETL steps).  
   - Description of calculated metrics and KPIs.  

2. **Automated Data Pipeline** (scheduled daily updates).  

3. **Final Power BI Dashboard** with:  
   - Operations overview (deliveries, on-time %, cancellations).  
   - Weather risk forecasts by city.  
   - Product sales analytics.  
   - Planting/harvest advisories.  

4. **Executive Summary** (1–2 pages) with key findings and recommendations.  

---

## 5. Suggested Metrics & KPIs  

### Operational KPIs  
- Total daily orders by city.  
- On-time delivery rate (%).  
- Cancellation rate (%).  
- Average delivery time (minutes).  

### Weather KPIs  
- Daily rainfall (mm).  
- Rain risk flag (rain ≥ 5 mm or ≥ 3 hours of rain).  
- Wind risk flag (wind ≥ 10 m/s).  
- Delivery risk index (combined rain/wind risk).  

### Agriculture KPIs  
- 7-day cumulative rainfall (mm).  
- Planting window flag (rain ≥ 20 mm in 7 days, no heatwave).  
- Weather risk to crops (heavy rain, high wind, or heat stress).  

---

## 6. Constraints & Considerations  
- Assume free tier API limits for OpenWeather.  
- Use public mock APIs for products and customers (no sensitive data).  
- Crop recommendations are educational and generic — actual farming decisions require local agronomy expertise.  

---

## 7. Expected Outcome  
By the end of the project, the team will have a **working analytics platform** that:  
- Automates data collection from multiple APIs.  
- Stores and models data in a relational database.  
- Produces actionable insights in an interactive Power BI dashboard.  
- Demonstrates the ability to link environmental data with operational and agricultural decisions.

## **8. Interview Questions**

1. **Data Acquisition**  
   - How would you authenticate and handle API rate limits when working with the OpenWeather API?  

2. **Data Modeling**  
   - Can you explain your relational data model for combining weather, orders, customers, and products?  

3. **Data Transformation**  
   - How did you calculate the daily rainfall totals from the 3-hour forecast data?  

4. **Automation**  
   - How does Apache Airflow schedule and manage your data pipeline tasks?  

5. **Performance Impact**  
   - What trends did you observe between weather conditions and delivery performance in this project?  

6. **Visualization**  
   - Which visualizations in your Power BI dashboard provide the most value for operational decision-making and why?  

7. **Agricultural Advisory**  
   - How did you define and calculate a “planting window” in your analytics?  

8. **Error Handling**  
   - If one API source fails during ETL, how does your pipeline ensure data completeness and reliability?  

9. **Scalability**  
   - How would you modify your solution to handle 10× more cities or additional weather variables?  

10. **Business Insight**  
    - Based on your findings, what operational or agricultural recommendations would you give to the company to improve performance and reduce weather-related risks?  

