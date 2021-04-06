# Traces

## Introduction
This is a publicly available industry-based trace of the _Concurrent iterative Graph Processing_ (CGP) jobs for research. 

Specifically, Traces feature more plan diversity, based on the range of large & small query plans that are realistic to the query patterns seen in large scaled companies. All Traces query plans are based on real Presto queries executed & profiled over Grab's datalake.

The jobs in the real trace from Tencent are periodically executed offline jobs, and can be classified into two categories: all-active algorithms (all vertices are active at the beginning) and non-all-active algorithms (a subset of vertices are active at the beginning). The proportion of the former is about 22.2%, and that of the latter is 77.8%. Specifically, the all-active algorithms are the variants of PageRank, WCC, k-core, Label propagation, Louvain modularity, k-means, Graph coloring, MIS, Maximal matching, and Degree centrality, while the non-all-active algorithms are implemented based on SSSP or BFS.

In order to emphasise the difference between the query plans under the TPC benchmarks and Grab-Traces, we plotted a sample of 245,849 logical plans, obtained over 2 consecutive months in Grab, on their node count and maximum tree depth. We contrasted these plans with TPC-DS & TPC-H templates. The maximum plan (size, depth) observed was (477, 38) for TPC-H, (883, 73) for TPC-DS and (4969, 321) for Grab. 

![traces](Figures/traces.png)

From the picture, two things become clear:
- Grab's query plans are diverse: We observed a range of very large and small plans issued to our Presto clusters

- Query volumes are large: We observed many distinct queries issued to our Presto clusters. At scale, many of the existing query featurization techniques may be highly inefficient.

## Classification of the CGP jobs
The CGP jobs traced from Tencent can be classified into two categories: all-active algorithms (all vertices are active at the beginning) and non-all-active algorithms (a subset of vertices are active at the beginning).

| All-active algorithms | Non-all-active algorithms |
| ----- | ----------- |
|  The variants of PageRank, WCC, k-core, Label propagation, Louvain modularity, k-means, Graph coloring, MIS, Maximal matching, and Degree centrality | The variants of SSSP and BFS | 

## Licensing 
All data is subjected to the MIT open source licensing scheme. 
For more details, please see [licensing](LICENSE)

## Citations
TODO: Fill in this page once paper is published
