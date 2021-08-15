# Finance Projects

- Quant Project 1
    - RSI_BACKTESTING_RELIANCE

        - The goal of this assignment was to write a code to backtest a long-only trading system based on certain technical indicators
        - The technical indicator I used to get my buy and sell signal was RSI (Relative Strength Index).

    - Methodology Approach:
        - In the beginning, I import necessary libraries and download csv data from yahoo financials
        - After that, I load it into a pandas dataframe and calculate 100 days simple moving average (to show trend in the stock data) and 19 days RSI using Exponential moving average. I add these as columns in my original dataframe and plot them
        - Then I implement my trading strategy :
            - I go long when the RSI crosses horizontal 30 reference level from above
            - And sell when the RSI crosses horizontal 70 reference level from below
        - Based on this trading strategy (profit booking logic), buy and sell signals were generated. From these signals only those sell signals which were preceded by a buy signal and similarly for buy signals were chosen to represent the actual trading entry and exit points.
        - Furthermore, at each buy signal, the entire capital available was used in buying stocks. This is because, at the end of each trade, percentage profit will remain the same irrespective of the initial capital. Hence maximum profit will be extracted for maximum initial capital. So, all the capital available was used in buying stocks.
        - Transaction cost of 1% of the total amount traded is paid during each trade
        - Detailed trading plot and dataframe show all the trades done and portfolio price at that time
        - Finally, I compare the results between applying my trading strategy and just holding the stock

    - SMA_BACKTESTING_RELIANCE

        - Similar task to RSI_BACKTESTING, just the technical indicator used was SMA
