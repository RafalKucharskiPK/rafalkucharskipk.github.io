---
layout: project
project: OPUS
title: PostCorona Shared Mobility
description: Ride-pooling research studies and contribution
img: assets/img/NCN logo poziom.jpg
importance: 1
category: grants
---

<p align="center">
<img src="/./assets/img/p_opus/opus.jpg" alt="drawing" height="400"/>
</p>

> Modelling and controlling virus spread processes in shared mobility networks 2021-2024, 1mln PLN funded by National Science Centre under scheme OPUS 19

<p align="center">
<img src="/./assets/img/rp.jpg" width="350"/>
</p>

Ride-pooling is a complex topic that incorporates various research branches.
It combines perspctives of operations research, stochastic analysis, choice modelling, agent-based models, network science, epidemiology etc.
Rafał Kucharski started research on this topic at **TU Delft** with prof. Oded Cats and continued at Jagiellonian University, mainly with **Michał Bujak**.

The contributions to this field are as follows.

* [Development of an utility-based, strategic aglorithm for solving ride-pooling problem (ExMAS)](Utility-based,-strategic-algorithm)   <!-- exact-matching-of-attractive-shared-rides-(ExMAS)-for-system-wide-strategic-evaluations) -->
* [Study on the potential of the service based on NYC historic data](ride-pooling-potential)
* [Insights into accumulation and distribution of experienced delay among co-travellers](compounding-delay)
* [Analysis of emergence, topological properties, and introduction of udnerlying network structures](Networks-emergence,-properties,-and-new-representations) <!--(network-structures-of-urban-ride-pooling-problems-and-their-properties) -->
* [Recognition of variables determining pandemic risk within the ride-pooling service](modelling-virus-spreading)
* [Proposition of a virus preventing strategy which maintains high system efficiency](virus-mitigation-in-an-efficient-system)
* [Insights into the impact of the behavioural heterogeneity on the service performance](impact-of-the-behavioural-heterogeneity)
* [Development of a personalised pricing strategy that balances profit and travfeller acceptance](personalised-pricing)
* [Proposition of an extended pricing policy that incorporates trait learning and long-term loyalty](adaptive-pricing)



## Utility-based, strategic algorithm
> Kucharski, Rafał, and Oded Cats. "Exact matching of attractive shared rides (ExMAS) for system-wide strategic evaluations." Transportation Research Part B: Methodological 139 (2020): 285-310.

The premise of ride-sharing is that service providers can offer a discount, so that travellersare compensated for prolonged travel times and induced discomfort, while still increasingtheir revenues. While recently proposed real-time solutions support online operations, al-gorithms to perform strategic system-wide evaluations are crucially needed. We proposean exact, replicable and demand-, rather than supply-driven algorithm for matching tripsinto shared rides. We leverage on delimiting our search for attractive shared rides only,which, coupled with a directed shareability multi-graph representation and efficient graphsearches with predetermined node sequence, narrows the (otherwise exploding) search-space effectively enough to derive an exact solution. The proposed utility-based formula-tion paves the way for model integration in travel demand models, allowing for a cross-scenario sensitivity analysis, including pricing strategies and regulation policies.

<p align="center">
<img src="/./assets/img/exmas.jpg" width="600"/>
</p>

## Ride-pooling potential
> Shulika, Olha, Michał Bujak, Farnoud Ghasemi, and Rafał Kucharski. "Spatiotemporal variability of ride-pooling potential–Half a year New York City experiment." Journal of Transport Geography 114 (2024): 103767.

Ride-pooling systems, despite being an appealing urban mobility mode, still struggle to gain momentum. While we know the significance of critical mass in reaching system sustainability, less is known about the spatiotemporal patterns of system performance. Here, we use 1.5 million NYC taxi trips (sampled over a six-month period) and experiment to understand how well they could be served with pooled services. We use an offline utility-driven ride-pooling algorithm and observe the pooling potential with six performance indicators: mileage reductions, travellers' utility gains, share of pooled rides, occupancy, detours, and potential fleet reduction. We report distributions and temporal profiles of about 35 thousand experiments covering weekdays, weekends, evenings, mornings, and nights. We report complex spatial patterns, with gains concentrated in the core of the network and costs concentrated on the peripheries. 

<p align="center">
<img src="/./assets/img/nyc.jpg" width="500"/>
</p>

## Compounding delay
> Kucharski, Rafał, Andres Fielbaum, Javier Alonso-Mora, and Oded Cats. "If you are late, everyone is late: late passenger arrival and ride-pooling systems' performance." Transportmetrica A: Transport Science 17, no. 4 (2021): 1077-1100.

