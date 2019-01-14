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

3. [![easy][dif-easy]] 有些人认为使用 [电子烟](https://zh.wikipedia.org/wiki/%E9%9B%BB%E5%AD%90%E7%85%99) 对戒烟有帮助，另一些人认为电子烟有些潜在的隐患，比如它有高浓度的尼古丁。假设，通过收集与电子烟相关的微博，使用一些情感分析方法，你想调查一下公众对电子烟的看法。

    a.  在这个研究中，你最担心的三个可能产生误差的地方是什么？  

    b.  [Clark et al. (2016)](https://doi.org/10.1371/journal.pone.0157304) 刚好做了这个研究。首先，他们收集了 2012 年 1 月到 2014 年 12 月与电子烟等关键字相关的推文，收集到了 850，000 个推文。再详细检查后，他们发现很多推文都是自动而不是人产生的，而且很多自动生成的推文实质上是商业广告。他们开发了一个推文检测算法，将自动生成的推文从原始推文中分离。使用这个算法，他们发现有 大约 80% 的推文都是自动产生的。这个发现是否改变了你对问题 (a) 的回答？  

    c.  用情感分析的方法比较收集到的原始推文与自动产生的推文，他们发现自动产生的推文比原始推文的正向情感更多 ( 6.17 比 5.84 ) 。这个发现是否改变了你对问题 (b) 的回答？

4. [![easy][dif-easy]] 2009 年 11 月， Twiiter 将 tweet box 的提示语从「What are you doing?」改为「What's happening?」 (https://blog.twitter.com/2009/whats-happening)。  

    a. 你认为这个提示语的改变，将如何影响发推特的人，以及如何影响人们发的推文？  

    b. 举出一个你倾向于使用「What are you doing?」的项目，并解释原因。

    c. 举出一个你倾向于使用「What's happening?」的项目，并解释原因。  

5. [![easy][dif-easy]] 「转发」 (Retweets) 常被用来衡量推文的影响力，以及推文传播的速度。起初，用户复制黏贴他们喜欢的推文，并标注原始作者，然后在推文最前面手工输入「RT」，表示这是一篇转发。后来，在 2009 年，Twitter 添加了「转发」按钮。2006 年六月，Twitter 允许用户转发他们自己的推文 (https://twitter.com/twitter/status/742749353689780224)。你认为，这个改变会影响你在研究中使用「转发」的方式吗？为什么？

6. [![hardest][dif-hardest], ![cubes][cubes], ![code][code], ![favorite][favorite]] 在一篇广泛讨论的文章中，Michel 他们 ([2011](https://doi.org/10.1126/science.1199644)) 通过分析超过五百万本电子书，试图识别长期的文化趋势。他们使用的数据，现在发布了出来，叫做「Google NGrams」数据集。因此，现在我们来用这个数据复现并扩展他们的一些研究。  
这篇论文中，Michel 与他同事们认为，我们忘记的越来越快。对一个具体年份， 比如说 1883 年，他们计算了 1-grams 在 1875 年到 1975 年发布书籍中，「1883」年所发布的比例由多少。他们指出，这个比例可以衡量人们对当年所发生事件的关注度。在他们的图 3a 中，他们画出了 1883 年，1910 年 和 1950 年的轨迹线。这三个年份有相同的模式：年初很低，然后是一个突然上升，接着是下降。揭晓来，为了定量评估每年下降时的速度，Michel and colleagues calculated the “half-life” of each year for all years between 1875 and 1975. In their figure 3a (inset), they showed that the half-life of each year is decreasing, 他们由此认为，这表明我们遗忘过去的速度正在越来越快。他们使用了英文语料库的第一版，但接着 Google 就发行了这个语料库的第二版。请在你开始编码之前，阅读下面所有的问题。  
在这道题中，你会练习写出可复用的代码，解释结果，数据清洗——例如处理数据的格式问题和处理数据缺失情况。同时，这道题中，你还会在一个丰富的、有趣的数据集上建立，运行实验。  

    a. 从 「Google Books Ngram Viewer」网站上下载原始数据。具体的来说，建议你下载英文语料库的第二版，它在 2012 年 7 月 1 日发布，解压后文件大约有 1.4 GB。  

    b. 复现 [Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 中图 3a 的主要部分。为了完成这个任务，你需要两个文件：你在上疑问中下载的文件和一个「total counts」的文件，用这个文件可以将数量转换为比例。注意，「total counts」文件有它的结果，读起来可能有些困难。NGram 第二版的数据得到的结果是否与 [Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 中使用第一版数据得到的结果相似？  

    c. 现在，对比一下你得到的图片与使用 NGram Viewer 得到的图片。  

    d. 重新画出图 3a (main figure)，但将 *y* 轴从比例改为数量。  

    e. (b) 小问与 (d) 小问之间的差别，引起了你对 Michel et al. (2011) 中的结果进行重新评价吗？为什么？  

    f. 现在，用比例来替换图 3a 的内容。就是说，对在 1875 年至 1975 年之间的年份，计算它们的「half-life」。「half-life」定义为这一年被提及的比率到达它峰值的一半之前，所经历的年份数。注意，[Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 在估算「half-life」时有更为复杂的操作，见其中的 Ⅲ.6 节，但他们声称这两种方法会得到相似的结果。使用 NGram 第二版的数据得到了与 [Michel et al. (2011)](https://doi.org/10.1126/science.1199644) 中基于第一版数据相似的结果吗？（提示：如果不相同也不要感到惊讶）  

    g. 有发现遗忘的特别快或特变慢的异常年份吗？浅显的推测一下产生这些异常的原因，并解释你是如何识别出这些异常值的。  

    h. 现在，将数据集替换为 NGrams 中的中文，法语，德语，希伯来语，意大利语，俄语以及西班牙语，分别计算一次结果。  

    i. 在所有的这些语言之间做比较，有发现有发现遗忘的特别快或特变慢的异常年份吗？浅显的推测一下产生这些异常的原因。  

7. [![hardest][dif-hardest], ![cubes][cubes], ![code][code], ![favorite][favorite]] [Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) 研究了 2013 年 6 月沸沸扬扬的 [棱镜计划](https://zh.wikipedia.org/wiki/%E7%A8%9C%E9%8F%A1%E8%A8%88%E7%95%AB) 是否导致了维基百科上与隐私问题有关的话题的稳住浏览量的突然下降。如果是这样，大规模监控引起了 [寒蝉效应](https://zh.wikipedia.org/wiki/%E5%AF%92%E8%9F%AC%E6%95%88%E6%87%89_(%E6%B3%95%E5%BE%8B))。[Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) 使用了叫做「受干预时间序列」( [interrupted time seires design](https://en.wikipedia.org/wiki/Interrupted_time_series) ) ，与 2.4.3 节的方法类似。  
根据 [美国国土安全部](https://zh.wikipedia.org/wiki/%E7%BE%8E%E5%9C%8B%E5%9C%8B%E5%9C%9F%E5%AE%89%E5%85%A8%E9%83%A8) 用来跟踪监控社交媒体的列表，Penney 选择出隐私问题相关的关键字。国土安全部的列表里，将搜索的关键字分类为一系列的问题，例如「健康问题」，「[基础设施安全](https://en.wikipedia.org/wiki/Infrastructure_security)」，和「恐怖主义」。在他的研究中， Penny 使用了与「恐怖主义」相关的 48 个关键词 (见附录的表 8 )。接着，他统计了从 2012 年 1 月 到 2014 年 8 月，共 32 个月里，与这 48 个词有关的维基百科文章的点击量。为了增强说服力，他还比较了几组其他主题文章的点击量。  
现在，我们来重现并扩展 [Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) 的工作。这个任务中，你需要的所以原始数据都看在维基百科上获取到。或者你可以从 R 包 「wikipediatrend」 ([Meissner and R Core Team 2016](https://cran.r-project.org/package=wikipediatrend)) 中获取。在你开始之前，请确认使用了对应的数据。(注意，这个任务同样出现在了第 6 章)。通过这个任务，你会练习数据清洗，对大数据中的自然实验进行思考。同时，这也适合作你研究工作的一次预演。  

    a. 阅读 [Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) ，然后复现其中的「figure 2」。这幅图显示了与「恐怖主义」有关的页面在斯诺登事件前后的点击量。从中你发现了什么？  

    b. 接着，重现「figure 4A」，这幅图对比了实验组 (与「恐怖主义」相关的文章) 与对照组 (其他类别的文章，见附录的表 10 与脚注 139)。从中你发现了什么？  

    c. 在上一问中，你比较了实验组与一个对照组。Penney 也与其他两个对照组进行了比较，「基础设施安全」相关的文章 (附录中的表 11) 和维基百科上的热门页面 (附录中的表 12)。如果再选择一个对照组，测试一下结论的敏感性，你会选择哪个主题的文章做对照组？为什么？  

    d. Penney 用与「恐怖主义」相关的关键词来筛选维基百科的文章，因为防范恐怖主义是美国政府开展网上监控的关键理由。为了检查与恐怖主义相关的 48 个关键词， [Penney (2016)](https://doi.org/http://dx.doi.org/10.15779/Z38SS13) 在 [MTurk](https://en.wikipedia.org/wiki/Amazon_Mechanical_Turk) 上进行了评测，让人们在 Government Trouble, Privacy-Sensitive, 与 Avoidance 的纬度上给关键词打分 (见附录中的 表7 和 表8)。复现 MTurk 上的测验，与 Penney 的结果进行比较。  

    e. 根据你在第 4 问的结果以及你所阅读的文章，你是否支持 Penney 在这次研究中对关键词的选择？为什么？如果不支持，你会建议如何选择关键词？

8. [![esay][dif-easy]] [Efrati (2016)](https://www.theinformation.com/facebook-struggles-to-stop-decline-in-original-sharing) 在报告中说到，据可靠消息，Facebook 上的「total sharing」同比下降5.5 %，而「original broadcast」同比下降了 21 %。在年龄小于 30 岁的 Facebook 用户中，这个下降尤其明显。报道认为有两个因素导致了这个下降。其一，是因为用户在 Facebook 上的好友数量逐渐增多。另一个，是用户转以消息的方式进行分享，以及转而使用 Snapchat 等竞品软件。报道还透露了 Facebook 刺激用户进行分享的一些策略，包括改变「News Feed」的算法，使原创推文更显眼，以及在「On This Day」板块周期性的对原创推文进行提醒。这个发现，对于想使用 Facebook 数据进行研究的研究者有什么影响吗？

9. [![medium][dif-med]] 你认为社会学家与历史学家之间的不同的是什么？[Goldthorpe (1991)](https://doi.org/10.2307/590368) 认为，主要的区别在于对数据的控制力上。历史学家只能研究遗迹或文物，而社会学家可以为特定需求收集相应的数据。阅读 [Goldthorpe (1991)](https://doi.org/10.2307/590368)。你认为社会学与历史学之间的区别，和「custommades」与「readymades」的思想有什么关联？

10. [![hard][dif-hard]] 本题建立在第 9 题的基础上。[Goldthorpe (1991)](https://doi.org/10.2307/590368)  的观点引起了大量的批评意见，其中包括 Nicky Hart ([1994](https://doi.org/10.2307/591522)) 对 Goldthorpe 推崇的「tailor made data」(数据裁剪) 提出质疑。Hard 用 Goldthorpe 的项目「Affluent Worker Project」阐明了「tailor-made」数据的潜在缺陷。「Affluent Worker Project」是 Goldthorpe 与其同时们在 1960 年代中期进行的一个调查，探索社会阶级与投票之间的关系。与多数偏爱设计数据胜过收集数据的学者一样，「Affluent Worker Project」项目收集到的数据也经过了裁剪，来验证一个关于未来生活水平提高后的社会阶层理论。但是，Goldthorpe 不知为何「忘记」了收集女性的投票行为。下面是 Hicky Hart ([1994](https://doi.org/10.2307/591522)) 对整个故事的总结：  
    > 「...受限于典型的不考虑女性的逻辑，这个『tailor made」数据难免会忽略女性数据。在阶级主义与大男子主义的驱使下...，Goldthorpe 与他的同事们构建了一组经验证明，生长在他们的理论假设之上，而没有经过恰当的检验。」

    > “… it [is] difficult to avoid the conclusion that women were omitted because this ‘tailor made’ dataset was confined by a paradigmatic logic which excluded female experience. Driven by a theoretical vision of class consciousness and action as male preoccupations … , Goldthorpe and his colleagues constructed a set of empirical proofs which fed and nurtured their own theoretical assumptions instead of exposing them to a valid test of adequacy.”

    Hart 继续道：

    > 「从『Affluent Worker Project」中的经验发现，更多的表达了中世纪社会学的大男子主义价值观，而没有阐明物质生活，政策，以及阶级分层的过程。」

    > “The empirical findings of the Affluent Worker Project tell us more about the masculinist values of mid-century sociology than they inform the processes of stratification, politics and material life.”

    数据构建者的偏见对「tailor-made」数据可能产生影响，你还能想到其他的例子吗？这与「algorithmic confounding」问题相比如何？这种个问题对研究者何时使用「readymade」数据，何时使用「custommade」数据有什么影响？

11. [![medium][dif-med]] 本章中，我对比了以研究目的收集的数据进行与政府或公司的日志数据。有时称日志数据为「found data」，与之相反的是「designed data」。日志记录确实是研究者发现的，但这些数据同样是经过设计的。例如，科技公司们花费很大的力气来收集、展示他们的数据。因此，这些日志记录即使被发现的，也是经过设计的，这仅仅取决于你的角度 (图 2.12)。

    ![图 2.12](https://www.bitbybitbook.com/figures/chapter2/bitbybit2-12_duck_rabbit_illusion.png)
    > 图 2.12 这张图片可以看作是一直鸭子，也可以看作是一直兔子。你所看见的取决于你的角度。大数据资源即使被发现的，也是被设计的，也就是说，你所看到的取决于你的角度。举例来说，站在研究者的角度，手机的通话记录是「found data」。但是，从电信公司的财务部门的角度看，这个记录就是「designed data」。图片来源: Popular Science Monthly (1899)/[Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Duck-Rabbit_illusion.jpg)。

    举一个数据的例子，同时从「found data」与「designed data」的角度来看这个数据，对研究是有帮助的。

12. [![easy][dif-easy]] 在一篇深刻的论文中，Christian Sandvig and Eszter Hargittai ([2015](http://mitp-content-server.mit.edu:18180/books/content/sectbyfn?collid=books_pres_0&id=9386&fn=9780262029889_Chap1.pdf)) 根据将数字系统作为「工具」或「研究对象」，将数据时代的研究分为两大类。将系统作为工具的一个例子，是 Bengtsson ([2011](https://doi.org/10.1371/journal.pmed.1001083)]) 利用手机数据跟踪 2010 海地地震后的人口迁移。将系统作为研究对象的一个例子，是 Jensen ([2007](https://doi.org/10.1162/qjec.122.3.879)) 关于手机是如何在 Kerala (印度南部邦名) 普及的，以及这如何影响了印度鱼类市场的运作。我发现，进行这种区分对研究很有帮助。因为这阐明了使用相同的数据，也可以可以有完全不同的研究目的。为了使这个差别更清晰，描述四个你见过的研究：两个是将数字系统作为工具，另外两个是将数字系统作为研究对象。如果你愿意，也可以使用本章中出现的例子。
