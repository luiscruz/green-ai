---
layout: publication
author: Jieke Shi, Zhou Yang, Hong Jin Kang, Bowen Xu, Junda He, David Lo
journal: "ICSE-SEIS"
title: "Greening Large Language Models of Code"
year: 2024
arxiv: https://arxiv.org/pdf/2309.04076v2
abstract: "Large language models of code have shown remarkable effectiveness across various software engineering tasks. Despite the availability of many cloud services built upon these powerful models, there remain several scenarios where developers cannot take full advantage of them, stemming from factors such as restricted or unreliable internet access, institutional privacy policies that prohibit external transmission of code to third-party vendors, and more. Therefore, developing a compact, efficient, and yet energy-saving model for deployment on developers' devices becomes essential. 
To this aim, we propose Avatar, a novel approach that crafts a deployable model from a large language model of code by optimizing it in terms of model size, inference latency, energy consumption, and carbon footprint while maintaining a comparable level of effectiveness. The key idea of Avatar is to formulate the optimization of language models as a multi-objective configuration tuning problem and solve it with the help of a Satisfiability Modulo Theories (SMT) solver and a tailored optimization algorithm. The SMT solver is used to form an appropriate configuration space, while the optimization algorithm identifies the Pareto-optimal set of configurations for training the optimized models using knowledge distillation. We evaluate Avatar with two popular language models of code, i.e., CodeBERT and GraphCodeBERT, on two popular tasks, i.e., vulnerability prediction and clone detection. We use Avatar to produce optimized models with a small size (3 MB), which is 160x smaller than the original large models. On the two tasks, the optimized models significantly reduce the energy consumption (up to 184x less), carbon footprint (up to 157x less), and inference latency (up to 76x faster), with only a negligible loss in effectiveness (1.67\% on average)."
bibtex: |-
  @article{shi2024greening,
    title={Greening Large Language Models of Code},
    author={Shi, Jieke and Yang, Zhou and Kang, Hong Jin and Xu, Bowen and He, Junda and Lo, David},
    journal={ICSE-SEIS},
    year={2024}
  }
tags:
  - model optimization
  - energy estimation
annotation:  |-

  This paper shows an interesting approach to compress language models of code into smaller and more efficient models. The approach consists of using optimisation to deliver a model that minimises size, FLOPs (mentioned as a proxy of time, energy consumption, and carbon emission), and maximises model performance (refer to as effectiveness).
  
  While it seems to be a simple optimisation approach the paper proposes a few techniques that set it apart. For example, to evaluate the model performance, the authors do not train the model nor run it with a test set – they create a regression model using only the provided configuration as input. This metric is coined as effectiveness indicator.
  
  Another design choice of this approach is the usage of FLOPs as a proxy of time, energy consumption, and carbon emissions. Although I find this acceptable at the current preliminary stage of research in Green AI, this is a controversial approach. Related work has shown that FLOPs is a poor indicator of energy consumption – for example, it completely ignores the energy consumption of data transfers which are known to be energy intensive in AI operations (See ICSE paper by Georgiou, 2022). The issue is even more relevant when it comes to using FLOPs as a proxy of carbon emissions. While it is acceptable to say that reducing FLOPs implies reducing carbon emissions, assuming that the two variables reduce in the same proportion is not accurate. This hinders the optimisation step where models are compared: it could be that models with a lower carbon footprint but higher number of FLOPs are being discarded. For example, imagine that in one optimisation round the original model M is compressed into a new model M1, with 30% less FLOPs. On a second optimisation round, there is another new model M2 with 10% less FLOPs. Model M2 is not selected because we assume carbon emissions are higher than in M1 – this is a big assumption. Also the fact that a single metric FLOPs is used as a proxy of time, energy, and carbon altogether shows that the authors assumed the three variables are basically the same thing.
  
  Another threat in this study is the usage of ML CO2 Impact to compare carbon emissions. This tool is wonderful to report an estimate of carbon footprint in AI studies, but it is not suitable to answer research questions about the energy consumption or carbon emissions of AI models. First, given a particular hardware and datacenter, the metric computed by the tool ML CO2 Impact is a linear function of time. Second, it assumes that a GPU runs at a steady power consumption, with no variation. Note, for example, that state-of-the-art models leverage a GPU usage between 30% and 80% and it is still an open problem to make models that effectively use the GPU at 80% of its capacity (see study by Meta AI). This means that any assumption of steady GPU usage is prone to error and should be used carefully when answering research questions.
  
  Nevertheless, the paper shows that model optimisation with Microsoft Z3 can lead to models that are 160x smaller, inference latency up to 76x faster, with a negligible loss in effectiveness (1.67%). The numbers reported about energy consumption and carbon footprint should be taken with a grain of salt.
---
