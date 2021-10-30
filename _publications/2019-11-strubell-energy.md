---
layout: publication
author: Emma Strubell, Ananya Ganesh, Andrew McCallum
journal: Arxiv
title: "Energy and policy considerations for deep learning in NLP"
year: 2019
arxiv: https://arxiv.org/pdf/1910.09700.pdf
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
annotation: "Measured the energy consumption of training state-of-the-art natural language processing models. They estimated the energy consumption by collecting the reported time required to train those models and the average power consumption of the GPU hardware. The authors also factored in the energy consumption of cooling down the system: "
---
