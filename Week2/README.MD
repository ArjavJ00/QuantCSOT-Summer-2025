AMZN Stock Price Prediction & Strategy Backtesting
This project focuses on modeling Amazon (AMZN) stock prices using multiple machine learning and statistical models. It evaluates each model's prediction accuracy and simulates a simple trading strategy based on the best-performing model.

Contents
final_cleaned_df.pkl: Preprocessed stock data for multiple tickers including AMZN.

Amzn Stock Modeling.ipynb: Jupyter Notebook with all analysis and modeling.

Objectives
Predict next-day closing prices of AMZN using:

Linear Regression (Lag features)

ARIMA (Time series)

Random Forest (Technical indicators)

Evaluate each model using Mean Absolute Error (MAE)

Backtest a simple long-short strategy based on the best model

Visualize cumulative profit over time

⚙Methods
Models Used:
Model	Description
Linear Regression	Uses previous 5 days’ close prices to predict the next
ARIMA	ARIMA(5,1,0) on closing price series
Random Forest	Uses MA7, MA30, Daily Return, and Volatility30 as features

Evaluation:
MAE (Mean Absolute Error) on test set

Backtesting:
Strategy:

Buy (Long) if predicted price > actual

Sell (Short) if predicted price < actual

Compute daily PnL and cumulative profit over test period

Results
Model	MAE
Linear Regression	=> Lowest MAE
ARIMA	
Random Forest	

Linear Regression yielded the lowest prediction error and was used for backtesting.

How to Run
Install required packages:
pip install pandas numpy matplotlib scikit-learn statsmodels

Open the Jupyter notebook:
jupyter notebook "Amzn Stock Modeling.ipynb"

Ensure the final_cleaned_df.pkl file is in the same directory.

Output
MAE comparison table

Cumulative Profit plot

Final hypothetical profit from strategy
