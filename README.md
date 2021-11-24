# Crypto-Trading-Bot
Ever notice that when Bitcoin rallies so do the rest and when Bitcoins down your whole trading dashboard is red. 
The only difference between most of the altcoins issue in the short run is the delays between them following each others previous move forward. 
So instead of riding the wild market, this crypto bot looks at established coin pairs. When one coin drops 
relative to another it buys the falling coin, under the assumption that it will catch up with the rising coin resulting in an increase in number of coins held.
For example, take BTC price to be 60k and ETH price to be 4k (a ratio between their prices of 15), say BTC rallies up to 64k while ETH remains at 4k, the strategy 
assumes that ETH will now follow BTC, so if we buy 1 ETH currently worth 4/64 = 0.0625 BTC, then when 1 BTC is eventually worth 15 ETH again, we can swap from ETH to BTC.
Our capital has gone from being worth 1/16 BTC = 0.0625 to 1/15 BTC = 0.0667. Assuming that BTC holds its value with respect to fiat currency in the long term, 
We can keep trading off these fluctuations in ratios between coins - this is known as a mean reversion strategy.
The main parameters of the program are the percentage change in ratio at which we initiate the first trade and the coins on which we look for trades.
A low percentage of fluctuation will result in lots of trades very frequently each making a small amount of profit, while a larger percentage will produce fewer trades but each more profitable.
Since we are limited also by a 0.075% trading fee on the binance trading platform we must also take this into account when deciding whether a coin pair could make a profitable trade based on this strategy.
Through backtesting I have found that making trades at a 5% fluctuation in the coin pair from when the held coin was first entered is most profitable.
I am constantly trying different coin lists but stick to coins in the top 100 by market cap.
