Step 1: Reading & Structuring the Data
We imported libraries like pandas.

Chose 5 stocks: AAPL, AMZN, GOOG, MSFT, and TSLA.

Read their .txt files and combined them into one DataFrame.

Created a MultiIndex DataFrame where:

Rows are indexed by Ticker and Date.

Columns include Open, High, Low, Close, Volume, OpenInt.

Step 2: Data Cleaning
Converted the Date column to proper datetime format.

Sorted data by date within each ticker.

Identified and filled missing rows (including fully missing dates) using forward-fill.

Filtered the data to include only the last 10 years (from 2007-11-10 to 2017-11-10, since our data ends in 2017).

Step 3: Data Transformation
We added 4 useful columns for each stock:

Daily Return – % change in closing price day-to-day.

7-day Moving Average (MA7) – Smooths out short-term price trends.

30-day Moving Average (MA30) – Highlights longer trends.

30-day Rolling Volatility – Standard deviation of returns over the past 30 days.

Step 4: Exploratory Analysis
We answered:

Which stock had the highest average return?
→ Calculated the mean daily return for each stock.

Which stock and month were most volatile?
→ Grouped by month and ticker, then found the max rolling volatility.
