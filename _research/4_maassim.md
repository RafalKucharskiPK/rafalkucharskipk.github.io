---
layout: project
title: simulation
description: agent-based two-sided mobility platform simulator
img: assets/img/maassim.png
importance: 4
category: work
---

**Agent-based two-sided mobility platform simulator - lightweight open-source scientific software. Designed to support research of four PhDs and several master students under Critical MaaS grant - stream of papers in preparation.**

Preprint on [arxiv](https://arxiv.org/abs/2011.12827) (under review in _PLOS One_) 
and publicly available github [repo](https://github.com/RafalKucharskiPK/MaaSSim) with *Oded Cats*. 



<center><img src="https://github.com/RafalKucharskiPK/MaaSSim/raw/master/data/MaaSSim_animation.gif"></center>
<div class="col three caption">
    Figure 1: Operations of MaaSSim.
</div>


MaaSSim is an agent-based simulator, reproducing the dynamics of two-sided mobility platforms (like Uber and Lyft) in the context of urban transport networks. It models the behaviour and interactions of two kind of agents: (i) travellers, requesting to travel from their origin to destination at a given time, and (ii) drivers supplying their travel needs by offering them rides. The interactions between the two agent types are mediated by the platform, matching demand and supply. Both supply and demand are microscopic. For supply this pertains to the explicit representation of single vehicles and their movements in time and space (using a detailed road network graph), while for demand this pertains to exact trip request time and destinations defined at the graph node level. Agents are decision makers, specifically, travellers may reject the incoming offer or decide to use another mode than those offered by the mobility platform altogether. Similarly, driver may opt-out of the system (stop providing service) or reject/accept incoming requests. Moreover, they may strategically re-position while being idle.

All of above behaviours are modelled through user-defined decision modules, by default deterministic, optionally probabilistic, representing agents' taste variations (heterogeneity), their previous experiences (learning) and available information (system control). Each simulation run results in two sets of outputs, one being the sequence of recorded space-time locations and statuses for simulated vehicles and the other for travellers. Further synthesised into agent-level and system-wide KPIs for in-depth analyses.


<center><img src="{{ site.baseurl }}/assets/img/maassim.png"></center>
<div class="col three caption">
    Figure 1: 
</div>



