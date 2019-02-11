<!--
.. title: Statistical Thinking and Uncertainty in the Age of Computers
.. slug: statistical-thinking-and-uncertainty-in-the-age-of-computers
.. date: 2019-02-06 19:55:36 UTC
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. has_math: True
-->

# Historical Context

Current approaches to Data Science, Machine Learning, Artificial Intelligence, and so on ... basically deal with statistical distributions in high dimensions that are shaped by the algorithms and models used to operate upon and represent data, respectively.  This modern view was adopted by [Leo Breiman](https://www.google.com/url?q=https%3A%2F%2Fwww.stat.berkeley.edu%2Fusers%2Fbreiman%2F&sa=D) as  fundamental to his approach to Statistics and is clearly described in '[Statistical Modeling: The Two Cultures](https://www.google.com/url?q=https%3A%2F%2Fprojecteuclid.org%2Feuclid.ss%2F1009213726&sa=D)'.

Rewinding yet further, a watershed period in applied statistical and probabilistic thinking was perhaps defined by the work of [Henri Poincaré](https://www.google.com/url?q=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FHenri_Poincar%25C3%25A9&sa=D) and [Ludwig Boltzmann](https://www.google.com/url?q=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FLudwig_Boltzmann&sa=D). Games of chance or gambling paved the way for Probability and Statistics - start with uncertainty because determinism was beyond our calculations; however, at that time, the prevailing fundamental 'truth' was that the world is deterministic. Boltzmann changed that notion. He challenged the established Physics community with an 'atomic' view of the world which rendered determinism as a facade. The sheer magnitude of the numbers involved dictated a fundamentally statistical view of the world. Poincaré made the shift even more compelling by showing that even a formal description of a few components is rather hopeless. Instead, analysis of the characteristics of an 'ensemble' was powerful, revealing, and useful.

Hopefully, another watershed moment is near as a product of the 'Computer Age'. In the meantime, studying the nature of uncertainty in high dimensions  seems rather important. Note that the previous sentence is composed of many vague terms; why not just say 'probability distributions' or such? The matter is one of perspective. Freeing the mind from a strictly probability measure view of uncertainty is more 'fun' - so to say.  For instance, [fuzzy sets](https://www.google.com/url?q=http%3A%2F%2Fsipi.usc.edu%2F~mendel%2F&sa=D) allow for subjective uncertainty of an objective value, and [Bayesian nonparametrics](https://www.google.com/url?q=http%3A%2F%2Fwww.tamarabroderick.com%2Ftutorial_2016_mlss_cadiz.html&sa=D) deal with open-ended inference where measures do not necessarily integrate to 1 (see videos [II](https://www.youtube.com/watch?v=yfLoxwjCGNY) and [III](https://www.youtube.com/watch?v=2H2n4iUYpZE) in particular.) Implementation of methods like MCMC, variational Bayesian methods, ... suggest that likelihood is, in a computational sense, more important than probability distributions. The former is a mechanism for making decisions, and the latter is an object for book keeping. An important point to  keep in mind though is that the concept of normalization is paramount in the context of emergent patterns with respect to scaling. Basically, there is no need to shoehorn everything into a probability measure.

\[Note: '[Computer Age Statistical Inference](https://www.google.com/url?q=https%3A%2F%2Fweb.stanford.edu%2F~hastie%2FCASI%2F&sa=D)' by Bradly Efron and Trevor Hastie certainly influenced the title of this page.\]


<!-- 
Steins's Method
Concentration of Measure
Optimal Transport
Statistical Physics

http://www.hawking.org.uk/does-god-play-dice.html
Bayes
Bradley Efron and Trevor Hastie, '[Computer Age Statistical Inference](https://www.google.com/url?q=https%3A%2F%2Fweb.stanford.edu%2F~hastie%2FCASI%2F&sa=D)' 
-->