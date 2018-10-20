# 2.3.7 Drifting
> 大数据的三种变动性——使用人群的变动，使用方式的变动以及系统本身的变动，使得很难用它来进行长期趋势的研究。

大数据有个很好的优点，随着时间的推移，它不断的收集着数据。社会学家将这种时间序列数据称作 *纵向数据（longitudinal data）*。当然，纵向数据对研究变化很有帮助。然而，为了可高的观测变化，测量系统本书必须保持稳定。用社会学家 Otis Dudley Duncan 的话说，“if you want to measure change, don't change the measure”（[Fischer 2011]()）。（“怎么翻译啊TAT”）

不幸的是，很多大数据系统——尤其是商业系统——随时在变化，我把这个过程叫做 *漂移（drift)*。具体的说，系统的变化有三种主要形式：*使用人群的漂移（population drift）*，*使用方式的漂移（behavioral drift）*，*系统本身的漂移（system drift）*。这三种漂移方式意味着，任何从大数据中发现的模式也许是因为真实世界的重要变化，或者是因为某种形式的漂移。

第一种漂移——使用人群的漂移（population drift），同时可能在长时间和短时间维度上发生。例如，在 2012 年美国总统选举期间，关于政治话题的推文中，由女性发布的比例每天都在波动（[Diaz et al.2016]()）。因此，推文中情绪的变化也许是因为发文的人群发生了变化。除了短期的波动，使用和弃用 Twitter 的群体，他们的人口统计信息，在长时期上也有明确的变化趋势。

除了使用人群的变化，使用方式也可能会变化。我称这是行为漂移（behavioral drift）。例如，在2013土耳其占领盖齐公园的示威游行中，抗议者使用Twiter标签的方式在随着游行的进展而变化。通过观察Twitter和现场情况， Zeynep Tufekci 对抗议中的行为漂移这样描述：
> “What had happened was that as soon as the protest became the dominant story, large numbers of people … stopped using the hashtags except to draw attention to a new phenomenon … While the protests continued, and even intensified, the hashtags died down. Interviews revealed two reasons for this. First, once everyone knew the topic, the hashtag was at once superfluous and wasteful on the character-limited Twitter platform. Second, hashtags were seen only as useful for attracting attention to a particular topic, not for talking about it.”

> “当抗议发展为热点事件时，很多人用标签（hashtag）为新的现象吸引注意力。随着抗议的继续，甚至是冲突加剧，标签的热度逐渐消失。通过访谈揭示出两个原因。首先，一旦人们知道主题是什么，使用标签即使多余的，因为Twitter对推文有字数限制。其次，标签只对吸引注意力有用，对谈论这个话题没什么帮助。”

因此，由于行为漂移，使用Tiwter标签分析这次抗议行动的研究人员也许会有曲解。例如，认为有关抗议活动的讨论，在抗议结束之前就早早停止了。

第三种漂移是系统漂移（*system drift*）。这种漂移，不是由于适用人群或使用方式的变化，而是系统本身的改变。例如，随着时间的推移，Facebook 在不断增加当前状态的字数上限。因此，对 Facebook 用户当前状态的长时间维度研究，很容易受这种人为改变的影响。系统漂移与 algorithmic confounding 联系紧密，我将在 2.3.8 节讨论这个问题。

总的来说，很多大数据资源的漂移是因为使用人群的变化，使用方式的变化和系统本身的变化。这些数据源的变化，有时是个有趣的研究课题，但也使分析长时间趋势变得复杂。
