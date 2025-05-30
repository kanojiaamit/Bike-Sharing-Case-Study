# Bike Sharing Case Study

## Problem Statement

A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short-term basis for a price or free. Many bike-share systems allow people to borrow a bike from one location and return it at another.

BoomBikes, a US bike-sharing provider, has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is struggling to sustain itself and wants to understand the demand for shared bikes after quarantine ends. They have hired a consulting company to analyze the factors influencing bike demand and to build a model to predict daily bike demand based on several features.

## Business Goal

Model the demand for shared bikes using the available independent variables. The outcomes will help management understand how demands vary with different features and make data-driven decisions about inventory and marketing.

---

## Questions to Answer

- **Which variables are significant in predicting the demand for shared bikes?**
- **How well do those variables describe the bike demand?**

---

## Data

The dataset contains daily data on bike demand across the American market, including meteorological and calendar factors.

| Feature       | Description                                  |
|---------------|----------------------------------------------|
| season        | Season (spring, summer, fall, winter)        |
| yr            | Year                                         |
| mnth          | Month                                        |
| holiday       | Is holiday                                   |
| weekday       | Day of week                                  |
| workingday    | Is working day                               |
| weathersit    | Weather situation                            |
| temp          | Normalized temperature                       |
| hum           | Normalized humidity                          |
| windspeed     | Normalized windspeed                         |
| cnt           | Count of total rental bikes (target)         |

---

## Approach

- **Data Cleaning:** Removed redundant columns (e.g., 'instant', 'dteday', 'casual', 'registered', 'atemp'). Mapped categorical variables to descriptive names.
- **Exploratory Data Analysis (EDA):** Explored seasonality, weather, and trends influencing demand.
- **Feature Engineering:** Encoded categorical variables for modeling.
- **Modeling:** Built a linear regression model to predict demand, evaluated results, and interpreted feature importance.

---

## Key Visuals

### 1. Feature Distributions and Pairplot

![Pairplot of Features](images/pairplot.png)

### 2. Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

### 3. Bookings by Season and Month

![Bookings by Season](images/bookings_by_season.png)
![Bookings by Month](images/bookings_by_month.png)

### 4. Demand vs Weather Situation

![Demand by Weather](images/demand_by_weather.png)

---

## Main Findings

- **Seasons:** Spring and Fall have the most bookings, with Fall being the highest—optimal for increasing rentals.
- **Months:** June to October see higher bookings, aligning with Spring and Fall.
- **Weather:** Clear and misty weather show higher bookings; clear weather is preferred.
- **Holidays:** Most bookings occur on non-holidays, suggesting work-related or routine usage.
- **Growth:** Significant increase in bookings in 2019 indicates market growth.
- **Top Features Affecting Demand:**
    - Temperature (`temp`, coefficient: 0.3304)
    - Light rain (`light_rain`, coefficient: -0.2828)
    - Year (`yr`, coefficient: 0.2374)

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/kanojiaamit/Bike-Sharing-Case-Study.git
   cd Bike-Sharing-Case-Study
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:
   ```bash
   jupyter notebook "Bike Sharing Case Study.ipynb"
   ```

---

## Dependencies

- Python 3.x
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- jupyter

---

## Author

Amit Kanojia
