---
layout: publication
author: Alexandre Lacoste, Alexandra Luccioni, Victor Schmidt Thomas Dandres
journal: Arxiv
title: "Quantifying the carbon emissions of machine learning"
year: 2019
arxiv: https://arxiv.org/pdf/1910.09700.pdf
doi: 10.1007/978-3-030-69970-3_5
abstract: "From an environmental standpoint, there are a few crucial aspects of training a neural network that have a major impact on the quantity of carbon that it emits. These factors include: the location of the server used for training and the energy grid that it uses, the length of the training procedure, and even the make and model of hardware on which the training takes place. In order to approximate these emissions, we present our Machine Learning Emissions Calculator, a tool for our community to better understand the environmental impact of training ML models. We accompany this tool with an explanation of the factors cited above, as well as concrete actions that individual practitioners and organizations can take to mitigate their carbon emissions."
bibtex: |-
  @article{lacoste2019quantifying,
    title={Quantifying the carbon emissions of machine learning},
    author={Lacoste, Alexandre and Luccioni, Alexandra and Schmidt, Victor and Dandres, Thomas},
    journal={arXiv preprint arXiv:1910.09700},
    year={2019}
  }
image: "lacoste-quantifying.png"
tags:
  - Estimating Energy
  - Carbon Emissions
annotation: "Measured the energy consumption and carbon footprint of training state-of-the-art natural language processing (NLP) models. They estimated the energy consumption by collecting the reported time required to train those models and the average power consumption of the GPU hardware. The authors also factored in the energy consumption of cooling down the system, using the Power Usage Effectiveness (PUE) coefficient — 1.58 as of 2018. The carbon footprint is estimated based on the average CO2-eq produced for power consumed in US, as reported in 2018. Moreover, they calculated the carbon footprint of training their own NLP model, including the footprint of developing the model. Based on their development logs, they factored in 4789 jobs including for example, 123 hyperparameter grid searches. The cost of development is very important because training their model takes 120 hours, but it took 239942 hours of total training time to perform the full R&D required to develop the model. This paper calls for the importance of 1) reporting training time and sensitivity to hyperparameters, 2) having equitable access to computation resources amongst academics, 3) prioritising computationally efficient hardware and algorithms."
---
