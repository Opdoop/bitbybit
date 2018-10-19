# 2.3.6 Nonrepresentative
> 没有代表性的数据对样本外的泛化（*out-of-sample generalization*）没什么好处，但对样本内的对比（*within-sample comparisons*）却很有用。

很多社会科学家习惯于使用随机采样的数据，通常是来自界限明确的人群，比如特定国家的所有成年人。由于“代表”了一个更大的群体，这种数据通常叫做 *代表性 （representative）* 数据。有很多研究者赞美代表性数据。对于他们，代表性数据意味着它有严苛的科学定义，而没有代表性的数据意味着草率的原始数据。其中最极端的的怀疑者认为从非代表性的数据中发现不了任何有价值的东西。如果这是真的，由于大数据很多都是非代表性数据，我们能从中发现的东西十分有限。幸运的是，怀疑者们只对了一部分。确实非代表性数据不适合一些研究目标，但在其他的研究中大数据很有用。

让我们通过一个科学典故来理解这种区别：John Snow的研究，关于1853-54年在伦敦爆发的霍乱。在那时，很多医生认为霍乱是由于“糟糕的空气”造成的，但 Snow 认为有它是一种传染病，很可能由混入饮用水中的污水传播的。为了验证这个想法，Snow使用了我们现在所称的自然实验（natural experiment）。他比较了由两个供水商—— Lambeth 和 Southwark & Vauxhall 服务的住宅区的霍乱感染率。这两个公司为相似的住宅区服务，但他们有一很重要的不同点：在传染病发生前几年（1894年），Lambeth将它的水源移到了 London 污水排放处的上游，然而 South & Vauxhall 将它的水源留在了污水的下游。当 Snow 比较由这两个公司服务的地区时，发现它们的霍乱致死率有很大差距。喝被污染饮用水（产自Southwark & Vauxhall）的人，死于霍乱的概率比另一个地区的人高10倍。即使没用伦敦人的代表性样本，这个结果依然为 Snow 的假说提供了强有力的科学证据。

然而，使用这两个公司的数据却很难解决另一个问题：这场伦敦爆发的霍乱的患病率是多少？这个问题同样很重要。对于这个问题，用伦敦人的代表性样本也许更有帮助。

如 Snow 的工作所表明的，有一些科学问题使用非代表性数据十分有效，而另一些问题却不合适。粗略的区分方法是，有两种类型的问题。一些是关于样本内对比的，另一些是关于样本外泛化的。用另一个流行病学的经典研究可以进一步说明：British Doctors Study，它是一个抽烟会引起癌症的重要例证。在这项研究中，Richard Doll 和 A. Bradford Hill 跟踪记录了约25，000名医生长达几年。其中一些人从研究开始的时候也开始抽烟，通过将他们的死亡率与不抽烟的人对比，Doll 与 Hill（[1954](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC2085438/)）发现一个明显的反馈规律：吸烟越多的人，越可能患肺癌。当然，根据这群男医生的患病率来估计英国人的肺癌患病率并不合理，但样本内的对比依然为抽烟会引起肺癌提供了例证。

