# Introduction

The simple-graph module contains basic functions for graph.

## Concept

A graph is a structure to hold a set of objects in which some pairs of the objects are connected.

A graph contains two components: __vertices__ and __edges__.

We consider both directed and undirected edges in this project.
If the edges are undirected, the graph is called undirected graph, on the other hand, it is called directed graph.

# License

simple-graph is a free software. See the file LICENSE for the full text.

# Install
```python
pip install simple-graph
```
or update
```python
pip install --upgrade simple-graph
```

# Usage

## Basic operations
```python
from simple_graph import Graph
G = Graph()
G.add_edge(1, 2)
print(G.has_edge(1, 2))
```
ouput: 
```shell
True
```

```python
G = Graph({0: [1, 2], 1: [2]})
print(G.neighbors(0))
```

output: 
```shell
[1, 2]
```

## Statistics

```python
G = Graph({ 
    "a" : ["c"],
    "b" : ["c","e","f"],
    "c" : ["a","b","d","e"],
    "d" : ["c"],
    "e" : ["b","c","f"],
    "f" : ["b","e"]
})

print(G.find_path('a', 'b'))
print(G.diameter())
```

output:
```shell
['a', 'c', 'b']
3
```

Check [Wiki](https://github.com/jiayingwang/simple_graph/wiki) for more details.

# Authors

![qrcode_for_wechat_official_account](https://wx3.sinaimg.cn/mw1024/bdb7558bly1gjo23b3jrmj207607674r.jpg)

