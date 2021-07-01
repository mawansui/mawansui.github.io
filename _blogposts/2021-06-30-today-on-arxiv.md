---
title: "Today on arXiv (#1)"
collection: blogposts
permalink: /blog/2021-06-30-today-on-arxiv
excerpt: 'Recent intriguing pre-prints on arXiv: using ensembles of graph neural networks, making transformers geometry-aware, learning potentials from simulations data, and more!'
date: 2021-06-30
read_time: true
---

Hello! This post starts a series of short notes that aim at providing you with a (hopefully) daily overview of recently posted arXiv.org pre-prints, in some way related to chemoinformatics. The idea is to give a quick description of an interesting paper so that a curious reader could read it further – or suggest it for a detailed review in this blog. Please note that the short summaries I provide under each article are based on a brief examination of the article text and are prone to errors, though I try to make them as correct as possible. Thank you for your understanding.

So, here are some recent arXiv picks (circa 30.06.2021):

- [__On Graph Neural Network Ensembles for Large-Scale Molecular Property  Prediction__](http://arxiv.org/abs/2106.15529v1) (Kosasih et al.; 29.06.2021).

  <u>My short summary</u>: Machine learning on graphs is the new hot topic, but many recent papers test some new approaches on small synthetic datasets. The Open Graph Benchmark Large-Scale Challenge was suggested as an alternative approach to testing new methodologies. The challenge offered a dataset of ~3.8 million SMILES with their respective calculated HOMO-LUMO gap values, useful to study "reactivity, photo-chemical or photo-physical molecule properties". These values were calculated using slow DFT calculations, and the idea was to train a graph neural network (GNN) to predict this gap and avoid slow calculations. The authors of this arXiv pick trained an ensemble of graph neural networks and beat the baseline model by 7%.
  
- [__Geometry-aware Transformer for molecular property prediction__](http://arxiv.org/abs/2106.15516v1) (Kwak et al.; 29.06.2021)

  <u>My short summary</u>: using graph neural networks on molecular data is fun and all, but the implied limitation of aggregating the node values over some close neighboring environment is counter-intuitive: in chemistry, it is believed that long-range interactions between atoms are as important as close-range ones. The authors of this arXiv pick suggest a geometry-aware transformer model which they claim to be able to capture these interactions, hence increasing the predictive performance of the models.
  
- [__A Mechanism for Producing Aligned Latent Spaces with Autoencoders__](http://arxiv.org/abs/2106.15456v1) (Jain et al.; 29.06.2021)

  <U>My short summary</u>: Autoencoders are a special kind of neural networks that can learn a latent space representation of the input data space – meaning they can learn "vector spaces that capture similarity
between data points". In some vector spaces, it becomes possible to visually see some alignment in the input data: e.g., an autoencoder can visualize the fact that the words "sure" and "unsure" are antonyms, or have distinctly different latent vectors. Turns out, it is also possible to do something similar with the gene expression data. The authors of this arXiv pick prove that it is possible to direct the training of the autoencoders in such a way that allows for better latent space aligning, hence – better predictive performance of the models.

- [__GraphPiece: Efficiently Generating High-Quality Molecular Graph with Substructures__](http://arxiv.org/abs/2106.15098v1) (Kong et al.; 29.06.2021)

  <u>My short summary</u>: Generating new molecules is extremely cool, especially when you can do so to get some structure with the desired property. One of the approaches to molecule generation is to construct the new compounds atom-by-atom. Frankly, it's not the best, as it takes too much computational time and sometimes ignores the fact that often it's not the individual atom, but a whole substructural fragment that is responsible for a desired molecular property. In this work, the authors of this arXiv pick first train a model to extract these important substructures from available molecular data and then use the trained models to efficiently construct new molecules in a substructure-aware fashion.
  
- [__PFP: Universal Neural Network Potential for Material Discovery__](http://arxiv.org/abs/2106.14583v1) (Takamoto et al.; 28.06.2021)

  <u>My short summary</u>: When developing new materials, it is very common to rely on atomistic simulations. Some of the simulation methods are based on thorough theory, but are not fit to be scaled up to model complex systems and are rather slow. Other methods use more or less empirically pre-defined potentials to perform the modeling, but these potentials are often suited to study a limited number of compound classes. The authors of this arXiv pick claim to have used neural networks to learn the potentials from available simulations datasets, and used these potentials to sufficiently well model the behaviour of a wide range of other chemical systems.

- [__Inferring a Continuous Distribution of Atom Coordinates from Cryo-EM Images using VAEs__](http://arxiv.org/abs/2106.14108v1) (Rosenbaum et al.; 26.09.2021)

  <u>My short summary</u>: Proteins are essential macromolecules that perform lots of important functions in living organisms and cells. We can largely benefit from modulating proteins' behaviour, but for this we need to know their structures. One of the protein structure determination techniques is called cryo-EM. In brief, this method makes it possible to take a noisy image of the electron cloud surrounding the protein, and then infer the structural information from this low-scale image. While it's a breakthrough in itself, it can only reconstruct one protein conformation. However, some proteins have very labile regions, and thus it would have been great to infer not one, but a multitude of protein conformations from the cryo-EM experimental images. The authors of this arXiv pick used some variational autoencoders to do exactly that. Albeit they were only able to demonstrate moderate performance on a simulated dataset, there are still hopes that the approach could be further improved and used on real-life cryo-EM data.
  
  
That's it for today's arXiv picks! Did you like the list? Would you like me to give a more detailed examination of some of them? Let me know on [Medium](https://medium.com/chemoinformatics), [Twitter](https://twitter.com/mdshev7) or [Instagram](https://www.instagram.com/chemoinfo/). I will also add the comments section to this blog soon. Thank you for your kind attention and feedback. See you next time. Cheers!
