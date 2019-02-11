<!--
.. title: Sparse High-Dimensional Regression
.. slug: sparse-high-dimensional-regression
.. date: 2019-02-11 12:29:47 UTC
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. has_math: True
-->

# What!?

This one falls under the 'mind-bending' category that has initiated a personal re-examination of the whole practice of regression. Bertsimas and Van Parys released ['Sparse High-Dimensional Regression: Exact Scalable Algorithms and Phase Transitions'](https://arxiv.org/abs/1709.10029) upon the world and upended my beliefs. 

[Professor Bertsimas's](http://www.mit.edu/~dbertsim/) [Hotelling lecture](https://www.youtube.com/watch?v=7w9aRrYgGEs) is a good video presentation of his approach to the topic.
\[Note: Optimization is a foundational showcase of the power of computing - pay attention to this field.\] An earlier paper ['Best Subset Selection via a Modern Optimization Lens'](https://arxiv.org/abs/1507.03133) started the buzz and elicited Trevor Hastie, Robert Tibshirani, and Ryan Tibshirani to respond with ['Extended Comparisons of Best Subset Selection, Forward Stepwise Selection, and the Lasso'](https://arxiv.org/abs/1707.08692).

The problem: regression, although very useful, has always had some associated arbitrariness. Leo Brieman's dissatisfaction with the somewhat 'fickle' nature of statistical regression lead him to develop predictive methods based on algorithms rather than statistical models. One of Brieman's [Wald Lecture](https://www.stat.berkeley.edu/~breiman/wald2002-2.pdf) describes the state of affairs that motivated his work. For instance, given the same data, practitioners would arrive at a multitude of different models with different predictor variables that should have similar predictive abilities. The problem was not with the skills of those doing the analysis (page 11 of lecture) but with the method itself. Bertsimas and Van Parys suggest that a more 'exact' approach could be at hand.

---

# Mixed Integer Optimization (MIO)

Loosely stated, MIO has been shown in practice to be highly efficient and effective in regularizing to the zero norm of a regression model; finding the support of the variables under selection. In theory, this should be a daunting prospect (NP-Complete) and rather hopeless for very high dimensional problems. This paper shows otherwise and hints at some sort of phase-transition taking place. Phase-transitions are typically associated with the universal behavior of matter in different phases undergoing a competition to reach stability near what are known as 'critical' points where both phases co-exist - again loosely stated.

MIO are mysterious to me and begs for study. What could constitute the two-phases (duality is two faces of the same problem)? What exactly are the mechanisms of MIO?

...

---