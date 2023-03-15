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

# Table of Content 
* [Spreading Task](#spreading-task)
* [Backtracking Task](#backtracking-task)
* [Diffusion Learning Task](#diffusion-learning-task)
* [Explanability Task](#explanability-task)
* [Installation](#installation)

{{< icon name="terminal" pack="fas" >}} Terminal  
{{< icon name="python" pack="fab" >}} Python  
{{< icon name="github" pack="fab" >}} R

<script src="https://gist.github.com/aquastar/d56d90865c578621eee10958ded7e7f9.js"></script>




{{< math >}}
$$
\gamma_{n} = \frac{ \left | \left (\mathbf x_{n} - \mathbf x_{n-1} \right )^T \left [\nabla F (\mathbf x_{n}) - \nabla F (\mathbf x_{n-1}) \right ] \right |}{\left \|\nabla F(\mathbf{x}_{n}) - \nabla F(\mathbf{x}_{n-1}) \right \|^2}
$$
{{< /math >}}

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


# Multilayer

- percolation
- synchronization

Question: main-stream task of single and multilayer network has little overlap. So they can be extended to each other.

## Benchmarks

## Implemented Baselines

## Evaluation

## Create your own models




# Installation

XFlow is available for Python 3.7 to Python 3.10.

### Pip Wheels

We alternatively provide pip wheels for all major OS/PyTorch/CUDA combinations, see [here](https://data.XFlow.org/whl).

For additional but optional functionality, run

```
pip install torch_cluster torch_spline_conv -f https://data.XFlow.org/whl/torch-1.12.0+${CUDA}.html
```


## Cite

Please cite [our paper](https://arxiv.org/abs/1903.02428) (and the respective papers of the methods used) if you use this code in your own work:

```
@inproceedings{XXX,
  title={XXX},
  author={XXX},
  booktitle={XXX},
  year={2023},
}
```

Feel free to [email us](mailto:zchen@cse.msstate.edu) if you wish your work to be listed in this repo.
If you notice anything unexpected, please open an [issue](XXX) and let us know.
If you have any questions or are missing a specific feature, feel free [to discuss them with us](XXX).
We are motivated to constantly make XFlow even better.






<a class="github-button" href="https://github.com/aquastar/awesome-network-flow" data-icon="octicon-star" data-size="large" data-show-count="false" aria-label="Star XFlow">Awesome Network Flow</a>