---
layout: publication
author: Eva García-Martín, Crefeda Faviola Rodrigues, Graham Riley, Håkan Grahn
journal: J. Parallel Distrib. Comput.
title: "Estimation of energy consumption in machine learning"
year: 2019
doi: 10.1016/j.jpdc.2019.07.007
abstract: "Energy consumption has been widely studied in the computer architecture field for decades. While the adoption of energy as a metric in machine learning is emerging, the majority of research is still primarily focused on obtaining high levels of accuracy without any computational constraint. We believe that one of the reasons for this lack of interest is due to their lack of familiarity with approaches to evaluate energy consumption. To address this challenge, we present a review of the different approaches to estimate energy consumption in general and machine learning applications in particular. Our goal is to provide useful guidelines to the machine learning community giving them the fundamental knowledge to use and build specific energy estimation methods for machine learning algorithms. We also present the latest software tools that give energy estimation values, together with two use cases that enhance the study of energy consumption in machine learning."
bibtex: 
image: "garciamartin-estimation.png"
tags:
  - Estimating Energy
  - Literature Review
annotation: |-
  Everything there is to know about the theory behind creating power models. The paper also shows an overview of five existing tools that help creating power models: ARM Streamline Powmon, Intel Power Gadget McPAT, PAPI. Although it describes the compatibility of the tools in terms of operating system, it does not describe which CPU architecture it supports (e.g., Intel, AMD, Apple M1, etc.). The paper also delves into related work on estimating energy consumption in neural networks. The presented strategies use metrics such as number of floating-point operations, number of weights of a model, kernel size, number of layers, number of arithmetic operations (multiply-add and activation function).
  The paper also references previous work on energy-aware development of neural network – i.e., a priori energy use. Finally, two use cases are presented to study the energy consumption of particular machine learning techniques: 1) concept drift detection – yielding 11% more energy usage — and different convolutional network architectures — MobileNet yielded less energy usage than Inception-v3 and DenseNet. The paper used the SyNERGY approach to estimate energy consumption in neural networks. The estimated energy had an error of roughly 30%, but was able to keep the order of energy efficiency results across different measurements — e.g., both the estimation and real energy measurement agreed on the most energy efficient neural network.
---
