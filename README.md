### **Capstone Project:** Kenya Weather-Aware E-Commerce & Agri-Logistics Dashboard  

---
## 1. Background / Problem Statement  
A Kenya-based e-commerce and produce-delivery startup operates in multiple cities (Nairobi, Mombasa, Kisumu, Eldoret, Nakuru). The company delivers goods ranging from electronics to fresh farm produce. The operations team has noticed that **weather conditions** — especially rainfall and wind — significantly impact delivery times, cancellations, and even supply availability. For agricultural produce, weather also affects planting and harvesting windows, which in turn influences stock levels and delivery demand.  

Currently, the company lacks a **centralized analytics system** to:  
- Monitor and forecast weather conditions for each city.  
- Predict operational risks to deliveries.  
- Offer simple, data-driven planting/harvest advisories for suppliers.  
- Integrate sales, customer, and product data into one interactive dashboard.  

---

## 2. Project Goal  
Design and implement an **end-to-end data analytics solution** that automatically collects, processes, and visualizes both **operational data** (orders, deliveries, customers) and **environmental data** (weather forecasts).  

The solution should help the company:  
- Identify days and locations with **high delivery risk** due to adverse weather.  
- Recommend adjustments to **delivery schedules and routing**.  
- Provide simple **agricultural advisories** to suppliers based on weather forecasts.  
- Track sales, top products, and customer trends alongside weather impact.  

---

## 3. Objectives  
1. **Data Acquisition**  
   - Pull product data from a public e-commerce API.  
   - Pull customer and order data from a mock API.  
   - Pull 5-day/3-hour weather forecast data for each target city from **OpenWeather API**.  

2. **Data Processing & Storage**  
   - Clean and merge datasets into a relational model (e.g., products, customers, orders, weather).  
   - Create derived metrics: daily rainfall (mm), rain risk flag, wind risk flag, delivery SLA performance, crop planting windows.  

3. **Data Automation**  
   - Use a workflow orchestrator (e.g., Airflow) to schedule daily data collection and updates.  

4. **Analytics & Insights**  
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

## 4. Deliverables  
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

## 5. Suggested Metrics
