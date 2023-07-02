# Crypto_time_series_analysis

This project aims to analyze cryptocurrency price data and make predictions using time series analysis and machine learning techniques.

## Prerequisites

Make sure you have the following libraries installed:

- pandas
- seaborn
- numpy
- pymysql
- sqlalchemy
- tqdm
- python-binance
- matplotlib
- statsmodels
- arch

## Installation

1. Clone the repository: git clone https://github.com/kings-data-quest/Crypto_time_series_analysis
2. Install the required packages: pip install -r requirements.txt


## Examples

### Collecting Data

```python
import pandas as pd
from binance import Client

client = Client()
symbol = 'BTCUSDT'
interval = client.KLINE_INTERVAL_1HOUR
start = '2021-01-01'
end = '2022-01-01'

data = client.get_historical_klines(symbol, interval, start, end)
df = pd.DataFrame(data, columns=['Timestamp', 'Open', 'High', 'Low', 'Close', 'Volume'])
df.to_csv('btc_data.csv', index=False)





