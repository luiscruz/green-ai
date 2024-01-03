layout: publication
author: 
journal: "ICSE"
title: "Green AI: do deep learning frameworks have different costs?"
year: 2022
preprint: https://www.tusharma.in/preprints/green-ai_preprint.pdf
abstract: |-
  The use of Artificial Intelligence (ai), and more specifically of Deep Learning (dl), in modern software systems, is nowadays widespread and continues to grow. At the same time, its usage is energy demanding and contributes to the increased CO2 emissions, and has a great financial cost as well. Even though there are many studies that examine the capabilities of dl, only a few focus on its green aspects, such as energy consumption.
  
  This paper aims at raising awareness of the costs incurred when using different dl frameworks. To this end, we perform a thorough empirical study to measure and compare the energy consumption and run-time performance of six different dl models written in the two most popular dl frameworks, namely PyTorch and TensorFlow. We use a well-known benchmark of dl models, DeepLearningExamples, created by nvidia, to compare both the training and inference costs of dl. Finally, we manually investigate the functions of these frameworks that took most of the time to execute in our experiments.
  
  The results of our empirical study reveal that there is a statistically significant difference between the cost incurred by the two dl frameworks in 94% of the cases studied. While TensorFlow achieves significantly better energy and run-time performance than PyTorch, and with large effect sizes in 100% of the cases for the training phase, PyTorch instead exhibits significantly better energy and run-time performance than TensorFlow in the inference phase for 66% of the cases, always, with large effect sizes. Such a large difference in performance costs does not, however, seem to affect the accuracy of the models produced, as both frameworks achieve comparable scores under the same configurations. Our manual analysis, of the documentation and source code of the functions examined, reveals that such a difference in performance costs is under-documented, in these frameworks. This suggests that developers need to improve the documentation of their dl frameworks, the source code of the functions used in these frameworks, as well as to enhance existing dl algorithms.
bibtex: |-
  @inproceedings{georgiou2022green,
    title={Green ai: Do deep learning frameworks have different costs?},
    author={Georgiou, Stefanos and Kechagia, Maria and Sharma, Tushar and Sarro, Federica and Zou, Ying},
    booktitle={Proceedings of the 44th International Conference on Software Engineering},
    pages={1082--1094},
    year={2022}
  }
tags:
  - Deep Learning
  - AI frameworks
annotation:  |-

---
