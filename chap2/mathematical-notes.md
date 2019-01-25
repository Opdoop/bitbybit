# 数学原理简介

在本篇附录中，我将用更数学化的语言，回顾一下在使用「非实验数据」推测因果效应时的一些思想。主要有两种方法：因果图 ([*causal graph*](https://en.wikipedia.org/wiki/Causal_graph)) 架构，与 Judea Pearl 他们的工作联系地最紧；潜在结果 (*potential outcomes*) 架构，与 [Donald Rubin](https://en.wikipedia.org/wiki/Rubin_causal_model) 他们的工作联系地最紧。我将介绍「潜在结果架构」，因为这个思想与第三章和第四章的数学原理简介联系更紧密。有关「因果图架构」的介绍，我推荐 [Pearl, Glymour, and Jewell (2016)](https://www.wiley.com/en-us/Causal+Inference+in+Statistics%3A+A+Primer-p-9781119186847) 作为入门读物，[Pearl (2009)](https://dl.acm.org/citation.cfm?id=1642718) 作为进阶读物。有关结合「因果图架构」与「潜在结果架构」做因果推断 (*casual inference*) 的书，我推荐 [Morgan and Winship (2014)](https://www.cambridge.org/core/books/counterfactuals-and-causal-inference/5CC81E6DF63C5E5A8B88F79D45E1D1B7)。

本篇附录的目标是让你熟悉「潜在结果」传统的记号与风格，帮助你过渡到到更的偏向技术的读物。首先，介绍「潜在结果框架」。接着，用它来描述一个「自然实验」，例如 [Angrist (1990)](http://www.jstor.org/stable/2006669) 的工作，研究服兵役对收入的影响。本篇附录大量引用了 [Imbens and Rubin (2015)](https://www.cambridge.org/core/books/causal-inference-for-statistics-social-and-biomedical-sciences/71126BE90C58F1A431FE9B2DD07938AB) 的内容。

## 「潜在结果框架」
「潜在结果框架」(*potential outcomes framework*) 有三个主要组成元素：单位「units」，处理「treatments」，潜在结果「potential outcomes」。为了介绍这个框架，让我们以 [Angrist (1990)](http://www.jstor.org/stable/2006669) 的经典问题为例：服兵役对收入有什么影响？在这个例子中，可以定义 1970 年美国彩票草案中的合格者为「units」，并且我们可以对每个人建立引索「index」，$i = 1   ,\dots, N$。「treatments」在这个例子中就是「服兵役」和「不服兵役」。我定义受试情况「treatment and control conditions」为 $W$，$W_{i} = 1$ 表示第 $i$ 个人在试验组，也就是「服兵役」，$W_{i} = 0$ 表示第 $i$ 个人在控制组，也就是「不服兵役」。最后，「potential outcomes」是可能会发生的事情，由于这是「潜在」的结果，在概念理解上有些困难。对于每个彩票草案中的合格者，我们可以假想，如果他们「服兵役」，在 1978 年时每个人可以挣的钱是 $Y_{i}(1)$ ，如果他们「不服兵役」，在 1978 年每个人可以挣 $Y_{i}(0)$ 。在「潜在结果框架」中，认为 $Y_{i}(1)$ 和 $Y_{i}(0)$ 是固定的，而 $W_{i}$ 是随机变量。

对「单位」，「处理」，「结果」的选择非常重要，因为这决定了你的研究能发现什么规律，而不能发现什么规律。在这个例子中，「单位」选择为 1970 草案中的合格者，这不包含女性。因此，没有额外的假设，这项研究无法解释任何服兵役对女性的影响。对「处理」和「结果」的定义同样重要。比如说，「处理」应该关注在服兵役还是参战经历？「结果」应该关注在收入还是对工作的满意程度？根本上说，科学和政策上的目标决定了对「单位」，「处理」和「结果」的选择。

给定「单位」，「处理」和「潜在结果」，「处理」对第 $i$ 个人的因果效应 $\tau_{i}$ 可以定义为：
$$\tau_{i} = Y_{i}(1) - Y_{i}(0) \quad (2.1)$$

也就是说，比较第 $i$ 个人服兵役和不服兵役时的收入。对我来说，公式 2.1 最清晰的定义了因果效应。尽管极其简化，这个框架可以在很多重要的有趣的方面进行推广 ([Imbens and Rubin 2015](https://www.cambridge.org/core/books/causal-inference-for-statistics-social-and-biomedical-sciences/71126BE90C58F1A431FE9B2DD07938AB))。

当使用「潜在结果框架」时，我发现写出每个单位「units」的处理「treatment」，潜在结果「potential outcomes」以及处理所产生的影响「treatment effects」，像表 2.5 那样，会帮助理解。在你的研究中，如果你想象不出这个表的样子，那么也许你需要更准确的定义你的「units」，「treatments」以及「potential outcomes」。

> 表 2.5 ：潜在的结果

|人的编号|如果去「服兵役」的收入|如果「不服兵役」的收入|「处理」所产生效应|
|---|---|---|---|
|1|$Y_{1}(1)$|$Y_{1}(0)$|$\tau_{1}$|
|2|$Y_{2}(1)$|$Y_{2}(0)$|$\tau_{2}$|
|$\vdots$|$\vdots$|$\vdots$|$\vdots$|
|N|$Y_{N}(1)$|$Y_{N}(0)$|$\tau_{N}$|
|平均值|$\bar{Y}(1)$|$\bar{Y}(0)$|$\bar{\tau}$|

然而，但我们用这种方式定义因果效应时，会遇到一些问题。在大多数情况，我们不能同时观测到这两个「潜在结果」。就是说，一个人要么「服兵役」，要么「不服兵役」。因此，我们只能观测到其中一个潜在结果——$Y_{i}(1)$ 或者 $Y_{i}(0)$。不能同时观测这两个「潜在结果」是个很关键的问题，以至于 [Holland (1986)](https://doi.org/10.2307/2289064) 称之为 「因果推测的根本问题」(*Fundamental Problem of Causal Inference*)。

幸运的是，当我们做研究时，并不只观测一个人。相反的，我们有可以观测很多人。这提供了一种绕过「因果推测的根本问题」的方法。与其尝试在个体层面 (*individual-level*) 估计处理效应 (*treatment effect*)，我们可以估计「平均处理效应」(*average treatment effect*)：
$$ ATE = \bar\tau = \frac{1}{N} \sum_{i=1}^N \tau_{i} \quad (2.2) $$

使用简单的代数方法 ([Gerber and Green (2012)](https://isps.yale.edu/research/data/d081) 中的 公式2.8)，将 公式2.1 带入 公式2.2，我们可以消除 $\tau_{i}$，得到：
$$ ATE = \frac{1}{N} \sum_{i=1}^N Y_{i}(1) - \frac{1}{N} \sum_{i=1}^N Y_{i}(0) \quad (2.3) $$

公式 2.3 说明，如果我们能估计试验组的平均结果 ($N^{-1} \sum_{i=1}^{N} Y_{i}(1)$) 以及控制组的平均结果 ($N^{-1} \sum_{i=1}^{N} Y_{i}(0)$) ，那么我们就可以估计「平均处理效应」。

现在，我们定义了需要估计的值，接下来即使如何通过数估算这些值。我们的问题是，对于每个人可能的「潜在结果」，只能观测得到其中的一个，$Y_{i}(1)$ 或 $Y_{i}(0)$ （表 2.6）。通过比较所有「服兵役」于「不服兵役」的人的收入，我们可以估测出「平均处理效应」：
$$ \widehat {ATE} = \underbrace{\frac{1}{N_{t}} \sum_{i:W_{i}=1} Y_{i}(1)}_{average\ earnings,\ treatment} - \underbrace{\frac{1}{N_{c}} \sum_{i:W_{i}=0} Y_{i}(0)}_{average \ earning,\ control} \quad (2.4)$$

其中 $N_{t}$ 是在试验组的人数，也就是「服兵役」的人数。$N_{c}$ 是控制组的人数，也就是「不服兵役」的人数。如果「处理」的分配与「潜在结果」是无关的，这种方法很有效。这个假设有时称作 「可忽略性」 ([*ignorability*](https://en.wikipedia.org/wiki/Ignorability))。不幸的是，在缺乏实验的情况下，「可忽略性」常常无法满足。也就是说，如果「处理」不是随机分配的，「处理」的分配很可能与「潜在结果」有相关性。这意味着公式 2.4 中的估测值也许会有误差。

> 表 2.6 ：观测到的结果

|人的编号|如果去「服兵役」的收入|如果「不服兵役」的收入|「处理」所产生效应|
|---|---|---|---|
|1|$？$|$Y_{1}(0)$|$？$|
|2|$Y_{2}(1)$|$？$|$？$|
|$\vdots$|$\vdots$|$\vdots$|$\vdots$|
|N|$Y_{N}(1)$|$？$|$？$|
|平均值|$？$|$？$|$？$|

在第四章，我将介绍「随机对照实验」 (*randomized controlled experiments*) 如何帮助研究者在进行「因果推测」。下面我将介绍研究者如何利用「自然实验」，比如彩票法案，进行因果推测。

## 「自然实验」
不进行实验来推测因果效应的一种方法，是在现实世界中寻找随机指派任务的事件。这种方式称作「自然实验」。不幸的是，在很多情况，自然情况下，这些「处理」并不是随机分派给你所关注的人群。然而，有时候，某些相关的「处理」是自然分配的。我将介绍由「二级处理」 (*secondary treatment*) 来激励 (*encourage*) 人们接受「一级处理」 (*primary treatment*) 的情况。举例来说，彩票草案可以被看作是随机分配的「二级处理」，激励人们接受「一级处理」——服兵役。这种设计称作「激励设计」 (*encouragement design*)。我将介绍一种分析方法，称作「工具变量」 (*instrumental variables*)，可以处理这种情况。在一些假设的前提下，研究者可以用这个激励机制来研究「一级处理」对于特定单元的影响。

为了区分「一级处理」与「二级处理」，我们需要一些新符号。假设一些人是在彩票草案中被随机抽中的 ($Z_{i} = 1$)，而一些人没有被抽中 ($Z_{i} = 0$)。在这种情况下，$Z_{i}$ 被称作「工具变量」。

在彩票法案中被抽中的人，有些去服兵役了 ($Z_i = 1,\ W_i = 1$) 而有些没有去 ($Z_i = 1,\ W_i = 0$)。同样的，在那些没被抽中的人中，有些自愿去服兵役 ($Z_i = 0,\ W_i = 1$)，而有些没去 ($Z_i = 0,\ W_i = 0$)。那么，「潜在结果」就可以同时描述「一级处理」和「二级处理」的状态。举例来说，$Y(1, W_i(1))$ 表示第 $i$ 个人被抽中时的收入，其中 $W_i(1)$ 表示他在控制组里。更进一步，我们可以把人分为四组：「乖宝宝」(*compliers*)，「懒汉」(*never-takers*)，「反抗者」(*defiers*)，「活雷锋」(*Always-takers*)，如表 2.7 所示。

> 表 2.7： 人群的四个分类

|类型|如果被征召，是否去服役|如果没被征召，是否去服役|
|---|---|---|---|
|乖宝宝|去，$W_i(Z_i=1)=1$|不去，$W_i(Z_i=0)=0$|
|懒汉|不去，$W_i(Z_i=1)=0$|不去，$W_i(Z_i=0)=0$|
|反抗者|不去，$W_i(Z_i=1)=0$|去，$W_i(Z_i=0)=1$|
|活雷锋|去，$W_i(Z_i=1)=1$|去，$W_i(Z_i=0)=1$|

在讨论如何估计「处理」（比如「服兵役」）产生的效应之前，我们可以定义激励（比如被征召」的两个效应。首先，我们可以定义这种激励对「一级处理」的影响。接着，我们可以定义这种激励对「二级处理」的影响。结果显示，这两种效应可以结合起来，来估计「处理」对特定人群的影响。

首先，对于第 $i$ 个人，激励对「处理」的影响可以定义为：
$$ ITT_{W,i} = W_i(1) - W_i(0) \quad (2.5)$$

然后，可以在人群层面定义这个量：
$$ ITT_W = \frac{1}{N} \sum_{i=1}^N [W_i(1) - W_i(0)] \quad (2.6)$$

最后，我们可以用数据来估计 $ITT_W$ ：
$$\widehat{ITT_W} = \bar{W}_1^{obs} - \bar{W}_0^{obs} \quad (2.7)$$

其中 $\bar{W}_1^{obs}$ 代表在观测人群中，「处理」产生激励效应的比例；$\bar{W}_0^{obs}$ 代表观测人群中，「处理」没有产生激励效应的比例。$ITT_W$ 有时 被称为 「吸收率」 (*uptake rate*)。

接下来，对于第 $i$ 个人，激励对结果的影响可以定义为：
$$ ITT_{Y,i} = Y_i(1,W_i(1)) - Y_i(0,W_i(0)) \quad (2.8)$$

然后，可以在人群层面定义这个量：
$$ ITT_Y = \frac{1}{N} \sum_{i=1}^N [Y_i(1,W_i(1)) - Y_i(0,W_i(0))] \quad (2.9)$$

最后，我们可以用数据来估计 $ITT_Y$ :
$$\widehat{ITT_Y} = \bar{Y}_1^{obs} - \bar{Y}_0^{obs} \quad (2.10)$$

其中 $\bar{Y}_1^{obs} 代表在观测人群中，受到激励的人的结果（例如：被征召的人的收入）；$\bar{Y}_0^{obs}$ 代表在观测人群中，未受到激励的人的结果。

最后，来看看我们关注的效应：「一级处理」对结果的影响（例如：服兵役对收入的影响）。不幸的是，通常来说，我们不能在所有的「单位」(*units*) 层面上估计这个效应。然而，在一些假设下，研究者可以估计「处理」对「乖宝宝」（例如，被征召就去服役，没被征召就不去服役的人，表 2.7）的影响。我把这个估计量叫做 *complier average causal effect (CACE)*（有时也叫做 *local average treatment effect*, LATE）：
$$ CACE = \frac{1}{N_{co}} \sum_{i:G_i=co} [Y(1, W_i(1)) - Y(0, W_i(0))] \quad (2.11) $$

其中 $G_i$ 表示第 $i$ 个人所在的组别（见表 2.7），$N_{co}$ 表示「乖宝宝」的人数。也就是说，公式 2.11 比较了「乖宝宝」中被征召 $Y_i(1,W_i(1))$ 和没有被征召的 $Y_i(0,W_i(0))$。然而，公式 2.11 的估计量看起来很难从观测数据中估测，因为从观测数据中看不出哪些人是「乖宝宝」（区分谁是「乖宝宝」，你需要知道当他们被征召时是否去服役，同时知道当他们没被征召时是否去服役）。

结果上来看多少有点让人意外。如果观测数据中有「乖宝宝」，那么在三个额外的假设下，有可能来估计 CACE。第一个假设，是假设「处理」的分派是随机的。这个假设在彩票草案的例子中还算符合。然而，某些中「自然实验」，对「处理」的分派并不依赖物理意义上的随机，比如抽签或掷色子，这个假设就可能会问题。第二个假设，是假设观测数据中没有「反抗者」（这个假设有时称作「单调性假设」(*monotonicity assumption*)）。在彩票草案的情景中，认为几乎没有人自愿服役，也没有人被征召了但不去服兵役，也说得过去。第三个，也是最后一个假设，是最关键的假设，称作「排他性约束」(*exclusion restriction*)。在「排他性约束」中，认为激励不会直接对结果产生影响。比如说，在彩票草案中，征召只能通过服兵役来对收入产生影响（图 2.11）。「排他性约束」可能会被违反，比如说，为了躲避服役，有些人会多在学校里待几年，又或者说，也许雇主们不太喜欢服过兵役的人。

![图 2.11](https://www.bitbybitbook.com/figures/chapter2/bitbybit2-11_exclusion_restriction.png)

> 图 2.11： 在「排他性约束」下，激励只能通过「处理」对结果的产生影响，比如，在彩票法案中被征召只能通过服兵役来对它的收入产生影响。

如果满足这三个假设：随机指派，没有「反抗者」，以及「排他性约束」，那么：
$$ CACE = \frac{ITT_Y}{ITT_W} \quad (2.12) $$

然后我们可以估计 CACE：
$$ \widehat{CACE} = \frac{\widehat{ITT_Y}}{\widehat{ITT_W}} \quad (2.13)$$

一种理解 CACE 的方式是，在「吸收率」下，受到激励与没受到激励的人之间结果的差异。

有两个重要的注意事项需要牢记。首先，「排他性约束」是个强假设，需要对每个场景进行检验，这通常需要领域专家的帮助。「排他性约束」不能通过激励的随机性来证明。比如，彩票法案中抽签的随机性，不能证明被征召只会通过服兵役对人的收入产生影响。第二，当激励对「处理」的影响很小时，比如期末考试对是否接着浪的影响很小，使用「工具变量」分析因果效应就会有些问题。这称作「弱工具变量」(*weak instrument*)，并且这会引起各种麻烦 ([Imbens and Rosenbaum 2005](https://doi.org/10.1111/j.1467-985X.2004.00339.x); [Murray 2006](http://www.jstor.org/stable/30033686))。一种解释是，也许由于违反了「排他性约束」，$\widehat{CACE}$ 中的 $\widehat{ITT_Y}$ 会变得很敏感，并且还会因为 $\widehat{ITT_W}$ 很小，而放大这种敏感性（见公式 2.13）。笼统的说，如果自然事件中的「处理」对你所关注的「处理」没有多大影响，那么你将有一段艰难的时期，来研究你所关注的「处理」。

更正式的介绍，见 [Imbens and Rubin (2015)](https://www.cambridge.org/core/books/causal-inference-for-statistics-social-and-biomedical-sciences/71126BE90C58F1A431FE9B2DD07938AB) 第 23 章和 24 章。传统的计量经济学角度，是从那些估测公式介绍「工具变量」，并不是「潜在结果」。更多其他角度的介绍，见 [Angrist and Pischke (2009)](https://press.princeton.edu/titles/8769.html)。这两种角度的对比，见 [Imbens and Rubin (2015)](https://www.cambridge.org/core/books/causal-inference-for-statistics-social-and-biomedical-sciences/71126BE90C58F1A431FE9B2DD07938AB) 的 24.6 节。作为替代的，[Gerber and Green (2012)](https://isps.yale.edu/research/data/d081) 的第 6 章，用不太正式的方式介绍了「工具变量」。更多有关「排他性约束」的介绍，见 [D.Jones (2015)](http://www.nber.org/papers/w21391)。[Aronow and Carnegie (2013)](https://doi.org/10.1093/pan/mpt013) 介绍了额外的一组假设，可以估测 ATE 而不止 CACE 。解释「自然实验」时会遇到的一些问题，见 [Sekhon and Tituinik (2012)](https://doi.org/10.1017/S0003055411000542) 。不只是「工具变量」，一些对「自然实验」中常见方法的介绍，例如「断点回归」，见 [Duning (2012)](https://www.cambridge.org/core/books/natural-experiments-in-the-social-sciences/96A64CBDC2A2952DC1C68AF77DE675AF) 。