Sharing rides in on-demand systems allow passengers to reducetheir fares and service providers to increase revenue, though at thecost of adding uncertainty to the system. Notably, the uncertaintyof ride-pooling systems stems not only from travel times but alsofrom unique features of sharing, such as the dependency on otherpassengers’ arrival time at their pick up points. In this work, we theo-retically and experimentally analyse how late arrivals at pick up loca-tions impact shared rides’ performance. We find that the total delayis equally distributed among sharing passengers. However, delaycomposition gradually shifts from on-board delay only for the firstpassenger to waiting delay at the origin for the last passenger. Sadly,trips with more passengers are more adversely impacted. Strate-gic behaviour analysis reveals Nash equilibria that might emerge.We analyse the system-wide effects and find that when latenessincreases passengers refrain from sharing and eventually opt-out.

<p align="center">
<img src="/./assets/img/late.jpg" width="500"/>
</p>

## Networks emergence, properties, and new representations
> Bujak, Michal, and Rafal Kucharski. "Network structures of urban ride-pooling problems and their properties." Social Network Analysis and Mining 13, no. 1 (2023): 89.

Graph (network) structures, starting with the seminal paper by Santi et al. (2014), were the algorithmic backbone of the proposed algorithms. Various methods introduce ride-pooling travellers and drivers as nodes in simple and bipartite representations. Network algorithms were leveraged to find optimal results. Although networks were an intermediate tool, neither their emergence nor their properties had been studied so far. In the this article, for the first time, we formalised four distinct network structures within ride-pooling. We introduce new, weighted representations that contain more information, based on stochastic analysis. To understand the role of the topologies of ride-pooling networks, we studied the correlation between a sharing discount (the control variable), network properties, and system performance indicators. Our analysis highlighted the existence of a critical mass embedded in network topology. This means that based on certain topological properties, we can assess the demand level required for the ride-pooling to become efficient.

<p align="center">
<img src="/./assets/img/nets.jpg" width="400"/>
</p>

## Modelling virus spreading
> Kucharski, Rafał, Oded Cats, and Julian Sienkiewicz. "Modelling virus spreading in ride-pooling networks." Scientific Reports 11, no. 1 (2021): 7201.

The potential of ride-pooling rides to serve as a safe and effective alternative given the personal and public health risks considerations associated with the COVID-19 pandemic is hitherto unknown. To answer this, we combine epidemiological and behavioural shareability models to examine spreading among ride-pooling travellers, with an application for Amsterdam. Findings are at first sight devastating, with only few initially infected travellers needed to spread the virus to hundreds of ride-pooling users. Without intervention, ride-pooling system may substantially contribute to virus spreading. Notwithstanding, we identify an effective control measure allowing to halt the spreading before the outbreaks (at 50 instead of 800 infections) without sacrificing the efficiency achieved by pooling. Fixed matches among co-travellers disconnect the otherwise dense contact network, encapsulating the virus in small communities and preventing the outbreaks.

<p align="center">
<img src="/./assets/img/model.jpg" width="650"/>
</p>

## Virus mitigation in an efficient system
> Proszewska, Magdalena, Michał Bujak, Rafał Kucharski, Marek Śmieja, and Jacek Tabor. "Optimising network efficiency in the epidemic scenario." Available at SSRN 4976648 (2024).

Efficiency of a system network often relies on high connectivity. However, strongly connected networks are vulnerable in a case of a spreading virus. In the study, we propose a clustering method which balances the two opposing factors: maintains a high system efficiency yet minimises the spreading potential. Our Deep Epidemic Efficiency Network (DEEN) model leverages Graph Convolutional Neural Networks and a novel loss function. In an unsupervised setting, we seek a partition that maximises the system utility while restraining the transmission rate to a desired level. We show that proposed method successfully solves three reallife problems: ride-pooling service in New York City, economic exchange between regions in Poland, and information sharing via peer-to-peer network.

<p align="center">
<img src="/./assets/img/gnn1.jpg" width="245.3"/>
<img src="/./assets/img/gnn2.jpg" width="250"/>
</p>

## Impact of the behavioural heterogeneity
> Bujak, Michał, and Rafał Kucharski. "Ride-pooling service assessment with heterogeneous travellers in non-deterministic setting." Transportation (2024): 1-24.

Certain aspects of a trip, such as distance, travel time, and waiting time, are physical measures known to an operator. However, how these characteristics influence the perception of an individual traveller, expressed via utility equations, is subject to their individual behavioural traits, such as value-of-time and willingness-to-share. These traits are typically latent to the operator. In most studies, authors simplify the setting and assume that the population is homogeneous. This leads to deterministic utility equations with constant and homogeneous parameters.
Population diversity and model uncertainty remain uncaptured, which leads to a high cancellation rate. As a result, ride-pooling systems often do not reach critical mass which limits their profitability and ultimately leads to failure.

