
# S&P 500 Stock Backtesting Strategy

This project provides a Python-based backtesting strategy for S&P 500 stocks. It utilizes Yahoo Finance data to download stock prices and calculate various features to evaluate short-term reversals and rank stocks based on these features. The strategy involves ranking stocks and then simulating a trading strategy over a specified time range.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Backtesting](#backtesting)
- [Output](#output)
- [Contributing](#contributing)
- [License](#license)

## Installation

### Prerequisites

- Python 3.9+
- Required packages:
  - `pandas`
  - `numpy`
  - `yfinance`
  - `pytz`

Install the required packages using pip:

```bash
pip install pandas numpy yfinance pytz
```

## Usage

1. **Set Up Dates and Download Data**: The code downloads S&P 500 data for a given date range and computes various stock features.
2. **Calculate Stock Features**: Calculates stock returns, volatility, momentum, and detrended volume.
3. **Analyze Short-Term Reversals**: Evaluates short-term reversals based on volume and price changes.
4. **Backtest Strategy**: Simulates a simple long-only trading strategy based on ranked stocks.

### Running the Script

1. Download S&P 500 tickers:
    ```python
    tickers = get_sp500_tickers()
    ```

2. Set start and end dates for downloading data:
    ```python
    start_date = '2024-01-01'
    end_date = '2024-10-05'
    ```

3. Download stock data:
    ```python
    stock_data = download_data(tickers, start_date, end_date)
    ```

4. Backtest strategy between specified dates:
    ```python
    backtest_start_date = '2024-09-30'
    backtest_end_date = '2024-10-05'
    backtest_results = backtest_strategy(stock_data, backtest_start_date, backtest_end_date)
    print(backtest_results)
    ```

## Features

- **Stock Feature Calculation**: Includes return, log return, and volume calculations for the selected stock symbols.
- **Short-Term Reversal Analysis**: Evaluates reversals in stock prices based on trading volume and price trends.
- **Ranking Stocks**: Ranks stocks based on multiple features such as momentum, volatility, and short-term reversal percentages.

## Backtesting

The strategy simulates buying and selling stocks based on their rank. The backtesting script will output the performance over the backtested period and the selected stocks.

## Output

- **Portfolio Value**: Displays the portfolio value over the backtested dates.
- **Held Stocks**: Lists the stocks held during each trading day in the backtesting period.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or new features.

## License

This project is open-source and available under the MIT License.
