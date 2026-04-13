# The K₁/K₂/P₃ Trichotomy and a Six-Way Dictionary for Simple Graphs Without Small Components

*K₁/K₂/P₃ 三分法：无小分量简单图的六路字典*

**Jason Xin**

---

## Abstract / 摘要

We show that for a simple graph, the following six conditions are equivalent: (1) no two distinct vertices share the same edge-incidence profile; (2) no isolated vertices and no isolated edges whose endpoints both have degree 1; (3) every vertex lies on an edge with at least one endpoint of degree at least 2; (4) every connected component has at least 3 vertices; (5) every vertex lies in a P₃ subgraph; (6) the graph has no K₁ or K₂ components. We also prove a local trichotomy: every vertex falls into exactly one of three cases — K₁ (isolated), K₂ (an endpoint of an isolated edge), or P₃ (lies on a path of length 2). The point of the note is organizational rather than priority-claiming: the individual implications are largely folklore, but the closed six-way dictionary and the local trichotomy are useful to have in a single self-contained place.

证明简单图的以下六个条件等价：(1) 没有两个不同顶点具有相同的边关联剖面；(2) 无孤立顶点且无两端均为度 1 的孤立边；(3) 每个顶点都落在某条至少一端度数 ≥ 2 的边上；(4) 每个连通分量至少有 3 个顶点；(5) 每个顶点都落在某个 P₃ 子图中；(6) 不存在 K₁ 或 K₂ 连通分量。同时证明一个局部三分法：每个顶点恰好落入三种情形之一——K₁（孤立）、K₂（孤立边端点）、P₃（落在长度为 2 的路径中）。本文的价值主要在组织与翻译，而不是对单条图论蕴涵主张优先权：各单条蕴涵大体属于已知或 folklore，但把它们压成一个闭合六路字典并配上自含证明，仍然有独立说明价值。

---

## Scope and Positioning / 范围与定位

This note is expository. It does not claim that each graph-theoretic implication below is new. Instead, it packages a small cluster of standard or folklore observations into a single self-contained dictionary that can be read in several equivalent ways: incidence language, local-condition language, component language, and subgraph-witness language.

本文是一篇说明性短文。它的目标不是主张下文每一条图论蕴涵都是新的，而是把一小簇标准或 folklore 观察压成一个自含的等价字典，使同一事实可以在多种语言中被直接读取：边关联语言、局部条件语言、连通分量语言、以及子图见证语言。

This organizational role is mathematically modest but still useful: it separates the core obstruction into K₁ and K₂, isolates P₃ as the minimal positive witness, and makes the six-way equivalence available as a single reference point.

这种组织性的作用在数学上是克制的，但仍然有价值：它把核心障碍精确拆成 K₁ 与 K₂，把 P₃ 抽成最小正见证，并把六路等价压成一个可以直接调用的参考点。

---

## 1. Setup / 基本设置

Throughout this note, G = (V, E) denotes a simple graph: no loops, no multiple edges, isolated vertices allowed. All graphs are undirected.

本文中 G = (V, E) 表示简单图：无自环、无重边、允许孤立顶点。所有图都是无向图。

**Definition 1** (Edge-incidence profile / 边关联剖面).
For a vertex v ∈ V, define:

对顶点 v ∈ V，定义：

```
inc(v) := { e ∈ E : v ∈ e }
```

This is the set of all edges incident to v. Two distinct vertices u, v are called **edge-incidence twins** if inc(u) = inc(v).

即 v 所关联的全部边的集合。若两个不同顶点 u, v 满足 inc(u) = inc(v)，则称它们为**边关联双生**。

**Definition 2** (Isolated-edge / 孤立边).
An edge e = {u, v} ∈ E is called an **isolated edge** if both endpoints have degree exactly 1:

一条边 e = {u, v} ∈ E 被称为**孤立边**，若其两个端点的度数都恰为 1：

```
deg(u) = deg(v) = 1.
```

Equivalently, u and v are each other's only neighbor, and the connected component containing e is isomorphic to K₂.

