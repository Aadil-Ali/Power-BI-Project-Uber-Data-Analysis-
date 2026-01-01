# 🚖 Uber Trip Analysis Dashboard | Power BI

### 📊 Project Overview
This Power BI project provides a comprehensive analysis of Uber trip data to help stakeholders track booking trends, revenue, and operational efficiency. The goal was to transform raw trip data into actionable insights for optimizing pricing strategies, driver allocation, and understanding customer behavior.

**Live Project Link:** [Insert Link Here if available]

---

### 🛠️ Tech Stack & Skills Used
| Category | Tools & Concepts |
| :--- | :--- |
| **Visualization Tool** | Microsoft Power BI |
| **Data Processing** | SQL, Power Query (ETL) |
| **Data Modeling** | Star Schema, Inactive Relationships (USERELATIONSHIP) |
| **Advanced DAX** | CALCULATE, SWITCH, Time Intelligence, Dynamic Measures |
| **Features** | Drill-Through, Bookmarks, Page Navigation, Parameter Fields |

---

### 💡 Key Features & Analysis

#### 1. Overview Dashboard (Strategic Insights)
A high-level view for management to track KPIs and location performance.
- **Dynamic Measure Selector:** Implemented a disconnected table to allow users to toggle charts between *Total Bookings, Total Revenue, and Trip Distance*.
- **Location Analysis:** Used complex DAX to analyze Pickup vs. Drop-off locations (handled **Inactive Relationships** in the data model).
- **KPI Cards:** Tracked Total Bookings (103.7K), Revenue ($1.6M), and Avg. Trip Time.
- **Vehicle Stats:** Grid view analyzing performance across UberX, Uber Black, and Uber Green.

#### 2. Time Analysis (Operational Trends)
Focused on identifying peak hours to optimize driver availability.
- **Heatmap Analysis:** A matrix grid showing demand hotspots by *Hour of Day vs. Day of Week*.
- **Peak Hour Identification:** 10-minute interval charts revealed maximum ride requests between **5 PM - 7 PM (Evening Rush)**.
- **Day-Type Logic:** Segregated data into Weekday vs. Weekend patterns.

#### 3. Granular Details (Drill-Through)
- **Deep Dive:** Enabled **Drill-Through functionality**, allowing users to right-click on any data point (e.g., a specific city or time) and jump to a detailed grid view of those specific trips.

---

### 📸 Dashboard Screenshots

#### 🔹 Page 1: Overview & Location Intelligence
*Visualizes payment methods, vehicle types, and critical location insights like the "Farthest Trip" and "Most Frequent Pickup Points".*
![Overview Dashboard](image_2ae0a7.png)

#### 🔹 Page 2: Time Analysis & Heatmaps
*Analyzes demand over time using 10-minute intervals and daily trends.*
![Time Analysis](image_299268.png)

#### 🔹 Page 3: Detailed Grid View
*Granular transaction-level data accessible via Drill-Through.*
![Details View](image_299252.png)

---

### 🧠 Technical Challenges Solved
1.  **Inactive Relationships:** The dataset had two location fields (`Pickup Location` and `Drop-off Location`) linking to a single `Location Master` table. I used the `USERELATIONSHIP` function in DAX to activate the Drop-off relationship only when needed.
2.  **Dynamic Titles:** Charts titles update automatically based on the selected metric (e.g., "Total Revenue by City" changes to "Total Bookings by City").
3.  **Optimization:** Used variables (`VAR`) in DAX measures to improve dashboard performance and reduce loading time.

---

### 📈 Project Conclusion
The analysis revealed that while **UberX** drives the highest volume, **Uber Black** yields significantly higher margins per mile. The heatmaps successfully identified underserved time slots, suggesting a need for dynamic pricing adjustments during late-night weekend hours.

---
*Created by Aadil Ali | [LinkedIn Profile Link]*
