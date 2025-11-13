---
layout: project
title: COeXISTENCE
project: COeXISTENCE
description: ERC Starting Grant on COeXISTENCE between humans and machines in urban mobility
img: assets/img/p_coexistence/logo_coexistence.jpg
importance: 1
category: grants
---

<img width="350" src="/./assets/img/logo_COeXISTENCE.jpeg" alt="drawing" class="responsive-logo"/><img src="/./assets/img/LOGO-ERC.jpg" alt="drawing" height="100"/>


> What will be the future of our cities with autonomous vehicles, using any kind of ML algorithms to make collective routing decisions? **Let's see what we know so far**


We pioneer the very specific problem that our cities may face in the future, when autonomous vehicles are efficiently navigating across our cities. 
They will, individually or collectively, make routing decisions. The same decisions that are now made daily by millions of human drivers worldwide, and resulting in traffic jams and complex congestion patterns, will be delegated to machines.
What will it change? **Let's see**


### 📚 This is what we know so far from our research:

(click for short overview) 
* <span style="color:red">Alarming:</span>
  - [Fleet strategy controls the overall system performance](#fleet-strategy-controls-the-overall-system-performance)
  - [CAVs may form exclusive clubs](#cavs-may-form-exclusive-clubs)
  - [Creating travel time oscillations is a good strategy to maximise fleet market share](#creating-travel-time-oscillations-is-a-good-strategy-to-maximise-fleet-market-share)
  - [State-of-the-art RL algorithms fail even on trivial routing tasks.](#state-of-the-art-rl-algorithms-fail-even-on-trivial-routing-tasks)
* <span style="color:green">Promising:</span>
  - [Traffic assignment can be both Nash optimal and equilibrated with CAVs](#traffic-assignment-can-be-both-nash-optimal-and-equilibrated-with-cavs)
  - [It is better to be a good socially aware CAV than selfish](#it-is-better-to-be-a-good-socially-aware-cav-than-selfish)
  - [Unsocial fleet behaviours can be detected.](#unsocial-fleet-behaviours-can-be-detected)
  - [The ML community shall compete to develop efficient algorithms](#the-ml-community-shall-compete-to-develop-efficient-algorithms)

* Tools and software we created to answer those questions
  - [RouteRL](#how-to-simulate-such-a-future-system) Multi-Agent Reinforcement Learning framework is a central tool, along with otherson this repo: [COeXISTENCE Project GitHub](https://github.com/COeXISTENCE-PROJECT)


---

#### Problem formulation and overall methodology:



<p align="center">
  <img src="/./assets/img/scirep.jpg" alt="drawing" width="600"/> 
</p>

See the brief problem overview [here](https://raw.githubusercontent.com/RafalKucharskiPK/rafalkucharskipk.github.io/master/assets/pdf/flyer.pdf) and a longer kick-off talk  [presentation](https://raw.githubusercontent.com/RafalKucharskiPK/rafalkucharskipk.github.io/master/assets/pdf/Wyklad_ERC.pdf).

> **Disclaimer** <span style="color:red"> we do not address the autonomous driving itself and operations. We assume that AVs can navigate well in our cities, including starting, driving, cruising, detecting objects, stopping, obeying traffic rules, and parking. </span> Dozens of excellent research teams already contribute to this. We address the follow-up problem: _What happens when CAVs will start making their own decisions, specifically routing decisions_. We anegdotically compare it to the case of a toddler who learns how to walk, but the true problems come with teenagers who may start to decide (e.g., on the colour of hair, tattoos, career, etc). Notably, we assume that traffic flow operations of CAVs are indistinguishable from human driving (differences found here may amplify when we include CAV traffic flow advantages).
> 
---

# Findings:

Brief overview of the most important findings from our research:

#### CAVs may form exclusive clubs

> We show that [Equilibria in routing games with connected autonomous vehicles will not be strong, as exclusive clubs may form](https://arxiv.org/pdf/2510.12862)

CAVs will be able to break from the Nash equilibrium and form coalitions, collaborating to devise a joint routing pattern that allows them to arrive faster. However, with limited resources, i.e., the capacity in road networks, a
group arriving faster will gain at the expense of others arriving later. Also, not everyone can be invited to join the group as it remains efficient only until
some point. Thus, such groups will be exclusive, and, like other exclusive goods, they will be available to the masses and limited to upper classes only. Threatening the equity of using public space of our cities.

<p align="center">
<img width="500" src="/./assets/img/overview.png" alt="drawing" class="responsive-logo"/>
</p>

#### Creating travel time oscillations is a good strategy to maximise fleet market share

> We demonstrate the fleet may intentionally bring chaos to our cities to maximise market share - [here](arxiv)

What is the optimal strategy to maximise market share and convince most drivers to join the CAV fleet? Surprisingly, **bringing chaos** may be quite effective. Controlled oscillations of traffic flows, predictable by fleet operators but surprising to humans, may be frustrating enough to convince others to abandon human driving and join a fleet. Individually tailored offers (just like Uber, Amazon, or Ryanair) leveraging on our behavioural traits may be exploitable as well, and our low expectations (due to low budget or high urgency) may enable network-wide strange assignment plans, ultimately leading to increasing market shares. Those are initial results from a monopoly, where a single operator competes with humans, which are likely to be even worse in the case when competing fleets launch aggressive campaigns deployed in our cities.

<p align="center">
<img width="800" src="/./assets/img/oscillations.jpg" alt="drawing" />
</p>

#### Traffic assignment can be both Nash optimal and equilibrated with CAVs

> New concept of Wardrop Cyclical Equilibrium is both optimal and fair for CAVs as we show [here](https://arxiv.org/pdf/2507.19675)

Connected and Autonomous Vehicles (CAVs) open the possibility for centralized routing with full compliance, making System-Optimal traffic assignment attainable. However, as System Optimum makes some drivers better off than others, voluntary acceptance seems dubious. To overcome this issue, we propose a new concept of _Wardropian cycles_, which, in contrast to previous utopian visions, ensures both fairness and optimality, thereby satisfying Wardrop's principles. Such cycles, represented as sequences of permutations in the daily assignment matrices, always exist and equalize, after a limited number of days, the average travel times among travelers (similar to User Equilibrium), while preserving the everyday optimality of path flows (similar to System Optimum). In Barcelona, 670 vehicle-hours of Price-of-Anarchy are eliminated using cycles with a median length of 11 days. 

<p align="center">
<img width="600" src="/./assets/img/grafika_latest.png" alt="drawing" />
</p>

#### How to simulate such a future system

> We created [RouteRL](https://github.com/COeXISTENCE-PROJECT/RouteRL), a Multi-Agent Reinforcement Learning framework for modeling and simulating the collective route choices of humans and autonomous vehicles - [SoftwareX](https://doi.org/10.1016/j.softx.2025.102279)
<p align="center">
  <img src="https://github.com/COeXISTENCE-PROJECT/RouteRL/raw/main/docs/_static/logo.png" alt="drawing" width="150"/> 
</p>

RouteRL is a novel framework that integrates multi-agent reinforcement learning (MARL) with a microscopic traffic simulation to develop efficient collective route choice strategies for autonomous vehicles (AVs). The proposed framework models the daily urban route choices of driver agents of two types: human drivers, emulated using behavioral route choice models, and AVs, modeled as MARL agents optimizing their policies for a predefined objective. RouteRL aims to advance research in MARL, transport modeling, and human–AI interaction for transportation applications. 
  
<p align="center">
<img src="/./assets/img/RouteRL.jpg" width="800"/>
</p>

#### State-of-the-art RL algorithms fail even on trivial routing tasks.

> Only a few of the SOTA Reinforcement Learning algorithms managed to find the optimal routing strategy in a trivial case with 10 AVs and two routes, as we report in this [paper](https://arxiv.org/pdf/2502.13188)

Autonomous vehicles (AVs), which may utilize Multi-Agent Reinforcement Learning (MARL) for simultaneous route optimization, may destabilize traffic networks, potentially leading to longer travel times for human drivers. We study this interaction by simulating human drivers and AVs. Our experiments with standard MARL algorithms reveal that, both in simplified and complex networks, policies often fail to converge to an optimal solution or require long training periods. This problem is amplified by the fact that we cannot rely entirely on simulated training, as there are no accurate models of human routing behavior. At the same time, real-world training in cities risks destabilizing urban traffic systems, increasing externalities, such as CO2 emissions, and introducing non-stationarity as human drivers will adapt unpredictably to AV behaviors.


<p align="center">
<img width="800" src="/./assets/img/storyline.png"/>
</p>


#### The ML community shall compete to develop efficient algorithms

> We introduced [URB](https://github.com/COeXISTENCE-PROJECT/URB), an Urban Routing Benchmark for MARL algorithms on the fleet routing tasks - [NeurIPS 2025](https://arxiv.org/abs/2505.17734)
<p align="center">
   <img src="https://github.com/COeXISTENCE-PROJECT/URB/raw/main/docs/urb.png" alt="drawing" width="150"/> 
</p>

 `URB` is a comprehensive benchmarking environment that unifies evaluation across **29** real-world traffic networks paired with realistic demand patterns. `URB` comes with a catalog of predefined tasks, multi-agent RL (MARL) algorithm implementations, three baseline methods, ten domain-specific performance metrics, and a modular configuration scheme. 

`URB` aims to:

  1. Identify which state-of-the-art algorithms outperform others in this class of tasks,
  2. Drive competition for future algorithmic improvements, and
  3. Clarify the impact of collective CAV routing on congestion, emissions, and sustainability in future cities, equipping policymakers with solid arguments for CAV regulations.

<p align="center">
<img src="/./assets/img/urb_overview.png"  width="800"/>
</p>

#### It is better to be a good socially aware CAV than selfish

> Autonomous vehicles need social awareness in their reward to find optima in multi-agent reinforcement learning routing games, as we show [here](https://arxiv.org/pdf/2510.11410)

Previous work has shown that when multiple selfish Autonomous Vehicles (AVs) are introduced to future cities and start learning optimal routing strategies using Multi-Agent Reinforcement Learning (MARL), they may destabilize traffic systems, as they would require a significant amount of time to converge to the optimal solution, equivalent to years of real-world commuting.
We demonstrate that moving beyond the selfish component in the reward significantly relieves this issue. If each AV, apart from minimizing its own travel time, aims to reduce its impact on the system, this will be beneficial not only for the system-wide performance but also for each individual player in this routing game.
By introducing an intrinsic reward signal based on the marginal cost matrix, we significantly reduce training time and achieve convergence more reliably. 
Our results optimistically indicate that social awareness (i.e., including marginal costs in routing decisions) improves both the system-wide and individual performance of future urban systems with AVs.

<p align="center">
<img src="/./assets/img/marginal.png"  width="800"/>
</p>


#### Fleet strategy controls the overall system performance

>  In this [study](https://www.nature.com/articles/s41598-025-90783-w), we show that the strategy CAVs are allowed to adopt may result in human drivers either benefiting or being systematically disadvantaged and urban networks becoming either more or less optimal.

Studying the simplest of the two-route bottleneck macroscopic network, we discover that:

* The choices of CAVs that replace a given share of HDVs differ significantly from the choices of the remaining HDVs.
* In different scenarios the average travel time of both HDVs and CAVs may increase or decrease.
* If the fleet of CAVs applies the selfish strategy, it may improve its collective travel time at a cost to human drivers when the share of CAVs is small.
* For a large share of CAVs, the selfish or social strategies of CAVs may result in improvement of travel times for all the drivers. This, however, comes at a price of reduced equity.
* Human driver populations with low perception bias may be less prone to exploitation by intelligent fleets of CAVs than more diverse and less optimal populations.
* Heavily congested systems, where the choices of HDVs and CAVs tend to be similar, may be less susceptible to exploitation by CAVs. Conversely, uncongested networks could be easily exploited by machines.

<p align="center">
<img src="/./assets/img/scirep2.jpeg" width="900"/>
</p>

#### Unsocial fleet behaviours can be detected.

> Antisocial individual vehicles of a coordinated fleet will be detectable, as we prove in this [paper](https://arxiv.org/pdf/2506.22966)

Detection of collectively routing fleets of vehicles in future urban systems may become important for the management of traffic, as such routing may destabilize urban networks, leading to deterioration of
driving conditions. To address this issue, we address two related problems:

* Is it possible to determine the flow of fleet vehicles on all routes given the fleet size and behaviour as well as the combined total flows?

We prove that the answer is **yes** for myopic fleet strategies which are more _selfish_ than _altruistic_, and
**no** otherwise. 

* Is it possible to identify the individual vehicles of a coordinated fleet from daily route choice observations of individual vehicles?

Our finginds indicate that the answer is likely to be **yes** for anisocial fleet objectives and _no_ for pro-social fleet objectives. 

<p align="center">
<img src="/./assets/img/detect.jpg" width="800"/>
</p>



----


<!---
We want to understand the future of Urban Mobility and foresee what happens when our cities are shared with autonomous, intelligent robots - competing with us for limited resources. 
* We demonstrated the novel phenomena on simple topologies [here](https://www.nature.com/articles/s41598-025-90783-w)
* We created the dedicated MARL environment for our experiments [paper](https://arxiv.org/pdf/2502.20065) and repository on [GitHub](https://github.com/COeXISTENCE-PROJECT/RouteRL)
* We have some preliminary results from [EWRL](https://openreview.net/pdf?id=88zP8xh5D2)
* We identified issues with convergence and reported them [here](https://arxiv.org/pdf/2502.13188)

For updates and new contributions you may consult our [GitHub](https://github.com/COeXISTENCE-PROJECT) or follow us on social media. 

For collaborations, please contact us or simply start contributing on our repos.



. We create virtual environments where individual agents compete to arrive faster, more reliably and cheaper at their destinations.  Human agents are simulated with detailed behavioural models, estimated and calibrated on the field data to reproduce how we behave and adapt in the cities. In the same environment the deep learning agents try the same - they  use deep reinforcement learning to maximise their rewards. This creates a harsh competition in which machines have upper-hands strong enough to beat us. 



*COeXISTENCE* is a broad and deep experiment in virtual environment on future cities, aimed to discover the new phenomena and propose the new solutions. 
It spans between fields as diverse as:

* game theory;
* deep reinforcement learning;
* complex social systems;
* sustainability;
* urban mobility;
* agent based modelling;
* discrete choice theory.
--->


### About us:

This content was made as part of [COeXISTENCE](https://www.rafalkucharskilab.pl/research/coexistence/) (ERC Starting Grant, grant agreement No 101075838) and is a team work at Jagiellonian University in Kraków, Poland by: [Ahmet Onur Akman](https://github.com/aonurakman), [Anastasia Psarou](https://github.com/AnastasiaPsarou), [Łukasz Gorczyca](https://github.com/Limexcyan), [Michał Hoffmann](https://github.com/Crackhoff), [Lukasz Kowalski](https://github.com/LukaszKowalski2013), [Paweł Gora](https://github.com/pgora), and [Grzegorz Jamróz](https://github.com/GrzegorzJamroz), within the research group of [prof. Rafał Kucharski](https://www.rafalkucharskilab.pl).

<p align="center">
<img src="/./assets/img/p_coexistence/team_coexistence.jpg" alt="team coexistence" height="400"/>
</p>






----

### Vacancies

We are always collaborators hungry, free to reach us out to understand more about opportunities at **coexistence@uj.edu.pl**

----

<p align="center">
  <img src="https://github.com/COeXISTENCE-PROJECT/URB/raw/main/docs/credits.png" width="50%"/>
</p>







<sub>**Disclaimer**: Funded by the European Union. Views and opinions expressed are however those of the author(s) only and do not necessarily reflect those of the European Union or European Research Council Executive Agency (ERCEA). Neither the European Union nor the granting authority can be held responsible for them.</sub>

<sub>**Funding acknowledgement**: This project has received funding from the European Research Council (ERC) under the European Union’s Horizon Europe research and innovation programme  (grant agreement No 101075838).</sub>

