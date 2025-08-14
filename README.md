# **Predicting COVID-19 Outbreak Severity** 🦠

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

| Country  | Visualization |
|----------|--------------|
| **China** | ![China Mobility](images/China%20—%20Mobility%20Trends.png) |
| **India** | ![India Mobility](images/India%20—%20Mobility%20Trends.png) |
| **Pakistan** | ![Pakistan Mobility](images/Pakistan%20—%20Mobility%20Trends.png) |

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
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# Install dependencies
pip install -r requirements.txt

# Open the Jupyter Notebook
jupyter notebook notebooks/COVID_19_Google_Health_dataset_handsOn_practice.ipynb
```
---
# COVID-19-Data-Analysis
This project performs exploratory data analysis and predictive modeling on the Google Health COVID-19 dataset.
# **Predicting COVID-19 Outbreak Severity** 🦠

This project uses the Google Health COVID-19 dataset to perform an in-depth exploratory data analysis (EDA) and develop a predictive model to forecast outbreak severity. The analysis focuses on the relationship between COVID-19 cases, government policy responses, human mobility, weather conditions, and demographic factors for Pakistan, India, and China.

-----

### **Dataset**

The dataset used in this project is the **Google Health COVID-19 Open Data** set. It is a rich, granular time-series dataset that includes daily updates on:

  * **Epidemiological Data**: Confirmed cases, deceased cases, and rolling averages.
  * **Government Policy**: Stringency Index, school closures, and restrictions on gatherings.
  * **Human Mobility**: Trends in retail, transit stations, and workplaces.
  * **Demographics**: Population density, GDP per capita, and health-related statistics.
  * **Weather Data**: Temperature, rainfall, and humidity.

-----

### **Exploratory Data Analysis (EDA)**

The EDA phase focused on visualizing key trends and relationships within the data to gain a better understanding of the pandemic's progression.

#### **1. Time-Series Trends**

The analysis began by visualizing the daily confirmed cases and their trends over time.

#### **2. Government Policy and Stringency**

We explored how government interventions, such as lockdowns and public health policies, correlated with the number of confirmed cases.

  * **China**: 
  * **India**: 
  * **Pakistan**: 

#### **3. Human Mobility Trends**

The visualizations show how mobility patterns changed in response to the pandemic and policy measures.

  * **China**: 
  * **India**: 
  * **Pakistan**: 

#### **4. Weather Variables**

We examined the relationship between weather variables like temperature and humidity and the number of COVID-19 cases.

  * **China**: 
  * **India**: 
  * **Pakistan**: 

-----

### **Predictive Modeling**

The final phase of the project involved building a predictive model to forecast daily new confirmed cases per capita.

#### **Preprocessing and Feature Selection**

To handle the high dimensionality of the dataset (95 columns), a meticulous preprocessing pipeline was designed. This included:

  * **Feature Selection**: Dropping redundant and irrelevant columns.
  * **One-Hot Encoding**: Transforming categorical features like `country_name` into a machine-readable format.
  * **Data Splitting**: Splitting the data chronologically into training and testing sets.
  * **Scaling**: Using `StandardScaler` to normalize numerical features.

#### **Model Performance**

A predictive model was trained on the preprocessed data, with the following results:

  * **RMSE**: 0.000015
  * **MAE**: 0.000004
  * **R²**: 0.5679
  * **MSE**: 0.0000000002

These results indicate that the model captures a decent portion of the variance in the target variable, though the tiny error values are due to the small scale of the target variable (`new_confirmed_per_capita`).

> **Note**: This is an initial model. The temporal nature of the data requires more advanced time-series modeling techniques (e.g., ARIMA, LSTMs) for optimal results.

-----

### **How to Run**

To explore this project, clone the repository and open the Jupyter notebook in your preferred environment (e.g., Google Colab, JupyterLab).

1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd your-repo-name
    ```
3.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4.  Open the notebook:
    ```
    notebooks/COVID_19_Google_Health_dataset_handsOn_practice.ipynb
    ```
