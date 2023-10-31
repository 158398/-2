# -
记录数模第二次训练的代码，包括图片，思路和tex代码
# 问题分析
2020年美赛C题，这道题主要是关于数据分析方面的题，我们的模型的目的是从客户评分和评价的数据集中挖掘有价值的产品评价信息，利用这些信息来分析产品的声誉、发展和前景，并建立评分和评价之间的相关性。为了充分利用数据集中的丰富文本信息，我们提出了一种将词频统计、语义分析、向量操作和频繁项目集挖掘相结合，从文本中提取情绪和关键词的方法。为了充分利用各种形式的数据对产品进行评估，我们开发了一个全面的星级评级、情感评级和评论的可信度。最后，我们利用这些重要的指标和特征，结合时间模型、相关分析、可视化技术和机器学习算法来分析实际数据。
# 算法分析
我们首先考虑将多个指标整合为容易处理的几个指标，将相似的指标整合在一起，然后使用TFIDF技术针对数据集中的文本信息，以找到低频关键词。将高频关键词筛选为情感词和特征词进行分类。在对情绪词汇进行统计和向量化后，给出情绪特征向量，并进一步计算出文本的情绪得分。情绪分数反映了在文本中显示的情绪。经过统计处理后，得到了评论中的关键字集。利用fp增长算法，它可以得到所需的关键短语，即文本信息中的关键信息。从而提取了文本特征。文本功能可以反映用户的整体情绪倾向，以及产品最常见的优点或缺点。根据提取的文本特征等数据，根据各种指标创建每个产品的CSI。此外，根据本文每月提取的好评论和坏评论数量（根据星级评级），对本月和下月的评论数量进行相关分析，定量确定现有的评论伤口是否影响用户的评论数量和未来用户的好评率。采用两个相关指标对两者的相关性进行分析，从数据分布中可以看出相关性，并从计算出的相关指标中量化相关性大小。
# 文章总结
- 整合指标时没有说清楚关系，太套路刻板
- 文本数据的量化效果差
- 相关性分析不够科学
- 写作思路太差，模型与应用分离
- 文章刻意的长句太多，难以读懂
- 表格的标题应该在上方
- 结果可视化能力差，结果分析不足
- 排版间距
- 假设写的不好
- 公式无编号
# 学习计划和总结
## 写作
- 尝试着把学习到的写作技巧融入各部分的实战中，模仿优秀论文的句子和逻辑结构。学习了latex中一些经典的包的使用，包括页眉页码，公式算法流程图的设计。还学习了优秀论文的绘图思路，主要使用python实现，辅以origin和思维导图软件。尝试在阅读优秀论文的基础上对已有论文进行排版复现。
- 从这次的模拟赛中可以看出，队伍之间的配合和磨合不够，各队员的比赛经验明显不足，造成比赛时间安排不合理，留给写作内容和排版的时间太少，模型内容讲解不如优秀论文简洁有力，论文架构不够合理，对美赛题目的理解不够深入。需要在模拟赛中加快磨合，找到节奏。
- 第1周：学习最优化理论中的一些算法，尝试代码实现，主要学习凸函数理论。并学习Latex的一些排版技巧，阅读两篇论文。
第2周：继续学习凹极小值问题，线性规划。学习论文中introduction和methodology写法，阅读两篇论文。模仿并尝试复现美赛一篇优秀论文排版。
第3周：继续学习二次规划，半定规划。学习论文中model和result写法，阅读两篇论文。模仿并尝试复现美赛一篇优秀论文排版。
第4周：学习一些启发式算法。学习论文中discussion和conclusion写法，阅读两篇论文。模仿并尝试复现美赛一篇优秀论文排版。
第5周：整理代码和知识，学习绘图能使用PPT，AI，python，excel，Origin和其他一些软件网站绘图。阅读两篇论文。模仿并尝试复现美赛一篇优秀论文排版。
第6周：尝试与小组一起复现一到两篇论文，阅读两篇论文
## 编程
- a.图论方面：巩固了最短路、最小生成树、哈夫曼树方面的算法；学习了最大流、TSP方面的算法  b.ML/DM方面：掌握了多种分类（包括判别类模型与生成类模型）、聚类（包括基于原型、层次、密度、图的不同聚类模型）、降维（包括线性与非线性降维）方法以及回归（包括线性类、树类与概率类方法）模型并了解了其中一些复杂的算法；掌握了基本的关联分析方法  c.其它方面：掌握了动态规划；学习了时间序列模型，马尔科夫模型 
Pytnon方面：巩固了基本语法与一些基本库的使用，学习了正则表达式与DataFrame，了解了一些实用的库：networkx（图论库）、seaborn（绘图库）、statsmodel（统计库）以及nltk（NLP库），掌握了算法学习中大部分模型的实现方法
Matlab方面：巩固了基本语法，掌握了一些工具箱的实用方法
阅读了2019年CD题与2020年C题的优秀论文，理解了论文中使用的算法，使用的原因以及具体的使用方法。对数据类问题中的常用模型（如时序预测类、相关性分析类、回归类模型）有了大致了解并初步了解了网络类问题的建模思路
- 这段时间的学习基本达到目标，但存在以下方面的不足：a.虽然学习了很多模型，但还需要在遇到实际问题时快速想到该用什么模型并且能将实际问题通过一系列假设与转换转化为某个理论模型，在这方面还需要多在实践中训练  b.编程的能力与速度还不够，在实战中暴露出编程慢且花了不少时间debug的问题，说明对某些模块还不够熟悉，还需要多加练习  c.在建模过程中容易拘泥于细节而忽略了对整体问题把握  d.数据预处理与结果可视化方面掌握的还不够熟练  e.在实战中感觉毅力不足，由其在最后一天感觉想尽快了事，需要克服这种不良心态  在之后的学习中需要重视上述问题，以上问题其实都可以通过多加练习解决，在之后的学习中除了理论知识学习外还需要花更多时间在自行或与队友一起进行模拟训练并多借鉴优秀论文
- 学习计划：
巩固并加深对已了解的算法的理解，对于较为基础的算法，能掌握其中的原理，并了解其变种，在各种场合下能熟练应用.学习尚不了解的算法，对于其中较为复杂的算法，能大致了解其原理与应用场合.通过一些具体的例子（历年真题、数据集或小项目等），在实际中使用算法解决问题。
第1周：算法学习，图论方面：路与树方面的算法
ML/DM方面：基础的分类如LDA，ECOC编码，类别不平衡技术和SVM的学习、聚类如KNN，层次聚类法，密度聚类法、降维如主成分分析，独立成分分析基于特征值的方法等、回归如线性回归，Logistic回归，softmax回归、数据关联分析如基于粗糙集和基于模糊集的算法。
分析往年美赛题目及程序，总结其中用到的模型及代码
第2周：巩固python基础的数据结构与算法，学习并熟练使用numpy库、pandas库、sklearn库，重点掌握数据处理与分析以及机器学习方面的功能。分析往年美赛题目及程序，总结其中用到的模型及代码
第3周：算法学习，图论算法方面：网络与其它方面的算法 
ML/DM方面：一些基础算法的变种、集成学习如随机森林，XGBoost、概率及概率图模型、基础的深度学习如CNN，RNN和ANN
分析往年美赛题目及程序，总结其中用到的模型及代码
第4周：学习matlab中尚未掌握的功能，熟练使用常用函数，掌握数据可视化功能，熟悉各种工具箱的使用，如 Curve Fitting，Global Optimization，Simulink。分析往年美赛题目及程序，总结其中用到的模型及代码
第5周：将一些经典算法通过代码进行实现，使其在需要使用时经过少量修改即可调用，从网上收集复杂算法的代码，尝试理解并进行相应的修改。分析往年美赛题目及程序，总结其中用到的模型及代码
## 建模
- 进一步学习了运筹-规划论的内容，包括线性规划、整数规划、混合整数规划、凸规划、二次规划、目标规划、多目标规划以及动态规划等内容；学习了图论的一些基础内容，如最短路问题。
- 除阅读了2020年比赛C题的两篇O奖论文外，还阅读了2011年B题的两篇O奖论文（编号9440、10496），了解了其中的有关网络设计的建模思路，对这类问题有了一定的了解。
- 学习了数学物理方法以加强对数学物理类题型的基础，包括复变函数论以及数学物理方程，复变函数论中的傅里叶变换和拉普拉斯变换对信号处理类问题或其它离散型问题可以提供一定的思路，罗朗级数等板块也让我对奇异点的处理有了新的认识。整理学习了常见的数学物理方程以及最常见的解法，如波动方程的分离变量法及其推论（达朗贝尔公式等）
- 总的来说，我没有完成原定的学习计划，主要在于花了一些时间在学习额外的数学物理方法上，主要是想进一步加强数学物理类问题的数理基础，但也因此耽误了一些原定计划的学习，如只读了原计划中需要读的一半数量的论文，原计划的随机规划论部分也没有完成学习。接下来的时间里面会在参与好集训活动的基础上，尽力保证计划中要求的内容。
- 第1周：复习线性规划，非线性规划及其他规划论内容，补充欠缺知识，阅读两篇论文。
第2周：学习随机规划论部分。阅读两篇论文。
第3周：学习离散型预测。阅读两篇论文。
第4周：学习微分方程模型。阅读三篇论文。
第5周：学习打分式评价模型。阅读三篇论文。
第6周：学习统计类评价模型（相关性检验与拟合优度检验）。
将精力放在对各种所要用到的模型的熟悉上，整理近年来美赛题目中的数学物理以及其他知识，建立属于自己的模型与实际问题对照库，归纳总结各种问题的共性。
## 论文阅读计划
序号	论文年份	论文编号	选题
1	2011	9440	B
2	2011	10496	B
3	2011	9159	A
4	2011	11199	A
5	2019	1910246	A
6	2019	1915782	B
7	2019	1906204	C
8	2018	72969	C
9	2018	77845	A
10	2019	1922748	D
11	2018	74316	B
12	2017	65448	A
13	2017	68303	B
14	2017	78826	D
