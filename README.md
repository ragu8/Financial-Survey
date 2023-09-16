# FinRL: Financial Reinforcement Learning 


<div align="center">
<img align="center" src= width="55%"/>
</div>



| Dev Roadmap  | Stage | Users | Project | Desription |
|----|----|----|----|----|
| 0.0 (Preparation) | entrance | practitioners | [FinRL-Meta](https://github.com/AI4Finance-Foundation/FinRL-Meta)| gym-style market environments |
| 1.0 (Proof-of-Concept)| full-stack | developers | [FinRL](https://github.com/AI4Finance-Foundation/FinRL) | automatic pipeline |
| 2.0 (Professional) | profession | experts | [ElegantRL](https://github.com/AI4Finance-Foundation/ElegantRL) | algorithms |
| 3.0 (Production) | service | hedge funds | [Podracer](https://github.com/AI4Finance-Foundation/FinRL_Podracer) | cloud-native deployment |


## Outline

  - [Overview](#overview)
  - [Tutorials](#tutorials)
  - [Publications](#publications)
  - [Data Sources](#data-sources)


## Overview

FinRL has three layers: market environments, agents, and applications.  For a trading task (on the top), an agent (in the middle) interacts with a market environment (at the bottom), making sequential decisions.

<div align="center">
<img align="center" src=figs/finrl_framework.png>
</div>

A quick start: Stock_NeurIPS2018.ipynb. Videos [FinRL](http://www.youtube.com/watch?v=ZSGJjtM-5jA) at [AI4Finance Youtube Channel](https://www.youtube.com/channel/UCrVri6k3KPBa3NhapVV4K5g).


## Tutorials

+ [Towardsdatascience] [Deep Reinforcement Learning for Automated Stock Trading](https://towardsdatascience.com/deep-reinforcement-learning-for-automated-stock-trading-f1dad0126a02)

A complete list at [blogs](https://github.com/AI4Finance-Foundation/Blogs)







## Publications

|Title |Conference |Link|Citations|Year|
|  ----  |  ----  |  ----  |  ----  |  ----  |
|**FinRL-Meta**: FinRL-Meta: Market Environments and Benchmarks for Data-Driven Financial Reinforcement Learning| NeurIPS 2022| [paper](https://arxiv.org/abs/2211.03107) [code](https://github.com/AI4Finance-Foundation/FinRL-Meta) | 1 | 2022 |
|**FinRL**: Deep reinforcement learning framework to automate trading in quantitative finance| ACM International Conference on AI in Finance (ICAIF) | [paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3955949) | 24 | 2021 |
|**FinRL-Podracer**: High performance and scalable deep reinforcement learning for quantitative finance | ACM International Conference on AI in Finance (ICAIF) | [paper](https://arxiv.org/abs/2111.05188) [code](https://github.com/AI4Finance-Foundation/FinRL_Podracer) | 9 | 2021 |
|Explainable deep reinforcement learning for portfolio management: An empirical approach| ACM International Conference on AI in Finance (ICAIF) | [paper](https://arxiv.org/abs/2111.03995) [code](https://github.com/AI4Finance-Foundation/FinRL-Meta/blob/master/tutorials/2-Advance/FinRL_PortfolioAllocation_Explainable_DRL/FinRL_PortfolioAllocation_Explainable_DRL.py](https://github.com/AI4Finance-Foundation/FinRL-Tutorials/tree/master/2-Advance))| 3 | 2021 |
|**FinRL**: A deep reinforcement learning library for automated stock trading in quantitative finance| NeurIPS 2020 Deep RL Workshop  | [paper](https://arxiv.org/abs/2011.09607) | 54 | 2020 |
|Deep reinforcement learning for automated stock trading: An ensemble strategy| ACM International Conference on AI in Finance (ICAIF) | [paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3690996) [code](https://github.com/AI4Finance-Foundation/FinRL-Meta/blob/master/tutorials/2-Advance/FinRL_Ensemble_StockTrading_ICAIF_2020/FinRL_Ensemble_StockTrading_ICAIF_2020.ipynb) | 103 | 2020 |
|Practical deep reinforcement learning approach for stock trading | NeurIPS 2018 Workshop on Challenges and Opportunities for AI in Financial Services| [paper](https://arxiv.org/abs/1811.07522) [code](https://github.com/AI4Finance-Foundation/DQN-DDPG_Stock_Trading](https://github.com/AI4Finance-Foundation/FinRL/tree/master/examples))| 131 | 2018 |



##  Data Sources

|Data Source |Type |Range and Frequency |Request Limits|Raw Data|Preprocessed Data|
|  ----  |  ----  |  ----  |  ----  |  ----  |  ----  |
|[Akshare](https://alpaca.markets/docs/introduction/)| CN Securities| 2015-now, 1day| Account-specific| OHLCV| Prices&Indicators|
|[Alpaca](https://alpaca.markets/docs/introduction/)| US Stocks, ETFs| 2015-now, 1min| Account-specific| OHLCV| Prices&Indicators|
|[Baostock](http://baostock.com/baostock/index.php/Python_API%E6%96%87%E6%A1%A3)| CN Securities| 1990-12-19-now, 5min| Account-specific| OHLCV| Prices&Indicators|
|[Binance](https://binance-docs.github.io/apidocs/spot/en/#public-api-definitions)| Cryptocurrency| API-specific, 1s, 1min| API-specific| Tick-level daily aggegrated trades, OHLCV| Prices&Indicators|
|[CCXT](https://docs.ccxt.com/en/latest/manual.html)| Cryptocurrency| API-specific, 1min| API-specific| OHLCV| Prices&Indicators|
|[EODhistoricaldata](https://eodhistoricaldata.com/financial-apis/)| US Securities| Frequency-specific, 1min| API-specific | OHLCV | Prices&Indicators|
|[IEXCloud](https://iexcloud.io/docs/api/)| NMS US securities|1970-now, 1 day|100 per second per IP|OHLCV| Prices&Indicators|
|[JoinQuant](https://www.joinquant.com/)| CN Securities| 2005-now, 1min| 3 requests each time| OHLCV| Prices&Indicators|
|[QuantConnect](https://www.quantconnect.com/docs/home/home)| US Securities| 1998-now, 1s| NA| OHLCV| Prices&Indicators|
|[RiceQuant](https://www.ricequant.com/doc/rqdata/python/)| CN Securities| 2005-now, 1ms| Account-specific| OHLCV| Prices&Indicators|
|[Tushare](https://tushare.pro/document/1?doc_id=131)| CN Securities, A share| -now, 1 min| Account-specific| OHLCV| Prices&Indicators|
|[WRDS](https://wrds-www.wharton.upenn.edu/pages/about/data-vendors/nyse-trade-and-quote-taq/)| US Securities| 2003-now, 1ms| 5 requests each time| Intraday Trades|Prices&Indicators|
|[YahooFinance](https://pypi.org/project/yfinance/)| US Securities| Frequency-specific, 1min| 2,000/hour| OHLCV | Prices&Indicators|


<!-- |Data Source |Type |Max Frequency |Raw Data|Preprocessed Data|
|  ----  |  ----  |  ----  |  ----  |  ----  |
|    AkShare |  CN Securities | 1 day  |  OHLCV |  Prices, indicators |
|    Alpaca |  US Stocks, ETFs |  1 min |  OHLCV |  Prices, indicators |
|    Alpha Vantage | Stock, ETF, forex, crypto, technical indicators | 1 min |  OHLCV  & Prices, indicators |
|    Baostock |  CN Securities |  5 min |  OHLCV |  Prices, indicators |
|    Binance |  Cryptocurrency |  1 s |  OHLCV |  Prices, indicators |
|    CCXT |  Cryptocurrency |  1 min  |  OHLCV |  Prices, indicators |
|    currencyapi |  Exchange rate | 1 day |  Exchange rate | Exchange rate, indicators |
|    currencylayer |  Exchange rate | 1 day  |  Exchange rate | Exchange rate, indicators |
|    EOD Historical Data | US stocks, and ETFs |  1 day  |  OHLCV  | Prices, indicators |
|    Exchangerates |  Exchange rate |  1 day  |  Exchange rate | Exchange rate, indicators |
|    findatapy |  CN Securities | 1 day  |  OHLCV |  Prices, indicators |
|    Financial Modeling prep | US stocks, currencies, crypto |  1 min |  OHLCV  | Prices, indicators |
|    finnhub | US Stocks, currencies, crypto |   1 day |  OHLCV  | Prices, indicators |
|    Fixer |  Exchange rate |  1 day  |  Exchange rate | Exchange rate, indicators |
|    IEXCloud |  NMS US securities | 1 day  | OHLCV |  Prices, indicators |
|    JoinQuant |  CN Securities |  1 min  |  OHLCV |  Prices, indicators |
|    Marketstack | 50+ countries |  1 day  |  OHLCV | Prices, indicators |
|    Open Exchange Rates |  Exchange rate |  1 day  |  Exchange rate | Exchange rate, indicators |
|    pandas\_datareader |  US Securities |  1 day |  OHLCV | Prices, indicators |
|    pandas-finance |  US Securities |  1 day  |  OHLCV  & Prices, indicators |
|    Polygon |  US Securities |  1 day  |  OHLCV  | Prices, indicators |
|    Quandl | 250+ sources |  1 day  |  OHLCV  | Prices, indicators |
|    QuantConnect |  US Securities |  1 s |  OHLCV |  Prices, indicators |
|    RiceQuant |  CN Securities |  1 ms  |  OHLCV |  Prices, indicators |
|    Tiingo | Stocks, crypto |  1 day  |  OHLCV  | Prices, indicators |
|    Tushare |  CN Securities | 1 min  |  OHLCV |  Prices, indicators |
|    WRDS |  US Securities |  1 ms  |  Intraday Trades | Prices, indicators |
|    XE |  Exchange rate |  1 day  |  Exchange rate | Exchange rate, indicators |
|    Xignite |  Exchange rate |  1 day  |  Exchange rate | Exchange rate, indicators |
|    YahooFinance |  US Securities | 1 min  |  OHLCV  |  Prices, indicators |
|    ystockquote |  US Securities |  1 day  |  OHLCV | Prices, indicators | -->



OHLCV: open, high, low, and close prices; volume. adjusted_close: adjusted close price

Technical indicators: 'macd', 'boll_ub', 'boll_lb', 'rsi_30', 'dx_30', 'close_30_sma', 'close_60_sma'. Users also can add new features.
