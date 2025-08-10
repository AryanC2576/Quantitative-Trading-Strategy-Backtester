# A Professional Walk-Forward Backtester for a Blended Quant Strategy

This repository contains the Python code for a robust, object-oriented framework designed to backtest a quantitative trading strategy. The project demonstrates a professional-grade research process, from feature engineering and signal blending to a rigorous walk-forward validation that minimizes lookahead bias.

The final strategy, tested on Oracle (ORCL) stock from 1995-2014, achieved a Sharpe Ratio of 3.49 with a Maximum Drawdown of only -10%.

[➡️ View the Full Interactive Notebook on Kaggle](https://www.kaggle.com/code/aryanchakravorty/blended-quant-strategy)

The Kaggle notebook provides a detailed, step-by-step narrative with explanations and interpretations for all plots and results.

## Key Features

* **Walk-Forward Engine:** The core of the framework. It avoids lookahead bias by simulating real-world performance with rolling train/test windows, ensuring the model only uses historical data to make predictions.

* **Blended Signal Strategy:** The strategy doesn't rely on a single idea. It combines four distinct alpha sources into a final trading signal:

* **Momentum:** A classic trend-following signal.

* **Regime-Aware RSI:** A mean-reversion signal that adapts its thresholds to market volatility.

* **MACD:** A trend and momentum indicator.

* **Machine Learning Model:** A Ridge Regression model trained on a rich set of features to predict next-day returns.

* **Advanced Risk Management:** The backtester includes two critical risk controls that were essential to the strategy's success:

A 2% daily stop-loss to cut losing trades quickly.

A volatility overlay that moves the strategy to cash during periods of extreme market turbulence.

* **Comprehensive Performance Analytics:** The framework automatically calculates a full suite of industry-standard metrics (Sharpe, Sortino, Calmar, Max Drawdown) and generates a dashboard of performance plots.

## Final Performance Metrics

<img width="470" height="281" alt="image" src="https://github.com/user-attachments/assets/17ad1e5b-0b56-4ef3-9ec9-f0788ed89fce" />

## Performance Dashboard Preview

### Technologies Used

* **Python 3**

* **Pandas & NumPy** for data manipulation

* **Scikit-learn** for machine learning (Ridge Regression)

* **TA (Technical Analysis Library)** for feature engineering

* **Matplotlib & Seaborn** for data visualization

### How to Run

1. Clone the repository:

    ```bash
    git clone https://github.com/AryanC2576/Quantitative-Trading-Strategy-Backtester.git
    ```

2. Install the required libraries:

    ```bash
    pip install pandas numpy scikit-learn ta matplotlib seaborn
    ````

3. Run the Notebook:

Open the .ipynb file in a Jupyter Notebook or JupyterLab environment and execute the cells.
