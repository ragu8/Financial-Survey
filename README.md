# FinRL: Financial Reinforcement Learning - Survey


<div align="center">
<img align="center" src=image/banner.png />
</div>



## Outline

  - [Overview](#overview)
  - [Recent Advances](#recent-advances)
  - [Publications](#publications)
  - [Related Works](#related-works)
  - [Data Sources](#data-sources)
  - [Tutorials](#tutorials)


## Overview

FinRL has three layers: market environments, agents, and applications.  For a trading task (on the top), an agent (in the middle) interacts with a market environment (at the bottom), making sequential decisions.

<div align="center">
<img align="center" src=image/finrl_framework.jpeg>
</div>
<br>
A quick start: [FinRL](http://www.youtube.com/watch?v=ZSGJjtM-5jA) 

## Recent Advances

A complete survey paper:

"[Recent advances in reinforcement learning in finance. Mathematical Finance, 2023. ](papers/Recent_Advances/Recent_Advances.pdf)" 

## Publications

|Title |Conference |Link|Citations|Year|
|  ----  |  ----  |  ----  |  ----  |  ----  |
|**FinRL-Meta**: FinRL-Meta: Market Environments and Benchmarks for Data-Driven Financial Reinforcement Learning| NeurIPS 2022| [paper](papers/Base_papers/FinRL-Meta.pdf) [code](https://github.com/AI4Finance-Foundation/FinRL-Meta) | 1 | 2022 |
|**FinRL**: Deep reinforcement learning framework to automate trading in quantitative finance| ACM International Conference on AI in Finance (ICAIF) | [paper](papers/Base_papers/FinRL-Meta.pdf) | 24 | 2021 |
|**FinRL-Podracer**: High performance and scalable deep reinforcement learning for quantitative finance | ACM International Conference on AI in Finance (ICAIF) | [paper](papers/Base_papers/FinRL-Podracer.pdf) [code](https://github.com/AI4Finance-Foundation/FinRL_Podracer) | 9 | 2021 |
|Explainable deep reinforcement learning for portfolio management: An empirical approach| ACM International Conference on AI in Finance (ICAIF) | [paper](papers/Base_papers/Empirical-Approach-portfolio.pdf) [code](https://github.com/AI4Finance-Foundation/FinRL-Meta/blob/master/tutorials/2-Advance/FinRL_PortfolioAllocation_Explainable_DRL/FinRL_PortfolioAllocation_Explainable_DRL.py](https://github.com/AI4Finance-Foundation/FinRL-Tutorials/tree/master/2-Advance))| 3 | 2021 |
|**FinRL**: A deep reinforcement learning library for automated stock trading in quantitative finance| NeurIPS 2020 Deep RL Workshop  | [paper](papers/Base_papers/Quantitative-Finance-FinRL-AST.pdf) | 54 | 2020 |
|Deep reinforcement learning for automated stock trading: An ensemble strategy| ACM International Conference on AI in Finance (ICAIF) | [paper](papers/Base_papers/Ensemble-Strategy-AST.pdf) [code](https://github.com/AI4Finance-Foundation/FinRL-Meta/blob/master/tutorials/2-Advance/FinRL_Ensemble_StockTrading_ICAIF_2020/FinRL_Ensemble_StockTrading_ICAIF_2020.ipynb) | 103 | 2020 |
|Practical deep reinforcement learning approach for stock trading | NeurIPS 2018 Workshop on Challenges and Opportunities for AI in Financial Services| [paper](papers/Base_papers/Practical-DRL-AST.pdf) [code](https://github.com/AI4Finance-Foundation/DQN-DDPG_Stock_Trading](https://github.com/AI4Finance-Foundation/FinRL/tree/master/examples))| 131 | 2018 |

## Related Works
  + [Most Relatable Works] [csv](Docs/most_relatable_work.csv)
+ [Similar Works] [csv](Docs/Similar_work.csv)

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



OHLCV: open, high, low, and close prices; volume.


## Tutorials
#### Books
<div align="center">
<img align="center" src=image/book.png />
</div>

+ [O'reilly] [Machine Learning & Data Science Blueprints for Finance](Books/DS_for_FIN.pdf)

#### ODSC - Open Data Science
+ [Medium] [First Steps Before Applying Reinforcement Learning for Trading](https://odsc.medium.com/first-steps-before-applying-reinforcement-learning-for-trading-f45c15e98bca)
  
+ [Towardsdatascience] [Deep Reinforcement Learning for Automated Stock Trading](https://towardsdatascience.com/deep-reinforcement-learning-for-automated-stock-trading-f1dad0126a02)
  
#### Conventional Machine Learning Methods
+ [Kaggle] [Mean-Variance Optimization of Portfolios](https://www.kaggle.com/code/vijipai/lesson-5-mean-variance-optimization-of-portfolios/notebook)
  
<details><summary> <i>[click to expand]</i></summary>
<div>


#### Xiao-Yang (Yanglet) Liu and Steven Li

+ [Towardsdatascience] [ElegantRL-Helloworld: A Lightweight and Stable Deep Reinforcement Learning Library](https://towardsdatascience.com/elegantrl-a-lightweight-and-stable-deep-reinforcement-learning-library-95cef5f3460b)
+ [Towardsdatascience] [ElegantRL: Mastering PPO Algorithms](https://medium.com/@elegantrl/elegantrl-mastering-the-ppo-algorithm-part-i-9f36bc47b791)
+ [Towardsdatascience] [ElegantRL-Podracer: A Scalable and Elastic Library for Cloud-Native Deep Reinforcement Learning](https://elegantrl.medium.com/elegantrl-podracer-scalable-and-elastic-library-for-cloud-native-deep-reinforcement-learning-bafda6f7fbe0)
+ [Towardsdatascience] [A New Era of Massively Parallel Simulation: A Practical Tutorial Using ElegantRL](https://medium.com/towards-data-science/a-new-era-of-massively-parallel-simulation-a-practical-tutorial-using-elegantrl-5ebc483c3385)
+ [Towardsdatascience] [ElegantRL-Podracer: A Scalable and Elastic Library for Cloud-Native Deep Reinforcement Learning](https://elegantrl.medium.com/elegantrl-podracer-scalable-and-elastic-library-for-cloud-native-deep-reinforcement-learning-bafda6f7fbe0)
+ [MLearning.ai] [ElegantRL Demo: Stock Trading Using DDPG (Part I)](https://elegantrl.medium.com/elegantrl-demo-stock-trading-using-ddpg-part-i-e77d7dc9d208)
+ [MLearning.ai] [ElegantRL Demo: Stock Trading Using DDPG (Part II)](https://medium.com/mlearning-ai/elegantrl-demo-stock-trading-using-ddpg-part-ii-d3d97e01999f)
+ [MLearning.ai] [ElegantRL: Much More Stable Deep Reinforcement Learning Algorithms than Stable-Baseline3](https://medium.com/mlearning-ai/elegantrl-much-much-more-stable-than-stable-baseline3-f096533c26db)


#### Bruce Yang

+ [Towardsdatascience] [Deep Reinforcement Learning for Automated Stock Trading](https://towardsdatascience.com/deep-reinforcement-learning-for-automated-stock-trading-f1dad0126a02)
+ [Towardsdatascience] [FinRL for Quantitative Finance: Tutorial for Using FinRL](https://towardsdatascience.com/finrl-for-quantitative-finance-tutorial-for-single-stock-trading-37d6d7c30aac)
+ [Towardsdatascience] [FinRL for Quantitative Finance: Tutorial for Multiple Stock Trading](https://towardsdatascience.com/finrl-for-quantitative-finance-tutorial-for-multiple-stock-trading-7b00763b7530)
+ [Towardsdatascience] [FinRL for Quantitative Finance: Tutorial for Portfolio Allocation](https://towardsdatascience.com/finrl-for-quantitative-finance-tutorial-for-portfolio-allocation-9b417660c7cd)
+ [Towardsdatascience] [End-to-End Guide to Building a Credit Scorecard Using Machine Learning](https://towardsdatascience.com/end-to-end-guide-to-building-a-credit-scorecard-using-machine-learning-6502d8bb765a)
+ [FinRL for Quantitative Finance: Install and Setup Tutorial for Beginners](https://ai4finance.medium.com/finrl-for-quantitative-finance-install-and-setup-tutorial-for-beginners-1db80ad39159)
+ [MLearning.ai] [FinRL for Quantitative Finance: plug-and-play DRL algorithms](https://medium.com/mlearning-ai/finrl-for-quantitative-finance-plug-and-play-drl-algorithms-11cf494d28b1)
+ [DataDrivenInvestor][Alpaca] [A Data Scientist’s Approach for Algorithmic Trading using Deep Reinforcement Learning: An End-to-end Tutorial for Paper Trading](https://alpaca.markets/learn/data-scientists-approach-algorithmic-trading-using-deep-reinforcement-learning/)
+ [DataDrivenInvestor] [FinRL-Meta: A Universe of Near Real-Market En­vironments for Data­-Driven Financial Reinforcement Learning](https://medium.datadriveninvestor.com/finrl-meta-a-universe-of-near-real-market-en-vironments-for-data-driven-financial-reinforcement-e1894e1ebfbd)
+ [DataDrivenInvestor] [FinRL-Meta User Guide](https://ai4finance.medium.com/finrl-meta-user-guide-f1d6911f1de5)
+ [DataDrivenInvestor] [FinRL-Meta: Market Environments and Benchmarks for Data-Driven Financial Reinforcement Learning](https://medium.datadriveninvestor.com/finrl-meta-market-environments-and-benchmarks-for-data-driven-financial-reinforcement-learning-7af8e747c4bd)
+ [Feature Importance with Deep Neural Network for Cryptocurrencies](https://ai4finance.medium.com/feature-importance-with-deep-neural-network-for-cryptocurrencies-f06191e2d562)

#### Ming Zhu
+ [MLearning.ai][Dynamic Datasets Driven Financial Reinforcement Learning — FinRL as an Example](https://medium.com/@zhumingpassional/dynamic-datasets-driven-financial-reinforcement-learning-finrl-as-an-example-c4d92dcd495a)
+ [MLearning.ai][How can we guide ChatGPT to generate financial factors, using volume-price divergence in FinRL as an example?](https://medium.com/@zhumingpassional/guide-chatgpt-to-write-financial-factors-volume-price-divergence-431841a2bac8)
+ [MLearning.ai] [Deep reinforcement learning based stock trading (Stable baselines3 + Dow Jones)](https://medium.com/@zhumingpassional/deep-reinforcement-learning-based-stock-trading-stable-baselines3-dow-jones-c7ed034eb9f0)

#### Joey Xia

+ [MLearning.ai] [Introduction to the World of Financial Reinforcement Learning: Part.1 Download Data](https://medium.com/mlearning-ai/introduction-to-the-world-of-financial-reinforcement-learning-part-1-download-data-1a8c0c5d03c5)
+ [MLearning.ai] [Introduction to the World of Financial Reinforcement Learning: Part.2 Train Agents](https://medium.com/mlearning-ai/introduction-to-the-world-of-financial-reinforcement-learning-part-2-train-agents-1d1fa8a18a5e)
+ [MLearning.ai] [Financial Metaverse as a Playground for Financial Machine Learning](https://medium.com/@zx2325/finrl-meta-from-market-environments-to-a-financial-metaverse-5db8490a83df)
+ [InsiderFinance Wire] [Introduction of Data APIs in FinRL — Tushare](https://medium.com/insiderfinance/introduction-of-data-apis-in-finrl-tushare-f720b8da4e46)
+ [InsiderFinance Wire] [Awesome Deep Reinforcement Learning in Finance](https://medium.com/insiderfinance/awesome-deep-reinforcement-learning-in-finance-f319f4302897)

#### Adam King

+ [Towards Data Science] [Create custom gym environments from scratch — A stock market example](https://towardsdatascience.com/creating-a-custom-openai-gym-environment-for-stock-trading-be532be3910e)
+ [Towards Data Science] [Rendering elegant stock trading agents using Matplotlib and Gym](https://medium.com/towards-data-science/visualizing-stock-trading-agents-using-matplotlib-and-gym-584c992bc6d4)
+ [Towards Data Science] [Creating Bitcoin trading bots don’t lose money](https://medium.com/towards-data-science/creating-bitcoin-trading-bots-that-dont-lose-money-2e7165fb0b29)
+ [Towards Data Science] [Optimizing deep learning trading bots using state-of-the-art techniques](https://medium.com/towards-data-science/using-reinforcement-learning-to-trade-bitcoin-for-massive-profit-b69d0e8f583b)
+ [Towards Data Science] [Trade and Invest Smarter — The Reinforcement Learning Way](https://medium.com/towards-data-science/trade-smarter-w-reinforcement-learning-a5e91163f315)

#### Barend

+ [Coinmonks] [Crypto feature importance for Deep Reinforcement Learning](https://medium.com/coinmonks/crypto-feature-importance-for-deep-reinforcement-learning-38416616c2a36-8416616c2a36)
+ [Coinmonks] [Best technical indicators for Bitcoin from TA-lib](https://medium.com/coinmonks/best-technical-indicators-for-bitcoin-fromta-lib-fa5518560e)
+ [Towards AI] [The Combinatorial Purged Cross-Validation method](https://medium.com/towards-artificial-intelligence/the-combinatorial-purged-cross-validation-method-363eb378a9c5)
+ [Towards AI] [Combinatorial PurgedKFold Cross-Validation for Deep Reinforcement Learning](https://medium.com/towards-artificial-intelligence/combinatorial-purgedkfold-cross-validation-for-deep-reinforcement-learning-f8df689ca874)
+ [Towards AI] [Deep Reinforcement Learning for Cryptocurrency Trading: Practical Approach to Address Backtest Overfitting](https://pub.towardsai.net/deep-reinforcement-learning-for-cryptocurrency-trading-practical-approach-to-address-backtest-2aebfd5fa030)

#### Astarag Mohapatra

+ [Analytics Vidhya] [A hitchhikers guide to FinRL: A Deep Reinforcement Learning Framework for Quantitative Finance](https://medium.com/analytics-vidhya/a-hitchhikers-guide-to-finrl-a-deep-reinforcement-learning-framework-for-quantitative-finance-e624c508f763)
+ [Analytics Vidhya] [Hyperparameter tuning using optuna for FinRL](https://medium.com/analytics-vidhya/hyperparameter-tuning-using-optuna-for-finrl-8a49506d2741)
+ [Analytics Vidhya] [Weights and Biases-ify FinRL with Stable Baselines3 models](https://medium.com/analytics-vidhya/weights-and-biases-ify-stable-baselines-models-in-finrl-f11b67f2a6a7)
+ [Analytics Vidhya] [Deep Reinforcement Learnig in Algorithmic (Part- I)](https://medium.com/analytics-vidhya/deep-reinforcement-learning-in-algorithmic-trading-part-i-7088a4befd60)
+ [Analytics Vidhya] [Deep Reinforcement Learnig in Algorithmic (Part- II)](https://medium.com/analytics-vidhya/deep-reinforcement-learning-in-algorithmic-trading-part-ii-b78db754961c)
+ [Analytics Vidhya] [Financial Data Streaming using Alpaca and Streamlit](https://medium.com/analytics-vidhya/financial-data-streaming-using-alpaca-and-streamlit-88aa21c75f27)
+ [MLearning.ai] [Hyperparameter Optimization using Ray tune for FinRL models](https://medium.com/mlearning-ai/hyperparameter-optimization-using-ray-tune-for-finrl-models-42df2937d53d)
+ [MLearning.ai] [Google Trends Data for automated stock trading using Reinforcement learning](https://medium.com/mlearning-ai/google-trends-data-for-automated-stock-trading-using-reinforcement-learning-9c0fd6d00678)
+ [MLearning.ai] [FinRL: Population-Based algorithms implementation using Ray tune and RLlib](https://medium.com/mlearning-ai/finrl-population-based-algorithms-implementation-using-ray-tune-and-rllib-cdce7df66208)
+ [MLearning.ai] [Population-Based Algorithms for Hyperparameter Optimization in Reinforcement learning](https://medium.com/mlearning-ai/population-based-algorithms-for-hyperparameter-optimization-in-reinforcement-learning-b04ce2165533)
+ [FinRL: Financial Reinforcement learning explainability using Shapley Values](https://medium.com/@athekunal/finrl-financial-reinforcement-learning-explainability-using-shapley-values-9a16bc24a934)
+ [Ray tune user guide for hyperparameter optimization](https://athekunal.medium.com/ray-tune-user-guide-for-hyperparameter-optimization-d6bdfa2b06)

#### Matthew Brulhardt

+ [Level Up Coding] [Using TensorTrade for Making a Simple Trading Algorithm](https://levelup.gitconnected.com/using-tensortrade-for-making-a-simple-trading-algorithm-6fad4d9bc79c)
+ [Level Up Coding] [Portfolio Allocation with TensorTrade: (Part 1/2)](https://levelup.gitconnected.com/portfolio-allocation-with-tensortrade-part-1-2-1d0c3b126bf6)
+ [Level Up Coding] [Portfolio Allocation with TensorTrade: (Part 2/2)](https://levelup.gitconnected.com/portfolio-allocation-with-tensortrade-part-2-2-9ac30a6bcbfe)

#### Prakhar Gurawa

+ [InsiderFinance Wire] [Transitioning from Supervised Learning systems to Multi-Agent Reinforcement learning for financial platforms - Part 1](https://wire.insiderfinance.io/transitioning-from-supervised-learning-systems-to-multi-agent-reinforcement-learning-for-financial-d96c2c56a6fd)
+ [InsiderFinance Wire] [Transitioning from Supervised Learning systems to Multi-Agent Reinforcement learning for financial platforms — Part 2](https://wire.insiderfinance.io/transitioning-from-supervised-learning-systems-to-multi-agent-reinforcement-learning-for-financial-7e8b6cd07d1e)
+ [InsiderFinance Wire] [Transitioning from Supervised Learning systems to Multi-Agent Reinforcement learning for financial platforms — Part 3](https://wire.insiderfinance.io/transitioning-from-supervised-learning-systems-to-multi-agent-reinforcement-learning-for-financial-e90cb394de2b)


#### Tom Grek
+ [Towardsdatascience] [A blundering guide to making a deep actor-critic bot for stock trading](https://medium.com/@tomgrek/heres-what-happened-when-i-gave-control-of-my-robinhood-account-to-an-ai-for-a-week-3309d62567c4)

#### Ranko Mosic at JP Morgan Chase

+ [Deep Reinforcement Learning Based Trading Application at JP Morgan Chase](https://ranko-mosic.medium.com/reinforcement-learning-based-trading-application-at-jp-morgan-chase-f829b8ec54f2)

#### Alpaca

+ [Comparing 3 Different Types of Neural Network Architectures in Finance](https://medium.com/automation-generation/comparing-3-different-types-of-neural-network-architectures-in-finance-9377902ae392)

#### NO-MAGIC on Kaggle

+ [Kaggle] [Deep Reinforcement Learning for Stock Trading - 1](https://www.kaggle.com/code/learnmore1/deep-reinforcement-learning-for-stock-trading-1)

#### Anmol Mann 

+ [WandB] [Optimize Portfolio Allocation using FinRL](https://wandb.ai/anmolmann/finRL-portfolio-allocation-2/reports/Optimize-Portfolio-Allocation-using-FinRL--Vmlldzo4MjE4MTM)

#### Mao Guan

+ [MLearning.ai] [An Empirical Approach to Explain Deep Reinforcement Learning in Portfolio Management Task](https://medium.com/mlearning-ai/an-empirical-approach-to-explain-deep-reinforcement-learning-in-portfolio-management-task-e65a42225d9d)

#### Mariko Sawada
 
+ [Automated stock trading using Deep Reinforcement Learning with Fundamental Indicators](https://medium.com/@mariko.sawada1/automated-stock-trading-with-deep-reinforcement-learning-and-financial-data-a63286ccbe2b)

#### Letian Wang

+ [The Startup] [Option Pricing Using Reinforcement Learning](https://medium.com/swlh/option-pricing-using-reinforcement-learning-ad2ddca7735b)
+ [From Reinforcement Gamer to Reinforcement Trader](https://letian-wang.medium.com/from-reinforcement-gamer-to-reinforcement-trader-8b0a7ef8b53f)

#### Harsha Andey

+ [Deep Reinforcement Learning for Trading Cryptocurrencies](https://medium.com/coinmonks/deep-reinforcement-learning-for-trading-cryptocurrencies-5b5502b1ece1)

#### Aaron Krumins

+ [DataDrivenInvestor] [Using the Game Engine for Automated Cryptocurrency Trading (Without a Single Line of Code)](https://medium.datadriveninvestor.com/using-the-game-engine-for-automated-stock-trading-without-a-single-line-of-code-31d46f548ab2)

#### Roshan Adusumilli

+ [DataDrivenInvestor] [Reinforcement Learning for Options Trading](https://medium.datadriveninvestor.com/reinforcement-learning-for-options-trading-765c84d0d97d)

#### Mohit Maithani

+ [Analyticsindiamag.com] [How To Automate Stock Market Using FinRL (Deep Reinforcement Learning Library)?](https://analyticsindiamag.com/stock-market-prediction-using-finrl/)

#### Andrey Babynin

+ [Reinforcement learning in trading (Part 1)](https://andreybabynin.medium.com/reinforcement-learning-in-trading-part-1-d0920d69b526)
+ [Reinforcement learning in Trading (part 2 - the last)](https://andreybabynin.medium.com/reinforcement-learning-in-trading-part-2-the-last-9af547fb4203)

#### Timothy Mutegi

+ [Model-Free Reinforcement Learning for Asset Allocation](https://mutegi-timothy.medium.com/model-free-reinforcement-learning-for-asset-allocation-9cf95dde069a)

#### EASON

+ [Use Reinforcement Learning to do Algorithmic Trading](https://espaceship.medium.com/use-reinforcement-learning-to-rule-over-algorithmic-trading-a32c891774)


#### Shivam Akhauri

+ [ETHER Labs] [TradeBot: Stock Trading using Reinforcement Learning — Part1](https://medium.com/ether-labs/tradebot-stock-trading-using-reinforcement-learning-part1-8b67c9603f33)

#### Zeynep Tufekci

+ [Reinforcement Learning in Stock Prediction with FinRL](https://medium.com/@zeyneptufekci.etu)

#### Dan Pavlovic

+ [Reinforcement learning for the financial market — FinRL](https://dannoc1996.medium.com/reinforcement-learning-for-the-financial-market-finrl-c0ceeb3712f2)

#### Art Krisada

+ [FinRL Multiple Stock Trading](https://krisadas.medium.com/finrl-multiple-stock-trading-6f4499d592d4)

#### Videos 

+ [NeurIPS 2021] [FinRL-Meta: A Universe of Near-Real Market Environments for Data-Driven Deep Reinforcement Learning in Quantitative Finance](https://slideslive.com/38971905/finrlmeta-a-universe-of-nearreal-market-environments-for-datadriven-deep-reinforcement-learning-in-quantitative-finance?ref=recommended)
+ [NeurIPS 2020] [FinRL: A Deep Reinforcement Learning Library for Automated Stock Trading in Quantitative Finance](https://crossminds.ai/video/finrl-a-deep-reinforcement-learning-library-for-automated-stock-trading-in-quantitative-finance-606fdc01f43a7f2f827bf5c9/)

</div>
</details>
