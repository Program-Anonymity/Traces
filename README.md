# Traces

## Introduction
This is the publicly available industry-based dataset of the concurrent iterative graph processing for research. 

Specifically, Traces feature more plan diversity, based on the range of large & small query plans that are realistic to the query patterns seen in large scaled companies. All Traces query plans are based on real Presto queries executed & profiled over Grab's datalake.

The jobs in the real trace from Tencent are periodically executed offline jobs, and can be classified into two categories: all-active algorithms (all vertices are active at the beginning) and non-all-active algorithms (a subset of vertices are active at the beginning). The proportion of the former is about 22.2%, and that of the latter is 77.8%. Specifically, the all-active algorithms are the variants of PageRank, WCC, k-core, Label propagation, Louvain modularity, k-means, Graph coloring, MIS, Maximal matching, and Degree centrality, while the non-all-active algorithms are implemented based on SSSP or BFS.

## Classification of the CGP jobs

| All-active algorithms | Non-all-active algorithms |
| ------- | ----------- |
|  PageRank, WCC, k-core, Label propagation, Louvain modularity, k-means, Graph coloring, MIS, Maximal matching, and Degree centrality | SSSP and BFS | 
