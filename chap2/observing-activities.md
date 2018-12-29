# 延伸活动

[dif-easy]: https://www.bitbybitbook.com/figures/icons/dif-easy.svg
[dif-med]: https://www.bitbybitbook.com/figures/icons/dif-med.svg
[dif-hard]: https://www.bitbybitbook.com/figures/icons/dif-hard.svg
[dif-hardest]: https://www.bitbybitbook.com/figures/icons/dif-hardest.svg
[math]: https://www.bitbybitbook.com/figures/icons/math.svg
[code]: https://www.bitbybitbook.com/figures/icons/code.svg
[cubes]: https://www.bitbybitbook.com/figures/icons/cubes.svg
[favorite]: https://www.bitbybitbook.com/figures/icons/favorite.svg

* 难度：简单 ![easy][dif-easy], 中等 ![medium][dif-med], 困难 ![hard][dif-hard], 极其困难 ![very hard][dif-hardest]
* 需要数学基础 (![math][math])
* 需要编程 (![code][code])
* 需要收集数据 (![cubes][cubes])
* 我的最爱 (![favorite][favorite])

1. [![medium][dif-med],![favorite][favorite]] Google Flu Trends 倍受算法变化所带来的困扰。阅读文章 [Lazer et al. (2014)](https://doi.org/10.1126/science.1248506) ，给 Google 工程师写一篇简明的 email，解释存在的问题，并给出一些修复问题的想法。

2. [![medium][dif-med]] [Bollen, Mao, and Zeng (2011)](https://doi.org/10.1016/j.jocs.2010.12.007) 称，使用 Twitter 数据可以预测股市。根据这个发现，产生了一个名为「Derwent Capital Markets」的对冲基金，它根据从 Twiiter 收集的数据来投资股市 ([Jordan 2010](http://www.bloomberg.com/news/articles/2010-12-22/hedge-fund-will-track-twitter-to-predict-stockmarket-movements))。在把你的钱放在这个基金之前，你希望发现哪些证据？

3. [![easy][dif-easy]] 有些人认为使用 [电子烟](https://zh.wikipedia.org/wiki/%E9%9B%BB%E5%AD%90%E7%85%99) 对戒烟有帮助，另一些人认为电子烟有些潜在的隐患，比如它有高浓度的尼古丁。假设，，通过收集与电子烟相关的微博，使用一些情感分析方法，你想调查一下公众对电子烟的看法。
    1.  在这个研究中，你最担心的三个可能产生误差的地方是什么？

    2.  [Clark et al. (2016)](https://doi.org/10.1371/journal.pone.0157304) 刚好做了这个研究。首先，他们收集了 2012 年 1 月到 2014 年 12 月与电子烟等关键字相关的推文，收集到了 850，000 个推文。再详细检查后，他们发现很多推文都是自动而不是人产生的，而且很多自动生成的推文实质上是商业广告。他们开发了一个推文检测算法，将自动生成的推文从原始推文中分离。使用这个算法，他们发现有 大约 80% 的推文都是自动产生的。这个发现是否改变了你对问题 (3.1) 的回答？

    3.  用情感分析的方法比较收集到的原始推文与自动产生的推文，他们发现自动产生的推文比原始推文的正向情感更多 ( 6.17 比 5.84 ) 。这个发现是否改变了你对问题 ( 3.2 ) 的回答？

4. [![easy][dif-easy]] 2009 年 11 月， Twiiter 将 tweet box 的提示语从「What are you doing?」改为「What's happening?」 (https://blog.twitter.com/2009/whats-happening)。
    1. 你认为这个提示语的改变，将如何影响发推特的人，以及如何影响人们发的推文？
    2. 举出一个你倾向于使用「What are you doing?」的项目，并解释原因。
    3. 举出一个你倾向于使用「What's happening?」的项目，并解释原因。

5. [![easy][dif-easy]] 「转发」 (Retweets) 常被用来衡量推文的影响力，以及推文传播的速度。起初，用户复制黏贴他们喜欢的推文，并标注原始作者，然后在推文最前面手工输入「RT」，表示这是一篇转发。后来，在 2009 年，Twitter 添加了「转发」按钮。2006 年六月，Twitter 允许用户转发他们自己的推文 (https://twitter.com/twitter/status/742749353689780224)。你认为，这个改变会影响你在研究中使用「转发」的方式吗？为什么？

6. [![hardest][dif-hardest], ![cubes][cubes], ![code][code], ![favorite][favorite]] 在一篇广泛讨论的文章中，Michel 他们 ([2011](https://doi.org/10.1126/science.1199644)) 通过分析超过五百万本电子书，试图识别长期的文化趋势。他们使用的数据，现在发布了出来，叫做「Google NGrams」数据集。因此，现在我们来用这个数据复现并扩展他们的一些研究。

这篇论文中，Michel 与他同事们认为，我们忘记的越来越快。对一个具体年份， 比如说 1883 年，他们计算了 1-grams 在 1875 年到 1975 年发布书籍中，「1883」年所发布的比例由多少。他们指出，这个比例可以衡量人们对当年所发生事件的关注度。在他们的图 3a 中，他们画出了 1883 年，1910 年 和 1950 年的轨迹线。这三个年份有相同的模式：年初很低，然后是一个突然上升，接着是下降。揭晓来，为了定量评估每年下降时的速度，Michel and colleagues calculated the “half-life” of each year for all years between 1875 and 1975. In their figure 3a (inset), they showed that the half-life of each year is decreasing, 他们由此认为，这表明我们遗忘过去的速度正在越来越快。他们使用了英文语料库的第一版，但接着 Google 就发行了这个语料库的第二版。请在你开始编码之前，阅读下面所有的问题。

在这道题中，你会练习写出可复用的代码，解释结果，数据清洗——例如处理数据的格式问题和处理数据缺失情况。同时，这道题中，你还会在一个丰富的、有趣的数据集上建立，运行实验。
  1. 从 「Google Books Ngram Viewer」网站上下载原始数据。具体的来说，建议你下载英文语料库的第二版，它在 2012 年 7 月 1 日发布，解压后文件大约有 1.4 GB。

  2. 复现 [Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 中图 3a 的主要部分。为了完成这个任务，你需要两个文件：你在上疑问中下载的文件和一个「total counts」的文件，用这个文件可以将数量转换为比例。注意，「total counts」文件有它的结果，读起来可能有些困难。NGram 第二版的数据得到的结果是否与 [Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 中使用第一版数据得到的结果相似？

  3. 现在，对比一下你得到的图片与使用 NGram Viewer 得到的图片。

  4. 重新画出图 3a (main figure)，但将 *y* 轴从比例改为数量。

  5. 第 2 小问与第 4 小问之间的差别，引起了你对 Michel et al. (2011) 中的结果进行重新评价吗？为什么？

  6. 现在，用比例来替换图 3a 的内容。就是说，对在 1875 年至 1975 年之间的年份，计算它们的「half-life」。「half-life」定义为这一年被提及的比率到达它峰值的一半之前，所经历的年份数。注意，[Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 在估算「half-life」时有更为复杂的操作，见其中的 Ⅲ.6 节，但他们声称这两种方法会得到相似的结果。使用 NGram 第二版的数据得到了与 [Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 中基于第一版数据相似的结果吗？（提示：如果不相同也不要感到惊讶）

  7. 有发现遗忘的特别快或特变慢的异常年份吗？浅显的推测一下产生这些异常的原因，并解释你是如何识别出这些异常值的。

  8. 现在，将数据集替换为 NGrams 中的中文，法语，德语，希伯来语，意大利语，俄语以及西班牙语，分别计算一次结果。

  9. 在所有的这些语言之间做比较，有发现有发现遗忘的特别快或特变慢的异常年份吗？浅显的推测一下产生这些异常的原因。

7. [![hardest][dif-hardest], ![cubes][cubes], ![code][code], ![favorite][favorite]] [Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) 研究了 2013 年 6 月沸沸扬扬的 [棱镜计划](https://zh.wikipedia.org/wiki/%E7%A8%9C%E9%8F%A1%E8%A8%88%E7%95%AB) 是否导致了维基百科上与隐私问题有关的话题的稳住浏览量的突然下降。如果是这样，大规模监控引起了 [寒蝉效应](https://zh.wikipedia.org/wiki/%E5%AF%92%E8%9F%AC%E6%95%88%E6%87%89_(%E6%B3%95%E5%BE%8B))。[Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) 使用了叫做「受干预时间序列」( [interrupted time seires design](https://en.wikipedia.org/wiki/Interrupted_time_series) ) ，与 2.4.3 节的方法类似。

根据 [美国国土安全部](https://zh.wikipedia.org/wiki/%E7%BE%8E%E5%9C%8B%E5%9C%8B%E5%9C%9F%E5%AE%89%E5%85%A8%E9%83%A8) 用来跟踪监控社交媒体的列表，Penney 选择出隐私问题相关的关键字。国土安全部的列表里，将搜索的关键字分类为一系列的问题，例如「健康问题」，「[基础设施安全](https://en.wikipedia.org/wiki/Infrastructure_security)」，和「恐怖主义」。在他的研究中， Penny 使用了与「恐怖主义」相关的 48 个关键词 (见附录的表 8 )。接着，他统计了从 2012 年 1 月 到 2014 年 8 月，共 32 个月里，与这 48 个词有关的维基百科文章的点击量。为了增强说服力，他还比较了几组其他主题文章的点击量。

现在，我们来重现并扩展 [Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) 的工作。这个任务中，你需要的所以原始数据都看在维基百科上获取到。或者你可以从 R 包 「wikipediatrend」 ([Meissner and R Core Team 2016](https://cran.r-project.org/package=wikipediatrend)) 中获取。在你开始之前，请确认使用了对应的数据。(注意，这个任务同样出现在了第 6 章)。通过这个任务，你会练习数据清洗，对大数据中的自然实验进行思考。同时，这也适合作你研究工作的一次预演。

  1. 阅读 [Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) ，然后复现其中的「figure 2」。这幅图显示了与「恐怖主义」有关的页面，在斯诺登事件前后的点击量。从中你发现了什么？

  2. 接着，重现「figure 4A」，这幅图对比了实验组 (与「恐怖主义」相关的文章) 与对照组 (其他类别的文章，见附录的表 10 与脚注 139)。从中你发现了什么？

  3. 在上一问中，你比较了实验组与一个对照组。Penney 也与其他两个对照组进行了比较，「基础设施安全」相关的文章 (附录中的表 11) 和维基百科上的热门页面 (附录中的表 12)。如果再选择一个对照组，测试一下结论的敏感性，你会选择哪个主题的文章做对照组？为什么？

  4.
