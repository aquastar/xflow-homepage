---
title: Graph
date: '2021-01-01'
type: book
weight: 20
math: true
tags:
  - 
---

Introduction to graphs data.

<!--more-->

XFlow incorporates existing dataset collections and can be extended easily.
Specifically, our implementation is compatible with any graph in NetworkX [^1] graph object, including graphs such as Watts-Strogatz small-world graphs, Barabási–Albert (BA), Erdős–Rényi (ER). See the full list in Graph Generators in NetworkX; 
Or graph objects in PyTorch Geometric such as Cora, Cite Seer, PubMed and co-purchasing networks (Amazon Photo, Computers) as well as synthetic graph generators. See torch\_geometric.datasets in PyTorch Geometric [^2].

[^1]: [NetworkX](https://networkx.org)
[^2]: [PyG](https://pytorch-geometric.readthedocs.io/en/latest/)