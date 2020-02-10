# Stock-market
Analyse and Interpret the Candle Sticks. Depending upon the Signal, Execute the Trade.


Approach 1:
Step 1: Check out the csv data

Step 2: Try to construct the candle sticks

Step 3: Connect the dots of csv files and candle sticks

Step 4: Create Equations which is the basis of construct along with the time Interval (3Mins - 5Mins)

Whenever we type the API key it shows an error 



Step 5: Write a Script which involves a function which is capable of creating candle stick of any particular stock.

Step 6: After creating the Candle sticks, we have to set the indicators which will be generating signals.

Whenever x goes less than y, the signal is short, whenever x goes above y. The signal is long. X is ema and y is super trend. 

X we can derive from here URL = "https://www.alphavantage.co/query?function=EMA&symbol=NSE:VEDL&interval=daily&time_period=7&series_type=close&apikey=Z13LQV3DUC249FO7"

Y is the Super Trend Supertrend is a trend following indicator like moving averages. It is calculated based on Average true range (ATR) and a multiplier value. ATR measures the degree of volatility of the market.

A buy signal is generated when Supertrend indicator closes above the price and a sell signal is generated when it closes below the closing price.

Below are the mathematical formulas involved in calculation of supertrend indicator:
True Range (TR) = Max of (High-Low, High-Close, Low-Close)
Average True Range (ATR) = Average of last n TR values (n is the first parameter in Supertrend indicator. 10 is default)
Basic Upperband  =  (High + Low) / 2 + Multiplier * ATR
Basic Lowerband =  (High + Low) / 2 – Multiplier * ATR
Final Upperband = IF( (Current Basic Upperband  < Previous Final Upperband) and (Previous Close > Previous Final Upperband)) Then (Current Basic Upperband) ELSE Previous Final Upperband)
Final Lowerband = IF( (Current Basic Lowerband  > Previous Final Lowerband) and (Previous Close < Previous Final Lowerband)) Then (Current Basic Lowerband) ELSE Previous Final Lowerband)
SUPERTREND = IF(Current Close <= Current Final Upperband ) Then Current Final Upperband ELSE Current  Final Lowerband


Approach 2:

Objective: Taking in the real time Graphical Charts, identify the call and Send the Message to the Telegram (ChatBot)


Step 1: Find a way to interpret those graphs and then think of a logic which can just operate the trade

