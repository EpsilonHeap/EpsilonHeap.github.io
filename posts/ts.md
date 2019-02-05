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

Educated as an Electrical engineer early in life and having more recently worked as a 'quant' for many years,the topic of time series analysis has evolved from a clean one to a bewildering hodgepodge of complications.

Some fundamental issues:

 + Transactional - data from markets are records of transactional events and not uniformly sampled; therefore, times series are non-homogeneous.
 
 + Stationarity - market data are not necessarily stationary and often have complicated time-delayed feedback structures. Moreover, change points (or regime shifts) are not uncommon.

 + Ergodicity - practitioners often analyze time series to aid in prediction; but under what condition can the histories of (single realizations of)sampled paths be considered representative of future behavior?

 There are other issues like low signal-to-noise, high dimensionality, missing values, and outliers. Although these are important, the three highlighted undermine the applicability of traditional methods.

---

## Transactional

Traditionally an engineer dealing with signals mainly work with Fourier transforms and related objects.

$$
f(x) = \int_{-\infty}^{\infty} \hat f(\xi) e^{2 \pi i \xi x} d\xi 
$$

Clean and elegant. This formalism is fundamental and will not likely ever diminish in stature. Yet quantitative-minded participants in finance, in particular currency traders of the late 1990's, pointed out a significant characteristics of the data of their trade that needed addressing:
[Operators on Inhomogeneous Time Series](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=208278). A central idea underlying inhomogeneous time series is that 'time' is proportional to the density of 'activity'. With regards to the 'information' content of inhomogeneous market data, this paper ['Discerning Information from Trade Data'](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1989555) describes a aggregated 'tick' or 'bar' approach - essentially integrating pieces of data partitioned by time into informational units for analysis. Aside: a good presentation of the many pitfalls encountered by financial professionals are in Marcos Lopez de Prado's ['Advances in Financial Machine Learning'](https://www.wiley.com/en-us/Advances+in+Financial+Machine+Learning-p-9781119482109). A Jupyter notebook in the blog post ['Exploring Alternative Price Bars'](http://www.blackarbs.com/blog/exploring-alternative-price-bars) illustrates this approach.

