## qsearch

Spatial quantum search (Grover's search) package based on the continuous time quantum walk.

### Dependencies

1. numpy
2. networkx
3. scipy

### Usage

Quantum walks

```
G = nx.complete_graph(5)
qwalker = Qwalker(G)
N = 1/len(G)
t = 10
localisations = walk(qwalker, 1/N, t, 0.1)

```

Quantum Search

```
G = nx.complete_graph(10)
qwalker = Qwalker(G)
N = len(G)
t = 10
oracle = createMarkedVertex(N, 0)
success_probability = evolve(qwalker, 1/N, oracle, t, 0.1)

```
