
## Sets and Subsets

Supposed we have $S = {A, B, C, D}$.

How many ways can we choose ==3-element== subsets are there of S?
i.e. how many ways are there to choose three of the four elements.

${4\choose3}$ or $4\choose1$ = 4.
- Choosing three to keep is the same as choosing one to delete.

## Strings

> [!summary]
> An **alphabet** $\Sigma$ is a set of *n* elements called **letters.** A **string** *S* of size *n* is an ordered sequence of *n* letters from $\Sigma$.
> 

### Example

#### Binary Strings
$\Sigma = {0, 1}$ -> 0 and 1 are "bits."

Strings: 01101 => A binary string of length 5.

#### DNA Sequences
$\Sigma = A, C, T, G$

Example string: ACCT, TCCA.

##### How many DNA Sequences are there of length $n$?
- It's not $4^n$, as forwards and backwards sequences are the same.
- For every sequence, it has a reverse
	- Except AAAA, CCCC, TTTT, GGGG

### Find all strings of length 6 over $\Sigma = 0, 1$ that don't have 10 as a substring.
- A zero can't follow a one, as it creates a substring 10.
	- It must have the form of zeroes at the start, then ones that follow.

There are 6 places for the ones to start, or they don't appear at all. ==So there are 7 strings==.

000000
000001
000011
000111
001111
011111
111111


## Permutations

> [!summary]
> A **permutation** *P* over an alphabet $\Sigma$ is a string over $\Sigma$ where every
> letter ==occurs exactly once==.

### Example

$\Sigma = 1, 2, 3$
Find all permutations.

- Write out as a dictionary would: 1 then 2 then three for each column.

1 2 3
1 3 2
2 1 3
2 3 1
3 1 2
3 2 1

#### How many permutations of a set of size $n$ are there?

With n spots: there are $n$ choices for the first spot, $n-1$ for the second, $n-2$ for the third ... $2$ choices for $n-1$ spot, and 1 choice for the $n$th spot.

$$=n\cdot(n-1)\cdot(n-2)\cdot\ \dots\ \cdot 2\cdot1 = n!$$

So for a set of size $n$, there are $n!$ permutations.
## Graphs
### Simple Graphs

>[!summary]
>A (simple) **graph** *G* is a pair (V, E) where *V* is a set of **vertices** and *E* is a set of unordered pairs of vertices called **edges**. 
>
>If $e = \{i,j\} \in E$ we say vertices *i* and *j* are **adjacent.** The degree of a vertex i in V is the number of vertices in V adjacent to vertex i.

+ A simple graph captures that there are no self-referring pairs (no loops)

#### Example
$V = \{1, 2, 3, 4, 5, 6\}$
$E = \{\{1, 2\}, \{1, 5\}, \{2, 3\}, \{2, 5\}, \{3, 4\}, \{4, 5\}, \{4, 6\}\}$

+ Vertices 1 and 2 are connected by an edge.
+ Vertex 2 has degree 3, since there are three ordered pairs with a 2 in them.

#### How many edges can a graph with *n* vertices have?
- A graph with one vertice has no edges
- Two vertices have one edge
- Three vertices have 3 edges
- Four vertices can have 6 edges

In total, a graph with $n$ vertices has $n\choose2$ edges. Either you pick a connection or you don't (2 choices.)
	Same thing as ${(n-1)n\over2}$.



### Complete Graphs

> [!summary]
> A graph $G = \left(V, E\right)$ is **complete** if $|V|\ge1$ and for all $i, j \in V$ the edge $\{i,j\} \in E$. The complete graph with $n$ vertices is denoted by $K_n$.



### Path Graphs

>[!summary]
> A graph $G = \left(V, E\right)$ is a **path** if $|V|\ge1$ and *V* may be ordered $v_1, v_2, \dots ,v_n$ so that $E = \{\{v_1,v_2\},\{v_2,v_3\}, \dots , \{v_{n-1}, v_n\}\}$. The path graph with *n* vertices is denoted by $P_n$.

- The number of edges is the size of the path graph.

### Cycle Graphs

> [!summary]
> A graph $G = \left(V, E\right)$ is a **cycle** if $|V|\ge3$ and *V* may be ordered $v_1, v_2, \dots ,v_n$ so that $E = \{\{v_1,v_2\},\{v_2,v_3\}, \dots , \{v_{n-1}, v_n\}, \{v_n, v_1\}\}$. The cycle graph with *n* vertices is denoted by $C_n$.

- A cycle graph is just an edge graph that reconnects the final vertex with the first one.

### Connected Graph

> [!summary]
> A graph $G = \left(V, E\right)$ is **connected** if there is a path in *G* from vertex $i\in V$ to vertex *j* for all $i \not= j$.