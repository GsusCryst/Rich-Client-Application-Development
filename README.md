# Rich-Client-Application-Development

## Termine

Bis 10.05

	NPM + webpack Pr�sentation

	5-10 S�tze Anwendungsbeschreibung bzw. Prosa der Projektidee 

Bis 17.05

	SWQ Tooling Pr�sentation

	Erste Version des Pflichtenheft

31.05 

	Pflichtenheft abgeschlossen


# Github Pages:

1. ES6
https://gsuscryst.github.io/Rich-Client-Application-Development/ES6.html

2. React.js
https://gsuscryst.github.io/Rich-Client-Application-Development/Reactjs.html

3. NPM + webpack

4. SWQ Tooling

# Projektbeschreibung - AlgoTrade

AlgoTrade constantly retrieves the trade data of a crypto exchange, computes the candlesticks in real time, derives several indicators and makes hold/buy/sell decisions based on all this data.

## References

1. MFI: http://stockcharts.com/school/doku.php?id=chart_school:technical_indicators:money_flow_index_mfi

2. RSI: http://stockcharts.com/school/doku.php?st=rsi&id=chart_school:technical_indicators:relative_strength_index_rsi

3. CCI: http://www.stockcharts.com/school/doku.php?id=chart_school:technical_indicators:commodity_channel_index_cci

4. EMA: http://stockcharts.com/school/doku.php?id=chart_school:technical_indicators:moving_averages

5. Candlestick: https://en.wikipedia.org/wiki/Candlestick_chart

6. Exchange Position (hold/buy/sell)
++ https://www.investopedia.com/terms/p/position.asp
++ https://www.investopedia.com/terms/h/hold.asp
++ https://www.investopedia.com/walkthrough/forex/getting-started/buying-selling.aspx

## Configuration
ToDo

## Design
### Challenges
1. Update indicators and make buy/sell decisions in real time (goal: every 10ms)
2. Handle algotrade downtimes, failsafe for open position handling 
3. Handle exchange API downtimes
4. Handle high latency networks
5. Implement indicators (MFI, RSI, CCI & EMA) with 1m/5m/15m/30m/1h/4h/1d/1w timeframes resolution
6. Save market data, indicators, trade decisions and executed order details in postgreSQL database

### Solution
We use a central event queue and a pub/sub-like implementation.
First, we always poll the exchange api as often as is allowed, check if there are any new trades and if so, add an event to the queue with the new data. 
Using a separate event queue solves challenge 1 and passing the event only on new data solves out-of-order responses and therefore challenge 4.
Secondly, we take the new trading data + the old and if they are continuous and complete enough (this solves challenges 2 and 3), we calculate the candlesticks, then add them to the queue
Thirdly, we calculate all indicators in parallel.
Fourthly, we make a hold/buy/sell decision based on the indicators.
Finally the market data, indicators and executed order details are stored into the database.

## Implementation notes
ToDo