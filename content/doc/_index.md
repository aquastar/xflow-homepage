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
from xflow.dataset import cora, random, ba
from xflow.diffusion import ic, si
from xflow.seed import random, degree, eigen
from xflow.method.im import celf, sigma

# graphs to test
gs = [cora, random, ba]

# diffusion models to test
df = [ic, si]

# seed configurations to test
se = [random, degree, eigen]

# methods to test
me = [celf, sigma, imrank]

# configurations of experiments
rt = run(graph=gs, diffusion=df, seed=se, method=me, eval='im', epoch=10, output=['animation', 'csv', 'fig'])
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
