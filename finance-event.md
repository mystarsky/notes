## Modeling Social Attention for Stock Analysis: An Influence Propagation Perspective
+ fill the gap between the usage of social media data and financial theories
+ Traditionally use **Event Study**
1. Capture dynamic influence propagation and  self-influence (or confidence) in a social network, i.e. Weibo
2. find positive relationship between the absolute value of abnormal return and DSA
3. verified the market volume is associated with DSA at most of time

## Incorporating Fine-grained Events in Stock Movement Prediction
+ existing works mainly adopt the coarse-grained events, which loses the specific semantic information of diverse event types
1. propose a professional finance event dictionary built by domain experts and use it to extract fine-grained events automatically from finance news
2. combine finance news with fine-grained event structure and stock trade data to predict the stock movement

## REST: Relational Event-driven Stock Trend Forecasting
+ two main shortcomings in existing event-driven methods: overlook 

## Gated Sequential Recommendation System with Social and Textual Information Under Dynamic Contexts
+ extract users' preference, consider dynammic contexts
1. a dual-GRU structure builds the **sequential dynamics**
2. a gating layer combines two views of data explicitly
3. a social attention module combines two views of data implicitly
### interests:
1. sequential dynamics
2. multi-dimension attention
3. how they build the graph and update it? note they use a pretrained social embedding from the work of SDNE
   > Wang, D., Cui, P., Zhu, W.: Structural deep network embedding. In: ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, New York, NY, USA, pp. 1225–1234 (2016)