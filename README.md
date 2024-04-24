# BB + ATR + MA Trading Strategy

This repository contains a trading strategy implemented in Pine Script for TradingView. The strategy combines Bollinger Bands (BB), Average True Range (ATR), and Moving Average (MA) indicators to generate buy and sell signals for trading NYSE-listed stocks.

## Strategy Components

### Bollinger Bands (BB)
- Parameters: Length = 14, Standard Deviation = 1.9
- Plots upper and lower bands on the price chart.
- Buy Signal: Crosses above upper band.
- Sell Signal: Crosses below lower band.

### Moving Average (MA)
- Parameters: Period = 300
- Plots a simple moving average (SMA) on the price chart.
- Buy Signal: Price above MA.
- Sell Signal: Price below MA.

### Average True Range (ATR)
- Parameter: Period = 14
- Plots ATR value on the price chart.
- Volatility filter: Buy/Sell if ATR > 55.

## Strategy Execution
- Long Entry: Buy signal triggered when all conditions (BB, MA, ATR) are met.
- Short Entry: Sell signal triggered when all conditions (BB, MA, ATR) are met.
- Exit conditions: Implemented trailing stop loss and take profit, along with stop loss and take profit based on percentage.
- Trail Stop: A trailing stop loss is applied as a percentage of the current close price.
- Trail Offset: After reaching the defined percentage, the trailing offset starts, and the trailing offset is a stop order placed at the defined trail offset percentage.

## Parameters
- Trailing Stop %: Percentage for trailing stop loss.
- Trailing Offset %: Percentage for trailing offset.
- SL: Stop loss percentage.
- TP: Take profit percentage.

## Usage
1. Apply the strategy on the TradingView platform to visualize the signals on stock charts.
2. Customize parameters according to risk tolerance and market conditions.
3. Backtest the strategy to evaluate performance under different market scenarios.

## Repository Structure
- `BB_ATR_MA_Strategy.pine`: Pine Script file containing the trading strategy code.
- `README.md`: This file providing an overview of the strategy and instructions for usage.

Feel free to explore and modify the strategy to suit your trading preferences and objectives.

