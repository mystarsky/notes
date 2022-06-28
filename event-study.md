# Daily Event Study：短期事件研究

# 简介
## 理论框架
1. 半强有效市场假说
2. 事件未被市场预期到
3. 窗口期无其他事件的混合影响

## 相关概念
1. 事件日->事件窗口期->实际收益率
2. 估计窗口->正常收益率
3. 实际收益率-正常收益率=异常收益率->窗口期累积异常收益率

## 估计模型
1. 市场模型
2. 市场调整模型
3. Fama三因子模型
4. Carhart四因素模型
5. 历史平均模型

## 相关介绍论文
> MacKinlay, A. C. (1997). Event Studies in Economics and Finance. Journal of Economic Literature, 35(1), 13–39. http://www.jstor.org/stable/2729691
> 
> 汉文 陈 and 向民 陈 (2002). 证券价格的事件性反应——方法、背景和基于中国证券市场的应用
> 
> Eugene F. Fama (1991). Efficient Capital Markets: II
> 
> Kim J. Heyden, Thomas Heyden, Market reactions to the arrival and containment of COVID-19: An event study, Finance Research Letters, Volume 38, 2021, 101745, ISSN 1544-6123, https://doi.org/10.1016/j.frl.2020.101745.

## 市场调整模型
$AR_{i,t}=R_{i,t}-\hat{R}_{i,t}=R_{i,t}-(\hat{\alpha}_i+\hat{\beta}_iR_{m,t})$

$CAR_i(t_1,t_2)=\sum_{t=t_1}^{t_2}AR_{i,t}$

## 因果
格兰杰因果

因果推理
1. 关联
2. 干预
3. 反事实

## Event Study (ESM) vs Difference-in-differences (DID)
1. ESM 是一重差分 (事件前和事件后)，DID 是双重差分 (i.事件前后差分；ii. 处理组和控制组之间的差分)；
2. 更加实用的判别方法是，如果研究中既有处理组又有对照组，那么 DID 是合适的研究设计；如果只有处理组，并且处理组的数据是时间序列数据，那么 ESM 则是合适的研究方法。
+ 启发：控制组的设置

# Eugene F. Fama (1991). Efficient Capital Markets: II
+ because they come closest to allowing a break between market efficiency and equilibrium-pricing issues, event studies give the most direct evidence on efficiency. And the evidence is mostly supportive.

the market model, the original event study
> Fama, E. L. Fisher, M. Jensen and R. Roll, 1969, The Adjustment of Stock Price to New Information, International Economic Review 10: 1 -21.

Reviews of research on financial decision event study
> Smith, Clifford W. Jr., 1986, Investment banking and the capital acquisition process, Journal of Financial Economics 15, 3-29.
> 
> Jensen, Michael C. and Richard S. Ruback, 1983, The market for corporate control: The scientific evidence, Journal of Financial Economics 11, 5-50.
> 
> Jensen, Michael C. and Jerold B. Warner, 1988, The distribution of power among corporate managers, shareholders, and directors, Journal of Financial Economics 20, 3-24.

Reviews of extensive event study literatures in accounting, industrial organization and macroeconomics
> Binder, John J., 1985, Measuring the effects of regulation with stock price data, Rand Journal of Economics 16, 167-182.
> 
> Santomero, Anthony, 1991, Money supply announcements: A retrospective, Journal of Economics and Business 43, 1-23.

+ Many of the corporate-control studies appear in finance journals, but the work goes to the heart of issues in industrial organization, law and economics, and labor economics.

# 汉文 陈 and 向民 陈 (2002). 证券价格的事件性反应——方法、背景和基于中国证券市场的应用
+ 如收益和非正常收益的分布对统计检验的影响 ;非同步交易(Non-synchronous trading)对模型参数估计的影响(Scholes 和 Williams 1977);事件日的不确定性与事件窗的长度(Ball 和 Torous 1988);事件日的集聚性(Clustering)的影响等(Bernard 1987)。

运用事件分析法对会计盈余报告的市场有用性进行经验证明
> Ball, R and P. Brown. 1968. An Empirical Evaluation of Accounting Income Numbers. Journal of Accounting Research: 159 -178.

对计算正常收益的模型进行比较
> Brown, S and J. Warner. 1980, Measuring Security Price Performance. Journal of Financial Economics 8: 205 -258
> 
> Brown and J. Warner. 1985, Using Daily Returns-a Case of Event Study. Journal of Financial Economics 8: 4 -31 


# MacKinlay, A. C. (1997). Event Studies in Economics and Finance
## Procedure for an event study
1. define the event of interest and identify the event window
2. determine the selection criteria for firms involved in the study. It is useful to summarize some sample characteristics and note any potential biases through the sample selection.
3. define normal return. There are two common ways to model the normal return: the constant mean return model and market model
4. define the estimation window
5. calculate the abnormal return
6. statistical test
## Models for measuring normal return
1. Constant Mean Return Model: Brown and Warner (1980, 1985) find it often yields results similar to those of more sophisticated models. This lack of sensitivity to the model can be attributed to the fact that the variance of the abnormal return is frequently not reduced much by choosing a more sophisticated model.
2. Market Model
3. Other Statistical Models, e.g. the *factor model*: The reason for the limited gains is the empirical fact that the marginal explanatory power of additional factors the market factor is small, and hence, there is little reduction in the variance of the abnormal return. The variance reduction will typically be greatest in cases where **the sample firms have a common characteristic**, for example they are all members of one industry or they are all firms concentrated in one market capitalization group.
4. Economic Models, the CAPM and the APT: They are dominated by statistical models.