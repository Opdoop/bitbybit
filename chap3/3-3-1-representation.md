# 3.3.1 代表性
> 代表性关乎与从受访者推论出被试人群的问题。

为了说明从受访者推论到目标人群的过程中有哪些坑，让我们来回顾一下「文学文摘」对 1936 年美国大选进行的一次预测。尽管是很多年前的事，这当中依然有很深刻的教训。

「[文学文摘](https://en.wikipedia.org/wiki/The_Literary_Digest)」曾是本畅销的通俗杂志。从 1920 年起，这本杂志就开始通过 [非正式民意测验](https://en.wikipedia.org/wiki/Straw_poll) 来预测美国的大选结果。他们进行预测的方法很简单，给人们发放大量的选票，然后将回收来的选票数量直接加起来。「文学文摘」层骄傲的称，回收来的选票从没有经过「加权，调整，或其他特殊处理」。通过这种方式，他们成果的预测了 1920 年，1924 年，1928 年以及 1932 年美国总统选举的胜出者。到了 1936 年，正值经济 [大萧条](https://zh.wikipedia.org/wiki/%E5%A4%A7%E8%90%A7%E6%9D%A1) 的中期，「文学文摘」向公众发放了 1，000 万张选票，这些人主要是从电话本和汽车注册记录上选的。下面是「文学文摘」对他们的方法论的描述：

> 「『文摘』像一个精密运转的机器，以它 30 多年的经验，将人们的猜测变为铁一般的事实...本周，有约 500 只笔，每天从登记簿上划去超过 25 万条住址信息。每天，在纽约第四大道的高大房间里，约 400 名工人熟练的分装着百万张选票，这些选票足够铺满 40 个街区。每小时，在『文摘』的邮局里，三个嗡嗡作响的邮资计费器将信封密封加盖邮戳；迅捷的『文摘』卡车车队，飞快地将信件运往专门的邮政列车...接下来的一周，写好的选票将如潮水般涌回来，在接受三次检测，验证，以及五重交叉分类后被统计出来。检查、计算完最后一张选票后，如果过去的经验是可靠的，这个国家将会知道 4000 万选民中，1% 的人的真实投票情况。」 (1936 年 8 月 22 日)


> “THE DIGEST’s smooth-running machine moves with the swift precision of thirty years’ experience to reduce guesswork to hard facts … This week 500 pens scratched out more than a quarter of a million addresses a day. Every day, in a great room high above motor-ribboned Fourth Avenue, in New York, 400 workers deftly slide a million pieces of printed matter—enough to pave forty city blocks—into the addressed envelops [sic]. Every hour, in THE DIGEST’S own Post Office Substation, three chattering postage metering machines sealed and stamped the white oblongs; skilled postal employees flipped them into bulging mailsacks; fleet DIGEST trucks sped them to express mail-trains . . . Next week, the first answers from these ten million will begin the incoming tide of marked ballots, to be triple-checked, verified, five-times cross-classified and totaled. When the last figure has been totted and checked, if past experience is a criterion, the country will know to within a fraction of 1 percent the actual popular vote of forty million [voters].” (August 22, 1936)

「文学文摘」对样本的数量是如此痴迷，与当今研究者对「大数据」的迷恋一样。「文学文摘」发出了约 1000 万张选票，令人振奋的，回收了月 240 万张。这比现在的联邦政治投票数的 1，000 倍还要多。 从这 240 万个回复来看，结果很清楚：阿尔夫·兰登将击败现任总统富兰克林·罗斯福。然而，事实上，罗斯福以压倒性的选票击败了兰登。「文学文摘」是怎样从如此多的数据中得出错误预测的？以我们现在对抽样的理解，可以分析出「文学文摘」犯了哪些错误，以此来爆出我们避免在未来犯类似的错误。

清晰的描述抽样，我们会涉及到四个不同的人群 (图 3.2)。首先，是 「target population」（目标人群） ，这是研究者定义的、他所关心的人群。在「文学文摘」的例子中，目标人群是 1936 年总统大选的所有选民。

在确定目标人群之后，研究者需要列个名单，看看可以从哪些人里进行抽样。这个名单被称作「sampling frame」（抽样框架」，这当中的人群被称作「frame population」（框内人群）。理想情况，目标人群与框内人群应该完全一样，但实践中几乎没有这样的例子。例如，在「文学文摘」的例子中，框内人群的名字主要来自于电话与汽车的等级记录上。目标人群与框内人群之间的差异被称作「coverage error」（覆盖误差）。覆盖误差本身并不一定会导致问题。然而，如果框内人群与目标人群存在系统性的差异，这会导致「coverage bias」（覆盖偏差）。这实际上就是「文学文摘」所犯的错误。在框内的人，更倾向于支持阿尔夫·兰登，一定程度上是因为他们更富有（在 1936年，电话和汽车都是时髦昂贵的东西）。所以，在「文学文摘」的民意调查中，覆盖误差导致了覆盖偏差。

![图 3.2](https://www.bitbybitbook.com/figures/chapter3/bitbybit3-2_representation_errors.png)
> 图 3.2 代表性误差

在定义了框内人群后，下一步就是确定「sample population」（抽样人群）。抽样人群就是研究者尝试去进行访谈的人群。如果抽样人群与框内人群有不同的特征，那么这个抽样就会引入「sampling error」（抽样误差）。在「文学文摘」的滑铁卢中，并没有进行抽样，「文摘」杂志联系了所有在框架人群里的人，因此并没有抽样误差。抽样误差是在调查的误差报告中可以被发现的一种典型的误差。但「文学文摘」的失败提醒我们，需要考虑各种可能的误差，包括随机误差和系统性误差两方面。

最后，在确定了抽样人群后，研究者将尝试与他们进行访谈。那些成功完成访谈的人被称作「respondent」（调查对象）。理想情况下，抽样人群与调查对象是完全一样的。但实际上，会有一些人拒绝进行访谈。也就是说，在被选定的样本中，有时不会参与访谈。如果同意访谈的人与拒绝访谈的人之间存在差异，这种差异就被称作「nonresponse bias」（无应答误差）。无应答误差是「文学文摘」的第二大文帝。收到选票的人中，只有 24 % 的人进行了答复。结果是支持兰登的人更倾向于进行答复。

「文学文摘」民意调查的例子，不仅仅是介绍「代表性」这个思想，它是一个经常被人提起的寓言故事，警示研究者们任意抽样的危险性。但我认为，很多人从中这个故事中学到的教训是错的。最常见的寓意是说，研究者从非随机采样（选择参与者时没有严格的概率和规则）中不能探索出任何有用的东西。在本章后面的部分中，我将证明这个观点并不对。相反的，我认为这个故事有两个寓意，这些寓意在 1936 年与今天同样有用。第一个教训是，任意收集的数据，即使量很大，也不能保证得到一个良好的估测结果。使用大量的数据，研究者有时可以为错误的方法得到一个准确的估计，这被称作「precisely inaccurate」（[McFarland and McFarland 2015](https://doi.org/10.1177/2053951715602495)）。第二个教训是，研究者在估测时需要解释他们是如何进行抽样的。具体来说，在「文学文摘」的失败中，他们的抽样方法对支持兰登的人有系统性的倾斜。因此，研究者需要使用更复杂的估测方式，调整某些调查对象的权重。本章后面的部分中，我将介绍一个加权方式——「post-stratification」（事后分层），这将使你从任意抽样中做出更好的估测。
