# VRP-Project--Tian
VRP Project at Columbia

## Introduction to VRP
In the Vehicle Routing Problem (VRP), the goal is to find optimal routes for multiple vehicles visiting a set of locations. (When there's only one vehicle, it reduces to the Traveling Salesperson Problem.)

But what do we mean by "optimal routes" for a VRP? One answer is the routes with the least total distance. However, if there are no other constraints, the optimal solution is to assign just one vehicle to visit all locations, and find the shortest route for that vehicle. This is essentially the same problem as the TSP.

A better way to define optimal routes is to minimize the length of the longest single route among all vehicles. This is the right definition if the goal is to complete all deliveries as soon as possible. The VRP example below finds optimal routes defined this way.


## Literature Review

VRP has a long history, but only recently people start to apply RL into this problem. Papers on VRP have been published by well-known riding APPs including Didi, Uber.

### Efficient Collaborative Multi-Agent Deep Reinforcement Learning for Large-Scale Fleet Management

https://arxiv.org/pdf/1802.06444.pdf

#### Abstract

Large-scale online ride-sharing platforms have substantially transformed our lives by reallocating transportation resources
to alleviate traffic congestion and promote transportation efficiency. An efficient fleet management strategy not only can significantly
improve the utilization of transportation resources but also increase the revenue and customer satisfaction. It is a challenging task to
design an effective fleet management strategy that can adapt to an environment involving complex dynamics between demand and
supply. Existing studies usually work on a simplified problem setting that can hardly capture the complicated stochastic demand-supply
variations in high-dimensional space. In this paper we propose to tackle the large-scale fleet management problem using reinforcement
learning, and propose a contextual multi-agent reinforcement learning framework including three concrete algorithms to achieve
coordination among a large number of agents adaptive to different contexts. We show significant improvements of the proposed
framework over state-of-the-art approaches through extensive empirical studies

#### My Conclusion on This Paper

1. One key challenge in ride-sharing platforms is to balance the demands and supplies, i.e., orders of the passengers and drivers available for picking up orders. 

2. Major supervised Learning methods for allocation policy are not ideal because changes in an allocation policy will impact future demand-supply, and it is hard for supervised learning approaches to capture and model these real-time changes.

3. Recent years witnessed tremendous success in deep reinforcement learning (DRL) in modeling intellectual challenging decision-making problems [9], [10], that were previously intractable. In the light of such advances, in this paper we propose a novel DRL approach to learn highly efficient allocation policies for fleet management.

4. The goal of the management is to maximize the gross merchandise volume (GMV: the value of all the orders served) of the platform by repositioning available vehicles to the locations with larger demand-supply gap than the current one. 

5. Using DNN + Q-Learning
