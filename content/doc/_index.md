---
title: Quick Start
linkTitle: Quick Start
summary: An example of using Wowchemy's Book layout for publishing online courses.
date: '2021-01-24'
type: book
tags:
  - 
---


{{< toc hide_on="xl" >}}

<!-- ## What you will learn in this page

- Installation 
- The first example -->
<!-- - {{<hl>}}Statistical concepts{{</hl>}} and how to apply them in practice
- Gain experience with the {{<hl>}}Scikit{{</hl>}}, including data visualization with {{<hl>}}Plotly{{</hl>}} and data wrangling with {{<hl>}}Pandas{{</hl>}} -->

## Installation
You may install XFlow library by pip
```shell
pip install xflow-net
```


## The First Example


```python
import xflow
from xflow.dataset.nx import BA, connSW
from xflow.dataset.pyg import Cora
from xflow.diffusion import SI, IC, LT
from xflow.seed import random as seed_random, degree as seed_degree, eigen as seed_eigen
from xflow.util import run

# graphs to test
fn = lambda: connSW(n=1000, beta=0.1)
fn.__name__ = 'connSW'
gs = [Cora, fn, BA]

# diffusion models to test
df = [SI, IC, LT]

# seed configurations to test
se = [seed_random, seed_degree, seed_eigen]

# run

# configurations of IM experiments
from xflow.method.im import pi as im_pi, degree as im_degree, sigma as im_sigma, celfpp as im_celfpp, greedy as im_greedy
me = [im_pi]
rt = run (
    graph = gs, diffusion = df, seeds = se,
    method = me, eval = 'im', epoch = 10, 
    budget = 10, 
    output = [ 'animation', 'csv', 'fig'])
```

<!-- {{< figure src="featured.jpg" >}} -->

## Documentation Structure

{{< figure src="xflow_framework.jpg" caption="Analysis Framework" numbered="true"  width="500">}}


The proposed analysis framework shown above includes five factors: source node set $\Omega$, activated sub-graph $\sigma$, graph structure $G$, diffusion model $D$, and flow routing $\mathcal{F}$. A graph flow problem designates some factors as the input while some other factors act as the output, and thereby it is possible to deduce the remaining factors based on the partial factors.

| Flow Tasks | Explicit Input               | implicit Input                        | Output           |
|-------------------|-----------------------------------------|-------------------------------------------------|----------------------------|
| IM                | graph  $G$                     | diffusion  $D$                             | seed set $\Omega$          |
| IBM               | graph  $G$, seed set $\Omega$  | diffusion  $D$                             | graph  $\Delta G$ |
| SL                | observation $\sigma$                    | graph  $G$, diffusion  $D$        | seed set $\Omega$          |
| Diffusion Pattern | seed set $\Omega$, observation $\sigma$ | graph  $G$, flow routing $\mathcal{F}$ | diffusion  $D$        |
| Path Study        | seed set $\Omega$, observation $\sigma$ | graph  $G$, diffusion  $D$        | flow routing $\mathcal{F}$ |


Three tasks were implemented to demonstrate our proposed framework, including influence maximization (IM), influence blocking maximization (IBM), and source localization (SL). They are formally identified below according to the framework presented above. Table above summarizes those three and some possible future tasks that can be included in the framework, and detailed formulations are elaborated below.

{{< list_children >}}

<!-- ## Meet your instructor

{{< mention "admin" >}} -->

<!-- ## FAQs

{{< spoiler text="Are there prerequisites?" >}}
There are no prerequisites for the first course.
{{< /spoiler >}}

{{< spoiler text="How often do the courses run?" >}}
Continuously, at your own pace.
{{< /spoiler >}}

{{< cta cta_text="Begin the course" cta_link="python" >}} -->
