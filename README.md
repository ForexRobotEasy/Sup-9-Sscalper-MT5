# Sup 9 Scalper MT5

This code is a sample implementation of the Sup 9 Scalper MT5 trading strategy developed by Forex Robot Easy Team. The strategy is designed for high volume auto forex trading on the MT5 platform.

## Product Description

Sup 9 Scalper MT5 is an advanced forex trading robot that uses a unique algorithm to identify market trends and execute trades automatically. It is designed for traders who prefer high volume trading with precise entry and exit points.

Key Features:
- High volume auto forex trading
- Precise entry and exit points based on market trends
- Adjustable trade volume, stop loss, and take profit levels
- Maximum trades per day limit to manage risk
- Real-time trade logging and result tracking

## How it Works

1. The program connects to a local database using the InrexEADB class and initializes the necessary libraries for trade execution and tick calculation.

2. The OnTick() function is the main entry point of the program and is called on every tick of the market. It first checks if the maximum number of trades per day has been reached. If so, it halts trading and prints a message.

3. The program retrieves the current market trend for the XAUUSD symbol from the database using the db.GetMarketTrend() function.

4. The tick value is calculated using the tickCalc.CalculateTickValue() function for the XAUUSD symbol.

5. The trade direction is determined based on the market trend. If the trend is positive, a buy order is placed; otherwise, a sell order is placed.

6. The trade.PlaceOrder() function is called to execute the trade with the specified trade volume, trade type, stop loss, and take profit levels.

7. The trade result is calculated based on the tick value and trade volume. It is then logged in the database using the db.LogTradeResult() function.

8. Trade information including the symbol, volume, trade type, and trade result is printed using the Print() function.

9. The OnInit() function is called during program initialization. It connects to the database, initializes trade execution and tick calculation. If any of these initialization steps fail, the program terminates and prints an error message.

10. The OnDeinit() function is called during program termination. It disconnects from the database and terminates trade execution and tick calculation.

11. The OnStart() and OnStop() functions are called when the program starts and stops respectively. They simply print a message indicating the program status.

## Disclaimer

This code is provided as a sample implementation of the Sup 9 Scalper MT5 trading strategy developed by Forex Robot Easy Team. ForexRobotEasy is not the official developer of this product. To find the official developer of this product and for detailed reviews and trading results, please visit [Forex Robot Easy - Sup 9 Scalper MT5 Review](https://forexroboteasy.com/forex-robot-review/sup-9-scalper-mt5-review-high-volume-auto-forex-trading/).

Please note that trading in the forex market involves substantial risk and may not be suitable for all investors. It is important to carefully consider your investment objectives, level of experience, and risk appetite before making any investment decisions.
