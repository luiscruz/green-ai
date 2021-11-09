---
layout: publication
author: Alexandre Lacoste, Alexandra Luccioni, Victor Schmidt Thomas Dandres
journal: Arxiv
title: "Quantifying the carbon emissions of machine learning"
year: 2019
arxiv: https://arxiv.org/pdf/1910.09700.pdf
website: https://mlco2.github.io/impact/ 
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
  - Tool
  - Position paper
annotation: "The paper presents a tool to estimate carbon emissions: the Machine Learning Emissions Calculator. Based on the Hardware type (e.g, Tesla P100), cloud provider (e.g., Google Cloud Platform), location of the data centre, and number of hours used, it computes the total carbon emitted in kg CO2eq. The paper also provides actionable advice on how to reduce the environmental impact of Machine Learning. 1) Always quantify carbon emissions. 2) Choose cloud providers wisely – in particular, choose providers that are certified carbon neutral, either using renewable sources or by offsetting carbon emissions through Renewable Energy Certificates. The paper also mentions that the power usage effectiveness (PUE) of the data centre should be considered – the lower the better. 3) Select data centre location, as different locations have different CO2eq per kWh. 4) Reduce wasted resources – i.e., opt for development and training techniques that make an efficient use of server resources. They provide the example that using random search instead of grid search can significantly accelerate hyperparameter search. Finally, 5) the authors recommend choosing energy efficient hardware – i.e., hardware that maximises the number of floating point operations per unit of power (e.g., FLOPs/W)."
---