等价地，u 和 v 互为唯一邻点，包含 e 的连通分量同构于 K₂。

---

## 2. Characterization of Edge-Incidence Twins / 边关联双生的刻画

**Proposition 1.** Let G = (V, E) be a simple graph and let u, v ∈ V with u ≠ v. Then inc(u) = inc(v) if and only if one of the following holds:

**命题 1.** 设 G = (V, E) 为简单图，u, v ∈ V 且 u ≠ v。则 inc(u) = inc(v) 当且仅当以下两种情形之一成立：

(a) inc(u) = inc(v) = ∅ (both are isolated); / 二者都是孤立顶点；

(b) There exists a unique edge e = {u, v} ∈ E such that inc(u) = inc(v) = {e} (they form an isolated edge). / 存在唯一边 e = {u, v} ∈ E 使得 inc(u) = inc(v) = {e}（二者构成一条孤立边）。

**Proof / 证明.**

Sufficiency is immediate for both cases. / 充分性在两种情形下都是直接的。

For necessity, suppose inc(u) = inc(v) with u ≠ v. If inc(u) = ∅, we are in case (a).

对于必要性，设 inc(u) = inc(v) 且 u ≠ v。若 inc(u) = ∅，则属于情形 (a)。

Otherwise, pick some e ∈ inc(u) = inc(v). Since e is incident to u, write e = {u, w} for some w ∈ V. Since e ∈ inc(v) as well, v must be an endpoint of e, so v ∈ {u, w}. As u ≠ v, we get v = w, hence e = {u, v}.

否则，取某条 e ∈ inc(u) = inc(v)。因为 e 关联 u，记 e = {u, w}。又因为 e ∈ inc(v)，故 v 是 e 的端点，即 v ∈ {u, w}。由 u ≠ v 得 v = w，故 e = {u, v}。

Now pick any f ∈ inc(u). By the same argument applied to f ∈ inc(v), f must have both u and v as endpoints, so f = {u, v}. Since G is simple (no multiple edges), f = e. Thus inc(u) = {e}, and we are in case (b). ∎

现取任意 f ∈ inc(u)。对 f ∈ inc(v) 施行同样论证，得 f 必须以 u 和 v 为两端，故 f = {u, v}。因 G 是简单图（无重边），f = e。因此 inc(u) = {e}，属于情形 (b)。∎

---

## 3. The Six-Way Equivalence / 六路等价

**Theorem 1.** For a simple graph G = (V, E), the following six conditions are equivalent:

**定理 1.** 对简单图 G = (V, E)，以下六个条件等价：

**(C1)** G has no isolated vertices and no edge-incidence twins. That is, the map v ↦ inc(v) is an injection from V into P(E) \ {∅}.

**(C1)** G 无孤立顶点且无边关联双生。即映射 v ↦ inc(v) 是从 V 到 P(E) \ {∅} 的单射。

**(C2)** G has no isolated vertices and no isolated edges.

**(C2)** G 无孤立顶点且无孤立边。

**(C3)** Every vertex lies on some edge that has at least one endpoint of degree ≥ 2. In symbols:

**(C3)** 每个顶点都落在某条至少一端度数 ≥ 2 的边上。用符号写：

```
∀v ∈ V, ∃w ∈ V, ∃e ∈ E :
  e = {v, w} ∧ (deg(v) ≥ 2 ∨ deg(w) ≥ 2).
```

**(C4)** Every connected component of G has at least 3 vertices.

**(C4)** G 的每个连通分量至少有 3 个顶点。

**(C5)** Every vertex lies in some P₃ subgraph (a path on 3 vertices, i.e., two edges sharing exactly one endpoint).

**(C5)** 每个顶点都落在某个 P₃ 子图中（3 个顶点的路径，即两条恰共享一个端点的边）。

**(C6)** G has no K₁ component and no K₂ component.

**(C6)** G 不含 K₁ 分量且不含 K₂ 分量。

---

**Proof / 证明.**

