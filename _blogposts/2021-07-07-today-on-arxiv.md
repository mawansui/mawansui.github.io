---
title: "Today on arXiv (#3)"
collection: blogposts
permalink: /blog/2021-07-07-today-on-arxiv
excerpt: "Recent intriguing pre-prints on arXiv: optimizing coarse-grained MD simulations with particle swarm optimization, ensembling deep neural nets for better drug-target interaction prediction, and a new dataset for temporal graph NN benchmarking."
date: 2021-07-07
read_time: true
---

Hi! Today, I invite you to discuss some of the recent arXiv preprints:
  
---

- [__Automatic Middle-Out Optimisation of Coarse-Grained Lipid Force Fields__](http://arxiv.org/abs/2107.01012v1) (Empereur-mot et al.; submitted 02.07.2021).

  <u>My short summary</u>: Molecular dynamics (MD) simulation is an important computational method that often helps researchers to understand the behaviour of complex supramolecular systems, especially when it is impossible to experimentally study them in full detail. 
  
  There are several ways how MD experiments can be run. As such, first you can have an all-atom MD, which models the behaviour of all the atoms in a system. However, it is very computationally expensive.
  
  To fight this, researchers have introduced coarse-grained molecular models, which, instead of modeling the behaviour of single atoms, do so for large atom groups.
  
  Understandably, the quality of coarse-grained experiments depends on the used force field. The force fields for CG simulations can be produced either in a <i>top-down</i> manner (meaning, by finding such parameters that allow for direct computational reproduction of experimental results) or in a <i>bottom-up</i> one (meaning, deriving the force field parameters from computationally expensive all-atom simulations).
  
  The authors of this work introduce a <i>middle-out</i> force field optimization strategy, which means they take the results of all-atom MD simulations and redefine the force fields by performing some particle swarm optimization of the CG atom representations to achieve the best matching with experimental values.
  
  The best part about this approach is that the authors claim it is transferrable – i.e., once more or less correct force field parameters are found for given lipid bilayers, they can be applied to correctly model any other type of lipid bilayers.

---

- [__Toward Robust Drug-Target Interaction Prediction via Ensemble Modeling  and Transfer Learning__](http://arxiv.org/abs/2107.00719v1) (Kao et al.; submitted 02.07.2021).

  <u>My short summary</u>: When performing virtual screening, one of the key steps is to estimate the drug-target interaction (DTI) between a screened ligand and the target protein. One of the most popular approaches for this is protein-ligand docking. However, it is resource-consuming, and different docking software may give different docking scores for the same drug-target pair.
  
  Of course, given the recent advances in deep learning, there were many works that tried to avoid these pitfalls by using the wealth of protein-ligand interaction data. In general, these approaches represented both the small molecules and the macromolecules as some kinds of textual or numerical sequences, processed this data by some of the most popular methods (e.g., simple one-hot encoding, or applying either convolutional or long short-term memory neural networks), and made predictions on some averaged representations.
  
  The authors of this work, on the other hand, went one step further and created an ensemble of neural networks, each representing the ligand and the protein using different combinations of representations and treatment methods. Then they basically asked each neural network to make a prediction, and then averaged the obtained values. 
  
  As a result, they demonstrate that the ensemble obtains the state-of-the-art performance when predicting dissociation constant (Kd), inhibition constant (Ki), or the half-maximal inhibitory concentration (IC50) for protein-ligand complexes coming from different datasets. 
  
  It's no wonder, though – ensembles of weak learners are long known to perform better than each weak model on its own. But what's cool is that the authors also show it's possible to quickly re-train the ensemble models on previously unseen data using transfer learning (i.e., by "initializing the neural network with pre-trained weights [...] from previously learned tasks").

---

- [__DPPIN: A Biological Dataset of Dynamic Protein-Protein Interaction  Networks__](http://arxiv.org/abs/2107.02168v1) (Fu et al.; submitted 05.07.2021)

  <u>My short summary</u>: Graphs are mathematical objects that are very useful to describe interactions in complex real-life entities, e.g., social networks, banking operations, etc. However, researchers often consider only the static graphs, i.e. such graphs that don't change in time. In reality, complex systems are often dynamic, with the graph topology and node features being dependent on time. In part, this is because there aren't many public datasets available that deal with temporal graphs.
  
  To facilitate research in this direction, the authors of this work introduce "a new biological dataset of dynamic protein-protein interaction networks (DPPIN), which consists of twelve dynamic protein-level interaction networks of yeast cells at different scales".
  
  In brief, the authors first took a set of 12 static protein-protein interaction networks. Then for each network, they examined "the active gene that codes proteins at a certain timestamp". After that, they "determined the co-expressed protein pairs at that timestamp [and] only preserved active and co-expressed proteins for dynamic protein interactions at that timestamp".
  
  As such, the authors generated 12 temporal graph networks basing on the 12 initial static graphs. On average, each of the temporal graphs has ~1000 nodes and a large number of dynamic edges at 36 timestamps. 
  
  The authors claim that their dataset could be used to develop and benchmark novel approaches in "dense community detection, graph querying, node similarity retrieval, node property prediction, and graph
property prediction in the dynamic setting".
  
---

That's all for today's arXiv picks! Did you like the list? Would you like me to give a more detailed examination of some of them? Let me know on [Medium](https://medium.com/chemoinformatics), [Twitter](https://twitter.com/mdshev7) or [Instagram](https://www.instagram.com/chemoinfo/).

Thank you for your kind attention and feedback. See you next time. Cheers!
