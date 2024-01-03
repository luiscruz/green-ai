---
layout: publication
author: Timur Babakol, Yu David Liu
journal: "ICSE-SEIS"
title: "Tensor-Aware Energy Accounting"
year: 2024
preprint: https://arxiv.org/abs/2311.11424
abstract: |-
  With the rapid growth of Artificial Intelligence (AI) applications supported by deep learning (DL), the energy efficiency of these applications has an increasingly large impact on sustainability. We introduce Smaragdine, a new energy accounting system for tensor-based DL programs implemented with TensorFlow. At the heart of Smaragdine is a novel white-box methodology of energy accounting: Smaragdine is aware of the internal structure of the DL program, which we call tensor-aware energy accounting. With Smaragdine, the energy consumption of a DL program can be broken down into units aligned with its logical hierarchical decomposition structure. We apply Smaragdine for understanding the energy behavior of BERT, one of the most widely used language models. Layer-by-layer and tensor-by-tensor, Smaragdine is capable of identifying the highest energy/power-consuming components of BERT. Furthermore, we conduct two case studies on how Smaragdine supports downstream toolchain building, one on the comparative energy impact of hyperparameter tuning of BERT, the other on the energy behavior evolution when BERT evolves to its next generation, ALBERT.
bibtex: |-
  @article{babakol2024tensor,
    title={Tensor-Aware Energy Accounting},
    author={Babakol, Timur and Liu, Yu David},
    journal={ICSE-SEIS},
    year={2023}
  }
tags:
---
