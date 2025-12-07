# 📘 **US Road Accident Analysis – Exploratory Data Analysis (EDA)**

This project performs an in-depth **Exploratory Data Analysis (EDA)** on the **US Accidents Dataset** sourced from Kaggle.
The dataset contains **7.6+ million** accident records collected from 2016–2023 across the United States.

The goal of this project is to analyze accident patterns, understand contributing factors, identify trends, and generate insights that help in **road safety planning, hazard detection, and risk mitigation**.

---

## 🚀 **Project Objectives**

* Understand the **distribution and characteristics** of road accidents in the US.
* Find which **states, cities, roads, and weather conditions** have the highest accident frequencies.
* Explore **time-based patterns**: yearly, monthly, weekly, hourly.
* Analyze how **weather, visibility, humidity, and temperature** affect accident severity.
* Identify **top dangerous locations** and **accident hotspots**.
* Perform **correlation analysis** among key numerical features.
* Detect **missing values**, **data imbalance**, and **outlier patterns**.

---

## 📂 **Dataset Overview**

**Dataset Name:** US Accidents (2016–2023)
**Source:** Kaggle – by *Sobhan Moosavi*
**Size:** ~7.6 Million rows | 47 Columns
**Geographical Coverage:** 49 US states (except Alaska & Hawaii)

### 🔑 **Key Features**

| Column                    | Description                                    |
| ------------------------- | ---------------------------------------------- |
| `Severity`                | Accident severity (1–4, where 4 = most severe) |
| `Start_Lat`, `Start_Lng`  | Accident latitude/longitude                    |
| `Distance(mi)`            | Estimated distance of accident                 |
| `Weather_Condition`       | Weather at the accident time                   |
| `Visibility(mi)`          | Visibility distance                            |
| `Temperature(F)`          | Temperature                                    |
| `Humidity(%)`             | Humidity level                                 |
| `Pressure(in)`            | Atmospheric pressure                           |
| `Wind_Speed(mph)`         | Wind speed                                     |
| `Sunrise_Sunset`          | Day/Night indicator                            |
| `State`, `City`, `Street` | Location info                                  |
| `Start_Time`              | Timestamp                                      |

---

## 🧹 **Data Cleaning & Preprocessing**

The following steps were performed:

### ✔ Handling Missing Values

* Checked missing percentages for all columns.
* Removed columns having **>45% missing values** (e.g., WindChill).
* Imputed missing values using:

  * Mean/Median (numerical)
  * Mode (categorical)

### ✔ Datetime Transformation

* Extracted:

  * Year
  * Month
  * Day of week
  * Hour
* Converted to proper datetime format.

### ✔ Removing Duplicates & Outliers

* Dropped duplicate accident IDs.
* Detected outliers in:

  * `Distance(mi)`
  * `Temperature(F)`
  * `Visibility(mi)`
  * `Wind_Speed(mph)`

### ✔ Feature Engineering

* Created derived features:

  * `Is_Rush_Hour`
  * `Is_Weekend`
  * `Part_of_Day` (Morning, Noon, Evening, Night)

---

## 📊 **Exploratory Data Analysis**

Comprehensive EDA includes:

### 🔹 Accident Severity Distribution

* Most accidents fall under **Severity 2**.
* Severity 4 cases are rare but critical.

### 🔹 State-wise Accident Count

Top 5 highest accident states:

1. **California**
2. **Texas**
3. **Florida**
4. **North Carolina**
5. **Ohio**

### 🔹 City-level Insights

* Cities with the highest accident frequency:
  **Los Angeles, Houston, Miami, Charlotte, Dallas**

### 🔹 Time-based Patterns

* **Morning (6–10 AM)** and **Evening (3–7 PM)** peaks.
* Weekdays see more accidents than weekends.

### 🔹 Weather Impact

Accidents are highly frequent during:

* **Rain**
* **Fog**
* **Snow**
* **Thunderstorms**

Visibility often drops during accidents.

### 🔹 Correlation Analysis

* `Visibility(mi)` and `Weather_Condition` strongly affect severity.
* Traffic congestion hours correlate with higher accident rates.

### 🔹 Geo-spatial Analysis

* Plotted heatmaps for accident hotspots using Folium.
* California, Texas, and Florida show the hottest clusters.

---

## 🛠️ **Technologies Used**

| Category      | Tools                           |
| ------------- | ------------------------------- |
| Programming   | Python                          |
| IDE           | Google Colab / Jupyter Notebook |
| Data Analysis | Pandas, NumPy                   |
| Visualization | Matplotlib, Seaborn, Plotly     |
| Geo-mapping   | Folium                          |
| Other         | Kaggle API                      |

---

## 📁 **Project Structure**

```
US-Accident-EDA/
│── notebooks/
│   └── US_Accident_EDA.ipynb
│── data/
│   └── US_Accidents.csv (ignored via .gitignore)
│── images/
│   └── plots & heatmaps
│── README.md
│── requirements.txt
```

---

## 📉 **Key Findings**

* Rush hour and workdays observe the **highest number of accidents**.
* Weather conditions like **rain, snow, and fog** significantly increase accident risk.
* **California** has the highest accident density.
* Accidents are heavily concentrated in **urban areas**.
* Accident severity increases when **visibility drops**.
* Majority of accidents occur during **daytime**, but severe accidents tend to occur at **night**.

---

## 🎯 **Future Work**

* Build a **Machine Learning model** to predict accident severity.
* Create a **real-time accident risk prediction system**.
* Develop a **dashboard** using Dash/Streamlit/Tableau.
* Integrate live weather & traffic APIs.

---
