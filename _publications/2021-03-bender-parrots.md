---
layout: publication
author: Emily M. Bender, Timnit Gebru, Angelina McMillan-Major, Shmargaret Shmitchell
journal: "FAccT '21: Conference on Fairness, Accountability, and Transparency"
title: "On the Dangers of Stochastic Parrots: Can Language Models Be Too Big? 🦜"
year: 2021
doi: 10.1145/3442188.3445922
abstract: "The past 3 years of work in NLP have been characterized by the development and deployment of ever larger language models, especially for English. BERT, its variants, GPT-2/3, and others, most recently Switch-C, have pushed the boundaries of the possible both through architectural innovations and through sheer size. Using these pretrained models and the methodology of fine-tuning them for specific tasks, researchers have extended the state of the art on a wide array of tasks as measured by leaderboards on specific benchmarks for English. In this paper, we take a step back and ask: How big is too big? What are the possible risks associated with this technology and what paths are available for mitigating those risks? We provide recommendations including weighing the environmental and financial costs first, investing resources into curating and carefully documenting datasets rather than ingesting everything on the web, carrying out pre-development exercises evaluating how the planned approach fits into research and development goals and supports stakeholder values, and encouraging research directions beyond ever larger language models."
bibtex: |-
  @inproceedings{bender2021dangers,
    title={On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?🦜},
    author={Bender, Emily M and Gebru, Timnit and McMillan-Major, Angelina and Shmitchell, Shmargaret},
    booktitle={Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency},
    pages={610--623},
    year={2021}
  }
image: "bender-parrots.png"
tags:
  - NLP
  - Position Paper
annotation: |-
  A call for the realignment of the research directions in the NLP research community. This position paper does a reflection on current societal issues of the development of NLP models and their potential risks and harms.
  Mostly, it brings awareness to the fact that NLP models can reproduce or amplify unwanted biases that can propagate stereotypes and other problematic associations. Furthermore, NLP models can be used as powerful tools to deliberately disseminate falsehoods to mislead public opinion.
  In sum, this paper calls for a research agenda that focuses on value-sensitive design. Instead of aiming at creating the biggest model with the largest dataset, the community should start looking at how the models will form part of socio-technical systems. In particular, we should focus on how to create models that are fair, trustworthy, and climate-neutral.
  In practice, the authors suggest using pre-mortems analyses as a way of anticipating the risks of a model and discussing alternatives beforehand.
  
  The paper is not bringing anything new into discussion and there is not a scientific contribution per se. However, it will always be emblematic because of the controversy around 3 out of 7 authors that were required by their employer to remove their names – allegedly because of the critical view on the way tech giants are leading innovation on NLP. Nevertheless, it provides a clear snapshot of the potential harms of NLP and a strong case on the need for a groundbreaking change to make NLP less social-agnostic – including less carbon-agnostic.
---
