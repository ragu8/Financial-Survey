# FinRL: Financial Reinforcement Learning - Survey


<div align="center">
<img align="center" src=image/banner.png />
</div>



## Outline

  - [Overview](#overview)
  - [Recent Advances](#recent-advances)
  - [Publications](#publications)
  - [Related Works](#related-works)
  - [Observations](#observations)
  - [Data Sources](#data-sources)
  - [White Papers](#white-papers)
  - [Tutorials](#tutorials)


## Overview

FinRL has three layers: market environments, agents, and applications.  For a trading task (on the top), an agent (in the middle) interacts with a market environment (at the bottom), making sequential decisions.

<div align="center">
<img align="center" src=image/finrl_framework.jpeg>
</div>
<br>
A quick start:<br>

+ [FinRL](http://www.youtube.com/watch?v=ZSGJjtM-5jA)

## Recent Advances

A complete survey paper:

+ [Recent advances in reinforcement learning in finance. Mathematical Finance, 2023. ](papers/Recent_Advances/Recent_Advances.pdf)

+ [Reinforcement learning in financial markets - a survey, 2018. ](papers/Recent_Advances/RL-fin.pdf)

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
  + Most Relatable Work [csv, ](Docs/most_relatable_work.csv)  [pdf](papers/Relatable-papers)
  + Similar Works [csv](Docs/Similar_work.csv)  
  + Research Rabbit [Links](https://www.researchrabbitapp.com/collection/public/PZ9MYDP0LO)

## Observations
<details>
  <summary><i>FinRL-Meta</i></summary>
  <div>
    <table>
      <thead>
        <tr>
          <th>Component</th>
          <th>Observation</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Environments</td>
          <td>The paper models stock trading as an MDP, with states representing market factors, actions being buying/selling, and rewards tied to portfolio value changes.</td>
        </tr>
        <tr>
          <td>DRL Agents</td>
          <td>DDPG algorithm with actor-critic neural networks is used for action determination and evaluation.</td>
        </tr>
        <tr>
          <td>Application</td>
          <td>The primary goal is to optimize stock trading strategies for maximizing returns in dynamic markets.</td>
        </tr>
        <tr>
          <td>Framework</td>
          <td>DDPG is employed within a reinforcement learning framework for learning optimal trading strategies.</td>
        </tr>
        <tr>
          <td>Existing Libraries</td>
          <td>While specific libraries aren't mentioned, popular deep learning libraries like TensorFlow or PyTorch are likely used.</td>
        </tr>
        <tr>
          <td>Data Processing</td>
          <td>Historical daily stock prices are used for training, with data preprocessing involving splitting into training/validation/trading sets.</td>
        </tr>
        <tr>
          <td>Benchmarks</td>
          <td>DDPG strategy is benchmarked against DJIA and traditional min-variance portfolio allocation strategies.</td>
        </tr>
        <tr>
          <td>Advantages</td>
          <td>- DDPG tackles stock trading complexity.<br>- Results indicate DDPG-based strategy outperforms traditional methods in terms of return and Sharpe ratio.</td>
        </tr>
        <tr>
          <td>Disadvantages</td>
          <td>- Lack of specific neural network architecture details limits reproducibility.<br>- Unaddressed issues like overfitting and generalization to various market conditions.</td>
        </tr>
        <tr>
          <td>Tutorials</td>
          <td>The paper does not include tutorials but mentions the availability of online resources with DDPG and RL implementations for stock trading.</td>
        </tr>
        <tr>
          <td>Conclusion</td>
          <td>The paper introduces DDPG and RL for optimizing stock trading, suggesting its superiority over traditional methods. Further research is needed for broader applicability and addressing practical challenges.</td>
        </tr>
      </tbody>
    </table>
  </div>
</details>

<details>
  <summary><i>FinRL</i></summary>
  <div>
    <table>
      <thead>
        <tr>
          <th>Component</th>
          <th>Observation</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Environments</td>
          <td>The environment layer is crucial in FinRL, as it provides the simulation environment for trading tasks. It supports both standard datasets and user-imported data.</td>
        </tr>
        <tr>
          <td>DRL Agents</td>
          <td>FinRL allows users to utilize various DRL algorithms from libraries like Stable Baselines 3, RLlib, and ElegantRL, making it adaptable to different trading strategies.</td>
        </tr>
        <tr>
          <td>Application</td>
          <td>The application layer enables users to define and customize their trading strategies using DRL within the FinRL framework.</td>
        </tr>
        <tr>
          <td>Framework</td>
          <td>The FinRL framework is designed to provide a structured and modular approach to algorithmic trading with DRL, simplifying the development process.</td>
        </tr>
        <tr>
          <td>Existing Libraries</td>
          <td>The paper highlights the use of existing DRL libraries like Stable Baselines 3, RLlib, and ElegantRL as part of the framework.</td>
        </tr>
        <tr>
          <td>Data Processing</td>
          <td>While not explicitly mentioned, data processing is a crucial aspect, as the framework handles various data sources and formats, essential for financial data.</td>
        </tr>
        <tr>
          <td>Benchmarks</td>
          <td>The paper doesn't explicitly mention benchmarks, but it emphasizes the reproducibility of trading tasks within the framework.</td>
        </tr>
        <tr>
          <td>Advantages</td>
          <td>The advantages of the FinRL framework include modularity, extensibility, simplicity, and applicability to various financial markets, making it a practical tool for algorithmic trading.</td>
        </tr>
        <tr>
          <td>Disadvantages</td>
          <td>The paper does not discuss specific disadvantages of the framework, which may need further exploration or evaluation.</td>
        </tr>
        <tr>
          <td>Tutorials</td>
          <td>The framework provides hands-on tutorials in a beginner-friendly fashion to help users get started with algorithmic trading using DRL.</td>
        </tr>
        <tr>
          <td>Conclusion</td>
          <td>The FinRL framework aims to simplify the development of algorithmic trading strategies using DRL and offers a practical option for financial tasks, especially with the ElegantRL library.</td>
        </tr>
      </tbody>
    </table>
  </div>
</details>

<details>
  <summary><i>FinRL-Podracer</i></summary>
  <div>
    <table>
      <thead>
        <tr>
          <th>Component</th>
          <th>Observation</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>RLOps in Finance Paradigm</td>
          <td>Introduces the concept of RLOps (Reinforcement Learning Operations) in finance for continuous training and integration of trading strategies.</td>
        </tr>
        <tr>
          <td>FinRL-Podracer Framework</td>
          <td>A cloud-based solution leveraging GPU clouds to improve trading performance and training efficiency with DRL-driven strategies.</td>
        </tr>
        <tr>
          <td>Generational Evolution Mechanism</td>
          <td>Employs a generational evolution mechanism with an ensemble strategy to enhance DRL agent trading performance and automate hyperparameter search.</td>
        </tr>
        <tr>
          <td>Scalable Evolution Layer</td>
          <td>Coordinates parallel agents using generational evolution, including an evaluator and selector, for efficient hyperparameter tuning and agent selection.</td>
        </tr>
        <tr>
          <td>Packaging Worker-Learner into Pod</td>
          <td>Decomposes DRL training into worker (exploration), replay buffer, and learner (exploitation) components, scalable in GPU pods.</td>
        </tr>
        <tr>
          <td>High-Performance Training Layer</td>
          <td>Optimizes components with GPU acceleration, efficient replay buffer, and parameter communication for improved training efficiency.</td>
        </tr>
      </tbody>
    </table>
    <table>
      <thead>
        <tr>
          <th>Insights</th>
          <th>Key insights from the paper</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>RLOps in Finance Paradigm</td>
          <td>Integrating multiple finance processes into a DRL agent can lead to more automated and efficient trading strategies.</td>
        </tr>
        <tr>
          <td>FinRL-Podracer</td>
          <td>Addresses challenges in handling large-scale financial data and efficient DRL agent training.</td>
        </tr>
        <tr>
          <td>Generational Evolution</td>
          <td>Mitigates overfitting and hyperparameter sensitivity, improving training stability and efficiency.</td>
        </tr>
        <tr>
          <td>Scalability & Performance</td>
          <td>Scalability and hardware optimizations are crucial for handling the computational demands of DRL-driven trading strategies.</td>
        </tr>
        <tr>
          <td>Performance Comparison</td>
          <td>FinRL-Podracer outperforms existing DRL libraries in annual return, Sharpe ratio, and training time.</td>
        </tr>
      </tbody>
    </table>
    <table>
      <thead>
        <tr>
          <th>Advantages</th>
          <th>Advantages of FinRL-Podracer</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Cloud-Based Solution</td>
          <td>Offers a cloud-based solution for developing and deploying DRL-driven trading strategies with high performance and scalability.</td>
        </tr>
        <tr>
          <td>Hyperparameter Automation</td>
          <td>Automates hyperparameter tuning and efficiently handles large-scale financial data.</td>
        </tr>
        <tr>
          <td>Enhanced Stability</td>
          <td>The generational evolution mechanism improves training stability and performance.</td>
        </tr>
      </tbody>
    </table>
    <table>
      <thead>
        <tr>
          <th>Disadvantages</th>
          <th>Disadvantages of the proposed framework</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Lack of Discussion</td>
          <td>The paper does not discuss potential limitations or challenges in implementing the proposed framework.</td>
        </tr>
      </tbody>
    </table>
    <table>
      <thead>
        <tr>
          <th>Tutorials</th>
          <th>Information about tutorials or guides provided in the paper</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Tutorial Availability</td>
          <td>The paper does not provide tutorials or step-by-step guides for implementing FinRL-Podracer.</td>
        </tr>
      </tbody>
    </table>
    <table>
      <thead>
        <tr>
          <th>Conclusion</th>
          <th>Summary and conclusion of the paper's contributions and findings</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Framework Summary</td>
          <td>Introduces FinRL-Podracer, a framework for accelerating DRL-driven trading strategies in quantitative finance, addressing key challenges.</td>
        </tr>
        <tr>
          <td>Promising Approach</td>
          <td>Emphasizes the importance of RLOps in finance and demonstrates the framework's potential to enhance quantitative trading.</td>
        </tr>
      </tbody>
    </table>
  </div>
</details>

<details>
  <summary><i>Empirical Approach</i></summary>
  <div>
    <table>
      <thead>
        <tr>
          <th>Component</th>
          <th>Observation</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Environments</td>
          <td>The paper evaluates the proposed approach in the context of a portfolio management task involving Dow Jones 30 constituent stocks. The data spans from January 1, 2009, to September 1, 2021.</td>
        </tr>
        <tr>
          <td>DRL Agents</td>
          <td>The paper highlights the challenge of explaining DRL-based trading strategies due to the black-box nature of deep neural networks. It emphasizes the need for understanding the decision-making processes of DRL agents in the financial context.</td>
        </tr>
        <tr>
          <td>Framework</td>
          <td>The authors propose an empirical approach to explain the strategies of DRL agents for portfolio management. The approach involves using linear models in hindsight as reference models and integrated gradients to define feature weights for DRL agents.</td>
        </tr>
        <tr>
          <td>Data Processing</td>
          <td>The paper uses features related to stock returns and covariances as input for both linear models and DRL agents. It focuses on quantifying the relationship between portfolio returns and these features.</td>
        </tr>
        <tr>
          <td>Advantages</td>
          <td>The approach aims to provide explanations for DRL-based portfolio management strategies, which can be crucial for investment banks, asset management companies, and hedge funds. It helps traders understand the potential risk of a strategy.</td>
        </tr>
        <tr>
          <td>Disadvantages</td>
          <td>While the paper presents an empirical approach, it doesn't delve into the specific implementation details of the DRL agents or machine learning methods used. The generalizability of the approach to different financial datasets or markets is not extensively discussed.</td>
        </tr>
        <tr>
          <td>Tutorials</td>
          <td>The paper doesn't provide tutorials or step-by-step guides for implementing the proposed approach. Readers interested in replicating or extending the research may need to refer to other sources or documentation.</td>
        </tr>
        <tr>
          <td>Conclusion</td>
          <td>The paper concludes that the proposed approach empirically reveals that DRL agents exhibit a stronger multi-step prediction power than machine learning methods in the context of portfolio management.</td>
        </tr>
      </tbody>
    </table>
  </div>
</details>

<details>
  <summary><i>Quantitative Finance</i></summary>
  <div>
    <table>
      <thead>
        <tr>
          <th>Component</th>
          <th>Observation</th>
        </tr>
      </thead>
      <tbody>
          <td>Environments</td>
          <td>- Evaluates DRL approach in portfolio management using Dow Jones 30 stocks from 2009 to 2021.</td>
        </tr>
        <tr>
          <td>DRL Agents</td>
          <td>- Highlights challenges in explaining DRL-based trading strategies due to their black-box nature.</td>
        </tr>
        <tr>
          <td>Application</td>
          <td>- Mentions three application demonstrations: single stock trading, multiple stock trading, and portfolio allocation.</td>
        </tr>
        <tr>
          <td>Framework</td>
          <td>- Introduces FinRL, a DRL library for quantitative finance, easing the development of trading strategies.</td>
        </tr>
        <tr>
          <td>Existing Libraries</td>
          <td>- Compares FinRL to other machine learning libraries and highlights its features.</td>
        </tr>
        <tr>
          <td>Data Processing</td>
          <td>- Uses stock returns and covariances as input, focusing on the relationship with portfolio returns.</td>
        </tr>
        <tr>
          <td>Benchmarks</td>
          <td>- Provides performance metrics and baseline trading strategies for evaluation.</td>
        </tr>
        <tr>
          <td>Advantages</td>
          <td>- Emphasizes completeness, hands-on tutorials, and reproducibility for beginners.</td>
        </tr>
        <tr>
          <td>Disadvantages</td>
          <td>- Notes the complexity of implementing DRL strategies and the need for backtesting.</td>
        </tr>
        <tr>
          <td>Tutorials</td>
          <td>- Demonstrates the library's use through practical examples and walk-through tutorials.</td>
        </tr>
        <tr>
          <td>Conclusion</td>
          <td>- Summarizes the contributions and potential of FinRL in quantitative finance.</td>
        </tr>
      </tbody>
    </table>
  </div>
</details>

<details>
  <summary><i>Automated Stock Trading: An Ensemble Strategy</i></summary>
  <div>
    <table>
      <thead>
        <tr>
          <th>Component</th>
          <th>Observation</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Environments</td>
          <td>- The stock trading problem is formulated as a Markov Decision Process (MDP). - The state space includes information like stock prices, stock shares, balance, technical indicators (e.g., MACD, RSI), and more. - The action space allows for buying, selling, or holding stocks in a continuous manner.</td>
        </tr>
        <tr>
          <td>DRL Agents</td>
          <td>**Advantage Actor Critic (A2C):** - A2C is used as one of the agents in the ensemble. - It employs an advantage function to reduce the variance of policy gradients. - Multiple agents interact with the environment and synchronize their updates through a global network. **Deep Deterministic Policy Gradient (DDPG):** - DDPG encourages maximum investment return. - It combines elements of Q-learning and policy gradient and is suitable for continuous action spaces. - It uses a replay buffer to store and sample transitions for training. **Proximal Policy Optimization (PPO):** - PPO is used to improve policy gradient updates and ensure stability. - It introduces a clipping term to the objective function to control policy changes. - PPO aims to restrict policy updates to prevent large changes.</td>
        </tr>
        <tr>
          <td>Application</td>
          <td>- The ensemble strategy is applied to automated stock trading with the goal of maximizing investment return. - It adapts to different market conditions and risk constraints.</td>
        </tr>
        <tr>
          <td>Framework</td>
          <td>- The authors use the OpenAI Gym framework to implement the trading environment.</td>
        </tr>
        <tr>
          <td>Existing Libraries</td>
          <td>- The paper doesn't mention specific existing libraries, but it uses deep reinforcement learning algorithms like A2C, DDPG, and PPO.</td>
        </tr>
        <tr>
          <td>Data Processing</td>
          <td>- Technical indicators such as MACD, RSI, CCI, and ADX are calculated from stock price data. - The paper employs a load-on-demand technique to efficiently manage memory when dealing with large datasets.</td>
        </tr>
        <tr>
          <td>Benchmarks</td>
          <td>- The proposed ensemble strategy is evaluated on a dataset consisting of 30 Dow Jones stocks with adequate liquidity. - Performance is compared with the Dow Jones Industrial Average index and a traditional min-variance portfolio allocation strategy. - The Sharpe ratio is used to measure risk-adjusted returns.</td>
        </tr>
        <tr>
          <td>Advantages</td>
          <td>- The ensemble strategy combines multiple DRL algorithms for improved robustness. - It can adapt to various market conditions. - Risk management is incorporated through the turbulence index. - The load-on-demand technique helps handle large datasets efficiently.</td>
        </tr>
        <tr>
          <td>Disadvantages</td>
          <td>- The paper does not discuss potential limitations or challenges in implementing the proposed framework.</td>
        </tr>
        <tr>
          <td>Tutorials</td>
          <td>- The paper doesn't provide tutorials or step-by-step guides for implementing the proposed approach. Readers interested in replicating or extending the research may need to refer to other sources or documentation.</td>
        </tr>
        <tr>
          <td>Conclusion</td>
          <td>- The proposed ensemble strategy outperforms individual algorithms and traditional portfolio allocation strategies in terms of risk-adjusted return, as measured by the Sharpe ratio.</td>
        </tr>
      </tbody>
    </table>
  </div>
</details>
<details>
  <summary><i>Practical DRL Approach for Stock Trading</i></summary>
  <div>
    <table>
      <thead>
        <tr>
          <th>Component</th>
          <th>Observation</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Environments</td>
          <td>The paper models the stock trading process as an MDP, considering stock prices, holdings, and balance. Actions include buy, sell, or hold, with rewards based on portfolio value changes.</td>
        </tr>
        <tr>
          <td>DRL Agents</td>
          <td>The paper utilizes the DDPG algorithm, which comprises actor and critic neural networks. The actor-network determines actions, while the critic network evaluates their quality.</td>
        </tr>
        <tr>
          <td>Application</td>
          <td>The primary application is optimizing stock trading strategies to maximize investment returns in a complex and dynamic stock market.</td>
        </tr>
        <tr>
          <td>Framework</td>
          <td>The DDPG algorithm is used within the reinforcement learning framework to learn optimal trading strategies.</td>
        </tr>
        <tr>
          <td>Existing Libraries</td>
          <td>While specific libraries are not mentioned, it's likely that popular deep learning libraries like TensorFlow or PyTorch were used for neural network implementations.</td>
        </tr>
        <tr>
          <td>Data Processing</td>
          <td>Historical daily stock prices are employed for training and trading data. Data preprocessing involves data splitting into training, validation, and trading sets.</td>
        </tr>
        <tr>
          <td>Benchmarks</td>
          <td>The paper benchmarks the DDPG-based trading strategy against the Dow Jones Industrial Average (DJIA) and a traditional min-variance portfolio allocation strategy.</td>
        </tr>
        <tr>
          <td>Advantages</td>
          <td>- DDPG is applied to handle the complexity of stock trading. - The paper provides a well-defined problem formulation for reinforcement learning. - Results suggest outperformance of traditional methods in terms of return and Sharpe ratio.</td>
        </tr>
        <tr>
          <td>Disadvantages</td>
          <td>- Lack of specific details about neural network architectures for actor and critic networks. - Unaddressed issues like overfitting or generalization to different market conditions. - Limited data range covering 30 stocks from 2009 to 2018.</td>
        </tr>
        <tr>
          <td>Tutorials</td>
          <td>The paper does not include tutorials, but online resources offer tutorials and implementations of DDPG and other reinforcement learning algorithms for stock trading.</td>
        </tr>
        <tr>
          <td>Conclusion</td>
          <td>The paper explores the use of DDPG for optimizing stock trading strategies, showing the potential outperformance of traditional methods. Further research is needed for broader applicability.</td>
        </tr>
      </tbody>
    </table>
  </div>
</details>

    
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



## White Papers  

+ [DERA] [High-Frequency Trading Synchronizes Prices in Financial Markets](white-papers/HFT-White_paper01.pdf)

+ [STEVENS] [ON THE IMPACT AND FUTURE OF HFT](white-papers/HFT-White_paper02.pdf)

+ [Frankfurt] [High-Frequency Trading](white-papers/HFT-White_paper03.pdf)

+ [STEVENS+IRRC] [HIGH-FREQUENCY TRADING: a white paper](white-papers/HFT-White_paper04.pdf)


## Tutorials
#### Books
<div align="center">
<img align="center" src=image/book.png />
</div>
<br>

+ [O'reilly] [Machine Learning & Data Science Blueprints for Finance](Books/DS_for_FIN.pdf)

<div align="center">
<img align="center" src=image/book1.png />
</div>
<br>

+ [MIT Press] [Reinforcement Learning: An Introduction](Books/RLI.pdf)

#### ODSC - Open Data Science
+ [Medium] [First Steps Before Applying Reinforcement Learning for Trading](https://odsc.medium.com/first-steps-before-applying-reinforcement-learning-for-trading-f45c15e98bca)
  
+ [Towardsdatascience] [Deep Reinforcement Learning for Automated Stock Trading](https://towardsdatascience.com/deep-reinforcement-learning-for-automated-stock-trading-f1dad0126a02)
  
#### Conventional Machine Learning Methods
+ [Kaggle] [Mean-Variance Optimization of Portfolios](https://www.kaggle.com/code/vijipai/lesson-5-mean-variance-optimization-of-portfolios/notebook)
  
<details><summary> <I> More </i></summary>
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
