---
layout: project
permalink: /COeXISTENCE/
title: COeXISTENCE
project: COeXISTENCE
description: ERC Starting Grant COeXISTENCE focuses on the coexistence of humans and autonomous vehicles in urban mobility systems. Explore experiments on future traffic systems, machine reinforcement learning, and social systems through innovative research led at Jagiellonian University in Kraków. Follow results and developments on GitHub and engage in collaborations.
nav: false
---


<img width="350" src="/./assets/img/logo_COeXISTENCE.jpeg" alt="drawing" class="responsive-logo"/>


> What will be the future of our cities with autonomous vehicles, using any kind of ML algorithms to make collective routing decisions?
>
> Let's see!

We pioneer the very specific problem that our cities may face in future, when autonomous vehicles are efficiently navigating across our cities. 
They will, individually or collectively, make routing decisions. The same decisions which are now daily made by millions of human drivers worldwide and result in traffic jams and complex congestion patterns, will be delegated to machines.
What will it change? **Let's see**


### This is what we know so far from our research:


short_list_todo

explained in bit more detail below

### Simulation framework to answer those questions:

<p align="center">
  <img src="https://github.com/COeXISTENCE-PROJECT/RouteRL/raw/main/docs/_static/logo.png" alt="drawing" width="150"/> 
