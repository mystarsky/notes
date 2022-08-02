# Modeling Social Attention for Stock Analysis: An Influence Propagation Perspective
+ fill the gap between the usage of social media data and financial theories
+ Traditionally use **Event Study**
1. Capture dynamic influence propagation and  self-influence (or confidence) in a social network, i.e. Weibo
2. find positive relationship between the absolute value of abnormal return and DSA
3. verified the market volume is associated with DSA at most of time

# Incorporating Fine-grained Events in Stock Movement Prediction
+ existing works mainly adopt the coarse-grained events, which loses the specific semantic information of diverse event types
1. propose a professional finance event dictionary built by domain experts and use it to extract fine-grained events automatically from finance news
2. combine finance news with fine-grained event structure and stock trade data to predict the stock movement

# REST: Relational Event-driven Stock Trend Forecasting
## 问题和启发
1. 他怎样捕捉股票相关的上下文的
   + stock-dependent context of the event for directly related stock
      直接相关股票是指？
   + 通过同时考虑同一股票的历史事件和后续股价和交易量反应，建模上下文
      1. 但他是用the relative change of stock price and transaction volume，这是不是仍包含了事前的模式
2. 设计新的传播机制，而非直接用GCN
   1. 边类型不同，传播的影响不同：分别计算不同类别边的传播作用，最终加总
   2. 两个股票之间的传播强度是动态的：将一对股票的上下文纳入考虑，建模传播的动态强度
   3. 影响的传播是多步的：堆积传播层
3. 他怎么构建connection的，特别是implicit connection
   + 经验pre-defined关系
      1. in the same industry
      2. have the same business
      3. have the same shareholder
      4. downstream/upstream
4. 一个event可能不是一个单点事件，而是有前后多个子事件构成的过程，即event是个过程
   + 他考虑的过去事件只考虑了过去几天，但事件往往不是连续发生的？比如前后间隔半个月
5. 他处理event时使用了类别标签辅助判断，通过注意力计算event文本中哪个token对event type贡献最大
## 标题和出处
1. 数据来源
   1. the announcement data: http://www.cninfo.com.cn
   2. the stock relations: https://tushare.pro/
   3. daily stock price and volume data: http://xueqiu.com
## 贡献
1. 文章想解决，应用事件信息预测时：
   1. 相似事件对不同股票影响不同
   2. 会对直接相关的股票和有隐含联系的股票产生显著影响
## 可以看一看的相关工作
1. 预测股票的综述
   > Rashmi Sutkatti and D TORSE. 2019. Stock market forecasting techniques: A survey. International Research Journal of Engineering and Technology 6, 5 (2019).
   >
   > Qing Li, Yan Chen, Jun Wang, Yuanzhu Chen, and Hsinchun Chen. 2017. Web media and stock markets: A survey and future directions from a big data perspective. IEEE Transactions on Knowledge and Data Engineering 30, 2 (2017), 381–399.
