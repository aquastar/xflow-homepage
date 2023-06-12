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
You may install from pip
```shell
pip install networkx ndlib xflow-net
```
for xflow, you can also install from github
```shell
pip install xflow-net
```


## The First Example


```python
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
