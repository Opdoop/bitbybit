# 数学原理简介
本篇附录中，我将用稍微数学一点的形式介绍本章出现的一些思想。希望你能熟悉这些记号和数学框架，以便你平缓的转移到更专业的资料上。我将从概率抽样开始，然后是有无响应的概率抽样，最后是非概率抽样。

## 概率抽样
假想我们的目标是估测美国的失业率。我们来定义 $U = \{1,...,k,...,N\}$ 为目标人群，定义 $y_k$ 为第 $k$ 个人的输出值。这个例子中 $y_k$ 代表第 $k$ 个人是否失业。最后，让我们定义 $F=\{1,...,k,...,N\}$ 为框内人群，为了简化，我们假设框内人群与目标人群一样。

一个基本的抽样，是有放回的随机抽取。在这个例子中，每个人在样本 $s=\{1,...,i,...,n\} 内的概率都是相等的。用这种方式收集好数据后，研究者可以通过简单的计算样本的平均失业率：

$$ \hat{\bar{y}} = \frac{ \sum_{i\in{s}} {y_i} }{n} \quad (3.1) $$

其中 $\bar{y}$ 代表人群的平均失业率，$\hat{\bar{y}}$ 代表估测的平均失业率（$\hat{}$ 常常用来表示估计量）。

实际上，研究者很少用有放回的随机抽样。原因有很多，样本被抽到的概率常常不同。比如说，也许抽取到佛罗里达人的概率比加利福尼亚人的概率要高。在这个情况下，样本的平均值（公式 3.1）也许就不是一个好的指标。相反的，当样本抽到的概率不同时，研究者会用：

$$ \hat{\bar{y}} = \frac{1}{N} \sum_{i\in{S}} \frac{y_i}{\pi_{i}} \quad (3.2)$$