2. Event信息的应用
   ### news
   > Shumin Deng, Ningyu Zhang, Wen Zhang, Jiaoyan Chen, Jeff Z Pan, and Huajun Chen. 2019. Knowledge-Driven Stock Trend Prediction and Explanation via Temporal Convolutional Network. In Companion Proceedings of The 2019 World Wide Web Conference. ACM, 678–685.
   >
   > Xiao Ding, Yue Zhang, Ting Liu, and Junwen Duan. 2016. Knowledge-driven event embedding for stock prediction. In Proceedings of coling 2016, the 26th international conference on computational linguistics: Technical papers. 2133–2142.
   >
   > Junwen Duan, Yue Zhang, Xiao Ding, Ching-Yun Chang, and Ting Liu. 2018. Learning Target-Specific Representations of Financial News Documents For Cumulative Abnormal Return Prediction. In Proceedings of the 27th International Conference on Computational Linguistics. 2823–2833.
   >
   > Ziniu Hu, Weiqing Liu, Jiang Bian, Xuanzhe Liu, and Tie-Yan Liu. 2018. Listening to chaotic whispers: A deep learning framework for news-oriented stock trend prediction. In Proceedings of the Eleventh ACM International Conference on Web Search and Data Mining. ACM, 261–269.
   >
   > Qikai Liu, Xiang Cheng, Sen Su, and Shuguang Zhu. 2018. Hierarchical complementary attention network for predicting stock price movements with news. In Proceedings of the 27th ACM International Conference on Information and Knowledge Management. 1603–1606.
   >
   > Arman Khadjeh Nassirtoussi, Saeed Aghabozorgi, Teh Ying Wah, and David Chek Ling Ngo. 2015. Text mining of news-headlines for FOREX market prediction: A Multi-layer Dimension Reduction Algorithm with semantics and sentiment. Expert Systems with Applications 42, 1 (2015), 306–324.
   >
   > Manuel R Vargas, Beatriz SLP De Lima, and Alexandre G Evsukoff. 2017. Deep learning for stock market prediction from financial news articles. In 2017 IEEE International Conference on Computational Intelligence and Virtual Environments for Measurement Systems and Applications (CIVEMSA). IEEE, 60–65.
   ### social media
   > Huizhe Wu, Wei Zhang, Weiwei Shen, and Jun Wang. 2018. Hybrid deep sequential modeling for social text-driven stock prediction. In Proceedings of the 27th ACM International Conference on Information and Knowledge Management. 1627–1630.
   >
   > Yumo Xu and Shay B Cohen. 2018. Stock movement prediction from tweets and historical prices. In Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers), Vol. 1. 1970–1979.
   >
   > Steve Y Yang, Sheung Yin Kevin Mo, and Anqi Liu. 2015. Twitter financial community sentiment and its predictive relationship to stock market movement. Quantitative Finance 15, 10 (2015), 1637–1656.
   >
   > Zhenkun Zhou, Jichang Zhao, and Ke Xu. 2016. Can online emotions predict the stock market in China?. In International conference on web information systems engineering. Springer, 328–342.
   ### discussion board
   > Qing Li, TieJun Wang, Ping Li, Ling Liu, Qixu Gong, and Yuanzhu Chen. 2014. The effect of news and public mood on stock movements. Information Sciences 278 (2014), 826–840.
   >
   > Thien Hai Nguyen, Kiyoaki Shirai, and Julien Velcin. 2015. Sentiment analysis on social media for stock movement prediction. Expert Systems with Applications 42, 24 (2015), 9603–9611.
   >
   > David Zimbra, Hsinchun Chen, and Robert F Lusch. 2015. Stakeholder analyses of firm-related web forums: Applications in stock return prediction. ACM Transactions on Management Information Systems (TMIS) 6, 1 (2015), 1–38.

3. 可以比较的模型
   1. ARIMA
   2. TGCN
      
      TGCN leverages a variant of graph convolutional networks to propagate the historical price information on the stock graph for stock trend forecasting. It only uses historical price data and does not use the event information.

      > Daiki Matsunaga, Toyotaro Suzumura, and Toshihiro Takahashi. 2019. Exploring Graph Neural Networks for Stock Market Predictions with Rolling Window Analysis. arXiv preprint arXiv:1909.10660 (2019).

   3. HAN(2018)
      
      A model that utilizes the hierarchical attention mechanism over media information for stock trend forecasting.

      > Ziniu Hu, Weiqing Liu, Jiang Bian, Xuanzhe Liu, and Tie-Yan Liu. 2018. Listening to chaotic whispers: A deep learning framework for news-oriented stock trend prediction. In Proceedings of the Eleventh ACM International Conference on Web Search and Data Mining. ACM, 261–269.

   4. Relational GCN(2020)
      
      This method uses the Relational GCN propagation layer to propagate the effect of event information. It can learn the different event effects under **different relations** compared with the GCN model.

      > Wei Li, Ruihan Bao, Keiko Harimoto, Deli Chen, Jingjing Xu, and Qi Su. 2020. Modeling the Stock Relation with Graph Network for Overnight Stock Movement Prediction. 4491–4497.

# Gated Sequential Recommendation System with Social and Textual Information Under Dynamic Contexts
+ extract users' preference, consider dynammic contexts
1. a dual-GRU structure builds the **sequential dynamics**
2. a gating layer combines two views of data explicitly
3. a social attention module combines two views of data implicitly
## interests:
1. sequential dynamics
2. multi-dimension attention
3. how they build the graph and update it? note they use a pretrained social embedding from the work of SDNE
   > Wang, D., Cui, P., Zhu, W.: Structural deep network embedding. In: ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, New York, NY, USA, pp. 1225–1234 (2016)