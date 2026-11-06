---
layout: page
abstract_page: true
title: "Optimization for Transportation Planning and Periodic Task Scheduling: Rail Freight Crew Management under Train Delays, Line Planning, and Balanced Assignments"
permalink: /abstracts/2026/10-22-heloise-gachet/
---

**Speaker:** Héloïse Gachet  
**Date:** Thursday 22 October 2026

## Abstract

This thesis investigates optimization problems arising in transportation planning and periodic task scheduling, combining integer programming, combinatorial optimization, and stochastic modeling, with a strong application focus on rail freight operations at SNCF.

The first contribution addresses the crew management problem for rail freight drivers at SNCF: given periodic tasks (trains to be driven), we aim to build optimal cyclic rosters covering all tasks, while complying with numerous rules and regulations. Current industrial practice, motivated by a full body of literature, decomposes this problem into two sequential stages: first, the construction of duties (daily task sequences assigned to a single driver), then their organization into cyclic rosters.

This sequential approach introduces structural suboptimalities and makes it difficult to account for train delays. This work proposes first a deterministic integrated model formulated as a set-covering integer linear program and solved by column generation. The pricing subproblem is modeled as a Resource-Constrained Shortest Path (RCSP) problem on an acyclic graph and solved using a label correcting algorithm with additional speeding-up strategies.

Numerical experiments on real SNCF instances demonstrate significant cost reductions compared to the sequential pipeline. Building on this deterministic framework, we then extend the problem to account for train delays. A fragility score is introduced to measure the sensitivity of a roster to train delays: as exogenous delays arise and propagate within each duty, this score measures the expected number of disrupted trains and duties that would be operated by backup drivers in practice. This stochastic crew management problem then builds optimal cyclic rosters covering all trains, with an additional threshold constraint on the expected fragility. The corresponding model is solved by column generation with an enriched RCSP pricing subproblem that handles delay distributions. Results confirm that the integrated stochastic approach outperforms the current two-stage sequential approach at SNCF, both in terms of cost and robustness to disruptions.

Shifting to a different application domain, the second contribution of this work tackles the line planning problem in public transit networks. Given a passenger origin-destination demand matrix and a pool of candidate lines, the goal is to select lines and assign integer frequencies so as to minimize passengers' travel time, subject to budget and capacity constraints. A Dantzig-Wolfe reformulation of an arc-based model on a "change-and-go network" is solved with branch-and-price-and-cut. Numerical experiments compare the straightforward resolution of the arc-based model with the proposed algorithm.

Finally, the third contribution takes a more theoretical perspective and studies balanced assignments of periodic tasks, i.e., such that each worker performs every task with the same frequency over the long term. A structural connection is established between the existence of such assignments and properties of arc-colored Eulerian directed graphs. Existence and periodicity theorems, bounds on the minimal period, and complexity results are established, for a basic version first, then for an extended version introducing additional constraints.
