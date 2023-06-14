---
title: Task
date: '2021-01-01'
type: book
weight: 10
highlight: true
tags:

---
List of Benchmark Tasks

<!--more-->
Tasks are list below with implemented baselines.

## Influence Maximization

Given the graph structure information $G = (V, E, A)$ as the input and a pre-defined seed budget $k\in \mathbb{N}^{+}$, IM methods attempt to optimize the selection of a $k$-sized source node set $\Omega$ to maximize the expected influence spread $|\sigma(\Omega)|$ which is the size of the final activated subgraph $\sigma(\Omega)$. Except for the heuristic methods such as PageRank, degree, and eigen-centrality, the simulation-based and proxy-based methods also require a known diffusion model $D$ such as IC, LT, SI, or SIR. Thus, when the budget requirement is met ($|\Omega| = k$), IM aims at finding a seed set $\Omega$ such that:
{{< math >}}
$$
    \Omega = argmax_{\Omega^*}|\sigma(\Omega^*|G, D)|.
$$
{{< /math >}}

### Baselines
- simulation: [greedy](https://dl.acm.org/doi/10.1145/956750.956769), [CELF](https://dl.acm.org/doi/abs/10.1145/1281192.1281239), and [CELF++](https://dl.acm.org/doi/10.1145/1963192.1963217), 
- proxy: [PI ($\pi$)](https://ojs.aaai.org/index.php/AAAI/article/view/21694), [sigma](https://ieeexplore.ieee.org/document/8661648), degree, and [eigen-centrality](https://en.wikipedia.org/wiki/Eigenvector_centrality)
- sketch: [RIS](https://epubs.siam.org/doi/abs/10.1137/1.9781611973402.70), [SKIM](https://dl.acm.org/doi/10.1145/2661829.2662077), [IMM](https://dl.acm.org/doi/10.1145/2723372.2723734) 
       
## Blocking Maximization

IBM problem can be either against a set of known diffusion seeds or to prevent any future diffusion on the network. On the one hand, when graph structure $G = (V, E, A)$, diffusion model $D$, and the seed set $\Omega$ are known inputs, an IBM method aims to find part of $G$, namely $\Delta G$ such that the expected influence spread $|\sigma(\Omega)|$ is minimized if $\Delta G$ is blocked before the diffusion starts. Note that $\Delta G$ can be a set of nodes or edges, and there is usually a budget constraining the size of $\Delta G$. On the other hand, if the diffusion seed set is unknown, the goal of an IBM method is to minimize the expected influence spread of any diffusion starting from any set of seeds. This is usually achieved by removing $\Delta G$ from $G$ to weaken its connectivity. Annotating $G_{new} = G - \Delta G$, we have
{{< math >}}
$$
    \Delta G = argmin_{\Delta G^*}|\sigma(\Omega|G_{new}, D)|
$$
{{< /math >}}

### Baselines
- [greedy](https://dl.acm.org/doi/10.1145/956750.956769)
- [PI ($\pi$)](https://ojs.aaai.org/index.php/AAAI/article/view/21694)
- [sigma](https://ieeexplore.ieee.org/document/8661648)
- [eigen-centrality](https://en.wikipedia.org/wiki/Eigenvector_centrality)
- degree
  
## Source Localization

Given a snapshot of graph $G = (V, E, A)$ as the observation of the diffusion status at a certain time, the activated subgraph $\sigma$ of the snapshot is the propagation result of an unknown seed set $\Omega$. The goal of an SL method is to find out $\Omega$ based on the activated subgraph $\sigma$, the graph structure $G$, and the diffusion model $D$. It is achieved by finding the most likely seed set resulting in the activated subgraph $\sigma$.
{{< math >}}
$$
    \Omega = argmax_{\Omega^*}Pr(\Omega^*|\sigma, G, D)
$$
{{< /math >}}

### Baselines
- [NETSLEUTH](https://ieeexplore.ieee.org/document/6413787) (Legacy and Fast versions)
- [Jordan Centrality](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=7913632)
- [LISN](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8697898)

{{< callout note >}}
## Planned Extension
- Comparative Influence Maximation
- Dynamic Influence Maximization
- Percolation and Synchronization
- Computational Fluid Mechanism
- Multilayer Dynamics
- Higher-order Dynamics (hypergraph and simplicial complex)
- Multi-Flow
{{< /callout >}}

