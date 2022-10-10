# Knowledge Graph

## Knowledge-Driven Stock Trend Prediction and Explanation via Temporal Convolutional Network
2019, 浙大AZFT
### 现状
Deep neural networks have achieved promising results in stock trend prediction.
### 问题
However, most of these models have two common drawbacks, including (i) current methods are not sensitive enough to abrupt changes of stock trend, and (ii) forecasting results are not interpretable for humans.
### 思路
To address these two problems, we propose a novel Knowledge-Driven Temporal Convolutional Network (KDTCN) for stock trend prediction and explanation.
### 亮点
Firstly, we extract structured events from financial news, and utilize external knowledge from knowledge graph to obtain event embeddings. Then, we combine event embeddings and price values together to forecast stock trend.
### 效果
We evaluate the prediction accuracy to show how knowledge-driven events work on abrupt changes. We also visualize the effect of events and linkage among events based on knowledge graph, to explain why knowledge-driven events are common sources of abrupt changes. Experiments demonstrate that KDTCN can (i) react to abrupt changes much faster and outperform state-of-the-art methods on stock datasets, as well as (ii) facilitate the explanation of prediction particularly with abrupt changes.
### 兴趣点
1. 这种说法，abrupt changes of stock trend
2. event embedding怎么做的: event extraction + knowledge graph
3. 好像效果还不错？整个TCN的效果看起来精度不错
---

## Knowledge-Driven Event Embedding for Stock Prediction
2016, 哈工大SCIR
### 现状
Representing structured events as vectors in continuous space offers a new way for defining dense features for natural language processing (NLP) applications. Prior work has proposed effective methods to learn event representations that can capture syntactic and semantic information over text corpus, demonstrating their effectiveness for downstream tasks such as event-driven stock prediction.
### 问题
On the other hand, events extracted from raw texts do not contain background knowledge on entities and relations that they are mentioned.
### 思路
To address this issue, this paper proposes to leverage extra information from knowledge graph, which provides ground truth such as attributes and properties of entities and encodes valuable relations between entities.
### 亮点
Specifically, we propose a joint model to combine knowledge graph information into the objective function of an event embedding learning model.
### 效果
Experiments on event similarity and stock market prediction show that our model is more capable of obtaining better event embeddings and making more accurate prediction on stock market volatility.
### 兴趣点
1. 缺乏领域知识的说法，它使用KG来引入的？
2. event embedding怎么做的
3. 怎么精度效果也不错？
4. 哈工大SCIR
---

# Attention

## Learning Target-Specific Representations of Financial News Documents For Cumulative Abnormal Return Prediction
2018, 哈工大SCIR
### 现状
Texts from the Internet serve as important data sources for financial market modeling. Early statistical approaches rely on manually defined features to capture lexical, sentiment and event information, which suffers from feature sparsity. Recent work has considered learning dense representations for news titles and abstracts.
### 问题
Compared to news titles, full documents can contain more potentially helpful information, but also noise compared to events and sentences, which has been less investigated in previous work.
### 思路
To fill this gap, we propose a novel target-specific abstract-guided news document representation model.
### 亮点
The model uses a target-sensitive representation of the news abstract to weigh sentences in the news content, so as to select and combine the most informative sentences for market modeling.
### 效果
Results show that document representations can give better performance for estimating cumulative abnormal returns of companies when compared to titles and abstracts. Our model is especially effective when it used to combine information from multiple document sources compared to the sentence-level baselines.
### 兴趣点
1. 手动构建的特征有feature sparsity的说法，而全文有噪声
2. event embedding怎么做的，他用新闻摘要辅助从全文中抽取
---

## Listening to chaotic whispers: A deep learning framework for news-oriented stock trend prediction
2018, 微软AI for Finance
### 现状
Stock trend prediction plays a critical role in seeking maximized profit from the stock investment. However, precise trend prediction is very difficult since the highly volatile and non-stationary nature of the stock market. Exploding information on the Internet together with the advancing development of natural language processing and text mining techniques have enabled investors to unveil market trends and volatility from online content. 
### 问题
Unfortunately, the quality, trustworthiness, and comprehensiveness of online content related to stock market vary drastically, and a large portion consists of the low-quality news, comments, or even rumors.
### 思路
To address this challenge, we imitate the learning process of human beings facing such chaotic online news, driven by three principles: sequential content dependency, diverse influence, and effective and efficient learning.
### 亮点
In this paper, to capture the first two principles, we designed a Hybrid Attention Networks (HAN) to predict the stock trend based on the sequence of recent related news. Moreover, we apply the self-paced learning mechanism to imitate the third principle.
### 效果
Extensive experiments on real-world stock market data demonstrate the effectiveness of our framework. A further simulation illustrates that a straightforward trading strategy based on our proposed framework can significantly increase the annualized return.
### 兴趣点
1. 新闻、评论等低质量，他们模仿人类的三个学习准则
2. 什么是self-paced learning mechanism?
3. 这是怎么衡量准确率的？
---

