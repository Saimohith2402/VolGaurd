# 🛡️ Vol-Guard: Nifty 50 Volatility Forecasting Engine

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Notebook-Colab-orange)
![Deep Learning](https://img.shields.io/badge/Model-LSTM-red)

**Vol-Guard** is a Deep Learning-based volatility forecasting tool designed to predict the realized volatility of the **Nifty 50 Index**. Unlike traditional statistical methods (like GARCH), this project utilizes **Long Short-Term Memory (LSTM)** networks to capture non-linear market patterns and long-term dependencies in price data.

## 📂 Repository Structure

* `VolGaurd.ipynb`: The main Jupyter Notebook containing the end-to-end pipeline (Data fetching -> Preprocessing -> LSTM Training -> Evaluation).
* `vol_forecast_output_split.zip`: Contains pre-trained model weights and processed datasets (Unzip this to skip training).

## 🚀 Key Features

* **Deep Learning Architecture:** Implements a Stacked LSTM model using TensorFlow/Keras to prevent the vanishing gradient problem.
* **Automated Data Pipeline:** Fetches live historical data for `^NSEI` (Nifty 50) directly using `yfinance`.
* **Visual Analysis:** Plots "Actual vs. Predicted" volatility to identify market stress periods and regime changes.

## 🛠️ Quick Start

### Option 1: Run Locally
1.  **Clone the repository**
    ```bash
    git clone [https://github.com/Saimohith2402/VolGuard.git](https://github.com/Saimohith2402/VolGuard.git)
    cd VolGaurd
    ```

2.  **Install Dependencies**
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn tensorflow yfinance
    ```

3.  **Launch the Notebook**
    ```bash
    jupyter notebook VolGuard.ipynb
    ```

### Option 2: Google Colab
Since the file was created in Colab, you can simply upload `VolGuard.ipynb` to [Google Colab](https://colab.research.google.com/) and run the cells sequentially.

## 📊 Methodology

1.  **Preprocessing:** Converts Daily Closing Prices into Log Returns and calculates Realized Volatility over a rolling window.
2.  **Feature Scaling:** Applies `MinMaxScaler` to normalize data between 0 and 1 for optimal LSTM convergence.
3.  **Sequence Generation:** Creates time-step sequences (Look-back window) to transform time-series data into a supervised learning problem.
4.  **Forecasting:** Predicts future volatility and calculates error metrics (RMSE, MAE).

---
**Author:** [Sai Mohith](https://github.com/Saimohith2402)
