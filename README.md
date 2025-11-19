# task-1-download-data-in-csv-file-
This project provides a REST API built using Flask that downloads stock market OHLCV data (Open, High, Low, Close, Volume) using Yahoo Finance, resamples it into custom time intervals, cleans the data, fixes datetime serialization issues, and returns JSON-ready candlestick data.  The API supports any NSE/BSE stock symbol as well as global tickers.

How It Works (Short Explanation)

The API receives stock symbol + date range + interval.
Downloads OHLCV data using yfinance.
Cleans column names and detects the datetime column.
Resamples the data using Pandas (Open = first, High = max, Low = min, Close = last, Volume = sum).
Converts Python datetime objects into strings so JSON can handle them
Returns the final structure as a clean JSON list.
