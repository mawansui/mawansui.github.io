---
title: "Today on arXiv (#1.1)"
collection: blogposts
permalink: /blog/2021-07-01-today-on-arxiv
excerpt: "Recent intriguing pre-prints on arXiv: learning to quickly model the ionic liquids and pre-processing existing graphs to increase the models' predictive performace."
date: 2021-07-01
read_time: true
---

Hello! Let us indulge in some most recent chemoinformatics-related arXiv picks:

- [__A Differentiable Neural-Network Force Field for Ionic Liquids__](http://arxiv.org/abs/2106.16220v1) (Montes-Campos et al.; published 30.06.2021).

  <u>My short summary</u>: Ionic liquids are a very promising class of mixtures with potential applications as powerful green solvents or electrolytes. There are billions of ion combinations that could be used to create such mixtures. How do we select the best ones? Well, definitely not but brute-force experimentation! Scientists use molecular dynamics simulations to model the behaviour of such ionic systems, thus selecting the most promising compositions for further experimental validation. However, these simulations are either extremely slow or not really precise. To speed this whole process up, the authors of this work used a neural network to learn the way compounds in ionic liquids interact with each other from pre-existing molecular dynamics simulations. Then they demonstrate the performance of the trained network by quickly and accurately modeling the ethylammonium nitrate system on par with more complicated and resource-consuming methods.
  
- [__Edge Proposal Sets for Link Prediction__](http://arxiv.org/abs/2106.15810v1) (Singh et al.; published 30.06.2021).

  <u>My short summary</u>: A graph is a very useful data type, utilized to describe interactions between many elements in complex systems (e.g., protein-protein interactions). One thing you could do with a graph is to train a predictive model that could predict whether or not two elements (nodes) should have an interconnection (an edge between them). It is a fairly complicated task, because training set graphs often have missing or incorrect edges, which significantly lowers the predictive performances of the models. The authors of this work suggest that adding <i>per se</i> non-existent edges between nodes in the original graph input (a so-called proposal set of edges) may guide the common algorithms to a direction of better decisions if the edges follow the general structure of the graph. Benchmarking shows that adding the proposed edge sets increases the performance of link-prediction models.
  
  
That's all for today's arXiv picks! Did you like the list? Would you like me to give a more detailed examination of some of them? Let me know on [Medium](https://medium.com/chemoinformatics), [Twitter](https://twitter.com/mdshev7) or [Instagram](https://www.instagram.com/chemoinfo/). The comment section will also come to this blog soon. 

Thank you for your kind attention and feedback. See you next time. Cheers!
