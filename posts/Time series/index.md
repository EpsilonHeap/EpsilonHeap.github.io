<!--
.. title: Time series
.. slug: Time series
.. date: 2019-02-04 19:34:54 UTC
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. has_math: True
-->

# Time Series

Educated as an Electrical engineer early in life and having more recently worked as a 'quant' for many years, the topic of time series analysis has evolved from a clean one to a bewildering hodgepodge of complications; pretty much all of it because of the stochastic nature of markets.

Some fundamental issues:

 + Transactional - data from markets are records of transactional events and not uniformly sampled; therefore, times series are non-homogeneous.
 
 + Stationarity - market data are not necessarily stationary and often have complicated time-delayed feedback structures. Moreover, change points (or regime shifts) are not uncommon.

 + Ergodicity - practitioners often analyze time series to aid in prediction; but under what condition can the histories of (single realizations of) sampled paths be considered representative of future behavior?

 There are other issues like low signal-to-noise, high dimensionality, missing values, and outliers. Although these are important, the three highlighted undermine the applicability of traditional methods.

---

## Transactional

Traditionally an engineer dealing with signals mainly work with Fourier transforms and related objects.

$$
f(x) = \int_{-\infty}^{\infty} \hat f(\xi) e^{2 \pi i \xi x} d\xi 
$$

Clean and elegant. This formalism is fundamental and will not likely ever diminish in stature. Yet quantitative-minded participants in finance, in particular currency traders of the late 1990's, pointed out a significant characteristics of the data of their trade that needed addressing:
[Operators on Inhomogeneous Time Series](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=208278). A central idea underlying inhomogeneous time series is that 'time' is proportional to the density of 'activity'. With regards to the 'information' content of inhomogeneous market data, this paper ['Discerning Information from Trade Data'](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1989555) describes a aggregated 'tick' or 'bar' approach - essentially integrating pieces of data partitioned by time into informational units for analysis. Aside: a good presentation of the many pitfalls encountered by financial professionals are in Marcos Lopez de Prado's ['Advances in Financial Machine Learning'](https://www.wiley.com/en-us/Advances+in+Financial+Machine+Learning-p-9781119482109). A Jupyter notebook in the blog post ['Exploring Alternative Price Bars'](http://www.blackarbs.com/blog/exploring-alternative-price-bars) illustrates this approach.

---

## Non-Stationary Data

Over an intermediate time-span, market data fluctuate in a relatively well-behaved manner, and statistical observations like mean-reversion are relevant and expected. On a longer time-scale, statistically 'rare' events are not so uncommon in real markets. In other words, statistical models stop making sense when markets go wild - a good indicator that market prices are not necessarily stationary (see [Integration, Cointegration, and Stationarity](https://www.youtube.com/watch?v=Pn_RiDbK82M&t=160s) for examples of non-stationary time series that are rather tame. Beware though that using integer differentiation may remove information content. See chapter 5 of ['Advances in Financial Machine Learning'](https://www.wiley.com/en-us/Advances+in+Financial+Machine+Learning-p-9781119482109) or look up fractional differentiation for financial data.)

<!---
memory effects
-->
Bottom line is that market data needs to be analyzed and transformed before statistical methods are applicable as intended. Then again, many methods of Machine Learning work well in practice without a rigorous understanding of why they work. In any case, a usual suspect for why a model has limited or no predictive ability post construction is because the model was formulated with non-stationary data. Good sites examining fundamental issues in applying scientific theory to economics is [Ergodicity Economics](https://ergodicityeconomics.com/) and to markets is [Quantitative Finance](http://www.quantresearch.info/).

---

## Ergodicity

Equivalence of ensemble-average and time-average with respect to some sampled statistics is an important subject. [Gaveau and Schulman](https://arxiv.org/abs/1401.7224) questioned whether ergodicity is a reasonable hypothesis - many applications only require 'reasonably'-sized samples. An article by [Persi Diaconis](https://statweb.stanford.edu/~cgates/PERSI/papers/mixing.pdf) explore this for practitioners. [Ole Peters](https://www.youtube.com/watch?v=LGqOH3sYmQA) has put forth commendable effort at explaining
the real-world implications of using ensemble quantities when individuals experience but one life. [Nassim Taleb](https://www.youtube.com/watch?v=qA_6BWkC4og) discusses ergodicity from a trader's perspective.

Even though the age of immense computing power and massive data collection is upon us, A better understanding of how many representative examples are enough for a good approximation is more important then ever. Reason being that society is putting more faith than ever into systems trained by examples, whether they are generated (games and such) or collected.

---
