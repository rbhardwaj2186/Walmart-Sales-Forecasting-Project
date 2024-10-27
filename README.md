# 🛒 Walmart Sales Forecasting Project

![dataset-cover](https://github.com/user-attachments/assets/d7171710-d837-4d08-9b40-c1f890a10be6)


## 📋 Project Overview
Walmart experiences significant seasonal fluctuations in sales. Predicting these peaks and troughs enables Walmart to manage inventories, forecast revenue, and strategically plan effective campaigns. This project builds a robust predictive model to help Walmart make data-driven decisions on stock arrangements, revenue projections, and investment planning.

## 💡 Problem Statement
Walmart faces considerable challenges with fluctuating sales, influenced by various seasonal events. Mismanaging these can lead to potential revenue loss and stock price impact. This project addresses the need for accurate forecasting to help Walmart optimize its supply chain and improve decision-making, particularly around seasonal sales.

---

## 🎯 Project Objectives
### 1. **Data Understanding and Cleaning**
   - Identify missing values and handle appropriately.
   - Format date columns for consistency.
   - Explore relationships among key variables such as temperature, CPI, and sales.
   - Detect and address data quality issues.

### 2. **Exploratory Data Analysis (EDA)**
   - Identify seasonal sales patterns and trends.
   - Examine performance across stores, departments, and holidays.
   - Visualize the distribution of sales and explore external influencing factors.

### 3. **Feature Engineering and Preparation for Modeling**
   - Engineer lag variables, rolling averages, and holiday indicators.
   - Encode categorical variables like store types and holiday flags.
   - Scale continuous variables for optimized model training.

### 4. **Model Development**
   - Implement **Random Forest Regressor** and **ARIMA/Exponential Smoothing** for time-series forecasting.
   - Evaluate model performance using Weighted Mean Absolute Error (WMAE).

### 5. **Insights and Recommendations**
   - Identify top-performing stores and departments.
   - Offer actionable strategies for inventory and stock management.

---

## 🧰 Data Description
The dataset includes weekly sales data from Walmart, with fields such as:

| Column         | Description                                  |
|----------------|----------------------------------------------|
| **Date**       | Sales record date.                          |
| **Store**      | Unique identifier for Walmart stores.       |
| **Department** | Identifier for each department.             |
| **Weekly Sales** | Weekly revenue for each department.       |
| **IsHoliday**  | Indicates if the sales week includes a holiday. |
| **Markdowns**  | Promotional discounts applied.              |
| **CPI**        | Consumer Price Index for the area.          |
| **Fuel Price** | Weekly fuel prices.                         |
| **Temperature** | Temperature data.                          |
| **Unemployment** | Unemployment rates.                       |

---

## 🧠 Model Selection
1. **Random Forest Regressor**  
   - Selected based on feature importance, achieving a WMAE of 1801.

2. **ARIMA and Exponential Smoothing**  
   - Applied to stationary data (transformed by log and differencing) with Exponential Smoothing yielding the lowest error (821).

---

## 📊 Key Findings
- **Seasonal Sales**: Sales peak around holidays like Christmas, Thanksgiving, and Black Friday.
- **Store and Department Variability**: Sales vary significantly based on store types (A, B, C).
- **Holiday Patterns**: Weeks preceding Christmas see the highest sales, with notable peaks in Thanksgiving and Black Friday weeks.
- **Economic Indicators**: Minimal impact from external factors like CPI and temperature on weekly sales.

---

## 🚀 Future Improvements
- Enhance stationarity techniques and expand feature engineering.
- Incorporate more holidays and seasonal data.
- Create specialized models for high-demand stores or departments.
- Perform market basket analysis for better department-wise demand predictions.

---

## 📅 Project Roadmap
| Goal           | Objective                                      | Tasks                                                                                           |
|----------------|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **Goal 1**     | Data Understanding and Cleaning                | Handle missing values, format dates, and explore relationships.                                |
| **Goal 2**     | Exploratory Data Analysis (EDA)                | Visualize seasonal trends and analyze store/department performance.                             |
| **Goal 3**     | Feature Engineering and Preparation            | Generate lag features, holiday indicators, and encode variables.                                |
| **Goal 4**     | Modeling and Evaluation                        | Train models and optimize using Weighted Mean Absolute Error (WMAE).                            |
| **Goal 5**     | Insights and Recommendations                   | Identify top performers and suggest inventory strategies.                                       |

---

## 📂 Repository Structure
- **`features.csv`**: Engineered features for model training.
- **`stores.csv`**: Store-specific information.
- **`train.csv`**: Training dataset for model building.
- **`test.csv`**: Testing dataset for evaluating model performance.
- **`Walmart_Sales_Forecasting.ipynb`**: Jupyter Notebook containing full analysis, model development, and evaluation.
- **`Roadmap.docx`** & **`problem.docx`**: Documentation for project goals, methodology, and problem context.

---

## 📝 Conclusion
This project demonstrates an end-to-end data science approach to sales forecasting, utilizing machine learning and time-series analysis to support Walmart’s operational and strategic decision-making. Accurate predictions enable Walmart to improve inventory management, reduce stockouts, optimize promotions, and enhance customer satisfaction.

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details.