其中 $\hat{\bar{y}}$ 表示预测的失业率，$\pi_i$ 表示第 $i$ 个人被抽到的概率。根据标准的做法，我们称公式 3.2 为「Horvitz-Thompson estimator」。这个值非常有用，因为它将任意的抽样设计都转化为无偏估计（[Horvitz and Thompson 1952](https://doi.org/10.1080/01621459.1952.10483446)）。因为「Horvitz-Thompson estimator」很常见，所以了解它另一个写法也很有帮助：

$$ \hat{\bar{y}} = \frac{1}{N} \sum_{i\in{S}} w_i y_i \quad (3.3) $$

其中 $w_i = 1/\pi_i$。如同公式 3.3 所示，「Horvitz-Thompson estimator」是样本的加权平均值， 权重是它被抽取概率的倒数。也是说，这个人被抽到的概率越小，他在估计量中的权重就越大。

之前提到的，又是研究者的抽样中，样本被抽到的概率是不同的。「stratified sampling」（分层抽样）就是其中的一种。由于它与「post-stratification」事后分层关系紧密，所以我们先来理解一下分层抽样。在分层抽样中，研究者将目标人群分为 $H$ 个互斥组。这些组被称作「strate」（阶层），用 $U_1,...,U_h,...U_H$ 表示。在我们的例子中，这里的阶层是行政区化。每个组的大小用 $N_1,...,N_h,...,N_H$ 表示。使研究者选用分层抽样，也许是为了确保每个州里都有足够的样本来估测这个州的失业情况。

将人群分层后，假设研究者使用简单的有放回的方式，对州 $h$ ，抽取 $n_h$ 个样本。并且，假设每个被抽到的人都会参与实验（在下一节再考虑有无响应的情况）。这时候，有效样本的概率是：

$$ \pi_i = \frac{n_h}{N_h} \: for \: all \: i \in h \quad (3.4) $$

因为每个人的概率都可能不同，所以要用「Horvitz-Thompson estimator」的加权平均（公式 3.2）。

即使「Horvitz-Thompson estimator」是无偏估计，但结合「auxiliary information」（辅助信息），研究者可以得到更准确，方差更小的估计。有时，即使完美的执行了概率抽样，使用辅助信息有帮助。这个方法尤其重要，因为辅助信息对于从有无响应情况的概率抽样和从非概率抽样进行预测十分关键。

一种常见的使用辅助信息的方法是「post-stratification」（事后分层）。比如说，研究者知道这 50 个州分别有多少男性和女性。为了结合这个辅助信息，我们将样本分为 $H$ 个组，在这个例子中是 100 。我们用 $N_1,N_2,...N_{100}$ 表示这个组的大小。我们可以对每个组进行估计，然后计算所以组的加权平均在：
$$ \hat{\bar{y}}_{post} = \sum_{h \in H} \frac{N_h}{N} \hat{\bar{y}}_h \quad (3.5) $$

粗略的说，由于公式 3.5 使用了已知信息 $H_h$，因此可以修正潜在的抽样数量的偏差。

总的来说，这节介绍了一些抽样方法：有放回的随机抽样，非等概率抽样，以及分层抽样。同时还介绍了两个估计中的思想：「Horvitz-Thompson estimator」和事后分层。更多概率抽样的正式定义，见 [Särndal, Swensson, and Wretman (2003)](https://www.springer.com/us/book/9780387406206) 的第二章。完整的分层抽样的介绍，见 [Särndal, Swensson, and Wretman (2003)](https://www.springer.com/us/book/9780387406206) 的 3.7节。有关「Horvitz-Thompson estimator」性质的介绍，见 [Horvitz and Thompson (1952)](https://doi.org/10.1080/01621459.1952.10483446)，[Overton and Stehman (1995)](https://doi.org/10.2307/2684196)。更多事后分层的正式介绍，见 [Holt and Smith (1979)](https://doi.org/10.2307/2344652)，[Smith (1991)](https://doi.org/10.2307/2348284)，[Little (1993)](https://doi.org/10.2307/2290792)，或者 [Särndal, Swensson, and Wretman (2003)](https://www.springer.com/us/book/9780387406206) 的 7.6节。

## 有无响应的概率抽样
实际中，几乎所有的调查都有无响应情况，这是说，不是所有的样本人群都会回答所有的问题。无响应主要有两种：「item nonresponse」和「unit nonresponse」（分项无响应 和 个体无响应）。在分享无响应中，有些受访者对于一些问题拒绝回答，比如，他们拒绝回答对他来说敏感问题。在个体无响应中，有些样本人群中受访者对调查无响应。个体无响应的常见原因有两个，无法联系到这个人，或者联系到了这个人，但他拒绝参加调查。在本节中，我关注于个体无响应；对分享无响应的读者，可以阅读 Little and Rubin ([2002](https://www.wiley.com/en-us/Statistical+Analysis+with+Missing+Data%2C+2nd+Edition-p-9780471183860))

对于有个体无响应的调查，研究者通常将抽样过程看作有两个阶段。第一个阶段中，研究者以概率 $\pi_i$ （$0<\pi_i\leqslant1$) 进行抽样。接着，第二个阶段中，样本以 $\phi_i$ （$0<\phi_i\leqslant1$) 的概率对调查进行响应。这两个劫夺后，得到了最终的参与者 $r$ 。这两个阶段中很重要的不同点是，研究者可以控制第一个阶段，但他们不能控制第二个阶段。将这两个阶段结合，得到某人成为受访者的概率是：

$$ pr(i \in r) = \pi_i \phi_i \quad (3.6) $$

为了简化问题，我们先考虑使用简单的有放回随机抽样的情况。如果研究者抽了 $n_s$ 个样本，得到了 $n_r$ 个受访者，并且忽略无响应者，直接用受访者的均值作为估计值，那么这个估计的偏差就是：

$$ bias \: of \: sample \: mean = \frac{cor(\phi,y)S(y)S(\phi)}{\bar{\phi}} \quad (3.7) $$

其中 $cor(\phi,y)$ 是参与者的偏好与结果——失业状态的相关系数，$S(y)$ 是结果的标准差，$S(\phi)$ 是受访者偏好的标准差，$\bar{\phi}$ 是受访者偏好的平均值（[Bethlehem, Cobben, and Schouten 2011, sec. 2.2.4](https://www.wiley.com/en-us/Handbook+of+Nonresponse+in+Household+Surveys-p-9780470542798)）

公式 3.7 表明，当以下任意一种情况满足时，无响应就不会引入误差：
* 受访者的失业状态没有方差：$S(y) = 0$
* 受访者的偏好没有方差：$S(\phi) = 0$
* 受访者的偏好与其是失业状态见没有关联关：$cor(\phi,y) = 0$

然而，没有一个条件看上去可以满足。如果说受访者的失业状态没有方差，或是受访者的偏好没有方差，都令人难以置信。因此，公式 3.7 的关键就是关联性：$cor(\phi,y)$。也就是说，如果失业者更倾向于参加调查，那么失业率将会向上偏差。

解决无响应问题的关键是使用辅助信息。比如事后分层就是一种使用辅助信息的方式（回想上面的公式 3.5）。事后分层的估计量的偏差可以写作：

$$ bias(\hat{\bar{y}}_post) = \frac{1}{N} \sum_{h=1}^H \frac{N_h cor(\phi,y)^{(h)} S(y)^{(h)} S(\phi)^{(h)}}{\bar{\phi}^{(h)}} \quad (3.8)$$

其中 $cor(\phi,y)^{(h)}, S(y)^{(h)}, S(\phi)^{(h)}$ 和 $\bar{\phi}^{(h)}$ 的定义与上面相同，但限制为第 $h$ 个组的人（[Bethlehem, Cobben, and Schouten 2011, sec. 8.2.1](https://www.wiley.com/en-us/Handbook+of+Nonresponse+in+Household+Surveys-p-9780470542798)）。因此，如果每个分组的误差比较小的画，那总体误差就会比较小。我认为有两种方式可以降低魅族的偏差。首先，你可以尝试构建同质性高的组，这样他们的偏好差异就会很小，$S(\phi)^{(h)}\approx 0$ 并且结果的差异也会更小 $S(\phi)^{(h)}\approx 0$ 。其次，尝试构建对各种人抽到概率相近的组，$cor(\phi,y)^{(h)} \approx 0$。通过比较公式 3.7 和公式 3.8 可以清晰的到事后分层较少无响应误差的条件。

总的来说，本节介绍了随机抽样中无响应带来的误差，以及用事后分层的方式调节误差。[Bethlehem (1988)](http://www.jos.nu/Articles/abstract.asp?article=43251) 提供了更通用的抽样方式中有无响应引起的各种复查。对于使用事后分层调节无响应情况，见 [Smith (1991)](https://doi.org/10.2307/2348284) 和 [Gelman and Carlin (2002)](https://www.researchgate.net/publication/2816095_Poststratification_and_Weighting_Adjustments) 。事后分层属于「calibration estimator」（估计量校准）的一部分，更多有关介绍见 [Zhang (2000)](https://doi.org/10.1080/00031305.2000.10474542) 和 [Särndal and Lundström (2005)](https://www.wiley.com/en-us/Estimation+in+Surveys+with+Nonresponse-p-9780470011331)。一些其他的对无响应问题的调节方式，见 [Kalton and Flores-Cervantes (2003)](http://www.jos.nu/articles/abstract.asp?article=192081), [Brick (2013)](https://doi.org/10.2478/jos-2013-0026) 和 [Särndal and Lundström (2005)](https://www.wiley.com/en-us/Estimation+in+Surveys+with+Nonresponse-p-9780470011331) 。

## 非概率抽样
非概率抽样有各种方式（[Baker et al. 2013](https://doi.org/10.1093/jssam/smt008)）。Wang 与其同事们对 Xbox 用户使用的非概率抽样，见 [W.wang et al. 2015](https://doi.org/10.1016/j.ijforecast.2014.06.001)。你可以认为，这种抽样所关注的不是 $\pi_i$ 而是 $\phi_i$。当然，这并不是什么理想的方式，因为 $\phi_i$ 并不确定。但是，Wang 的工作说明，即使样本中存在巨大的覆盖误差，通过使用合适的辅助信息以及合适的统计学模型，研究者可以解决这些问题。

[Bethlehem (2010)](https://doi.org/10.1111/j.1751-5823.2010.00112.x) 中扩展了更多使用事后分层解决无响应与覆盖误差的例子。除了事后分层，还有一些其他的方法可以解决概率抽样和非概率抽样中的覆盖误差与无响应问题，包括「sample matching」样本匹配（[Ansolabehere and Riers 2013](https://doi.org/10.1146/annurev-polisci-022811-160625)），「propensity score weighting」倾向评分的加权分析法（[Lee 2006](http://www.jos.nu/Articles/abstract.asp?article=222329); [Schonlau et al. 2009](https://doi.org/10.1177/0049124108327128)），以及「calibration」校准（[Lee and Valliant 2009](https://doi.org/10.1177/0049124108329643)。这些方法存在共同的主题：使用辅助信息。