下面介绍样本内对比与样本外泛化的区别。首先，很自然的会问到，在英国男医生上发现的规律能否扩展到女性样本、全英国的医生，或者英国男性工人和德国女性工人等其他的样本上去。这个问题既有趣又关键，但这与将样本规律泛化到其他人群上的问题不同。注意，也许你会说抽烟与得肺癌的规律，虽然是从英国男医生上发现的，但在其他的人群里可能有一样的规律。这种结论的外推，不是因为英国男医生来自于随机抽样，而是理解了抽烟与肺癌背后的原理。因此，由样本泛化到采样人群是个统计上的问题，而模式从一个群体到另一个群体的可迁移性（*transportability*）是个非统计上的问题（[Pearl and bareinboim 2014](https://doi.org/10.1214/14-STS486), [Pearl 2015]https://doi.org/10.1515/jci-2015-0025)）。

从这点上说，怀疑论者会指出，大多社会模式的可迁移性，不像抽烟引起肺癌的规律一样，能从一个群体推广到另一个群体。这种看法我是同意的。模式有多大程度上可迁移最终是一个科学上的问题，需要根据理论和证据来决定。不应该先入为主，认为这种模式是可迁移的，或是认为它不可迁移。关于迁移性问题，研究者们有些抽象的讨论，关于大学生的行为能否推广到一般的人类行为（[Sears 1986](https://doi.org/10.1037/0022-3514.51.3.515), [@henrich_most_2010](https://doi.org/10.1037/0022-3514.51.3.515)）。如果关注这个讨论，你会对可迁移下更了解。尽管有各种争论，但是，说研究者们通过研究大学生的行为不能得到任何结果是说不讲理的。

第二个注意点。很多研究者并没有像 Snow 或 Doll和Hill 一样慎重的使用非代表性数据。使用非代表性数据进行样本外泛化会，研究者可能会得出错误的结论。下面用Andranik Tumasjan（[2010](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM10/paper/viewFile/1441/1852)）的一项关于2009年德国议会选举的研究来说明。通过分析超过 100，000 条推文，他们发现，推文中提及政党的比例与它们在选举中获得的选票比例很接近（图 2.3）。 In other words, it appeared that Twitter data, which was essentially free, could replace traditional public opinion surveys, which are expensive because of their emphasis on representative data.（yoyo来译一下？）

通过你对Twitter的了解，你也许会很快就快意他的结论。2009年使用Twitter的德国人，不是德国选民的随机抽样，同时一些政党的支持者也许比其他政党的支持者更喜欢发推文。Thus, it seems surprising that all of the possible biases that you could imagine would somehow cancel out so that this data would be directly reflective of German voters.（yoyo再译一句试试？）事实上，[Tumasjan et al.(2010)](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM10/paper/viewFile/1441/1852)的结果好得令人难以置信。一篇随之而来的论文中，[Andreas Jungherr, Pascal Jürgens, and Harald Schoen(2012)](https://doi.org/10.1177/0894439311404119)指出，原始的分析中排出了在Twitter上被提及最多的政党：the Pirate Party——一个抗议政府对互联网的监管的小政党。将 the Pirate Party 加入数据后，用 Twitter 上被提及的情况来预测选票，得到的结果很糟糕（图 2.3）。这个例子说明，使用非代表性大数据来做样本外泛化可能得到完全错误的结论。还有，你会发现这 100，000 条推文基本上是无关的：lots of nonrepresentative data is still non-representative（啥东西？），我在第三章讨论调查还会提到。

![图 2.3](https://www.bitbybitbook.com/figures/chapter2/bitbybit2-3_tumasjan_predicting_2010_tab4.png)
> 图 2.3 ：2009 年 德国政党在 Twitter 上的热度似乎可以预测德国大选的结果（[Tumasjan et al. 2010](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM10/paper/viewFile/1441/1852)），但排出了被提及最多的政党：Pirate Party（ [Jungherr, Jürgens, and Schoen 2012](https://doi.org/10.1177/0894439311404119)）。见[Tumasjan et al.(2012)](https://doi.org/10.1177/0894439311404123)，为什么排出了 Pirate Party。图片来自[Tumasjan et al. 2010](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM10/paper/viewFile/1441/1852)的表 4 和 [Jungherr, Jürgens, and Schoen 2012](https://doi.org/10.1177/0894439311404119)的表 2.

总的来说，很多大数据并不是边界清晰的人群中代表性样本。使用非代表性数据来进行泛化会有一系列的问题。但是在样本内对比的问题上，非代表性数据很有用。前提是研究者清楚样本的特性，并且说明可移植性的理论或经验上的依据。事实上，我希望通过使用大数据，研究人员在更多的非代表性群体间能做更多的样本内对比。并且我推测，使用不同组的估测比使用一个随机采样组的估测对研究者更有利。