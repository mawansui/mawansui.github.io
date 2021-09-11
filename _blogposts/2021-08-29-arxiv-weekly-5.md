---
title: "arXiv weekly (#5)"
collection: blogposts
permalink: /blog/2021-08-29-arxiv-weekly-5
excerpt: "Recent intriguing pre-prints on arXiv: IUPAC names for _de novo_ generation, a database of _apo_ protein conformations, and more!"
date: 2021-08-29
read_time: true
---

Hi everybody! After a summer break, I am back with more chemoinformatics-related posts. With that, I decided to make the arxiv review weekly (instead of daily). I kept the arxiv review numbering, though. So, please welcome the "arXiv weekly" for the past week: 21.08.21 - 28.08.21.

To my taste, there were only three pre-prints that are worth noticing. [The first](https://arxiv.org/abs/2108.10307) is a very curios work – the authors trained a transformer language model to input a missing part of an IUPAC name with the goal of improving a given target property's value. It's not often that you see IUPAC names used in de novo design-related works, though the authors give some worthy arguments for this choice (basically, IUPAC is semantically-rich and operate in the abstractions of functional groups, and not individual atoms like SMILES or graph representations).

[The second one](https://arxiv.org/abs/2108.09926) is about a soon-to-be-released dataset called APObind. Essentially, the authors took the PDBbind proteins (in their holo forms) and computationally adjusted them to "look like" apo structures. To me it seems to be a bit of a stretch, but maybe I just need to dig into the pre-print to understand it better. Still, the reasoning is good: newly established crystal structures of new proteins are often in the apo form, and most deep learning-based approaches work only with holo- forms, so why not augment the commonly used dataset to better represent the apo conformations? Sounds curious to me.

Lastly, we have [a pre-print](https://arxiv.org/abs/2108.09637?context=physics) that tackles the problem of low-energy molecular conformation search using graph convolutional neural networks. The catch? They additionally implement the inter-atomic interactions within the graphs they construct for each molecule.


---

I guess that's all interesting that was published on arXiv recently. Can't wait to see what's going to be there on next week. Did you like the list? Would you like me to give a more detailed examination of some of them? Let me know on [Medium](https://medium.com/chemoinformatics), [Twitter](https://twitter.com/mdshev7) or [Instagram](https://www.instagram.com/chemoinfo/).

Thank you for your kind attention and feedback. See you next time. Cheers!
