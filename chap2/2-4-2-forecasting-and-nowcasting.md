# 2.4.2 预测和即时预测
> 预测未来很困难，但预测现在相对容易。

研究者使用观测数据的第二个策略是 *预测（forecasting）*。对未来的情况进行猜测是出了名的难，也许就是因为这个，预测在当前的社会学研究中才不是主要部分（尽管这在人口学，经济学，流行病学和政治学是一个小而重要的部分）。然而，我将重点介绍一种特殊的预测：*即时预测（nowcasting）*——将 “now” 与 “forecasting” 而得到的词。即时预测不是预测未来，而是尝试使用预测中的思想来观测世界当前的状态；它试图 “预测现在”（predict the present）（[Choi and Varian 2012](https://doi.org/10.1111/j.1475-4932.2012.00809.x)）。对于需要及时准确的观测世界的政府与公司来说，即时预测尤其有用。

流行病学这个领域需要及时准确的测量。以流感为例（“the flu”）。每年，季节性流感在全世界会感染上百万人，以及夺走成百上千人的生命。此外，每年都可能会产生新式流感，有可能导致上百万人死亡。例如，1918 年爆发的那次流感，据估计导致了 50 到 100 万人死亡（[Morens and Fauci 2007](https://doi.org/10.1086/511989)）。为了跟踪以及可即时相应流感的爆发，世界各地的政府都建立了流感的监查系统。如美国的疾病防控中心（the Centers for Disease Control and Prevention (CDC)）会定期的系统性收集来自国内精选医生的信息。尽管这个系统能产生高质量的数据，但它的报告有个延后。因为从医生那里收集到的数据需要时间来清洗、预处理以及发布，疾病防控中心（CDC）发布的是流感两周前的估测情况。但是，当处理新兴的流行病时，公共健康部门的官员并不想知道两周前的流感情况，他们希望知道当前的流感情况。

在疾病防控中心（CDC）收集数据与跟踪流感时，Google 也在收集流感的流行情况， 虽然形式不同。世界各地的人不断的使用 Google 搜索，其中一些的查询，例如 “流感补救措施（flu remedies）” 和 “流感症状（flu symptoms）”，可能预示着查询的人得了流感。但使用这些搜索查询来估测流感情况颇为微妙（*tricky*）：不是所有得了流感的人都会进行搜索，也不是所有搜索的人都得了流感。

Jeremy Ginsberg 与一个 由 Google 和 CDC 人员组成的小组（[2009](https://doi.org/10.1038/nature07634)），巧妙的结合了这两种数据。简单的来说，通过使用一种统计学的“点金术”，研究人员能够把迅速但不准确的搜索数据与准确但滞后的 CDC 数据结合起来，得到对流感情况既准确又即时的估测。另一种角度来说，他们使用搜索数据来 “加速” CDC 的数据。

具体的来说，Ginsberg 他们使用 2003-2007 年的数据——CDC 的数据和 5000 万不同的关键词搜索数据——来估计流感流行度与关键词搜索量之间关系。使用这种纯数据驱动的、不需要任何具体医学知识的方式，研究者发现了 45 个不同的查询请求，最适合预测 CDC 流感流行度数据。接着，他们用 2007-2008 年流感季节的数据来测试他们的模型。发现，他们的模型确实可以提供有效的即使预测（图 2.6）。这个研究发表在《自然》杂志上，并得到了媒体的广泛报道。这项目叫做 「谷歌流感指数」（Google Flu Trends），称为了一个大数据改变世界的广为流传的寓言。

![图 2.6](https://www.bitbybitbook.com/figures/chapter2/bitbybit2-6_ginsberg_detecting_2009_fig3.png)
> 图 2.6 ：Jeremy Ginsberg 与他同事们创建的 「谷歌流感指数」（Google Flu Trends）。他们将 CDC 的数据与 Google 的搜索数据结合，来为 流感类疾病「influenza-like illness (ILI)」 进行即时预测。上面的结果图使用的是 2007-2008 年美国亚特兰大中部（mid-Atlantic）地区流感季节的数据。尽管「谷歌流感指数」 最初相当准确，随着时间的推移，它的性能逐渐衰退（[Cook et al. 2011](https://doi.org/10.1371/journal.pone.0023610); [Olson et al. 2013](https://doi.org/10.1371/journal.pcbi.1003256); [Lazer et al. 2014](https://doi.org/10.1126/science.1248506)）。图片来自 [Ginsberg et al. (2009)](https://doi.org/10.1038/nature07634)，figure 3 。

然而，这个表面上成功的故事，最终却是弄巧成拙。随着时间的推移，研究者发现「谷歌流感指数」有两个重大的缺陷，使得它的性能远不如最初。首先，它的性能不比简单模型（将 CDC 最近的两个流感流行度指标，用[线性外推法](https://en.wikipedia.org/wiki/Extrapolation#Linear)来预测（[Goel et al. 2010](https://doi.org/10.1073/pnas.1005962107)））好多少。并且，过了一段时间，「谷歌流感指数」的性能比这个简单方法还要差（[Lazer et al. 2014](https://doi.org/10.1126/science.1248506)）。换句话说，使用了大量数据，结合机器学习算法，以及消耗了大量计算力的「谷歌流感指数」，并不比简单的易于理解的[启发式方法](https://zh.wikipedia.org/wiki/%E5%90%AF%E5%8F%91%E6%B3%95)的效果好多少。这说明，当检验任何预测或即时预测的效果时，与基线进行对比很重要。

「谷歌流感指数」的第二个缺陷是它使用的数据，热词搜索量有两个大数据常见的不利特性—— *[drift](./2-3-9-dirty.md)* 和 *[algorithmic confounding](./2-3-8-algorithmically-confounded.md)*。这使预测结果在短期上容易错误，并且长期性上有能衰退。例如，在 2009 年的猪流感爆发时，「谷歌流感指数」严重高估了患流感的人群数量。这也许是因为人们对全球性疾病的恐惧感，改变了他们的搜素行为（[Cook et al. 2011](https://doi.org/10.1371/journal.pone.0023610); [Olson et al. 2013](https://doi.org/10.1371/journal.pcbi.1003256)）。除了这个短期问题，随着时间的推移，「谷歌流感指数」的性能也在逐渐衰退。由于 Google 的搜索算法是私有的，诊断长期性能衰退的原因十分困难。但似乎在 2011 年， 当人们搜索流感症状如 “发烧” 和 “咳嗽”，Google 会推荐相关的搜索关键词（这个功能似乎已经不再使用了）。从一个搜索引擎的角度来说，增加这个功能完全合理。但这个算法上的改变使得 「谷歌流感指数」 会收集到更多与健康相关的搜索请求，这导致它会高估流感的流行程度（[Lazer et al. 2014](https://doi.org/10.1126/science.1248506)）。

这两个缺陷使得即时预测在未来的研究工作复杂化，但这并等于宣判死刑。事实上，通过更加谨慎的方式，[Lazer et al. (2014)](https://doi.org/10.1126/science.1248506) 和 [Yang, Santillana, and Kou (2015)](https://doi.org/10.1073/pnas.1515373112) 已经可以避免这两个问题。更进一步的说，将研究者收集的数据与政府或企业的数据结合，我认为 *即时预测* 可以加速任何存在时间延后的常用指标，使估测更迅速更准确。像「谷歌流感指数」这样的即时预测项目，展现出研究中使用的传统数据与大数据结合的魅力。回想我们在第一章中的艺术类比，「即时预测」有潜力将 Duchamp 风格的 readymades 与 Michelangelo 风格的 custommades 结合，为决策者提供对当前以及近期情况更及时准确的估测。
