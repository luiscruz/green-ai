layout: publication
author: Ana Radovanovic, Ross Koningstein, Ian Schneider, Bokan Chen, Alexandre Duarte, Binz Roy, Diyue Xiao, Maya Haridasan, Patrick Hung, Nick Care, Saurav Talukdar, Eric Mullen, Kendal Smith, MariEllen Cottman, Walfredo Cirne
journal: "arXiv preprint"
title: "Carbon-Aware Computing for Datacenters"
year: 2021
arxiv: https://arxiv.org/abs/2106.11750
abstract: |-
  The amount of CO<sub>2</sub> emitted per kilowatt-hour on an electricity grid varies by time of day and substantially varies by location due to the types of generation. Networked collections of warehouse scale computers, sometimes called Hyperscale Computing, emit more carbon than needed if operated without regard to these variations in carbon intensity. This paper introduces Google's system for Carbon-Intelligent Compute Management, which actively minimizes electricity-based carbon footprint and power infrastructure costs by delaying temporally flexible workloads. The core component of the system is a suite of analytical pipelines used to gather the next day's carbon intensity forecasts, train day-ahead demand prediction models, and use risk-aware optimization to generate the next day's carbon-aware Virtual Capacity Curves (VCCs) for all datacenter clusters across Google's fleet. VCCs impose hourly limits on resources available to temporally flexible workloads while preserving overall daily capacity, enabling all such workloads to complete within a day. Data from operation shows that VCCs effectively limit hourly capacity when the grid's energy supply mix is carbon intensive and delay the execution of temporally flexible workloads to "greener" times.
bibtex: |-
  @misc{radovanovic2021carbonaware,
        title={Carbon-Aware Computing for Datacenters}, 
        author={Ana Radovanovic and Ross Koningstein and Ian Schneider and Bokan Chen and Alexandre Duarte and Binz Roy and Diyue Xiao and Maya Haridasan and Patrick Hung and Nick Care and Saurav Talukdar and Eric Mullen and Kendal Smith and MariEllen Cottman and Walfredo Cirne},
        year={2021},
        eprint={2106.11750},
        archivePrefix={arXiv},
        primaryClass={cs.DC}
  }
tags:
  - Green computing
  - Cloud computing
  - Carbon-aware datacenter
annotation: |-

  This paper presents Google's Carbon-Intelligent Computing System (CICS), that uses carbon-intensity data to shift datacenter jobs in time. 
  
  Based on carbon-intensity and power cost, the system computes a metric named **virtual capacity curve (VCC)** that limits the amount of CPU resources available in a cluster. This metric is then used by the system instead of the existing default/real cluster capacity that is typically used by job schedulers. This  approach makes the system scheduler agnostic, making it more modular.
  
  Internally, this strategy uses cpu usage as a proxy of memory, disk, and **power** usage. Hence the estimated power consumption of a given task is only based on the required cpu-load. However, it is not clear how the cpu-load is defined for a given task.
  
  Tasks are divided between flexible and inflexible – I assume this is specified by the users, although it was not entirely clear. Hence, task shifting is only affecting flexible workload.
  
  Flexible load is considered shapeable/shiftable as long as its total daily compute (CPU) demand is preserved.
  Moreover, if a cluster’s daily flexible demand is not met, the Carbon-Intelligent system is stopped for a week, allowing the forecasting models to adapt before reactivating it again.
  
  Since the system forecasts VCC values, it allocates jobs according to it: i.e., if the carbon intensity is expected to be high before finishing a given task it might not start in the first place. More details are given in the paper when discussing the **ramp-down period**. Because of that, I would argue that it does not seem to perform well if there are sudden changes in carbon intensity. This is not critical because carbon intensity seems to have smooth variations at the hour-level.
  
  Carbon intensity data is collected using electricityMap.org (previous Tomorrow). However, instead of using the carbon footprint directly, the system computes a cost metric in dollars using a factor expressed in dollars per kilogram of CO<sub>2</sub> emitted. What's more, they factor in an estimation of infrastructure costs driven by clusters peak power consumption, reducing demand for future infrastructure builds required to support peak workload. Although, this is not related to the power bill directly, it reduces the environmental impact of having the infrastructure in place – and, obviously, it reduces costs. 
    
  Future work will consider spatial-flexibility, shifting workload to datacenters in different location based on expected carbon intensity. The authors anticipate some challenges since load shifting to other locations has overheads that can increase the overall carbon emissions. Hence, there are plans to develop new models that explicitly characterise spatially flexible demand while considering rebound effects.
  
  While this solution is not targeting AI systems in particular, machine learning tasks can easily fit the definition of flexible jobs. In fact, this is mentioned in the paper. It would be interesting to see how some of these ideas can be exported to generic contexts, beyond the Google setting and the order of magnitude of savings in terms of carbon emissions.
  
image: radovanovi-carbon.svg
---
