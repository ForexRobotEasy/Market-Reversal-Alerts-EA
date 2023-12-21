# Market Reversal Alerts EA ReadMe File

## Description
The Market Reversal Alerts EA is an expert advisor that helps identify market structure shifts and triggers trades based on these reversals. It uses the Market Reversal Alert custom indicator to determine changes in market direction and the RSI indicator to confirm overbought or oversold conditions.

The EA draws support rectangles as price moves in the current trend direction, providing visual cues for potential support levels. When a sharp reversal occurs and the RSI value is below 30, the EA triggers a buy trade. Conversely, when a sharp reversal occurs and the RSI value is above 70, the EA triggers a sell trade.

Please note that ForexRobotEasy is not the official developer of this product. This code serves as a sample that can work based on the product's description. To find the official developer of this product, please refer to the MQL5 website.

For detailed reviews and trading results of this product, please visit [Market Reversal Alerts EA Review](https://forexroboteasy.com/forex-robot-review/market-reversal-alerts-ea-review-analyzing-forex-software-for-professional-traders/).

## Global Variables
- `RSI_Period`: The period used for calculating the RSI indicator (default: 14).
- `MA_Period`: The period used for calculating the Moving Average indicator (default: 20).
- `Risk_Percentage`: The risk percentage per trade (default: 2.0).

## Custom Indicator - Market Reversal Alert
This function implements the Market Reversal Alert indicator in the EA code to identify market structure shifts. It returns the indicator value calculated using the `iCustom` function.

## Function - Draw Support Rectangles
This function calculates support levels based on the Moving Average indicator and draws support rectangles on the chart. It uses the `iMA` function to calculate the support levels and the `ObjectCreate` and `ObjectSet` functions to draw the support rectangles.

## Function - Trigger Trades
This function triggers trades based on the market reversal alerts and the RSI indicator values. If a market reversal alert occurs and the RSI value is below 30, a buy trade is executed. If a market reversal alert occurs and the RSI value is above 70, a sell trade is executed. The `OrderSend` function is used to execute the trades.

## OnTick Event
This event is the main program loop of the EA. It calls the `DrawSupportRectangles` function to draw support rectangles and the `TriggerTrades` function to trigger trades.

## OnInit Event
This event is called during the EA initialization process. It adds necessary indicators to the chart using the `IndicatorSetString` and `IndicatorSetInteger` functions.

## OnDeinit Event
This event is called when the EA is deinitialized. It removes the support rectangles from the chart using the `ObjectDelete` function.

## Start Function
This is the program start function of the EA. It specifies the developer's site and name, and then calls the `OnTick` function.

Please note that this ReadMe file provides an overview of the code and its functionalities. For more detailed information, please refer to the official documentation or the product's website on MQL5.
