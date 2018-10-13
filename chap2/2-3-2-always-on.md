# 2.3.2 Always-on
> 实时（*Always-on*）大数据，开启了对突发事件和实时估测的研究。

很多大数据系统都是实时的（*Always-on*）：它们持续不断的收集着数据。这种实时性，给研究者提供了纵向数据（如：随时间推移的数据）。实时性（*Always-on*）对研究工作有两个重要影响。

首先，实时数据使得研究者以原本不可能的方式探索突发事件。例如，2013年夏季，土耳其发生的占领盖齐公园抗议事件，对它感兴趣的研究者们，通常关注于抗议者们在事件过程中的行为。[Ceren Budak and Duncan Watts(2015)](https://doi.org/10.15195/v2.a18)根据Twitter的实时性，研究了抗议者们在抗议发生前，过程中，以及结束及后的行为。同时，它们用未参与抗议的人，创建了相应的对照组（图2.2）。在数据中的 *事后板块（ex-post panel）* 中，共有30000人两年来的推文。通常使用的数据，由其他资源收集的抗议者信息。通过扩充常用数据，Budak和Watts能够进行更多的研究工作：它们能预测什么类型的人更可能参与到盖齐抗议中，以及从长期（发生前(pre-Gezi)对比发生后(post-Gezi)）和短期角度（发生前(pre-Gezi)对比进行中(during Gezi)），比较抗议者与非抗议者的态度变化。

![图2.2](https://www.bitbybitbook.com/figures/chapter2/bitbybit2-2_budak_dissecting_2015_schematic.png)
> 图2.2：2013年夏季土耳其的占领盖齐公园抗议事件中，[Budak and Watts(2015)](https://doi.org/10.15195/v2.a18)设计的数据。得益于Twitter的实时性（ *always-on*），用30000人两年来的推文，研究者构建了它们称为 *事后板块（ex-post panel）* 的数据。通常的数据关注于抗议者在实践中的行为，与之对比， *事后板块（ex-post panel）* 增加了： 1. 参与者发生前和事件结束后的行为数据。 2. 未参与抗议的人在事件前中后的数据。丰富的数据结构，使得Budak和Wastts能够估计什么类型的人更容易参与到占领盖齐的抗议中。以及从长期（发生前(pre-Gezi)与发生后(post-Gezi)）和短期角度（发生前(pre-Gezi)与进行中(during Gezi)），比较抗议者与非抗议者的态度变化。

一些怀疑论者可以能会说，有些估计不需要实时数据也可以做（比如，估计长时间跨度的态度变化）。虽然收集30000人两年的行为数据会很贵，理论上依然行得通。但是，即使是有无限的预算，我也想不到有什么其他方法，可以让研究者穿越到过去（*Travel back in time*）直接观察参与者的行为。最接近的替代方式也许是收集这些行为的回顾性报告（retrospective repots)，但这些报告粒度有限，同时准确性存疑。表2.1还提供了一些其他使用实时性数据研究突发事件的例子。

> 表2.1 使用实时性数据研究突发事件的例子

|突发事件|实时性数据源|引文引索|
|---|---|---|
|[土耳其的占领盖齐公园事件](https://zh.wikipedia.org/wiki/2013%E5%B9%B4%E5%9C%9F%E8%80%B3%E5%85%B6%E5%8F%8D%E6%94%BF%E5%BA%9C%E6%8A%97%E8%AE%AE%E8%BF%90%E5%8A%A8)|Twitter|[Budak and Watts(2015)](https://doi.org/10.15195/v2.a18)|
|[香港雨伞运动](https://zh.wikipedia.org/wiki/%E9%9B%A8%E5%82%98%E9%9D%A9%E5%91%BD)|微博|[Zhang(2016)](http://papers.ssrn.com/abstract=2647222)|
|纽约警察枪击事件|盘查报告|[Legewie(2016)](https://doi.org/10.1086/687518)|
|ISIS的先驱|Twitter|[Magdy, Darwish and Weber(2016)](https://doi.org/10.5210/fm.v21i2.6372)|
|[911恐怖袭击](https://zh.wikipedia.org/wiki/%E4%B9%9D%E4%B8%80%E4%B8%80%E8%A2%AD%E5%87%BB%E4%BA%8B%E4%BB%B6)|livejournal.com|[Cohn, Mehl, and Pennebaker(2014)](https://doi.org/10.1111/j.0956-7976.2004.00741.x)|
|[911恐怖袭击](https://zh.wikipedia.org/wiki/%E4%B9%9D%E4%B8%80%E4%B8%80%E8%A2%AD%E5%87%BB%E4%BA%8B%E4%BB%B6)|[BB机](https://zh.wikipedia.org/wiki/%E5%82%B3%E5%91%BC%E6%A9%9F)上的信息|[	Back, Küfner, and Egloff (2010), Pury (2011), Back, Küfner, and Egloff (2011)](https://doi.org/10.1177/0956797610382124)|

除了用来研究突发事件，实时大数据系统也可以用来进行实时信息估测。这有重要指导意义，对那些想对实时情况进行反馈的政策制定者——政府的或企业的——来说。例如，用社交媒体数据指导自然灾害的应急响应（[Castillo 2016](https://www.researchgate.net/publication/310250723_Big_Crisis_Data_Social_Media_in_Disasters_and_Time-Critical_Situations)）。还有，使用各种大数据资源，也可以对经济活动进行实时的估测（[Choi and Varian 2012](https://doi.org/10.1111/j.1475-4932.2012.00809.x)）。

总的来说，实时大数据系统使研究者可以研究突发事件以及为政策制定者提供实时信息。然而，我并不认为，实时大数据系统很适合跟踪长时间跨度的改变情况。这是因为，很多大数据系统在不断的更新——我称这个变化特性为 *drift*，我们将后面的章节里讨论它（2.3.7节）。
