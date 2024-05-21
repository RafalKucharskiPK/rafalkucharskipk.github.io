---
layout: project
title: modelling
description: Simulation of rerouting phenomena in Dynamic Traffic Assignment with the Information Comply Model
img: assets/img/ICM.png
importance: 5
category: varia
---

**Dynamic User Equilibrium well defines stable state of urban traffic network, but what if something unexpected happens? We propose a model, embedded in production-ready DTA solutions of PTV SISTeMA.**

Stream of papers with _Guido Gentile (La Sapienza)_ after wonderful years of cooperation with _PTV SISTeMA_ team in Rome during my PhD, summarized with this [paper](https://doi.org/10.1016/j.trb.2018.12.001) summed up with [this](https://www.iamigniting.com/rafal_kucharski/) nice coverage 

<center><img src="{{ site.baseurl }}/assets/img/ICM.png"></center>
<div class="col three caption">
    Figure 1: 
</div>

We present the Information Comply Model (ICM) which extends the framework for macroscopic within-day DTA proposed by Gentile (2016) to represent the rerouting of drivers wrt a single traffic event. Rerouting is reproduced as a two-stage process: first, drivers
become aware about the event and its consequences on traffic; second, drivers may decide to change path. At each arc, unaware drivers have a probability of being informed by multiple ATIS sources (radio, VMS, mobile apps), which depends not only on devise
penetration rates, but also on users space and time coordinates wrt the position and interval of the event. At each node, aware drivers, who are somehow reluctant to change, may finally modify their path based on a random rerouting utility, which is composed of expected gains and avoided losses. ICM is thus capable of representing the evolution of rerouting phenomena in time and space when the information about a traffic event and
its consequences on congestion spread among drivers and onto the network.

This way, ICM extends the concept of dynamic user equilibrium to a case of imperfect information related to availability and awareness rather than to individual perception, as well as to a case of bounded rationality with prudent drivers. Besides the model architecture and specification, this paper provides a workable methodology which can be applied both off-line for transport planning and in real-time for traffic management on large size networks.
