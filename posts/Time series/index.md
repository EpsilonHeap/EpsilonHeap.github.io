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

Some fudamental issues:

 + Transactional - data from markets are records of transactional events and not uniformaly sampled; therefore, times series are non-homogeneous.
 
 + Stationarity - market data are not necesarily stationary and often have complicated time-delayed feedback structures. Moreover, change points (or regime shfits) are not uncommon.

 + Ergodicity - practioners often analyze time series to aid in prediction; but under what condition can the histories of sampled paths be considered representative of future behavior?

 There are other issues like low signal-to-noise, high-dimensionality, and outliers -- these are more generic problems though.

---

Traditionally an engineer dealing with signals mainly work with Fourier transforms and related objects.

$$
f(x) = \int_{-\infty}^{\infty} \hat f(\xi) e^{2 \pi i \xi x} d\xi 
$$

Clean and elegant. This formalism is fundamental and will not likely ever diminish in stature.

