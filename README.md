Cryptocurrency 15 Minute Return Forecasting
====================================================

#### Authors: [Aidan Jackson](https://github.com/aidan-jackson-data) | [Piotr Parkitny](https://github.com/pparkitn) | [Sandip Panesar](https://github.com/sandzp)

Winter 2021

## Disclaimer

This work is for general informational purposes only and does not constitute financial, investment, or any other kind of advice. The authors do not endorse any specific content found here or linked elsewhere. Invest at your own risk.

## Description

This repository contains traditional time series approaches towards forecasting the 15 minute returns of various cryptocurrencies. Cryptocurrencies, such as Bitcoin, were first publicly released around ~2010 and have dramatically increased in market capitalization between 2020-2022. Individuals in commerce, technology, and the general public have taken strong opinions, both positive and negative, on the long term impact and value of cryptocurrencies. While the far future is uncertain, their short term volatility has already been [noted](https://www.youtube.com/watch?v=9MD77Us4_r4) in popular culture for its ability to bring riches or ruin to those who invest. Given this volatility, a method to forecast the market could grow an initial principal much faster than an equally precise method for other investments, such as stocks, precious metals, or foreign currencies.* 

To this end, G-Research hosted a Kaggle competition with the challenge of forecasting 15 minute returns, on an interval of every minute, for a period of three months. A 15 minute return refers to the return on investment 15 minutes into the future should an individual purchase a specific cryptocurrency in the current minute. Minute by minute price information on 14 different cryptocurrencies was aggregated going as far back as prior to 2010 when several coins first publicly appeared. Because historical price information is public, evaluation was done on the future three months worth of data once the competition ended. In order to have a single metric by which entries could be judged, a weighted average was taken from the correlation of predicted to actual returns across all 14 coins.

The 14 coins were:

* Binance Coin
* Bitcoin
* Bitcoin Cash
* Cardano
* Dogecoin
* EOS.IO
* Ethereum
* Ethereum Classic
* IOTA
* Litecoin
* Maker
* Monero
* Stellar
* TRON

Data was recorded in long format, with each entry representing a unique observation of a given cross section at a given time. For a given coin in a given minute, the following information was included:

* Target (15 Minute Return, the outcome variable to predict)
* Count (Number of transactions during the minute)
* Volume (Number of units traded during the minute)
* Open (Opening price at the start of the minute)
* Close (Closing price at the end of the minute)
* High (Maximum price during the minute)
* Low (Minimum price during the minute)
* VWAP (Volume Weighted Average Price during the minute)
* Asset ID (Unique identifier for each coin)
* Timestamp (Minute index)


*Note that some individuals and economic theories, such as the [efficient market hypothesis](https://en.wikipedia.org/wiki/Efficient-market_hypothesis), hold that characteristics such as price, and dependent quantities such as return or volatility, are impossible to predict by their nature. Whether or not this is correct, any set of repeated forecasts should take into consideration the number of attempts when judging the significance of a result. For example, if 100 different forecasts are made on the same time series, is it really surprising if 5 of them would have resulted in great returns? How much money would you be willing to stake if you repeat that forecast into the future?

## Results

In this project, the final three months worth of data was set aside as a test set. This is comparable to the Kaggle competition, but is not an exact match nor were these models entered. Their potential leaderboard ranking should they have been, assuming similar performance, is shown below.

|Model | Weighted Average Correlation | Potential Leaderboard Ranking |
|:------:|:-------:|:------------:|
|ARX(6) |0.0058|294/1969 (Top 15%)|
|VARX(15) |0.0077|196/1969 (Top 10%)|
  
### Citation

Orignal Kaggle Competition [Link](https://www.kaggle.com/c/g-research-crypto-forecasting)
  
