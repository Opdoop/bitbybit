# 数学原理简介

在本篇附录中，我将用更数学化的语言，回顾一下在使用「非实验数据」推测因果效应时的一些思想。主要有两种方法：因果图 ([*causal graph*](https://en.wikipedia.org/wiki/Causal_graph)) 架构，与 Judea Pearl 他们的工作联系地最紧；潜在结果 (*potential outcomes*) 架构，与 [Donald Rubin](https://en.wikipedia.org/wiki/Rubin_causal_model) 他们的工作联系地最紧。我将介绍「潜在结果架构」，因为这个思想与第三章和第四章的数学原理简介联系更紧密。有关「因果图架构」的介绍，我推荐 [Pearl, Glymour, and Jewell (2016)](https://www.wiley.com/en-us/Causal+Inference+in+Statistics%3A+A+Primer-p-9781119186847) 作为入门读物，[Pearl (2009)](https://dl.acm.org/citation.cfm?id=1642718) 作为进阶读物。有关结合「因果图架构」与「潜在结果架构」做因果推断 (*casual inference*) 的书，我推荐 [Morgan and Winship (2014)](https://www.cambridge.org/core/books/counterfactuals-and-causal-inference/5CC81E6DF63C5E5A8B88F79D45E1D1B7)。

本篇附录的目标是让你熟悉「潜在结果」传统的记号与风格，帮助你过渡到到更的偏向技术的读物。首先，介绍「潜在结果框架」。接着，用它来描述一个「自然实验」，例如 [Angrist (1990)](http://www.jstor.org/stable/2006669) 的工作，研究服兵役对收入的影响。本篇附录大量引用了 [Imbens and Rubin (2015)](https://www.cambridge.org/core/books/causal-inference-for-statistics-social-and-biomedical-sciences/71126BE90C58F1A431FE9B2DD07938AB) 的内容。

## 「潜在结果框架」
「潜在结果框架」(*potential outcomes framework*) 有三个主要组成元素：*units*「单位」，*treatments*「处理」，*potential outcomes*「潜在结果」。让我们以 [Angrist (1990)](http://www.jstor.org/stable/2006669) 的经典问题为例：服兵役对收入有什么影响？在这个例子中，可以定义 1970 年美国彩票草案中的合格者为「单位」，并且我们可以对每个人建立引索「index」，\$  i \eq 1   ,...,N \$。在这个例子中，「处理」

Here is some inline math: $$ a \ne 0 $$

$$ a \ne 0$$