</p>
[RouteRL](https://github.com/COeXISTENCE-PROJECT/RouteRL) Multi-Agent Reinforcement Learning framework for modeling and simulating the collective route choices of humans and autonomous vehicles 


along with other _tools and frameworks_ for the new class of urban routing games available on this public repositories [COeXISTENCE Project GitHub](https://github.com/COeXISTENCE-PROJECT)


---


#### 1. CAVs may form exclusive clubs

> We show that [Equilibria in routing games with connected autonomous vehicles will not be strong, as exclusive clubs may form](https://arxiv.org/pdf/2510.12862)

CAVs will be able to break from Nash equilibrium and form a coalitions, collaborating to devise a joint routing pattern, allowing them to arrive faster. However, with limited resources, i.e. the capacity in road networks, a
group arriving faster will gain at the expense of others, arriving later. Also, not everyone can be invited to join the group as remains efficient only until
some point. They will be exclusive, and ,as other exclusive goods, unavailable to masses and limited to upper classes only. Threatening equity of using public space of our cities.

<p align="center">
<img width="350" src="/./assets/img/overview.png" alt="drawing" class="responsive-logo"/>
</p>

#### 2. Creating travel time oscillations is a good strategy to maximise fleet market share

> We demonstrate the fleet may intentionally bring choas to our cities to maximise market share [here](arxiv)

What is the optimal strategy to maximise market share and convince most drivers to join own fleet? Surprisingly, **bringing chaos** may be quite effective. Controlled oscillations of traffic flows, predictable by fleet operator, surprising to humans may be frustrating enough to convince others to abandon human driving and join some fleet. Individually tailored offers (just like Uber, Amazon or Ryanair) leveraging on our behavioural traits may be exploitable as well, and our low expectations (due to low budget or high urgency) may enable network-wide strange assignment plans, ultimately leading to increasing market shares. Those are initial results from monopoly, where single operator competes with humans, strach pomyśleć co będzie when competing fleets launch aggressive campaigns deployed at our cities.

<p align="center">
<img width="350" src="/./assets/img/oscillations.jpg" alt="drawing" />
</p>

#### 3. Traffic assingnment be both Nash optimal and equilibrated with CAVs

> New concept of Wardrop Cyclical Equiblibruim is both optimal and fair for CAVs as we show [here](https://arxiv.org/pdf/2507.19675)

Connected and Autonomous Vehicles (CAVs) open the possibility for centralised routing with full compliance, making System Optimal traffic assignment attainable. However, as System Optimum makes some drivers better off than others, voluntary acceptance seems dubious. To overcome this issue, we propose a new concept of Wardropian cycles, which, in contrast to previous utopian visions, makes the assignment fair on top of being optimal, which amounts to satisfaction of both Wardrop's principles. Such cycles, represented as sequences of permutations to the daily assignment matrices, always exist and equalise, after a limited number of days, average travel times among travellers (like in User Equilibrium) while preserving everyday optimality of path flows (like in System Optimum). In Barcelona, 670 vehicle-hours of Price-of-Anarchy are eliminated using cycles with a median length of 11 days-though 5% of cycles exceed 90 days. 

<p align="center">
<img width="350" src="/./assets/img/grafika_latest.png" alt="drawing" />
</p>

#### 4. How to simulate such future system?

> We created [RouteRL](https://github.com/COeXISTENCE-PROJECT/RouteRL) Multi-Agent Reinforcement Learning framework for modeling and simulating the collective route choices of humans and autonomous vehicles - [SoftwareX](https://doi.org/10.1016/j.softx.2025.102279)
<p align="center">
  <img src="https://github.com/COeXISTENCE-PROJECT/RouteRL/raw/main/docs/_static/logo.png" alt="drawing" width="150"/> 
</p>

RouteRL is a novel framework that integrates multi-agent reinforcement learning (MARL) with a microscopic traffic simulation for the development of efficient collective route choice strategies for autonomous vehicles (AVs). The proposed framework models the daily urban route choices of driver agents of two types: human drivers, emulated using behavioral route choice models, and AVs, modeled as MARL agents optimizing their policies for a predefined objective. RouteRL aims to advance research in MARL, transport modeling, and human–AI interaction for transportation applications. 
  
<p align="center">
<img src="/./assets/img/RouteRL.jpg" height="400"/>
</p>

#### 5. Which (ML) algorithms are best for collective fleet routing?

> We introduced [URB](https://github.com/COeXISTENCE-PROJECT/URB) an Urban Routing Benchmark for MARL algorithms on the fleet routing tasks - [NIPS 2025](https://arxiv.org/abs/2505.17734)
<p align="center">
   <img src="https://github.com/COeXISTENCE-PROJECT/URB/blob/main/docs/urb.png" alt="drawing" width="150"/> 
</p>

 `URB` is a comprehensive benchmarking environment that unifies evaluation across **29 real-world traffic networks paired with realistic demand patterns**. `URB` comes with a catalog of **predefined tasks, multi-agent RL (MARL) algorithm implementations, three baseline methods, ten domain-specific performance metrics, and a modular configuration scheme**. 

Through this broad experimental scheme, `URB` aims to:

  1. Identify which state-of-the-art algorithms outperform others in this class of tasks,
  2. Drive competition for future algorithmic improvements, and
  3. Clarify the impact of collective CAV routing on congestion, emissions, and sustainability in future cities, equipping policymakers with solid arguments for CAV regulations.

<p align="center">
<img src="/./assets/img/urb_overview.png" height="400"/>
</p>



----



We want to understand the future of Urban Mobility and foresee what happens when our cities are shared with autonomous, intelligent robots - competing with us for limited resources. 
* We demonstrated the novel phenomena on simple topologies [here](https://www.nature.com/articles/s41598-025-90783-w)
* We created the dedicated MARL environment for our experiments [paper](https://arxiv.org/pdf/2502.20065) and repository on [GitHub](https://github.com/COeXISTENCE-PROJECT/RouteRL)
* We have some preliminary results from [EWRL](https://openreview.net/pdf?id=88zP8xh5D2)
* We identified issues with convergence and reported them [here](https://arxiv.org/pdf/2502.13188)

For updates and new contributions you may consult our [GitHub](https://github.com/COeXISTENCE-PROJECT) or follow us on social media. 

For collaborations, please contact us or simply start contributing on our repos.


<!---
. We create virtual environments where individual agents compete to arrive faster, more reliably and cheaper at their destinations.  Human agents are simulated with detailed behavioural models, estimated and calibrated on the field data to reproduce how we behave and adapt in the cities. In the same environment the deep learning agents try the same - they  use deep reinforcement learning to maximise their rewards. This creates a harsh competition in which machines have upper-hands strong enough to beat us. 



*COeXISTENCE* is a broad and deep experiment in virtual environment on future cities, aimed to discover the new phenomena and propose the new solutions. See the brief overview [here](https://raw.githubusercontent.com/RafalKucharskiPK/rafalkucharskipk.github.io/master/assets/pdf/flyer.pdf) and more thorough [presentation](https://raw.githubusercontent.com/RafalKucharskiPK/rafalkucharskipk.github.io/master/assets/pdf/Wyklad_ERC.pdf).

It spans between fields as diverse as:

* game theory;
* deep reinforcement learning;
* complex social systems;
* sustainability;
* urban mobility;
* agent based modelling;
* discrete choice theory.
--->

<p align="center">
<img src="/./assets/img/LOGO-ERC.jpg" alt="drawing" height="220"/><img src="/./assets/img/logo_kwadrat.jpg" alt="drawing" height="220"/>
</p>

----

### Vacancies

Our team is happily full at the moment, yet we are always happy to collaborate.

Nonetheless, we welcome Master Students, Visiting Professors (funded short term visits) or prospective PhD students in this project's ecosystem. 

Feel free to reach us out to understand more about opportunities at **coexistence@uj.edu.pl**

----


<sub>**Disclaimer**: Funded by the European Union. Views and opinions expressed are however those of the author(s) only and do not necessarily reflect those of the European Union or European Research Council Executive Agency (ERCEA). Neither the European Union nor the granting authority can be held responsible for them.</sub>

<sub>**Funding acknowledgement**: This project has received funding from the European Research Council (ERC) under the European Union’s Horizon Europe research and innovation programme  (grant agreement No 101075838).</sub>

