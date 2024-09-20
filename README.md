# 📊 Stock Portfolio Optimization and Backtesting using Python

This project demonstrates the process of **optimizing a stock portfolio** using historical data and evaluating its performance through **backtesting**. The optimization is performed using modern portfolio theory, where the goal is to maximize the portfolio's **Sharpe Ratio** (risk-adjusted return) with constraints on the minimum and maximum allocation for each asset. The project also integrates risk metrics, Monte Carlo simulations, and backtesting to assess how the optimized portfolio performs in both in-sample (training) and out-of-sample (testing) periods.

This project is implemented and run entirely in **Google Colab**, allowing easy access and usage without needing a local Python environment.

## Key Features:
1. **Data Fetching from Yahoo Finance**:
   - Real-time historical data is fetched for selected stock tickers using the `yfinance` API.

2. **Portfolio Optimization**:
   - The portfolio weights are optimized based on maximizing the **Sharpe Ratio**.
   - Constraints: Minimum 5% and maximum 95% allocation for each asset to maintain diversification.

3. **Risk Metrics**:
   - **Sharpe Ratio**: Measures the portfolio's risk-adjusted returns.
   - **Sortino Ratio**: Similar to Sharpe but focuses on downside risk.
   - **Maximum Drawdown**: The largest peak-to-trough loss during the given time period.
   - **Value at Risk (VaR)**: Estimates potential losses at a 95% confidence level.

4. **Monte Carlo Simulation**:
   - A Monte Carlo simulation projects the portfolio’s potential future performance by generating multiple simulated paths using the optimized portfolio weights.

5. **Train-Test Split for Backtesting**:
   - The dataset is split into **in-sample (training)** and **out-of-sample (testing)** periods.
   - The portfolio is optimized using the in-sample data and tested on the out-of-sample data to assess how the strategy performs on unseen data.

6. **Backtesting**:
   - The optimized portfolio is backtested on out-of-sample data to evaluate its performance in real-world market conditions, with risk metrics such as Sharpe Ratio and Maximum Drawdown calculated during the backtest.

7. **Visualization**:
   - Plot of cumulative returns over time.
   - Asset allocation pie chart.
   - Monte Carlo simulation plot.
   - Backtested performance with key risk metrics.

## How to Run This Project on Google Colab:

1. **Open Google Colab**: Go to [Google Colab](https://colab.research.google.com/).
2. **Upload the Notebook**: Upload the `.ipynb` file containing the code for portfolio optimization and backtesting.
3. **Install Required Libraries**:
   Make sure to run the following in the first code cell to install dependencies:
   ```python
   !pip install yfinance matplotlib pandas numpy scipy
