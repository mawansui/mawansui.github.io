---
title: "TorchDrug: a python library for drug design"
collection: blogposts
permalink: /blog/2021-08-20-torchdrug
excerpt: "Researchers from MILA (Canada) have released an open-source python library for rapid drug design prototyping using readily-available datasets and deep neural network models."
date: 2021-08-20
read_time: true
---

Hi! After a short break, I'm back with more posts! Today, let's discuss TorchDrug, a freshly-released open-source python library.

Recently, a group of scientists from MILA, a Canadian research institute, has made TorchDrug publicly available. The authors say the target audience for this tool is machine learning professionals who want to quickly build a model or two with a view to developing new drug molecules.

The authors point out the following advantages of their tool:

- It does not require domain knowledge in chemistry
- Provides pre-processed data sets for model training and benchmarking
- Provides the user with pre-compiled building blocks of complex neural networks (in fact, ready-made layers) from which you can easily aseemble a custom model
- Makes it easy to distribute the computations across any number of CPUs and GPUs.

At the moment, TorchDrug can be used to predict molecular properties (_QSAR_), extract molecular representations (embeddings), do _de novo_ molecular design and optimization, work with chemical reactions and retrosynthesis, and fill in missing links between nodes in a given biomedical graph (_Biomedical Knowledge Graph Reasoning_). The authors aim at adding support for protein representation learning soon.

All the code, tutorials and documentation of TorchDrug can be found at [https://torchdrug.ai/](https://torchdrug.ai/).
  

That's all for today's short review of a new chemoinformatics tool! Did you like the tool? Let me know on [Medium](https://medium.com/chemoinformatics), [Twitter](https://twitter.com/mdshev7) or [Instagram](https://www.instagram.com/chemoinfo/).

Thank you for your kind attention and feedback. See you next time. Cheers!