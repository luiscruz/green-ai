---
layout: publication
author: Emma Strubell, Ananya Ganesh, Andrew McCallum
journal: Arxiv
title: "Energy and policy considerations for deep learning in NLP"
year: 2019
arxiv: https://arxiv.org/abs/1906.02243
doi: 10.1007/978-3-030-69970-3_5
abstract: "Recent progress in hardware and methodology for training neural networks has ushered in a new generation of large networks trained on abundant data. These models have obtained notable gains in accuracy across many NLP tasks. However, these accuracy improvements depend on the availability of exceptionally large computational resources that necessitate similarly substantial energy consumption. As a result these models are costly to train and develop, both financially, due to the cost of hardware and electricity or cloud compute time, and environmentally, due to the carbon footprint required to fuel modern tensor processing hardware. In this paper we bring this issue to the attention of NLP researchers by quantifying the approximate financial and environmental costs of training a variety of recently successful neural network models for NLP. Based on these findings, we propose actionable recommendations to reduce costs and improve equity in NLP research and practice."
bibtex: |-
  @article{strubell2019energy,
    title={Energy and policy considerations for deep learning in NLP},
    author={Strubell, Emma and Ganesh, Ananya and McCallum, Andrew},
    journal={arXiv preprint arXiv:1906.02243},
    year={2019}
  }
image: "strubell-energy.png"
tags:
  - NLP
  - Estimating Energy
  - Carbon Emissions
annotation: |-
  Measures the energy consumption and carbon footprint of training state-of-the-art natural language processing (NLP) models. The authors estimate energy consumption by collecting the reported time required to train those models and the average power consumption of the GPU hardware. The authors also factored in the energy consumption of cooling down the system, using the Power Usage Effectiveness (PUE) coefficient – 1.58 as of 2018.

  The carbon footprint is estimated based on the average CO2eq produced for power consumed in US, as reported in 2018. Moreover, they calculated the carbon footprint of training their own NLP model, including the footprint of developing the model. Based on their development logs, they factored in 4789 jobs including, for example, 123 hyperparameter grid searches. The cost of development is very important because training their model takes 120 hours, but it took 239942 hours of training time to perform the full R&D required to develop the model.

  This paper calls for the importance of 1) reporting training time and sensitivity to hyperparameters of ML models, 2) having equitable access to computation resources amongst academics, 3) prioritising computationally efficient hardware and algorithms.
---
