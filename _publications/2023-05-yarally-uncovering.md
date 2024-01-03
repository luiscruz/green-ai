---
layout: publication
author: Tim Yarally, Luís Cruz, Daniel Feitosa, June Sallou, and Arie van Deursen
journal: "CAIN"
title: "Uncovering Energy-Efficient Practices in Deep Learning Training: Preliminary Steps Towards Green AI"
year: 2023
preprint: https://arxiv.org/pdf/2303.13972.pdf
abstract: |-
  Modern AI practices all strive towards the same goal: better results. In the context of deep learning, the term "results" often refers to the achieved accuracy on a competitive problem set. In this paper, we adopt an idea from the emerging field of Green AI to consider energy consumption as a metric of equal importance to accuracy and to reduce any irrelevant tasks or energy usage. We examine the training stage of the deep learning pipeline from a sustainability perspective, through the study of hyperparameter tuning strategies and the model complexity, two factors vastly impacting the overall pipeline’s energy consumption. First, we investigate the effectiveness of grid search, random search and Bayesian optimisation during hyperparameter tuning, and we find that Bayesian optimisation significantly dominates the other strategies. Furthermore, we analyse the architecture of convolutional neural networks with the energy consumption of three prominent layer types: convolutional, linear and ReLU layers. The results show that convolutional layers are the most computationally expensive by a strong margin. Additionally, we observe diminishing returns in accuracy for more energy-hungry models. The overall energy consumption of training can be halved by reducing the network complexity. In conclusion, we highlight innovative and promising energy-efficient practices for training deep learning models. To expand the application of Green AI, we advocate for a shift in the design of deep learning models, by considering the trade-off between energy efficiency and accuracy.
bibtex: |-
  @inproceedings{yarally2023uncovering,
    title={Uncovering energy-efficient practices in deep learning training: Preliminary steps towards green ai},
    author={Yarally, Tim and Cruz, Lu{\i}s and Feitosa, Daniel and Sallou, June and Van Deursen, Arie},
    booktitle={2023 IEEE/ACM 2nd International Conference on AI Engineering--Software Engineering for AI (CAIN)},
    pages={25--36},
    year={2023},
    organization={IEEE}
  }
tags:
---