We prove C1 ⇔ C2 ⇔ C4 ⇔ C6, then C4 ⇔ C5, then C4 ⇔ C3.

证明 C1 ⇔ C2 ⇔ C4 ⇔ C6，然后 C4 ⇔ C5，然后 C4 ⇔ C3。

---

**C1 ⇔ C2.**

By Proposition 1, edge-incidence twins in a graph with no isolated vertices arise only from isolated edges (case (b)). Therefore "no isolated vertices and no edge-incidence twins" is equivalent to "no isolated vertices and no isolated edges." ∎

由命题 1，在无孤立顶点的图中，边关联双生只来自孤立边（情形 (b)）。因此"无孤立顶点且无边关联双生"等价于"无孤立顶点且无孤立边"。∎

---

**C2 ⇔ C6.**

"No isolated vertices" means no K₁ component (a single vertex with no edges). "No isolated edges" means no K₂ component (an edge whose both endpoints have degree 1; such an edge and its endpoints form a connected component isomorphic to K₂). ∎

"无孤立顶点"即不含 K₁ 分量。"无孤立边"即不含 K₂ 分量（两端度数均为 1 的边及其端点构成同构于 K₂ 的连通分量）。∎

---

**C6 ⇔ C4.**

A connected component has 1 vertex iff it is K₁; it has exactly 2 vertices iff (in a simple connected graph) it is K₂. So "no K₁ and no K₂ components" is equivalent to "every component has ≥ 3 vertices." ∎

连通分量含 1 个顶点当且仅当它是 K₁；恰含 2 个顶点当且仅当它是 K₂（简单连通图中）。故"不含 K₁ 且不含 K₂ 分量"等价于"每个分量 ≥ 3 个顶点"。∎

---

**C4 ⇒ C5.**

Let v be any vertex and let C be its connected component with |V(C)| ≥ 3.

设 v 为任意顶点，C 为其所在连通分量，|V(C)| ≥ 3。

Case 1: deg_C(v) ≥ 2. Pick two distinct neighbors y, z of v. Then v-y and v-z form a P₃ containing v.

情形 1：deg_C(v) ≥ 2。取 v 的两个不同邻点 y, z。则 y-v-z 构成包含 v 的 P₃。

Case 2: deg_C(v) = 1. Let y be v's unique neighbor. Since C is connected with ≥ 3 vertices, y has some neighbor z ≠ v. Then v-y-z is a P₃ containing v.

情形 2：deg_C(v) = 1。设 y 为 v 的唯一邻点。因 C 连通且 ≥ 3 个顶点，y 有某个邻点 z ≠ v。则 v-y-z 是包含 v 的 P₃。

(Note: deg_C(v) = 0 is impossible since |V(C)| ≥ 3 and C is connected imply every vertex has degree ≥ 1 within C.) ∎

（注：deg_C(v) = 0 不可能，因为 |V(C)| ≥ 3 且 C 连通蕴涵每个顶点在 C 内度数 ≥ 1。）∎

---

**C5 ⇒ C4.**

If every vertex v lies in some P₃, then v's connected component contains at least 3 vertices. ∎

若每个顶点 v 都落在某个 P₃ 中，则 v 的连通分量至少含 3 个顶点。∎

---

**C4 ⇒ C3.**

Let v be any vertex in a component C with |V(C)| ≥ 3. Pick an edge e incident to v (exists since C is connected with ≥ 3 vertices). Write e = {v, w}.

设 v 为某个含 ≥ 3 个顶点的分量 C 中的任意顶点。取一条关联 v 的边 e（因 C 连通且 ≥ 3 个顶点，故存在）。记 e = {v, w}。

If deg(v) ≥ 2, the condition is satisfied immediately. If deg(v) = 1, then since |V(C)| ≥ 3 and C is connected, w must have another neighbor, so deg(w) ≥ 2. ∎

若 deg(v) ≥ 2，条件直接成立。若 deg(v) = 1，因 |V(C)| ≥ 3 且 C 连通，w 必有其他邻点，故 deg(w) ≥ 2。∎

