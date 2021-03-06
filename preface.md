## 作者序

2005年，哥伦比亚大学的一个地下室里，这本书开始成形。那时我还是研究生，正在进行一个线上实验，它最终成了我的学位论文。在第四章，我会将这个实验所有方法上的内容告诉你。但是现在我想说些别的，它不会出现在我的学位论文或者其他任何我的论文里。它从根本上改变了我对研究的想法。某天清晨，当我来到我的地下办公室，我发现昨夜有大约100个巴西人参与了我的实验。这件事对我产生了深远的影响。与此同时，我的一些朋友正在研究室进行传统的实验。我知道他们招募、监督以及付款给参与者的艰难险阻。如果一天可以进行10个人已经是很快的进度了。然而，在我的线上实验中，有100个人参与了实验，*在我睡觉的时候*。在睡觉时进行实验有些难以置信，但它真实发生了。技术的发展，尤其是从模拟时代（*analog age*）到数字时代（*digital age*）的变革，使得我们现在可以用新的方法收集和分析社会学数据。本书就是介绍用新方法做社会学研究。

本书是为想做数据科学的社会学家、想做社会科学的数据科学家，以及任何对这个交叉领域感兴趣的人写的。不言而喻，本书不只是针对学生或教授。尽管我正在大学（*Princeton*）供职，我同时也在政府（*US Census Bureau*）和科技公司（*Microsoft Research*）工作。因此我知道，在学校之外有很多令人激动的研究正在进行。无论你的工作或使用的技术是什么，只要你认为你所作的是社会学研究，那么这本书正适合你。

你可能已经注意到，本书的口吻有些不同于其他的学术书籍。这是刻意的。本书源于我从2007年起在普林斯顿大学社会学系（*Department of Sociology*）开设的关于计算社会科学（*computational social science*）的研究生研讨会。我从中整理出了一些思想的火花。具体的说，我希望这本书有三个特性：有启发性的，面向未来的以及乐观的。

**启发性**：我的目标是写一本对你有启发性的书。因此，我将用一种开放的，通俗的，实例驱动的（*example-driven*）的风格写这本书。因为最重要的是，我希望传递一种对社会研究（*social research*）的思考方式。同时，我的经验告诉我，最好的方法就是使用通俗的话，并且使用大量的实例。另外，在每章的结尾，设有“扩展阅读（*What to read next*）”。在那有本章所涉及话题更详细的和技术方法的读物。最后，我希望能启发你的研究以及启发你如何评价他人的研究。

**面向未来**：本书将启发你使用已经存在的 *和* 那些将会出现的数据系统来做社会学研究。我从2004年开始做这种研究，从那时起已经改变了很多。同时我相信，在你的职业生涯中，你也会看到很多的改变。紧跟时代的诀窍是 *抽象* 。例如，本书并不会教你如何使用Twitter API，相反，它会教你如何从大数据的来源中学习（*第二章*）。本书不会给你一个如何在Amazon Mechanical Turk上进行实验的说明手册，相反，它会教如何从你设计和解释一个依赖数字时代技术的实验中学习（*第四章*）。通过使用抽象，我希望本书在与时俱进的热点上永不过时。

**乐观**：本书交叉的两个群体————社会科学家与数据科学家，有迥异的背景和兴趣。除了那些与科学有关的差异外，我也注意到这两个群体有不同的风格。数据科学家大多比较乐观；他们倾向于认为杯子有一半是满的。与之相反，社会科学家大多比较悲观；他们倾向于认为杯子有一半是空的。在本书中，我采用了数据科学家那种乐观的口吻。因此，当我介绍实例时，我会告诉你我喜欢的那部分。没有实验是完美的，所以当我指出实例的问题时，我也会用一种积极的、乐观的角度。我不是因为悲观而吹毛求疵，我这么做是希望能帮你更好的进行研究。

在数字时代，社会学研究仍刚刚起步，但有些常见的误区我认为需要在这里解释一下。对于数据科学家来说，我见过两个常见的误解。一个是认为更多的数据可以自然而然的解决问题。然而，在社会学研究上，我的经验告诉我不是这样的。事实上，在社会学研究中，更好的数据而不是更多的数据会有更有帮助。另一个误解是，一些我见到的数据科学家认为社会科学只是将常识用精巧的语言包装一下。作为一个社会科学家，我并不同意这个观点。先贤已经花了很久是时间去理解人类的行为，无视这些累积的知识是不明智的。我希望这本书可以用一种通俗易懂的方式介绍这些智慧结晶。

对于社会科学家来说，我同样见过两个常见的误解。首先，我见过一些人因为几篇劣质论文而完全摒弃使用数字时代的工具。如果你正在阅读本书，也许你已经读过一堆平庸的或错误使用社交媒体数据的论文。我也读到过很多。然而，从这些例子得出结论，认为所有数字时代的社会学研究都是糟糕的，这是不可取的。事实上，你也许也读过一堆平庸的或错误使用调查数据（*survey data*）的论文，但你并没有摒弃所有使用调查数据的研究。这是因为你知道有很多优秀的研究也是使用调查数据。在本书中，我将展示一些同样优秀的研究使用的是数字时代的工具。

