---
layout: publication
author: "Jie You*, Jae-Won Chung*, Mosharaf Chowdhury"
journal: "NSDI '23"
title: "Zeus: Understanding and Optimizing GPU Energy Consumption of DNN Training"
year: 2023
full-text: https://www.usenix.org/conference/nsdi23/presentation/you
website: https://ml.energy/zeus
replication-package: https://github.com/SymbioticLab/Zeus
abstract: "Training deep neural networks (DNNs) is becoming increasingly more resource- and energy-intensive every year. Unfortunately, existing works primarily focus on optimizing DNN training for faster completion, often without considering the impact on energy efficiency.

In this paper, we observe that common practices to improve training performance can often lead to inefficient energy usage. More importantly, we demonstrate that there is a tradeoff between energy consumption and performance optimization. To this end, we propose Zeus, an optimization framework to navigate this tradeoff by automatically finding optimal job- and GPU-level configurations for recurring DNN training jobs. Zeus uses an online exploration-exploitation approach in conjunction with just-in-time energy profiling, averting the need for expensive offline measurements, while adapting to data drifts over time. Our evaluation shows that Zeus can improve the energy efficiency of DNN training by 15.3%–75.8% for diverse workloads."
bibtex: |-
  @inproceedings{zeus:nsdi23,
      author    = {Jie You and Jae-Won Chung and Mosharaf Chowdhury},
      booktitle = {USENIX NSDI},
      title     = {Zeus: Understanding and Optimizing {GPU} Energy Consumption of {DNN} Training},
      year      = {2023},
  }
tags:
  - Green computing
  - Cloud computing
  - Optimizing energy
  - Tool
annotation: 
---
