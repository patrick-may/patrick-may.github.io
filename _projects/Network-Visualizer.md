---
layout: page
title: Dijkstras Algorithm Visualizer
description: Understanding computer networks.
img: assets/img/networkxlogo.png
importance: 1
category: coursework
---

Dijkstra's algorithm is (in my opinion) one of the most interesting algorithms created, because of its simplicity, history, complexity, and extensibility.

This project utilized mathematical computing technologies such as **Matplotlib** and **Networkx** to iteratively create a visualization for dijkstra's algorithm.

*Terminology*: Graphs are collections of nodes and edges, where nodes are "points" and edges are "connections" between different nodes. Graphs have a million and a half different uses in computer science because they are so versatile. They exist to model relations between discrete objects. Within the context of this write-up, a *network* is used interchangeably with the idea of a graph. This is not *entirely* correct, although computer networks can be modeled using graphs, where each node is a computer terminal and each edge is a connection to other computers, modems, etc. 

## Examples

Here are a couple different graphs that can be visualized with this tool:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/graph1.gif" title="3-Regular Order 14 Graph" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A simple graph with Dijkstra's algorithm originating at node `0`.
</div>
