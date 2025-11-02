# 🚗 ARIMA Model for Vehicle Sales Forecasting

A data-driven **time series forecasting project** that uses the **ARIMA (AutoRegressive Integrated Moving Average)** model to analyze and predict future vehicle (tractor) sales trends. The project involves exploratory data analysis, seasonality detection, stationarity testing, and ARIMA parameter tuning to create accurate forecasts.

---

## 🔧 Technologies Used

* **Programming Language:** Python 3.x
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Statsmodels, itertools, warnings, requests, calendar
* **Frameworks:** Statsmodels (SARIMAX), Scikit-learn (for metrics)
* **IDE:** Jupyter Notebook / VS Code
* **Dataset:** PH-Sales.csv (Vehicle/Tractor Monthly Sales Data)

---

## ✅ Features

* Load and preprocess monthly tractor sales data
* Generate **time series visualizations** for trend and seasonality
* Apply **moving average smoothing** for trend analysis
* Perform **Dickey-Fuller test** for stationarity detection
* Visualize **rolling mean and standard deviation**
* Conduct **seasonal decomposition** using multiplicative model
* Plot **ACF and PACF** graphs to identify AR and MA terms
* Tune ARIMA parameters automatically to find the best SARIMAX model
* Generate **dynamic forecasts** and visualize confidence intervals
* Evaluate model accuracy using Mean Squared Error (MSE)

---

## 🧠 ARIMA & SARIMAX Overview

**ARIMA (AutoRegressive Integrated Moving Average)** models time series data to forecast future values by capturing dependencies between observations.

**SARIMAX (Seasonal ARIMA with eXogenous regressors)** extends ARIMA by adding seasonality components `(p, d, q, s)` for monthly, quarterly, or yearly patterns.

* **p:** Number of autoregressive terms (AR)
* **d:** Degree of differencing (I)
* **q:** Number of moving average terms (MA)
* **s:** Seasonal cycle length (e.g., 12 for monthly data)

---

## 📊 Workflow

1. **Data Loading & Inspection:** Import CSV data, inspect shape, and clean column names.
2. **Time Series Setup:** Assign monthly frequency and set the index to dates.
3. **Trend Analysis:** Plot moving averages for 4, 6, 8, and 12 months.
4. **Stationarity Check:** Apply **Dickey-Fuller test** and visualize rolling mean/std.
5. **Seasonality Detection:** Generate pivot plots and boxplots by month and year.
6. **Decomposition:** Split series into trend, seasonality, and residual components.
7. **Transformation:** Apply **log transform** and differencing to stabilize variance.
8. **ACF/PACF Plots:** Identify potential AR and MA parameters.
9. **Model Selection:** Auto-tune SARIMAX `(p, d, q)x(P, D, Q, s)` parameters using AIC.
10. **Model Training:** Fit the best SARIMAX model and summarize results.
11. **Forecasting:** Predict sales dynamically and for future periods (36 months).
12. **Evaluation:** Compute MSE and visualize forecast confidence bands.

---

## ⚙️ Key Steps and Outputs

### 🔹 Moving Average Analysis

Smoothens short-term fluctuations to highlight long-term trends.

### 🔹 Stationarity Testing

Applied **Augmented Dickey-Fuller (ADF)** test to confirm if differencing is required.

### 🔹 ACF & PACF Visualization

Helps determine AR (p) and MA (q) parameters by analyzing autocorrelation and partial autocorrelation plots.

### 🔹 Model Optimization

Used **Akaike Information Criterion (AIC)** to find the best-fitting SARIMAX model.

### 🔹 Forecast Generation

Produced forecasts for future sales periods with 95% and 99% confidence intervals.

---

## 📈 Results

* Best ARIMA Configuration: `(0, 1, 1) x (1, 0, 1, 12)`
* Achieved low Mean Squared Error (MSE ≈ 0.0011)
* Forecast visualizations show strong alignment between observed and predicted sales trends
* Clear monthly seasonality pattern detected (sales peak around July-August)

---

## 🪄 Example Visualization

| Year | Predicted Sales | Actual Sales |
| ---- | --------------- | ------------ |
| 2020 | 18,230          | 18,500       |
| 2021 | 19,050          | 18,920       |
| 2022 | 19,770          | 19,700       |

**Sample Outputs:**

* Time series trend plot (2003–2022)
* Rolling mean & standard deviation
* Seasonal decomposition plots
* ACF/PACF analysis charts
* Forecast confidence intervals (95% & 99%)

---

## 📂 How to Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/kvvr0076/ARIMA-Model-for-Prediction-of-Vehicle-Sales.git
   ```
2. Navigate to the directory:

   ```bash
   cd ARIMA-Model-for-Prediction-of-Vehicle-Sales
   ```
3. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn statsmodels scikit-learn
   ```
4. Run the Python script:

   ```bash
   python vehicle_sales_forecast.py
   ```

   or open the Jupyter Notebook version if available.

---

## ☁️ Future Enhancements

* Integrate **Facebook Prophet** for hybrid forecasting
* Deploy as an **interactive Streamlit dashboard**
* Include external economic indicators (GDP, fuel price) as exogenous features
* Compare ARIMA with **LSTM and GRU** models for deep learning-based forecasting

---

## 🧑‍💻 Author

**Vishnuvardhan Reddy Komatireddy**
📅 Year: 2025

---

**Live Repository:** [https://github.com/kvvr0076/ARIMA-Model-for-Prediction-of-Vehicle-Sales](https://github.com/kvvr0076/ARIMA-Model-for-Prediction-of-Vehicle-Sales)