---

**C3 ⇒ C4.**

Suppose C3 holds. First, every vertex has degree ≥ 1 (it lies on some edge), so no K₁ components.

假设 C3 成立。首先，每个顶点度数 ≥ 1（它落在某条边上），故无 K₁ 分量。

Now suppose some component is K₂, say {u, v} with a single edge e. Then deg(u) = deg(v) = 1. The only edge incident to u is e, and both endpoints of e have degree 1. This contradicts C3 applied to vertex u. So no K₂ components either, giving C4 via C6. ∎

再设某个分量为 K₂，记为 {u, v}，仅有一条边 e。则 deg(u) = deg(v) = 1。关联 u 的唯一边为 e，且 e 的两端度数均为 1。这与对顶点 u 应用 C3 矛盾。故也无 K₂ 分量，由 C6 得 C4。∎

---

This completes the proof that all six conditions are equivalent. ∎

六个条件的等价性证明完毕。∎

---

## 4. The Local Trichotomy / 局部三分法

**Theorem 2.** For a simple graph G = (V, E) and any vertex v ∈ V, exactly one of the following holds:

**定理 2.** 对简单图 G = (V, E) 及任意顶点 v ∈ V，以下三种情形恰有一种成立：

(T1) v is an isolated vertex (its component is K₁); / v 是孤立顶点（其分量为 K₁）；

(T2) v is an endpoint of an isolated edge (its component is K₂); / v 是某条孤立边的端点（其分量为 K₂）；

(T3) v lies in some P₃ subgraph. / v 落在某个 P₃ 子图中。

Moreover, the six equivalent conditions of Theorem 1 hold if and only if every vertex is in case (T3).

此外，定理 1 的六个等价条件成立，当且仅当每个顶点都处于情形 (T3)。

**Proof / 证明.**

Let C be the connected component containing v.

设 C 为包含 v 的连通分量。

If |V(C)| = 1, then v is isolated: case (T1). / 若 |V(C)| = 1，则 v 是孤立顶点：情形 (T1)。

If |V(C)| = 2, then C ≅ K₂ (simple and connected), so v is an isolated-edge endpoint: case (T2). / 若 |V(C)| = 2，则 C ≅ K₂（简单且连通），v 为孤立边端点：情形 (T2)。

If |V(C)| ≥ 3, then by the proof of C4 ⇒ C5 in Theorem 1, v lies in some P₃: case (T3). / 若 |V(C)| ≥ 3，由定理 1 中 C4 ⇒ C5 的证明，v 落在某个 P₃ 中：情形 (T3)。

These three cases are mutually exclusive (determined by component size: 1, 2, or ≥ 3) and exhaustive. The "moreover" follows directly from Theorem 1: the six conditions are equivalent to "every component has ≥ 3 vertices," which is equivalent to "no vertex falls in (T1) or (T2)." ∎

三种情形互斥（由分量大小决定：1、2 或 ≥ 3）且穷尽。"此外"部分直接由定理 1 得出：六个条件等价于"每个分量 ≥ 3 个顶点"，即"没有顶点落在 (T1) 或 (T2) 中"。∎

---

## 5. Remark on Twins / 关于双生顶点的注记

The graph-theoretic literature uses several non-equivalent notions of "twins":

图论文献中有多种"双生顶点"概念：

- **Open twins / 开双生**: N(u) = N(v) (same open neighborhood / 相同开邻域)
- **Closed twins / 闭双生**: N[u] = N[v] (same closed neighborhood / 相同闭邻域)
- **Edge-incidence twins / 边关联双生**: inc(u) = inc(v) (same set of incident edges / 相同边关联集)

The present note uses only the third notion. It is distinct from both the open-neighborhood and the closed-neighborhood notions.

本文真正使用的只有第三种概念。它既不等同于开双生，也不等同于闭双生。

