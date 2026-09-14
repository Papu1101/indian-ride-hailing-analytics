# indian-ride-hailing-analytics
Python-based analytics and machine learning project analyzing ride-hailing demand, fares, traffic, and high-demand city-hour zones across India.

An end-to-end Python analytics project focused on understanding ride-hailing demand, fare patterns, traffic conditions, vehicle performance, and high-demand city-hour combinations across major Indian cities.

---

## 📌 Project Overview

The Indian ride-hailing industry operates in a highly dynamic environment where customer demand, traffic conditions, driver availability, distance, and surge pricing directly influence ride fares and operational performance.

This project analyzes a synthetic ride-hailing dataset covering six major Indian cities:

- Bengaluru
- Mumbai
- Delhi
- Hyderabad
- Chennai
- Pune

The project uses Python for data cleaning, exploratory data analysis, predictive modeling, and demand-zone identification.

---

## 🎯 Business Objectives

The main objectives of this project are to:

1. Understand ride-hailing demand across Indian cities.
2. Analyze ride patterns based on time, traffic, and vehicle type.
3. Compare city-wise and country-level ride performance.
4. Identify factors influencing final ride fares.
5. Predict the final fare for new rides.
6. Identify high-demand city-hour combinations.
7. Support better driver allocation and operational planning.

---

## 📊 Dataset Description

The dataset is synthetically generated and contains **1,000 ride records** covering the period from **2025 to 2026**.

### Dataset Columns

| Column | Description |
|---|---|
| `User_ID` | Unique identifier for each user |
| `Driver_Name` | Name of the driver |
| `City` | City where the ride took place |
| `Ride_Date` | Date of the ride |
| `Hour_of_Day` | Hour when the ride occurred |
| `Day_of_Week` | Day of the week |
| `Distance_km` | Ride distance in kilometers |
| `Traffic_Level` | Traffic condition during the ride |
| `Type_of_vehicle` | Type of vehicle used |
| `No_of_active_drivers` | Number of active drivers |
| `Ride_Requests` | Number of ride requests |
| `Demand_Supply_Ratio` | Ratio between ride demand and driver supply |
| `Trip_Duration` | Trip duration in minutes |
| `Base_Fare` | Base fare of the ride |
| `Surge_Multiplier` | Surge pricing multiplier |
| `Final_Fare` | Final fare charged for the ride |

---

## 🛠️ Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- GeoPandas
- Jupyter Notebook

---

## 🔍 Project Workflow

### 1. Data Loading

- Imported the ride-hailing dataset using Pandas.
- Reviewed the dataset structure and data types.
- Checked the number of rows and columns.

### 2. Data Cleaning

The following data-quality checks were performed:

- Missing-value analysis
- Duplicate-row detection
- Date-format conversion
- Numerical-column validation
- Invalid fare and distance checks
- Validation of categorical values
- Handling missing driver names

The final dataset contained:

- **1,000 records**
- **16 columns**
- **0 missing values**
- **0 duplicate rows**

---

## 📈 Exploratory Data Analysis

### City-Level Analysis

The project analyzes individual cities to understand:

- Total ride requests
- Average distance
- Average trip duration
- Average active drivers
- Average demand-supply ratio
- Average surge multiplier
- Average base fare
- Average final fare

### Vehicle-Level Analysis

Vehicle performance was analyzed using:

- Total ride requests
- Average distance
- Average trip duration
- Average surge multiplier
- Average final fare
- Revenue and profit/loss comparison

### Traffic-Level Analysis

Traffic conditions were compared based on:

- Total ride requests
- Average surge multiplier
- Average demand-supply ratio
- Average final fare

### Time-Based Analysis

Ride demand was analyzed by:

- Hour of the day
- Day of the week
- Peak demand hours
- Surge pricing hours
- Demand-supply patterns

### Country-Level Analysis

The complete dataset was also analyzed at the overall India level to identify broader ride-hailing trends.

---

## 📊 Key Exploratory Findings

The country-level analysis produced the following results:

| Metric | Result |
|---|---:|
| Total Records | 1,000 |
| Total Ride Requests | 108,047 |
| Average Distance | 17.91 km |
| Average Trip Duration | 55.16 minutes |
| Average Active Drivers | 52.52 |
| Average Demand/Supply Ratio | 2.90 |
| Average Surge Multiplier | 1.44 |
| Average Base Fare | ₹257.48 |
| Average Final Fare | ₹370.21 |

### Peak Demand Findings

- The highest overall ride demand was observed around **22:00**.
- The highest average surge multiplier was observed around **21:00**.
- High-demand periods showed increased demand-supply pressure.
- Bengaluru, Pune, Chennai, Delhi, and Mumbai appeared frequently among the top city-hour demand combinations.

---

## 🤖 Predictive Modeling

### Final Fare Prediction

A Linear Regression model was developed to predict `Final_Fare`.

### Features Used

- `Hour_of_Day`
- `Distance_km`
- `No_of_active_drivers`
- `Ride_Requests`
- `Demand_Supply_Ratio`
- `Trip_Duration`
- `Base_Fare`
- `Surge_Multiplier`

### Model Performance

| Metric | Result |
|---|---:|
| Model | Linear Regression |
| R² Score | 0.9574 |
| Mean Squared Error | 1597.16 |
| RMSE | Approximately ₹39.96 |

The model achieved an R² score of approximately **0.9574**, indicating that it explained around **95.74% of the variation** in final ride fares within the dataset.

### Example Prediction

For a hypothetical ride with:

- Hour: 18:00
- Distance: 12 km
- Active Drivers: 80
- Ride Requests: 150
- Demand-Supply Ratio: 1.875
- Trip Duration: 35 minutes
- Base Fare: ₹250
- Surge Multiplier: 1.5



```text
₹381.13
