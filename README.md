# **Predicting COVID-19 Outbreak Severity**

This project uses the **Google Health COVID-19 Open Data** dataset to perform **exploratory data analysis (EDA)** and develop a **predictive model** for forecasting outbreak severity. The analysis investigates the relationship between:

- COVID-19 case trends  
- Government policy responses  
- Human mobility patterns  
- Weather conditions  
- Demographic factors  

The scope covers **Pakistan**, **India**, and **China**.

---

## **Dataset**

The dataset comes from **Google Health COVID-19 Open Data**, containing daily updates on:

- **Epidemiological Data**: Confirmed/deceased cases, rolling averages.
- **Government Policy**: Stringency Index, school closures, travel restrictions.
- **Human Mobility**: Retail, workplace, and transit mobility patterns.
- **Demographics**: Population density, GDP per capita, health indicators.
- **Weather Data**: Temperature, rainfall, humidity.

---

## **Exploratory Data Analysis (EDA)**

The EDA process focused on identifying trends, patterns, and correlations.

### **1. Time-Series Trends**
Tracking daily confirmed COVID-19 cases over time.

![7-Day Rolling Average](images/7-Day%20Rolling%20Average%20of%20Confirmed%20Cases%20Over%20Time.png)

Tracking COVID-19 Case Trends and Government Response Stringency (stringency 0-100, higher the better/stricter)

![COVID-19 Case Trends and Government Response Stringency (2020-2022](images/COVID-19%20Case%20Trends%20and%20Government%20Response%20Stringency%20(2020-2022).png)

---

### **2. Government Policy & Stringency**
Comparing policy interventions with case numbers.

| Country  | Visualization |
|----------|--------------|
| **China** | ![China Policy](images/COVID-19%20Cases%20Over%20Time%20with%20Policy%20Changes%20—%20China.png) |
| **India** | ![India Policy](images/COVID-19%20Cases%20Over%20Time%20with%20Policy%20Changes%20—%20India.png) |
| **Pakistan** | ![Pakistan Policy](images/COVID-19%20Cases%20Over%20Time%20with%20Policy%20Changes%20—%20Pakistan.png) |

---

### **3. Human Mobility Trends**
Analyzing mobility changes during the pandemic.

- A value of 0% indicates that mobility is at the same level as the baseline.
- A value of -50% means that mobility has decreased by 50% compared to the baseline.
- A value of +25% means that mobility has increased by 25% compared to the baseline.

| Country  | Visualization |
|----------|--------------|
| **China** | ![China Mobility](images/China%20—%20Mobility%20Trends.png) |
| **India** | ![India Mobility](images/Individual%20Mobility%20Trends%20in%20India%20with%20Context.png) |
| **Pakistan** | ![Pakistan Mobility](images/Individual%20Mobility%20Trends%20in%20Pakistan%20with%20Context.png) |

**Combined Trends Across Countries**

![COVID-19 Case Trends and Government Response Stringency (2020-2022)](images/COVID-19%20Case%20Trends%20and%20Government%20Response%20Stringency%20(2020-2022).png)

---

### **4. Weather Variables**
Exploring how temperature and weather conditions may relate to COVID-19 case counts.

| Country  | Visualization |
|----------|--------------|
| **China** | ![China Weather](images/Weather%20Variables%20and%20COVID-19%20Cases%20Over%20Time%20(China).png) |
| **India** | ![India Weather](images/Weather%20Variables%20and%20COVID-19%20Cases%20Over%20Time%20(India).png) |
| **Pakistan** | ![Pakistan Weather](images/Weather%20Variables%20and%20COVID-19%20Cases%20Over%20Time%20(Pakistan).png) |

---

## **Predictive Modeling**

The predictive model forecasts **daily new confirmed cases per capita**.

### **Preprocessing Steps**
- Removed irrelevant/redundant columns.
- One-hot encoded categorical variables (e.g., `country_name`).
- Scaled features with **StandardScaler**.
- Split data chronologically into training and test sets.

### **Model Performance**
- **RMSE**: `0.000015`
- **MAE**: `0.000004`
- **R²**: `0.5679`
- **MSE**: `0.0000000002`

These results indicate that the model captures a decent portion of the variance in the target variable, though the tiny error values are due to the small scale of the target variable (`new_confirmed_per_capita`).


![Actual vs Predicted](images/Actual%20vs%20Predicted%20COVID-19%20Cases.png)

> **Note**: This is an initial model. The temporal nature of the data requires more advanced time-series modeling techniques (e.g., ARIMA, LSTMs) for optimal results.
---

## **How to Run**

```bash
# Clone repository
git clone https://github.com/Muhammad-Lukman/COVID-19-Data-Analysis.git
cd COVID-19-Data-Analysis

# Install dependencies
pip install -r requirements.txt

```
---

## **Citation**

```bash
@article{Wahltinez2020,
  author = "O. Wahltinez and others",
  year = 2020,
  title = "COVID-19 Open-Data: curating a fine-grained, global-scale data repository for SARS-CoV-2",
  note = "Work in progress",
  url = {https://goo.gle/covid-19-open-data},
}
```
