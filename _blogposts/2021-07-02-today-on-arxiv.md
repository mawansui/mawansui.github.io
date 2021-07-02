---
title: "Today on arXiv (#2)"
collection: blogposts
permalink: /blog/2021-07-02-today-on-arxiv
excerpt: "Recent intriguing pre-prints on arXiv: NLP in biomedical data, a dataset of quantum properties for drug-like molecules, a neural network that replaces DFT methods, and a new optimization method for VAE generation."
date: 2021-07-02
read_time: true
---

Hi! Today, I invite you to discuss some of the recent arXiv preprints:

- [__Multimodal Graph-based Transformer Framework for Biomedical Relation  Extraction__](http://arxiv.org/abs/2107.00596v1) (Pingali et al.; submitted 01.07.2021).

  <u>My short summary</u>: Nowadays, scientists have access to a large corpus of biomedical publications' texts. It seems promising to use this data to extract some meaningful information, for example – knowledge on protein-protein interactions. There already are some approaches to do so, but their vast majority deals with only textual interaction within a set of sentences, ignoring the chemical structure data of the mentioned proteins. In this work, the authors complement the textual information graph with protein structure information. This way, they infer the protein-protein interaction not only basing on the fact of two proteins being present in the same sentence, but also thanks to learned protein structure interrelations.
  
- [__QMugs: Quantum Mechanical Properties of Drug-like Molecules__](http://arxiv.org/abs/2107.00367v1) (Isert et al.; submitted 01.07.2020).

  <u>My short summary</u>: This new preprint from the Gisbert Schneider group announces the release of `QMugs` - and open-access dataset of quantum-mechanical (QM) properties of druglike molecules. It has ~665k structures extracted from ChEMBL, each with already computed QM properties such as "single-point electronic properties, quantum mechanical wave
functions and density-functional theory (DFT) matrices". The authors reason that this dataset could be used as an alternative to conventional databases used for machine learning in chemoinformatics.


- [__OrbNet Denali: A machine learning potential for biological and organic chemistry with semi-empirical cost and DFT accuracy__](http://arxiv.org/abs/2107.00299v1) (Christensen et al.; submitted 01.07.2021).

  <u>My short summary</u>: The authors of this preprint report the development of `OrbNet Denali`: a neural network that predicts a molecule's energy using features from a low-cost quantum calculation. They claim that their method, trained "on a vast dataset of 2.3 million DFT calculations", produces results that are "on par with modern DFT methods while offering a speedup of up to three orders of magnitude".


- [__Improving black-box optimization in VAE latent space using decoder uncertainty__](http://arxiv.org/abs/2107.00096v1) (Notin et al.; submitted 30.06.2020).

  <u>My short summary</u>: Generative autoencoder models, such as vartiational autoencoders, generate new objects by sampling latent space around the latent vector of the input object (e.g., molecule). Sometimes, they tend to sample from regions of latent space which the decoder part doesn't really know how to interpret, leading to incorrect output. The authors of this paper suggest an approach to direct the sampling towards the regions of the latent space that could be reliably reconstructed.


  
That's all for today's arXiv picks! Did you like the list? Would you like me to give a more detailed examination of some of them? Let me know on [Medium](https://medium.com/chemoinformatics), [Twitter](https://twitter.com/mdshev7) or [Instagram](https://www.instagram.com/chemoinfo/).

Thank you for your kind attention and feedback. See you next time. Cheers!
