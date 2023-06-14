---
title: Diffusion
date: '2021-01-01'
type: book
weight: 20
---

Introduction to diffusion models

<!--more-->

Various diffusion models employ distinct mechanisms to depict the process by which a vertex is stimulated from an inactive state, under the influence of its neighboring vertices.

The independent cascade (IC) [^1] and linear threshold (LT) [^2] models are the most commonly used and well-studied progressive models. Well-known non-progressive models include the susceptible-infected (SI) model, the susceptible-infected-removed (SIR) model, and susceptible-infected-susceptible (SIS) models [^3]. The ongoing stage of XFlow will encompass the evaluation of IC, LT, and SI as the principal diffusion models, with intentions to integrate supplementary models in subsequent stages as expounded below. The diffusion model of IC, LT and SI is implemented by Network Diffusion Library (NDLib) [^4]. Take SI as example, NDLib implementation looks like:

```python
import networkx as nx
import ndlib.models.ModelConfig as mc
import ndlib.models.epidemics as ep

# Network topology
g = nx.erdos_renyi_graph(1000, 0.1)

# Model selection
model = ep.SIModel(g)

# Model Configuration
cfg = mc.Configuration()
cfg.add_model_parameter('beta', 0.01)
cfg.add_model_parameter("fraction_infected", 0.05)
model.set_initial_status(cfg)

# Simulation execution
iterations = model.iteration_bunch(200)
```

In use of XFlow, the user can call
```python
from xflow.diffusion import si

####
# some code here
####

# configurations of experiments
rt = run(graph=gs, diffusion=si, seed=se, method=me, eval='im', epoch=10)
```

### Other models
There also exist many variants of SIR models, including
SEIR extends the basic SIR model by introducing an additional compartment called "Exposed" (E);
SIRS where individuals can transition back to the susceptible state after recovering from the infection;
SIRD model expands upon the SIR model by including a compartment for "Dead" (D) individuals;
SEIRS model combines the features of the SEIR and SIRS models by including an exposed compartment and allowing individuals to become susceptible again after recovery.

It should be noted that most current diffusion models fall under the category of mean-field style, wherein each entity exhibits identical diffusion behavior. Nevertheless, the personalized diffusion model provides a more comprehensive representation of real-life interactions, yet it is frequently disregarded [^5].

[^1]: [IC paper](https://link.springer.com/article/10.1023/A:1011122126881)
[^2]: [LT paper](https://www.journals.uchicago.edu/doi/abs/10.1086/226707)
[^3]: [SI paper](https://royalsocietypublishing.org/doi/abs/10.1098/rspa.1927.0118)
[^4]: [NDLib](https://ndlib.readthedocs.io/en/latest/)
[^5]: [Personalized Propagation](https://dl.acm.org/doi/abs/10.1145/2505515.2505571)