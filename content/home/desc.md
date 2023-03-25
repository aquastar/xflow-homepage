---
widget: blank
headless: true

# ... Put Your Section Options Here (title etc.) ...
title: 
subtitle:
weight: 20  # section position on page

design:
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns: '1'
---

<script async defer src="https://buttons.github.io/buttons.js"></script>


<a class="github-button" href="https://github.com/aquastar/xflow" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star XFlow">Star XFlow</a>
<a class="github-button" href="https://github.com/aquastar/awesome-network-flow" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star Awesome Network Flow">Star Awesome Network Flow</a>

Xflow is a python library for design network flow problems.


* [Spreading Task](#spreading-task)
* [Backtracking Task](#backtracking-task)
* [Diffusion Learning Task](#diffusion-learning-task)
* [Explanability Task](#explanability-task)
* [Installation](#installation)



# Spreading Task 

[comment]: <> (put NIB here)

```python
# Example of code highlighting
input_string_var = input("Enter some data: ")
print("You entered: {}".format(input_string_var))
```


selected variants

- (max/min/understand/predict coverage, given diffusion process and starting nodes)
- important concept: ***Reverse Reachable Sets (RR set), K-core decomposition***
- IM and variants (node)
- simulation-based, proxy/heuristic based, sketch based
- Dynamic Influence Maximization, Competitive Influence Maximization
- competitive IM vs network interdiction
    - 2 or more competitors can remove/add edges or change nodes

    [](https://journals.aps.org/pre/pdf/10.1103/PhysRevE.105.044311)
    
## Benchmarks

## Implemented Baselines

## Evaluation

## Create your own models
    


# Backtracking Task

selected variants

[comment]: <> (write)


- (identify starting nodes, given diffusion process and coverage)
- If diffusion is not given
- Source Identification, or Identification of influential spreaders

## Benchmarks

## Implemented Baselines

## Evaluation

## Create your own models




# Diffusion Learning Task

selected variants

- Min-cost Max-Flow (edge), network simplex

## Benchmarks

## Implemented Baselines

## Evaluation

## Create your own models




# Explanability Task


[comment]: <> (write)


## Benchmarks

## Implemented Baselines

## Evaluation

## Create your own models


## physical flow

traffic 




# Installation

XFlow is available for Python 3.7 to Python 3.10.

### Pip Wheels

We alternatively provide pip wheels for all major OS/PyTorch/CUDA combinations, see [here](https://data.XFlow.org/whl).

For additional but optional functionality, run

```
pip install torch_cluster torch_spline_conv -f https://data.XFlow.org/whl/torch-1.12.0+${CUDA}.html
```


