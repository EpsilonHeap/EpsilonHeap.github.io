<!--
.. title: Ensemble Trees
.. slug: ensemble-trees
.. date: 2019-02-14 16:35:13 UTC
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. has_math: True
-->

# Chasing the Deep End
Deep this, deep that; not that there is anything wrong with that. Why? because deep neural-networks (now being referred to as [differential programming](https://www.facebook.com/yann.lecun/posts/10155003011462143) by one of its pioneers) is one of milestone advancements in ML/AI and have many applications. So generally powerful and useful that it is now a fundamental design component for higher-level systems tailored for specific domains (see [Stanford lecture](https://www.youtube.com/watch?v=QuELiw8tbx8) and [Deep Learning School presentation](https://www.youtube.com/watch?v=oGk1v1jQITw) by [Richard Sochar](https://www.socher.org/)). As an electrical engineer by academic title, this systems approach is comfortably familiar, very much like circuits design.

Another 'component' that has been very useful, powerful, and efficient falls under the category of ensemble trees - especially the [boosting](https://en.wikipedia.org/wiki/Gradient_boosting) variant. In a sense, ensemble trees are both deep and wide. The number of tree layers control depth versus breath, and an ensemble overlay offer wide exploration of features and relationships to observed outcomes. Yet more 'deepness' could be had by employing a component approach where elements are wired together.

Table 10.1 of ['The Elements of Statistical Learning'](https://web.stanford.edu/~hastie/ElemStatLearn/) compares trees-based methods to some contemporaries. Although much progress has been been made since its publication, most of the characterizations still hold. In particular, efficiency, forbearance with regards to feature data, and interpretability are outstanding advantages. 

# Results and Insights

 These qualities are differentiators where decisions are costly in terms of the cost of doing experiments, collecting data, and unsatisfactory consequences. Of course, mistakes are unavoidable and tree-base methods are typically less accurate, but being clueless about why something works or fails can be a [no go](https://www.risk.net/asset-management/6119616/blackrock-shelves-unexplainable-ai-liquidity-models) - you cannot learn from your mistakes. For medical use, a lack of reasoning is not comforting. In a research setting, gaining insights from interpretable models are more useful than raw accuracy. Tree-based methods can also be applied early on as part of a systematic application of data science - they are good at taking available data without much preprocessing and identifying influential features. They are fast and relatively easy to use.

# Building on a Good Idea

Ensembles, tree-based models, bagging, and boosting make for great companions. Some nifty variants on this combinations are:

1. Random Forests
1. Xgboost
2. Catboost
3. mboost
4. gamboostLSS

[annotate later]

---