社会科学家的另一个误解是把现在与未来混为一谈。当我们评估数字时代的社会学研究时，我们需要区分两个问题：“这种风格的研究在现在效果如何？”以及“这种风格的研究在未来会怎样？”研究者们精通于回答第一个问题，但我认为第二个问题更为重要。也就是说，尽管数字时代的社会学研究还没有大规模展开，也没有产生足以改变范式的效果。但数字时代研究的进步速度非常快。这种超越当下水平的快速改变使我非常兴奋（*exciting*）。

尽管这个方向在未来也许很有前景（*potential riches*），我并不会在这里向你推销某种特定的研究类型。我个人不持有Twitter, Facebook, Google, Microsoft, Apple或者其他任何科技公司的股份（为了透明，我应该说明，我曾经在Microsoft, Google和Facebook工作过或得到过它们的资助）。因此，在整本书中，我会以一个可信的叙述者的角度，告诉你这些新技术的可能性，同时帮你避开一些其中的陷阱（我见到其他人掉入其中，偶尔我自己也会失足）。

社会科学与数据科学的交叉领域有时会称作计算社会科学（*computational social science*）。有些人认为这是个技术领域，但本书不是传统意义上的工具书。比如，本书的主体内容中不会出现任何的数学公式。我选择这样写是因为我希望为数字时代的社会科学提供一个综合的观点，包括大数据资源，调研，实验，大规模协作以及道德准则。将所有这些主题写在一本书里，同时提供技术细节是不现实的。作为补充，我在每章结尾的“扩展阅读（*What to read next*）”中给出了更多的技术方面的资料。换句话说，这本书不是为了教你某种具体的算法，相反，它是为了改变你对社会研究的思考方式。

### 如何在课程中使用本书

如我之前提到的，本书产生于我从2007开始在普林斯顿大学开设的关于计算社会科学的研究生研讨会中。考虑到你可能会想在课程中使用本书，告诉你本书是如何从我的课程中产生的，以及我如何设想在其他的课程中使用它，也许会对你有所帮助。

这几年来，我开设的这门课程并没有教材，我只是指定一堆论文。当学生仅仅从这些论文中学习时，并没有如我所想产生观念的转变。因此，为了帮助学生看清蓝图，我在课上花费了大量的时间来描述远景，来龙去脉以及指导意见。本书是我以一种无需预备知识的方式，尝试写下所有远景，来龙去脉以及指导意见。

在长为一个学期的课程中，我建议将这本书与各种补充材料一起使用。例如，课程也许会花两周时间在实验上，你可以将相关主题的预备知识与第四章一起使用。如实验的分析与设计；在公司中进行大规模A/B测试时引发的统计与计算的问题；设计一个研究特定机制的实验；使用如Amazon Mechanical Turk这类线上劳动力时带来的操作、理论以及道德准则上的问题。同时，它也应与一些编程相关的阅读与活动搭配使用。具体的搭配需要根据你学生的背景与目标进行适当的选择（如：本科生、研究生或博士生）。

在长为一学期的课程中同样需要每周作业。每章的活动根据难度贴有不同的标签：简单(![dif-easy][dif-easy])，中等(![dif-med][dif-med])，困难(![dif-hard][dif-hard])，极其困难(![dif-hardest][dif-hardest])。同时我给每个问题需要的技能也贴了标签：数学(![math][math])，编程(![code][code])，以及数据收集(![cubes][cubes])。最后我标记了一些我个人最喜欢(![favorite][favorite])的活动。希望这些多样化的活动，可以帮你中找到适合你学生的活动。

为了帮助人们在课程中使用本书，我已经开始整理一些教学资料，例如大纲，幻灯片，推荐的扩展内容，其中包含每个章节以及一些问题的解决方案。你可以在 [http://www.bitbybitbook.com](http://www.bitbybitbook.com) 上找到这些资料或上传你的贡献。

[dif-easy]: https://www.bitbybitbook.com/figures/icons/dif-easy.svg
[dif-med]: https://www.bitbybitbook.com/figures/icons/dif-med.svg
[dif-hard]: https://www.bitbybitbook.com/figures/icons/dif-hard.svg
[dif-hardest]: https://www.bitbybitbook.com/figures/icons/dif-hardest.svg
[math]: https://www.bitbybitbook.com/figures/icons/math.svg
[code]: https://www.bitbybitbook.com/figures/icons/code.svg
[cubes]: https://www.bitbybitbook.com/figures/icons/cubes.svg
[favorite]: https://www.bitbybitbook.com/figures/icons/favorite.svg
