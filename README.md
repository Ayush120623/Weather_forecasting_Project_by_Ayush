
# 🌦️ Humidity Forecasting Using SARIMA  
*A Time Series Forecasting Project*

---

## 📌 **Project Overview**

This project focuses on forecasting daily humidity using the **SARIMA (Seasonal AutoRegressive Integrated Moving Average)** model.  
By learning from historical humidity trends, we build a robust statistical model that can accurately predict future humidity levels — an essential factor in **weather analysis, agriculture, and climate-based decision-making**.

---

## 🔍 **What I Did**

I started with a dataset of daily humidity values, conducted extensive preprocessing and exploratory analysis, and then applied a SARIMA model to both **understand** and **forecast** the humidity behavior.

---

## 🧹 **Step 1: Data Cleaning & Preparation**

- Loaded daily humidity data from a CSV file.  
- Converted date strings to proper datetime objects.  
- Set the date column as the index to prepare for time series modeling.  
- Visualized the data to get a feel of trends, seasonality, and noise.

---

## 📊 **Step 2: Exploratory Data Analysis (EDA)**

- Plotted humidity over time to identify patterns and anomalies.  
- Observed clear **seasonal trends**, likely linked to annual weather cycles.  
- Identified missing values or sudden drops and ensured data continuity.

---

## 🧪 **Step 3: Stationarity Check**

Before applying SARIMA, we must ensure the time series is stationary (i.e., constant mean and variance over time).

- Performed **rolling statistics** (mean and std) and plotted them.  
- Used **Augmented Dickey-Fuller (ADF)** test to statistically confirm stationarity.  
- Differenced the data and re-tested until the series passed the stationarity test.

---

## 🔧 **Step 4: Model Building (SARIMA)**

- Used `SARIMAX` from `statsmodels` to incorporate both non-seasonal and seasonal components.  
- Carefully chose the parameters: **(p, d, q) × (P, D, Q, s)** using grid search and visual intuition.  
- Fit the SARIMA model on the historical humidity data.

---

## 📉 **Step 5: Residual Diagnostics**

To validate that the model fits well:

- Plotted **residuals** to check for randomness (should resemble white noise).  
- Analyzed **density plots** and **ACF/PACF** plots of residuals.  
- ✅ Residuals looked normally distributed with no significant autocorrelation → Model is well-behaved.

---

## 📈 **Step 6: Forecasting**

### 🔹 **Short-Term Forecast (Validation)**

- Forecasted humidity from index 1080 to 1290 (a segment within the dataset).  
- Compared actual vs predicted values — and saw **strong alignment**.

### 🔹 **Long-Term Forecast (Future)**

- Forecasted humidity for the **next 100 days** beyond the dataset.  
- Plotted predicted values with a **99% confidence interval**.  
- ✅ The trend remained stable and realistic, without wild fluctuations.

---

### 🔚 **Conclusion:**

- The SARIMA model effectively captured the **seasonal** and **trend** components of humidity data.  
- Residual diagnostics confirm the model’s validity (no pattern or bias in errors).  
- The 100-day forecast remained consistent with past trends and was statistically sound.

### 📌 **Real-world Use Cases:**

- Climate monitoring  
- Agricultural irrigation planning  
- Health hazard predictions in humid zones

---

## 🛠 **Tech Stack**

- Python 🐍  
- Pandas & NumPy  
- Matplotlib & Seaborn (visualization)  
- Statsmodels (SARIMA modeling)  
- Jupyter Notebook

---


## 💡 **What I Learned**

- Hands-on experience with **SARIMA modeling**  
- The importance of **stationarity** and residual diagnostics  
- How to visualize and interpret **time series forecasts**  
- Confidence intervals and their role in forecasting reliability

---

#👋 Connect

Want to chat, collaborate, or hire me?

📬 Email: ayushsharma.mee@gmail.com

💼 LinkedIn : www.linkedin.com/in/ayush-sharma-a975862b5
