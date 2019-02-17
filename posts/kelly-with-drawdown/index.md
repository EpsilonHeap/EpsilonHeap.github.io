<!--
.. title: Kelly with Drawdown
.. slug: kelly-with-drawdown
.. date: 2019-02-07 20:43:54 UTC
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. has_math: True
-->

# Kelly Gambling

Portfolio management is a pillar of asset management. Given resources and many avenues for allocating said resources, how to allocate so as to achieve a desired effect? With regards to money, more is considered best, and with little chance of losing much would be ideal. Two views have received considerable attention on this topic. One approach is known as '[Modern Portfolio Theory](https://www.investopedia.com/terms/m/modernportfoliotheory.asp)' and the other is '[Kelly Criterion](https://www.investopedia.com/articles/trading/04/091504.asp)'. Warren Buffet [explains](http://undergroundvalue.blogspot.com/2008/02/notes-from-buffett-meeting-2152008_23.html) the difference when asked by students: take advantage of an 'edge' where possible, and seek safety in numbers otherwise.

Modern Portfolio Theory is taught in academia, and Kelly Criterion is mostly a method encountered by those asking 'is there another way?' This article on [Bernoulli](https://ergodicityeconomics.com/2018/02/16/the-trouble-with-bernoulli-1738/#more-3206) and another on [Laplace](https://ergodicityeconomics.com/2017/07/18/doing-a-laplace/#more-102) examine the fundamental difference of the two views and advocates for the Kelly approach. The latter article explains why the Kelly approach is less well known. Incidently, the criterion named after John Kelly is an of application of Claude Shannon's work to gambling - as detailed by [William Poundstone](http://home.williampoundstone.net/Kelly.htm). Yet another area Leo Breiman focused his energy was with ['Optimal Gambling Systems for Favorable Games'](https://projecteuclid.org/euclid.bsmsp/1200512159) where he explored the idea introduced by Kelly. [Thomas Cover](http://www-isl.stanford.edu/~cover/portfolio-theory.html) of information theory fame also examined the subject matter as well.

Enzo Busseti, Ernest Ryu, and [Stephen Boyd](http://web.stanford.edu/~boyd/) (who oversees several areas of exciting research) published '[Risk-Constrained Kelly Gambling](https://arxiv.org/abs/1603.06183)' which derives an approach to incorporate [drawdown](https://www.investopedia.com/terms/d/drawdown.asp) with Kelly gambling. When speaking of risks, drawdown would be top of the list for many - more so when following a Kelly approach. With concentrated positions, the prospects of some big bets going awry would be disastrous whereas a highly diversified portfolio would suffer the same fate as the market as a whole. This paper combines Kelly gambling with risk aversion in a systematic way, and do so by casting the problem as [convex optimization](http://web.stanford.edu/~boyd/cvxbook/).


$$
\begin{array}{cl}
maximize & \mathbb{E}\log({r^\intercal b}) \cr[2ex]
subject \; to & \begin{aligned}
\mathbb{E}(r^\intercal b)^{-\lambda} & \leq 1 \cr
\mathbb{I}^\intercal b & = 1, b \geq 0
\end{aligned}
\end{array}
$$

where \\(r\\) is a matrix of returns for a set of investments, \\(b\\) is a vector of allocations, and \\(r^\intercal b\\) is then the gain in wealth of a portfolio. \\( \mathbb{E}(r^\intercal b)^{-\lambda} \leq 1 \\) will be expanded upon later. This constraint effectively bounds how much risk one is willing to take.

A key result of the paper is that \\( \mathbb{E}(r^\intercal b)^{-\lambda} \leq 1 \Rightarrow \mathbb{Prob}(W^{min} \lt \alpha) \lt \beta\\). That is, the probability \\(W^{min}\\), a random variable of the minimum wealth, of being less that \\(\alpha\\) is less than \\(\beta\\), and is equivalent to the aforementioned 'degree' of risk constraint. A different symbolic way to see the interplay of \\(\alpha, \: \beta, \: and, \: \lambda \\) is \\( \mathbb{Prob}(W^{min} \lt \alpha) \lt \alpha^\lambda = \beta \\) where \\( \lambda = \frac{\log\beta}{\log \alpha} \\).

The paper carefully presents several variations of the Kelly gamble, establishes bounds, and performs a comparative study, but what is highlighted above constitutes the heart of the matter for realistic applications.

---