# 🚲 Bike Sharing Analysis and Prediction

## 📘 Overview
This project analyzes a **bike-sharing dataset** to understand user behavior, identify trends, and build predictive models for ride demand.  
The goal is to uncover insights that help optimize fleet management, improve user experience, and forecast ridership based on temporal and usage patterns.

The analysis includes:
- Data cleaning and preprocessing  
- Exploratory data analysis (EDA)  
- Feature engineering (e.g., distance, duration, monthly averages)  
- Visualizations for seasonal and user-type trends  
- Predictive modeling using regression techniques  
- Model evaluation using MAE and RMSE  

---

## 🧾 Dataset

| Column | Description |
|:--|:--|
| `ride_id` | Unique identifier for each ride |
| `rideable_type` | Type of bike used (classic, electric, docked) |
| `started_at`, `ended_at` | Start and end timestamps of each ride |
| `start_station_name`, `end_station_name` | Station names |
| `start_lat`, `start_lng`, `end_lat`, `end_lng` | Geographical coordinates |
| `member_casual` | User type – whether the rider is a member or casual user |
| `ride_length` | Duration of the ride (derived) |
| `distance_km` | Distance between start and end points (calculated using `geopy.distance`) |

---

## 🧹 Data Cleaning & Preparation
Steps performed in the notebook:
1. Handle missing values in station names and IDs  
2. Convert time columns to datetime format  
3. Create new features:
   - Ride duration in minutes  
   - Distance (km) between start and end points  
   - Month, day, and hour extracted from timestamps  
4. Filter out invalid or zero-duration rides  

---

## 📊 Exploratory Data Analysis (EDA)
EDA focuses on understanding patterns between:
- Member vs casual usage  
- Monthly and seasonal ride trends  
- Most popular start/end stations  
- Rideable type preferences  
- Average ride distance and duration trends  
- Correlation between ride distance, duration, and user type  

Visualizations include:
- Bar charts for monthly and user-level comparisons  
- Line and combination charts for time-based averages  
- Heatmaps and boxplots for ride pattern distribution  

---

## 🤖 Model Development
The predictive model aims to **forecast ride demand or ride duration** using historical trends.

Models tested:
- **Linear Regression**
- **Random Forest Regressor**

Performance metrics used:
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

---

## 📈 Results

| Metric | Value |
|:--|:--|
| MAE | 110.47 |
| RMSE | 171.39 |

These results indicate a reasonably good fit, suggesting the model can capture temporal trends but could be improved with additional external features (e.g., weather, holidays).

---

## 🧠 Insights
- Casual users tend to take longer rides, often during weekends.  
- Members have shorter, more frequent rides, likely for daily commuting.  
- Electric bikes show increasing adoption in recent months.  
- Peak ride activity aligns with morning and evening commuting hours.  

---

## 🧩 Technologies Used
- **Python**
- **Pandas**, **NumPy** – Data manipulation  
- **Matplotlib**, **Seaborn** – Visualization  
- **Scikit-learn** – Machine learning models  
- **Geopy** – Distance computation  
- **Jupyter Notebook**
