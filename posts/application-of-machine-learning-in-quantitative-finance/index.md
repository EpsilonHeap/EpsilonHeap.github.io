<!--
.. title: Application of Machine Learning in Quantitative Finance
.. slug: application-of-machine-learning-in-quantitative-finance
.. date: 2019-06-12 19:18:53 UTC
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. has_math: True
-->

---
# Two Worlds Colliding

Markets are noisy and ever changing; moreover, fluctuations can be rather large and persistent. The nature and character of markets offer significant challenges for machine learning (ML) algorithms. For instance:

* low signal-to-noise
    * 'signals' that convey information about markets are often highly obscured by 'noise'.
    * ML algorithms are designed to recognize or approximate patterns that are the most prevalent, and market are mostly noise.
* regime changes
    * markets are constantly evolving, fluctuations can be large, and statistical characteristics can change quickly.
    * current ML algorithms are specialists that do not handle outliers and new situations well.
* market inferences should be robust
    * 'signals' are not useful for market predictions if slight differences in what is observed lead to very different predictions.
    * some ML methods are brittle - see [video](https://www.youtube.com/watch?v=Yr1mOzC93xs) and [paper](https://arxiv.org/abs/1711.11561) by Bengio - and small difference in input lead to notably different predictions.
  
Recognition of the conflicting nature of markets and the current crop of ML algorithms is important in devising new approaches to using the ideas learned from ML in quantitative finance.

Emphasis here is on introducing the powerful, foundational ideas of ML to the design of trading algorithms as oppose to using existing ML methods as tools for trading. Or as [Steve Jobs](https://www.youtube.com/watch?v=CW0DUg63lqU) famously quoted of Picasso in an interview: “good artists borrow, great artists steal.”

# Ideas That Transcend
What ideas are considered great and transcend boundaries are to some degree subjective. Nevertheless, the following ideas from ML are at least worthy of consideration.

    1) Regularization of complexity as part of the learning process.
    2) Boosting a set of weak learners into a single strong learner.
    3) Stochastic gradient descent to drive exploration.

There are more but these are enough to form the foundation of a trading algorithm with desirable properties. The missing pieces are a model and the data structure(s) to represent the model, a decision mechanism to establish what is 'better', and a set of features.

The adage that, given a set of relevant features that span the distinguishing properties of the patterns of interest, just about any machine learning algorithm will perform well is not far from the truth. However, in the context of trading signals for markets though, these features will be very noisy, their relevance may be fleeting, yet they need to be robust. 'Quants' who have applied ML methods to trading will attest to significant impact of these problems. A trading algorithm would likely be well-served by addressing these inherent characteristics of trading signals.

Domain expertise is important for trading. End-to-end techniques like Deep Neural Nets may someday 'crack' the code and derive effective representations that are also interpretable. Meanwhile, developing methods that incorporate existing understanding of market behavior is the goal. A major assumption is the availability of a set of 'weak' features in the sense described above.

# Restate Again

Let's match what machine learning has to offer to the difficulties that need to be addressed.

Regularization can be interpreted in several ways. A useful view is that regularization is used to distinguish 'noise' from 'signal' with regards to the weights parameterizing a family of models under consideration. 'Signal' weights should be much larger than 'noise' weights. Something like regularization is needed for trading features.

[TBD ...]
