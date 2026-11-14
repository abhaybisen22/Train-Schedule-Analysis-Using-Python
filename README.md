# Train-Schedule-Analysis-Using-Python
Train Schedule Analysis Using Python is a comprehensive data analytics project developed during my internship at Sysslan IT Solutions. Using Python, Pandas, Matplotlib, and Seaborn, this pipeline explores, cleans, and validates raw railway timetable data to extract actionable insights. 

# 🚆 Train Schedule Analysis Using Python
A comprehensive end-to-end data analytics project built to explore, clean, process, and visualize railway schedule datasets—focusing on route durations, stoppage patterns, station traffic congestion, and corridor distributions[cite: 1, 2, 3, 5, 6, 7].

---

## 📌 Short Description / Purpose
The **Train Schedule Analysis** project is a structured Python-based analytical pipeline developed during my Data Analytics internship with **Sysslan IT Solutions**[cite: 2, 4]. It transforms raw railway timetable records into actionable operational insights by standardizing schedules, validating route sequences, and mapping station traffic patterns[cite: 1, 2, 3, 5, 6]. This repository is designed for transit analysts, operations planners, and data enthusiasts seeking to understand train frequency distributions, journey duration scaling across route types, and major railway junction bottlenecks[cite: 2, 3, 6, 7].

---

## 🛠️ Tech Stack
The analysis and visualizations were built using the following tools and technologies:
* 🐍 **Python 3** – Core programming language used for scripting, custom classification logic, and data workflows[cite: 2, 3, 8].
* 🐼 **Pandas & NumPy** – Data manipulation, missing value imputation, deduplication, `timedelta` duration calculations, pivot tables, and cross-tabulations[cite: 1, 3, 5, 7].
* 📊 **Matplotlib & Seaborn** – Data visualization libraries used for generating annotated bar charts, horizontal rankings, stacked distributions, and intensity heatmaps[cite: 6, 7].
* 📓 **Jupyter Notebook (VS Code)** – Interactive development environment used to structure the workflow into modular, reproducible level-wise notebooks[cite: 4].
* 📁 **File Formats** – `.csv` for raw and cleaned datasets, and `.ipynb` for step-by-step analytical execution.

---

## 📂 Data Source
**Source:** Internship Dataset (`Dataset1.csv`) provided by **Sysslan IT Solutions**[cite: 4].  
The dataset contains detailed stop-by-stop railway schedule records, structured with key attributes including:
* **Train & Route Identifiers:** `Train_No`, `Route_Number`, and stop sequence serial numbers (`SN`).
* **Station Details:** `Station_Code` and `Station_Name`.
* **Timings & Distance:** Scheduled `Arrival_time`, `Departure_Time`, and cumulative `Distance` (in km) from the origin station.
* **Accommodation Tiers:** Coach availability indicators (`1A`, `2A`, `3A`, `SL`).

*(Note: After performing missing schedule handling, deduplication, and monotonic distance validation in Level 3, the verified dataset was exported as `Cleaned_Train_Dataset.csv` for downstream visualization[cite: 5, 6]).*

---

## ✨ Features / Highlights

### 🔹 Business Problem
Raw railway schedule datasets contain thousands of stop-level rows, unstandardized string timestamps, overnight multi-day arrivals, and duplicate entries[cite: 3, 5]. Without structured processing and visual aggregation, critical operational questions—such as:
* *Which railway junctions experience the highest train congestion[cite: 6]?*
* *How do average journey durations scale across short, medium, and long-distance routes[cite: 3, 6]?*
* *What is the composition of long-distance versus regional trains at major terminals[cite: 7]?*
—remain difficult to answer quickly from raw tables alone.

### 🔹 Goal of the Project
To build a clean, reproducible 5-stage analytical pipeline that[cite: 2]:
1. Audits raw schedule dimensions, origin/terminus pairs, and stop counts per train[cite: 1].
2. Standardizes schedule timestamps and computes accurate journey durations (accounting for overnight transitions)[cite: 3].
3. Ensures high data integrity by cleaning nulls, removing duplicates, and validating sequential station distances[cite: 5].
4. Delivers clear comparative charts, pivot tables, and heatmaps to uncover network traffic hotspots[cite: 6, 7].

### 🔹 Walkthrough of Key Analyses & Visuals (Level 1 – Level 5)
* **Dataset Overview & Stoppage Profiling (Level 1):** Extracted total records and attributes, mapped exact starting and ending stations per train, and identified trains with maximum and minimum intermediate stops[cite: 1].
* **Schedule Processing & Route Classification (Level 2):** Converted string timings into standardized 24-hour formats, computed exact `Duration_Hours` with 24-hour wrap-around logic for overnight journeys, and classified trains into **Short (`<300 km`)**, **Medium (`300–800 km`)**, and **Long (`>800 km`)** routes[cite: 3].
* **Data Quality & Validation (Level 3):** Handled missing origin/terminus timings, eliminated duplicate train-station records, and verified monotonically increasing station distances along every route[cite: 5].
* **Average Journey Duration by Route Type (Bar Chart – Level 4):** Compares mean and median travel durations across Short, Medium, and Long corridors with exact hour annotations[cite: 6].
* **Top 10 High-Traffic Stations (Horizontal Bar Chart – Level 4):** Ranks the busiest railway stations based on the count of unique trains handled[cite: 6].
* **Station-Wise Train Distribution (Pivot Table & Stacked Bar Chart – Level 5):** Breaks down how Short, Medium, and Long-distance trains contribute to total traffic at the top 10 junctions[cite: 3, 7].
* **Station vs. Route Intensity (Cross-Tabulation & Heatmap – Level 5):** Uses color intensity and frequency cross-tabs to highlight high-density station-route intersections[cite: 7].

### 🔹 Operational Impact & Key Insights
* **Non-Linear Duration Scaling:** Long-distance routes (`>800 km`) show substantially higher average journey durations due to multi-day overnight schedules and higher intermediate stoppage counts.
* **Junction Traffic Concentration:** Railway traffic is heavily concentrated around a core set of major junction hubs, identifying primary network bottlenecks where platform turnaround and signal coordination are most critical.
* **Long-Corridor Dominance at Major Hubs:** Pivot table and heatmap analyses reveal that peak congestion at top stations is predominantly driven by long-distance trains, while select regional terminals balance both intercity commuter and long-haul traffic[cite: 7].
* **Data Reliability for Downstream Systems:** Enforcing monotonic distance validation and schedule standardization eliminates calculation anomalies, creating a reliable foundation for route enquiry tools[cite: 3, 5, 8].

---

## 📸 Screenshots / Demos
*(Tip: Apne Level 4 aur Level 5 ke charts ke screenshots repository me upload karke neeche unka link paste kar dena)*

* **Journey Duration & High-Traffic Stations Analysis:**  
  `![Level 4 Analysis](screenshots/level4_charts.png)`[cite: 6]
* **Pivot & Heatmap Comparative Analytics:**  
  `![Level 5 Comparative Visuals](screenshots/level5_heatmap.png)`[cite: 7]

---

## 👨‍💻 Author
**Abhay Nandlal Bisen**  
*Data Analytics Intern | Sysslan IT Solutions*[cite: 4]
