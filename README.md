# Statistical Modeling and Forecasting of Myanmar Tourism & Airline Arrivals using Python

## Project Overview
Predicting international tourist and airline arrivals is foundational for macroeconomic planning, hospitality resource allocation, and optimizing commercial airline logic. 

This project establishes a rigorous, production-ready statistical forecasting framework using Python. It cleans, structures, and processes historical tourism arrival matrices, systematically breaking them down through a standardized 5-step time-series methodology to deliver highly accurate data insights and minimize prediction errors.

---

## Tech Stack & Key Analytical Capabilities
* **Core Language:** Python 
* **Primary Data Frameworks:** `pandas`, `numpy` for data manipulation.
* **Statistical Modeling & Inference:** `statsmodels` (Advanced Time-Series Engine).
* **Data Visualization:** `matplotlib` for parsing trends and autocorrelation plots.
* **Core Competencies:** Automated Data De-noising, Seasonality Significance Testing, Parameter Optimization via Multiplicative Decomposition, and Non-Parametric Error Validation.

---

### Determining the Significance of the Seasonality
* **Objective:** Verify whether recurring seasonal spikes are statistically meaningful or merely random fluctuations.
* **Empirical Result:** The **Autocorrelation Function (ACF)** plot exhibited distinct, repeating spikes exactly at **Lag 12** and **Lag 24**. This provides empirical proof of a powerful **12-month cyclical seasonality** in Myanmar airline arrivals, heavily corresponding to the traditional annual peak tourism window (November to February).<img width="541" height="112" alt="image" src="https://github.com/user-attachments/assets/1649c39d-63f4-4dff-9ac7-1fb0de19c865" />


### Identifying Seasonal Differences to Model Seasonality and Trends
* **Objective:** Mathematically evaluate the structural relationship between the baseline trend and seasonal variations (Additive vs. Multiplicative structural properties).
* **Empirical Result:** Comprehensive variance analysis demonstrated that the amplitude of seasonal peaks expands proportionally with the long-term trend line. <img width="663" height="445" alt="image" src="https://github.com/user-attachments/assets/07c082ef-cbb3-4d7c-b09c-07e94c479429" />



### Deseasonalizing the Model
* **Objective:** Strip away cyclical seasonal noise to isolate and track the true underlying growth or contraction trend.
* **Empirical Result:** Utilizing classical Multiplicative Decomposition, the data was successfully decoupled. The resulting **Deseasonalized Series (Trend-Cycle component)** smoothly uncovers the true structural trajectory of arrival volumes, unclouded by annual high-season tourist spikes.<img width="693" height="465" alt="image" src="https://github.com/user-attachments/assets/28587ed3-205a-400c-a79f-df3afc52d5bb" />


### Applying the Least Squares Method (Model Estimation)
* **Objective:** Execute the statistical estimation engine to compute optimized parameters and assess model fitness weights.
* **Empirical Result:** The mathematical execution successfully converged across **84 historical monthly observations**.<img width="926" height="527" alt="image" src="https://github.com/user-attachments/assets/562d544d-1d2f-43b3-8815-4d69b0197f8d" />


###  Holt-Winters' Exponential Smoothing Model 
After completing all 5 framework steps, Holt-Winters' Exponential Smoothing (three parameters) both Additive & Multiplicative Models are chosen. Multiple evaluation metrics (SSE, MSE, RMSE, MAPE) were benchmarked across these two primary mathematical variations to guarantee high-performing, fast, and accurate insights.

### Additive Model
<img width="593" height="490" alt="image" src="https://github.com/user-attachments/assets/0c9be439-5bd7-4d24-82b8-1368d71c9226" />

### Multiplicative Model 
<img width="609" height="490" alt="image" src="https://github.com/user-attachments/assets/921cf6e0-9d7d-40bc-ad05-8094375d1602" />


### Forecasting 
<img width="566" height="381" alt="image" src="https://github.com/user-attachments/assets/beb40b9a-87d0-4bf9-a798-baa3ca6b4965" />



