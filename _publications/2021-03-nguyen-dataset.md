---
layout: publication
author: Timothy Nguyen, Zhourong Chen, Jaehoon Lee
journal: "International Conference on Learning Representations (ICLR)"
title: "Dataset Meta-Learning from Kernel Ridge-Regression"
year: 2021
arxiv: https://arxiv.org/abs/2011.00050
full-text: 
replication-package: https://github.com/google-research/google-research/blob/master/kip/
website: https://ai.googleblog.com/2021/12/training-machine-learning-models-more.html
preprint: https://openreview.net/pdf?id=l-PrrQrK0QR
abstract: |-
  One of the most fundamental aspects of any machine learning algorithm is the training data used by the algorithm. 
  We introduce the novel concept of ϵ-approximation of datasets, obtaining datasets which are much smaller than or are significant corruptions of the original training data while maintaining similar performance. 
  We introduce a meta-learning algorithm Kernel Inducing Points (KIP) for obtaining such remarkable datasets, drawing inspiration from recent developments in the correspondence between infinitely-wide neural networks and kernel ridge-regression (KRR).
  For KRR tasks, we demonstrate that KIP can compress datasets by one or two orders of magnitude, significantly improving previous dataset distillation and subset selection methods while obtaining state of the art results for MNIST and CIFAR10 classification.
  Furthermore, our KIP-learned datasets are transferable to the training of finite-width neural networks even beyond the lazy-training regime.
  Consequently, we obtain state of the art results for neural network dataset distillation with potential applications to privacy-preservation.
bibtex: |-
  @inproceedings{
  nguyen2021dataset,
  title={Dataset Meta-Learning from Kernel Ridge-Regression},
  author={Timothy Nguyen and Zhourong Chen and Jaehoon Lee},
  booktitle={International Conference on Learning Representations},
  year={2021},
  url={https://openreview.net/forum?id=l-PrrQrK0QR}
  }
tags:
  - Dataset Distillation
  - Data Efficiency
  - Green Data
annotation: |-
  This paper presents a technique called Kernel Inducing Points (KIP) to generate new smaller datasets that yield similar performance when used to train a machine learning model. In other words, KIP is an algorithm for *dataset distillation*.
  Although the paper does not primarily focus on energy efficiency, it shows an an enormous potential of using dataset distillation to reduce the energy consumption of machine learning models – in particular, neural networks.
  Besides improving efficiency, this technique can enable privacy-preservation on datasets, since the generated datasets are different from its raw version. This is different from the concept of extracting coresets – a subset selected from the original dataset that preserves or approximates the original properties. 
  The technique is tested for different compressed dataset sizes, yielding similar performance results when compressing datasets by one or two orders of magnitude. Note: sometimes, the results in the paper are a bit rushed, but all the details are provided in the appendices.
image: images/nguyen2021dataset.png
---
