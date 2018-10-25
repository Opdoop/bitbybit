# 2.3.10 Sensitive
> 政府和企业拥有的一些信息是敏感的。

健康保险公司有他们客户详细的病例信息。这些信息可以用在重要的研究课题中。但是，如果将这些数据公开，可能会导致一些精神伤害（如：难堪的事情被公开）或经济伤害（如：导致失业）。很多其他的大数据源同样包含 *敏感的* 信息，这也部分解释了为什么他们常常难以获取。

然而，确定哪些信息是敏感的，是个棘手的问题（[Ohm 2015](https://www.bitbybitbook.com/lawreview.usc.edu/issues/past/view/download/?id=1000030)）。我将在第五章介绍，2006年时，Netflix 发布了 100 万电影的评分。评分来自世界各地的大约 500，000 Netflix用户，这些评分信息可以提升 Netflix 推荐电影的性能。在发布之前，Netflix 消除了明显的个人信息，例如姓名。但发布仅仅两周后，Arvind Narayana 和 Vitaly Shmatikov （[2008](https://doi.org/10.1109/SP.2008.33)）发现可以从中得到具体的某个人对电影的评分。使用的跟踪方法我将在第六章介绍。即使攻击者能够推测出某人对电影的评分，这也算不上什么敏感信息。但对于 500，000 用户中的一部分来说，这些电影评分也是敏感信息。事实上，这之后一名未出柜的女同性恋者加入了对 Netflix 的集体诉讼中。在诉讼中，公开这些信息带来的问题是这样表述的（[Single 2009](http://www.wired.com/2009/12/netflix-privacy-lawsuit/)）：

>“[M]ovie and rating data contains information of a … highly personal and sensitive nature. The member’s movie data exposes a Netflix member’s personal interest and/or struggles with various highly personal issues, including sexuality, mental illness, recovery from alcoholism, and victimization from incest, physical abuse, domestic violence, adultery, and rape.”

>“电影与打分信息包含着很私人和敏感的信息。用户的电影偏好数据暴露了 Netflix 会员的个人兴趣爱好 并且/或者 一些很私人的问题，包括性取向，精神疾病，从酗酒中康复，或者是乱伦，虐待，家暴，通奸或强奸的受害者。”

这个例子说明，在善意的数据库中，某些信息对一些人来说也是敏感的。更进一步的，这显示出研究者用来保护敏感数据的去身份化方法，会以出人意料的方式失败。这两个观点将在第六章更详细的讨论。

最后是一些关于敏感数据的引起的道德问题。即使没有造成具体的损害，在人们没有意识到情况下收集数据依然会带来道德问题。这就像在一个人未意识到的情况下偷看他洗澡，这侵犯了个人隐私。需要注意，在未经同意的情况下区分敏感数据是极其困难的，这也会引起潜在的隐私问题。在第六章，我会再次讨论有关隐私的问题。

总的来说，政府或企业拥有的大数据，一般来说都不是为社会学研究建立的。今天和未来的大数据来源往往有10个特征。其中一些通常被认为是对研究有益的——big, always-on，和 nonreactive。这得益于数字时代的政府和企业有能力大范围收集各种数据，在之前这是不可能的。同样，还有很多特征通常被认为是对研究不利的—— incomplete，inaccessible，nonrepresentative，drifting，algorithmically confounded，inaccessible，dirty 和 sensitive。这是因为大数据不是为研究而建立的。到目前为止，我们将政府与企业的数据合在一起讨论，但是他们之间还有些不同点。在我的经验中，政府数据的 nonrepresentative, algorithmically confounded, 和 drifting 的问题往往更轻微。另一方面，企业数据往往更 always-on。理解这 10 个一般特征，有益于迈向大数据研究的第一步。现在，我们来看看使用这些数据的研究策略。