Proposition 1 shows that in a simple graph, edge-incidence twinning collapses to exactly two degenerate configurations: two isolated vertices, or the endpoints of an isolated edge. This is an incidence-level statement; it should not be read as saying that edge-incidence twinning is merely a stronger form of open or closed twinning.

命题 1 表明，在简单图中，边关联双生恰好塌缩为两种退化构型：两个孤立点，或一条孤立边的两个端点。这是一个 incidence-level 的陈述；它不应被理解成“边关联双生只是开/闭双生的更强版本”。

For example, the endpoints of K₂ are edge-incidence twins and closed twins, but not open twins. Conversely, two leaves of a star are open twins, but not edge-incidence twins. The present dictionary is therefore best read as a characterization of graphs without isolated vertices and without edge-incidence twins, rather than as a rebranding of the standard twin-free literature.

例如，K₂ 的两个端点既是边关联双生，也是闭双生，但不是开双生。反过来，星图的两个叶子是开双生，却不是边关联双生。因此，本文更适合被读成“无孤立点且无边关联双生”的等价刻画，而不是对标准 twin-free 文献术语的重新命名。

The open-neighborhood lineage is classically studied under the name point-determining graphs; see Sumner [2]. In later domination and location literature, "twin-free" is often used in the open- or closed-neighborhood sense; see Charon et al. [1] and Foucaud et al. [3].

开邻域这一支的经典术语是 point-determining graph；参见 Sumner [2]。在后来的 domination / location 文献里，"twin-free" 常按开/闭邻域意义来使用；参见 Charon 等 [1] 与 Foucaud 等 [3]。

---

## 6. Summary Table / 总结表

For quick reference, we summarize the equivalence dictionary and the local trichotomy below:

快速参考用的完整等价字典与局部三分类：

### Six-way equivalence / 六路等价

| # | Condition / 条件 |
|---|-----------------|
| C1 | No isolated vertices, no edge-incidence twins / 无孤立顶点且无边关联双生 |
| C2 | No isolated vertices, no isolated edges / 无孤立顶点且无孤立边 |
| C3 | Every vertex lies on an edge with ≥ 1 endpoint of degree ≥ 2 / 每个顶点都在某条至少一端度 ≥ 2 的边上 |
| C4 | Every component has ≥ 3 vertices / 每个连通分量 ≥ 3 个顶点 |
| C5 | Every vertex lies in a P₃ / 每个顶点都落在某个 P₃ 中 |
| C6 | No K₁, no K₂ components / 不含 K₁ 或 K₂ 分量 |

### Local trichotomy / 局部三分法

| Case / 情形 | Description / 描述 | Component / 分量 | Status / 状态 |
|-------------|-------------------|-----------------|--------------|
| T1 | Isolated vertex / 孤立顶点 | K₁ | Global obstruction / 全局障碍 |
| T2 | Isolated-edge endpoint / 孤立边端点 | K₂ | Global obstruction / 全局障碍 |
| T3 | Lies in a P₃ / 落在 P₃ 中 | ≥ 3 vertices / ≥ 3 个顶点 | Locally good case / 局部良性情形 |

---

## References / 参考文献

1. Charon, I., Honkala, I., Hudry, O., and Lobstein, A. (2007). Structural Properties of Twin-Free Graphs. *Electronic Journal of Combinatorics*, 14(1), R16. DOI: [10.37236/934](https://doi.org/10.37236/934).

2. Sumner, D. P. (1973). Point determination in graphs. *Discrete Mathematics*, 5(2), 179–187. DOI: [10.1016/0012-365X(73)90109-X](https://doi.org/10.1016/0012-365X(73)90109-X).

3. Foucaud, F., Henning, M. A., Löwenstein, C., and Sasse, T. (2016). Locating-dominating sets in twin-free graphs. *Discrete Applied Mathematics*, 200, 52–58. DOI: [10.1016/j.dam.2015.06.038](https://doi.org/10.1016/j.dam.2015.06.038). Preprint: [arXiv:1412.2376](https://arxiv.org/abs/1412.2376).
