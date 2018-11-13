# 2.3.4 incomplete
> 无论你用的数据量有多大，它很可能依然没有你想要的信息。

大部分大数据资源都是不完整的（*incomplete*），这是说你从中找不到所需的信息。在不是以研究为目的而建立的数据中，这是很常见的特征。很多社会科学家都有处理数据不完整性的经验，比如已有的调查（*survey*）没有提出他们需要的问题。不幸的是，大数据中的不完整性问题更多。在我的经验中，大数据常常缺少社会学研究需要的三种信息：参与者的人口统计信息（*demographic information*），在其他平台的行为数据，以及可以用来实践理论框架（*operationalize theoretical constructs*）的数据。

在这三种不完整性中，缺少实践理论框架的数据所带来的麻烦是最难解决的。同时，它经常被忽视。通俗的说，理论框架（*theoretical constructs*）是社会学家的一些抽象观念，实践（*operationalizing*）一个理论框架就是提出一个用可观测数据捕获这个框架的方法。不幸的是，这个听起来简单的过程常常十分困难。比如，有一个简单直观的假设：更聪明（*intelligent*）的人能赚更多的钱。如果我们想验证这个假设，我们首先要找到一种测量“聪明”程度的方法。但是，什么是聪明？[Gardner(2011)](https://books.google.com/books?id=2IEfFSYouKUC)认为聪明实际上由八中不同的类型。是否有一些方法能测量这些类型的聪明？尽管心理学家做大量的工作，这个问题仍然没有明确的答案。

从上面的例子看出，实践理论框架（*operationalize theoretical constructs*）的数据难以获取，即使一个相对简单的假设（*claim*），也很难评估（*assess empirically*）。还有一些重要但是难以实践的理论框架包括：“行为规范（*norms*）”，“基础设施（*social capital*）”，以及“民主（*democracy*）”。理论框架与数据的耦合程度，社会学家称为 *框架效度（construct validity）*（[Cronbach and Meehl, 1955](https://doi.org/10.1037/h0040957)）。即便有一个对框架设计的简短建议，社会学家依然与框架效度带来的麻烦缠斗了很多年。在我的经验里，当使用不以研究为目的的数据是，框架效度问题会带来更多麻烦（[Lazer 2015](http://citiespapers.ssrc.org/issues-of-construct-validity-and-reliability-in-massive-passive-data-collections/)）。

用框架来表述的和数据再表述的结果，来评估研究的框架效度，是一种快速有效的方法。比如，下面是两个对“更聪明的人能赚更多钱”这个假设的研究。再第一个研究中，研究者发现在[瑞文标准推理测验](https://zh.wikipedia.org/wiki/%E7%91%9E%E6%96%87%E6%B0%8F%E6%A8%99%E6%BA%96%E6%8E%A8%E7%90%86%E6%B8%AC%E9%A9%97)——一个经过充分检验的智力分析测试——中获得更高的成绩的人，在税收报告中的收入会更高（[Carpenter, Just and Shell 1990](https://doi.org/10.1037/0033-295X.97.3.404)）。在第二个研究中，研究者发现在Twitter上使用的单词长度越长，越有可能会提到奢侈品牌。这两个研究中，研究者都声称他们展示了更聪明的人能赚更多钱。然而，在第一个研究中理论框架在数据中很好的进行了实践，而第二个研究中没有。更进一步的，如前面所述，更多的数据并不能自然而然的解决框架效度的问题。无论在第二个实验中使用了100推文，10亿推文或万亿推文，你依然可以怀疑它的实验结果。对于不熟悉框架消毒思想的研究者，表2.2提供了一些使用数字轨迹数据实践理论框架的研究。

> 表2.2：使用数字轨迹实践理论框架的例子

|数据源|理论框架|引文引索|
|---|---|---|
|来自大学的电子邮件日志（仅元数据）|人际关系（Social relationships）|[Kossinets and Watts(2006)](https://doi.org/10.1126/science.1116869),[De Choudhury et al.(2010)](https://doi.org/10.1145/1772690.1772722)|
|发布在微博上的社交媒体数据|公民网络参与（Civic engagement）|[Zhang(2016)](http://papers.ssrn.com/abstract=2647222)|
|影院的电子邮件日志（完整内容和元数据）|组织中的文化契合（Cultual fit in an organization）|[Srivastava et al.(2017)](https://doi.org/10.1287/mnsc.2016.2671)|

即使大数据的不完整性，对实践理论框架带来的麻烦难以解决。其他几种不完整性——缺少人口统计学信息和缺少其他平带的行为数据——有一些常用解决方案。第一种方法就是去收集你所需的数据！我会在三张章介绍。第二种常用方法，数据科学家称作 *用户属性推理（user-attribute inference）*，社会科学家称作 *补插法（[imputation](https://en.wikipedia.org/wiki/Imputation_(statistics))）*。使用这种方法，研究者用他们已有的某些人的信息来推测其他人的信息。有时这个方法也称为 *记录链接（[record linkage](https://en.wikipedia.org/wiki/Record_linkage)）*。对于这方法，我最喜欢的一个类比，是[Dunn(1946)](https://doi.org/10.2105/AJPH.36.12.1412)在他的第一篇关于记录链接的论文的第一段中所写的：

> “Each person in the world creates a Book of Life. This Book starts with birth and ends with death. Its pages are made up of records of the principal events in life. Record linkage is the name given to the process of assembling the pages of this book into a volume.”

> "每个人都在写一本人生之书。这本书从出生开始，以死亡结束。每页上是人生中重要的记录。将书页编纂成一卷书的过程就记录链接（*record linkage*）。"

Dunn些这段话是，他想象的人生之书包括像出生，结婚，离婚和死亡这些重大事件。然而，现在的人有无数的记录，如果这些书页（如我们的电子轨迹）能够连接在一起，人生之书就会是一幅栩栩如生的画像。人生之书是研究者的重要资源。但是，在第六章（道德准则）将会谈到，它同时可能用于各种不道德的目的，[Ohm（2010）](https://www.bitbybitbook.com/www.uclalawreview.org/pdf/57-6-3.pdf)称之为“诸神黄昏（*database of ruin*）”。