As we show in this study, the assumption that population is homogeneous in value-of-time and willingness-to-share results in an underperforming system (cancellation rate over one-third). In utility equations, it is crucial to recognise heterogeneous characteristics. Many travellers, with high time sensitivity and/or who are more reluctant towards sharing, reject proposed pooled rides. On the other hand, many clients who gladly sacrifice their travel time for monetary savings are discarded as potential co-travellers. We extend the utility equations to allow for diverse population characteristics. We employ Monte Carlo stochastic analysis to show that heterogeneity yields significantly different modelling results compared to the baseline. The key performance indicators of the system change: the savings in mileage are lower, while the gains in utility for travellers are greater. As another highlight of the study, we used the network representations introduced in our earlier research to find travellers who are crucial to service performance.

<p align="center">
<img src="/./assets/img/het1.jpeg" width="180"/>
<img src="/./assets/img/het2.jpeg" width="176"/>
<img src="/./assets/img/het3.jpeg" width="179"/>
<img src="/./assets/img/het4.jpeg" width="197"/>
</p>


## Personalised pricing
> Bujak, Michał, and Rafał Kucharski. "Balancing Profit and Traveller Acceptance in Ride-Pooling Personalised Fares." arXiv preprint arXiv:2411.03370 (2024).

Certain travellers, whose trips are long and well aligned with other clients, are particularly valuable to the operator.
To ensure they are satisfied with the offer, the operator is inclined to offer a higher discount.
In our second study on heterogeneity [M4], we develop a stochastic framework for the assessment of pricing policies and propose a personalised pricing method.
Based on an external preference study, we derive and use a population distribution of the value-of-time and the willingness-to-share (penalty-for-sharing).
We assume that the operator does not know the individual traits of clients, yet applies the population distribution for calculations.
We introduce an acceptance probability function which, for a given sharing discount level, determines how likely a traveller is to accept a shared ride.
On top of the acceptance probability, we examine the resulting acceptance and rejection configurations along with the associated revenues and costs given by a pricing policy.
This framework helps us to mimic a real world scenario where heterogeneous behavioural preferences are latent and can be assessed solely in a probabilistic setting.
Next, we propose a personalised pricing policy.
We dissect the process into two levels which, as we rigorously prove, leads to efficient and optimal results.
We introduce the expected profitability measures that incorporates travellers' perspective into economic assessment by the operator.
Our method successfully recognises contribution of individuals to the system.
As we show in a numerical analysis, our method not only maximises the expected profitability in the system but also encourages compound rides and results in a high acceptance rate.
Compared to other pricing policies, it proves to be superior in economic and environmental aspects, and leads to higher attractiveness for travellers.

<p align="center">
<img src="/./assets/img/ind.jpeg" width="400"/>
</p>


## Adaptive pricing
> Bujak, Michał, and Rafał Kucharski. "Adaptive Optimisation of Ride-Pooling Personalised Fares in a Stochastic Framework." arXiv preprint arXiv:2508.20723 (2025).

Although the personalised pricing algorithm maximises the short-term profitability of the service, it does not address the long-term consequences. A satisfied client is more likely to remain loyal to the operator and requests rides more often. The long-term demand acquisition is vital to ensure that the ride-pooling critical mass is reached and maintained. However, so far researchers have focused solely on a single-day operations where role of the long-term attraction and loyalty was neglected. In this study, we propose a pricing policy to support the operator who aims to learn individual parameters and attract travellers while providing an efficient service. In this explore-exploit setting, we need to balance the short- and long-term perspective to attain all goals. We propose an adaptive personalised pricing model with Bayesian inference of individual behavioural traits. Taking the role of the operator, we enrich our objective function in the personalised discounts optimisation. Our method supplements the pricing optimisation with additional components which ensure the long-term demand attraction. While conducting day-to-day operations, we observe travellers' choices (who either accept or reject our offer) and increase operator's knowledge. We estimate current satisfaction (loyalty) levels and, by adopting the S-shaped learning curve, assess future value of a client in a stochastic setting. To uncover individual traits of travellers, we employ Bayesian learning which allows for a stronger personalisation. The proposed pricing policy provides good economic indicators since day one, attracts more clients daily, and generates more satisfaction among travellers.

<p align="center">
<img src="/./assets/img/ada.jpeg" width="400"/>
</p>


[See](https://rafalkucharskipk.github.io/assets/pdf/Merit%20report%20OPUS%2019.pdf) main achievements, results and impact of our project.