## Hierarchical complementary attention network for predicting stock price movements with news
2018, 北邮
### 现状
It has been shown that stock price movements are influenced by news. To predict stock movements with news, many existing works rely only on the news title since the news content may contain irrelevancies which seriously degrade the prediction accuracy.
### 问题
However, we observe that there is still useful information in the content which is not reflected in the title, and simply ignoring the content will result in poor performance.
### 思路
In this paper, taking advantage of neural representation learning, we propose a hierarchical complementary attention network (HCAN) to capture valuable complementary information in news title and content for stock movement prediction.
### 亮点
In HCAN, we adopt a two-level attention mechanism to quantify the importances of the words and sentences in a given news. Moreover, we design a novel measurement for calculating the attention weights to avoid capturing redundant information in the news title and content.
### 效果
Experimental results on news datasets show that our proposed model outperforms the state-of-the-art techniques.
### 兴趣点
1. 他说的many existing works rely only on the news title具体指哪些？现在还有参考价值吗？现在用全文还是标题多？
2. 计算注意力权重的新方法？
3. 哎，二分类精度也有60%？
---

## Exploiting Topic based Twitter Sentiment for Stock Prediction
2013, 港城大
### 现状

### 问题
This paper proposes a technique to leverage topic based sentiments from Twitter to help predict the stock market.
### 思路
We first utilize a continuous Dirichlet Process Mixture model to learn the daily topic set. Then, for each topic we derive its sentiment according to its opinion words distribution to build a sentiment time series. We then regress the stock index and the Twitter sentiment time series to predict the market.
### 亮点

### 效果
Experiments on real-life S&P100 Index show that our approach is effective and performs better than existing state-of-the-art non-topic based methods.
### 兴趣点
1. 就这二分类都有60%的准确率？？？
---

## Hybrid deep sequential modeling for social text-driven stock prediction
2018, 华师大
### 现状
In addition to only considering stocks’ price series, utilizing short and instant texts from social medias like Twitter has potential to yield better stock market prediction.
### 问题
While some previous approaches have explored this direction, their results are still far from satisfactory due to their reliance on performance of sentiment analysis and limited capabilities of learning direct relations between target stock trends and their daily social texts.
### 思路
To bridge this gap, we propose a novel Cross-modal attention based Hybrid Recurrent Neural Network (CH-RNN), which is inspired by the recent proposed DA-RNN model.
### 亮点
Specifically, CH-RNN consists of two essential modules. One adopts DA-RNN to gain stock trend representations for different stocks. The other utilizes recurrent neural network to model daily aggregated social texts. These two modules interact seamlessly by the following two manners: 1) daily representations of target stock trends from the first module are leveraged to select trend-related social texts through a cross-modal attention mechanism, and 2) representations of text sequences and trend series are further integrated.
### 效果
The comprehensive experiments on the real dataset we build demonstrate the effectiveness of CH-RNN and benefit of considering social texts.
### 兴趣点
1. learning direct relations他做到了吗
2. 准确率反而没达到59.15%？
3. cross-modal的说法
---

## Stock movement prediction from tweets and historical prices
2018, University of Edinburgh
### 现状

### 问题
Stock movement prediction is a challenging problem: the market is highly *stochastic*, and we make *temporally-dependent* predictions from *chaotic* data.
### 思路
We treat these three complexities and present a novel deep generative model jointly exploiting text and price signals for this task.
### 亮点
Unlike the case with discriminative or topic modeling, our model introduces recurrent, continuous latent variables for a better treatment of stochasticity, and uses neural variational inference to address the intractable posterior inference. We also provide a hybrid objective with temporal auxiliary to flexibly capture predictive dependencies.
### 效果
We demonstrate the state-of-the-art performance of our proposed model on a new stock movement prediction dataset which we collected.
### 兴趣点
1. recurrent, continuous latent variables是什麽，为什么能处理随机性
2. neural variational inference是什么，怎样处理the intractable posterior inference
3. hybrid objective with temporal auxiliary？
---

## Stakeholder Analyses of Firm-Related Web Forums: Applications in Stock Return Prediction
2015
### 兴趣点
1. stakeholder analysis， Expert systems
2. Stakeholder Theory of the Firm
---

## The effect of news and public mood on stock movements
2014
### 兴趣点
1. 有个对过往研究对比的表格，包括数据、方法
2. 就这样，精度都有0.5以上，可以作为对比？
---

## Web Media and Stock Markets : A Survey and Future Directions from a Big Data Perspective
2018, 四川金智金工和西南财经
### 兴趣点
1. 有个对过往研究对比的表格，包括所使用的信息来源（新闻、社交媒体、论坛）和Textual Representation方法
---

## A Multimodal Event-Driven LSTM Model for Stock Prediction Using Online News
2021, 四川金智金工和西南财经
### 现状
In finance, it is believed that market information, namely, fundamentals and news information, affects stock movements. Such media-aware stock movements essentially comprise a multimodal problem.
### 问题
Two unique challenges arise in processing these multimodal data. First, information from one data mode will interact with information from other data modes. A common strategy is to concatenate various data modes into one compound vector; however, **this strategy ignores the interactions among different modes.**

The second challenge is the heterogeneity of the data in terms of sampling time. Specifically, fundamental data consist of continuous values sampled at fixed time intervals, whereas news information emerges randomly. This heterogeneity can cause valuable information to be partially missing or can distort the feature spaces.

In addition, the study of media-aware stock movements in previous work has focused on the one-to-one problem, in which it is assumed that news affects only the performance of the stocks mentioned in the reports. However, news articles also impact related stocks and cause stock co-movements.
### 思路
In this article, we propose a tensor-based event-driven LSTM model to address these challenges.
### 亮点

### 效果
Experiments performed on the China securities market demonstrate the superiority of the proposed approach over state-of-the-art algorithms, including AZFinText, eMAQT, and TeSIA.
### 兴趣点
1. 新闻信息和股价数据时间上不一样