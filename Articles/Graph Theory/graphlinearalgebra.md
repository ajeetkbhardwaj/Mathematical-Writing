---
marp: true
theme: gaia
class: invert
size: 16:9
math: mathjx
footer: Ajeet Kumar | ajeetskbp9843@gmail.com | [Linkedin Profile](https:\\www.linkedin.com\in\ajeetkumar09)
---
# <!--fit-->Graph Linear Algebra


---
A graph $G = (V, E)$ consists of set of vertices $V$ and edges $E$. if we take some subsets of $V$ and $E$ s.t they form a set of subgraph $\mathbb{G} = \{G_1, G_2, G_3, \dots, G_k\}$ of $G$, where $G, G_2, \dots, G_k$ are circuits of graph G.

We know that the ring(direct) sum of two circuits is either a circuit or an edge disjoint union of circuits i.e Let $G_1, G_2$ be two circuits then their ring sum will be $G_1 \oplus G_2$ will also be a circuit or an edge disjoint union circuits. Thus, we can say that $\mathbb{G}$ will form a group under the $\oplus$ operation i.e $(\mathbb{G}, \oplus)$ is a group.

**Theorem-1 :** *Let $\mathbb{G}$ be the set of all circuits and edge disjoint union of circuits in a graph $G$ then $(\mathbb{G}, \oplus)$ will be an abelian group.*

**Theorem-2 :** *Let $\mathbb{G}$ be the set of all cutsets and edge disjoint union of cutsets in a graph $G$ then $(\mathbb{G}, \oplus)$ will be an abelian group.*
