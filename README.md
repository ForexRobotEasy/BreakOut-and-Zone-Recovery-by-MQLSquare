# BreakOut and Zone Recovery

This code implements the BreakOut and Zone Recovery strategy in the MQLSquare software for automated Forex trading. This strategy is designed to recover from losing trades by opening new trades in the opposite direction within a specific zone.

## Product Description

Forex Robot Easy presents the BreakOut and Zone Recovery strategy implemented in the MQLSquare software. This strategy aims to recover from losing trades by opening new trades within a predefined zone. By utilizing this strategy, traders can potentially mitigate losses and improve overall trading performance.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - BreakOut and Zone Recovery Review](https://forexroboteasy.com/forex-robot-review/breakout-zone-recovery-unbiased-review-on-mqlsquares-forex-software/). Please note that Forex Robot Easy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.

## Code Explanation

The code starts by including the necessary Trade library for managing trades. It also defines two constants: ZONE_SIZE, which represents the size of the zone around open losing trades, and MULTIPLIER, which is the multiplier for increasing the lot size in the zone recovery process.

Next, an instance of the CTrade object is created for executing trades. Two global variables, initialLotSize and currentLotSize, are defined to store the initial and current lot sizes for trading.

In the OnInit() function, the initial lot size is set using the Lots() function from the CTrade object. The current lot size is also initialized to the initial lot size.

The OnTick() function is the main logic of the trading strategy. It checks if there are any open losing trades by verifying if the total number of positions is greater than zero and the position profit is negative.

If there are open losing trades, the zone boundaries are calculated based on the open price of the losing trade and the zone size. The lower and upper zone boundaries are determined by subtracting and adding the zone size multiplied by the trade point, respectively.

The current price is then checked if it falls within the zone boundaries. If it does, a new trade is opened in the opposite direction within the zone using the Sell() and Buy() functions from the CTrade object. The lot size for the new trade is increased by multiplying the current lot size with the multiplier.

Finally, a message is printed to inform the user about the increased lot size.

The OnStart() function serves as the entry point of the program. It runs the trading process continuously by calling the OnTick() function and sleeping for 1 second between iterations using the Sleep() function.

## Disclaimer

Please note that Forex Robot Easy is not the official developer of this product. This code is only provided as a sample that can work as described in the mentioned product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - BreakOut and Zone Recovery Review](https://forexroboteasy.com/forex-robot-review/breakout-zone-recovery-unbiased-review-on-mqlsquares-forex-software/).
