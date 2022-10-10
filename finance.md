# Yield Prediction

## Stock Trend Prediction with Multi-Granularity Data: A Contrastive Learning Approach with Adaptive Fusion
1. Multi-granularity
2. Cross-Granularity and Cross-Temporal **contrast learning**

## Stock Selection via Spatiotemporal Hypergraph Attention Network: A Learning to Rank Approach
1. Modeling **relations** between related stocks' temporal price movement
2. Using profitable metrics and NDCG for ranking
3. Using Hawkes process as temporal attention

## Stock market forecasting using a multi-task approach integrating long short-term memory and the random forest framework
CCF None
+ An awesome table (table 1) Describes 43 technical indicators.

## Relation-aware dynamic attributed graph attention network for stocks recommendation
Using normalized Mutual Information as relations?

## NumHTML: Numeric-Oriented Hierarchical Transformer Model for Multi-task Financial Forecasting
1. d
2. Multi-task

## Robust Dual Recurrent Neural Networks for Financial Time Series Prediction
1. Classify noise-free samples and noisy samples
2. Cross-updating inspired bt co-training to overcome **sample-selection bias**

## Multi-scale Two-way Deep Neural Network for Stock Trend Prediction
1. Considering 2 different scale behavior by wavelet-based XGBoost and down-sampling-based RCNN
2. Datasets: FI-2010 and CSI-2016

## Long-term, Short-term and Sudden Event: Trading Volume Movement Prediction with Graph-based Multi-view Modeling
+ valuable target for further study
1. Predict trading volume instead of price
2. Emphasis on multi-view information, including long-term stock relation, short-term fluctuations and sudden events

## Learning Multiple Stock Trading Patterns with Temporal Routing Adaptor and Optimal Transport
+ model multiple stock trading patterns
1. the lack of **explicit identifiers** makes it quite challenging to train a router. So they design a learning algorithm based on Optimal Transport

## Investment Behaviors Can Tell What Inside: Exploring Stock Intrinsic Properties for Stock Trend Prediction
+ leverage stock intrinsic properties
+ extract stock intrinsic properties from mutual fund portfolios
+ use static stock properties in a dynamic way by measuring the correlation between the market and the stock
1. the representation of stock properties
    
    $Q^j$
    
    extracted from fund managers' preference
2. dynamic correlation
   
    **Why not $\hat{r}_{t+1}^j=MLP([\hat{D}_t^j,Q^j])$?**
    *The static stock properties cannot explicitly predict the stock trend in dynamic market*

    **market state**: 
    take $Q^j$s whose return ratio is ranked within top-$K_r$ at time t and average those $K_r$ $Q^j$s.

    then correlation $D_t^j=S_tQ^j$
    1. dynamic market state
        $\hat{D}_t^j \approx D_{t-1}^j$
    2. dynamic market trend
        predict $\hat{S}_t=LSTM(S_{<t})$
3. predict return ratio
    
    $\hat{r}_{t+1}^j=MLP([\hat{D}_t^j,Z_t^j])$
   
   1. $\hat{D}_t^j$ is the correlation
   2. $Z_t^j$ is embedding of stock's past performance, e.g. history price

## Individualized Indicator for All: Stock-wise Technical Indicator Optimization with Stock Embedding
+ graph embedding method
    > Shaosheng Cao, Wei Lu, and Qiongkai Xu. 2016. Deep neural networks for learning graph representations. In Thirtieth AAAI Conference on Artificial Intelligence. 1145–1152.
    > Aditya Grover and Jure Leskovec. 2016. node2vec: Scalable Feature Learning for Networks. 2016 (2016), 855–864.
    > Mathias Niepert, Mohamed Ahmed, and Konstantin Kutzkov. 2016. Learning convolutional neural networks for graphs. In International Conference on International Conference on Machine Learning. 2014–2023.
    > Bryan Perozzi, Rami Alrfou, and Steven Skiena. 2014. DeepWalk: online learning of social representations. (2014), 701–710.
    > Daixin Wang, Peng Cui, and Wenwu Zhu. 2016. Structural Deep Network Embedding. In ACM SIGKDD International Conference on Knowledge Discovery and Data Mining. 1225–1234.
+ Heterogeneous Graph

## “ 稳定 ” 还是 “ 扰动 ” ———基于上证50ETF期权的实证分析
事件研究法

