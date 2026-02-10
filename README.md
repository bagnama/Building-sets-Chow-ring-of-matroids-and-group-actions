# Building sets, Chow ring of matroids and group actions

In matroid theory one of the open problems since the 70's were the log-concavity and unimodal conjectures concerning coefficients of the characteristic polynomial associated to a matroid.
A sequence of number $(a_1, \dots, a_n)$ is called unimodal if
```math
    a_1 \le \dots \le a_l \ge a_{l+1} \ge \dots \ge a_n
```
and log-concave if
```math
    a_{k-1} \, a_{k+1} \le a_k^2
```
for all $k \le n$.
The chromatic polynomial for graph is the polynomial that count all the possible coloration of the graph. The log-concavity and unimodal conjectures for the chromatic polynomial of a graph state that the sequence of the coefficients of the chromatic polynomial is log-concave and unimodal. They were introduced respectively by Read and Heron in 1968 and 1974. These conjectures where latex extended from graphs to general matroids, that are objects that generalize graphs, by Rota and Heron in 1971 and 1972.

Given a matroid $\mathcal{M}$ of rank $r+1$ and defined $\omega_k$ as the absolute value of the coefficient of the characteristic polynomial $\Large\chi_{\small\mathcal{M}}$ associated to the matroid $\mathcal{M}$, the log-concavity conjecture state that the sequence of $(\omega_1, \dots, \omega_r)$ is unimodal and log-concave.

In 2018 Adiprasito, Huh and Katz provev these conjectures using as main tool a certain graded $\mathbb{Z}$-algebra $A = \bigoplus_{k=0}^r A^k$ associated to a matroid, called the Chow ring,  
introduced in 2004 by Feichtner and Yuzvinsky.
In particular they proved the Kähler package which is composed of three results about the ring $A$ that are the Poincarè duality, Hard Lefschetz and Hodge-Riemann relation. In particular they prove that the sequence $(a_1, \dots, a_k)$ with $a_k = rk_{\mathbb{Z}} A^k$ is unimodal as a consequence of Hard Lefschetz and symmetric as a consequence of Poincarè duality.
In the realizable case the Chow ring is isomorphic to he cohomology of the De Concini-Procesi wonderful model introduced by De Concini and Procesi.

The Chow ring is dependent on the choice of a building set.  Adiprasito, Huh and Katz, in their article, considered the Chow ring associated to the maximal building set and under this assumptions they proved the Kahler package. It was later generalized by Pagaria and Pezzoli for general building sets in 2023 and by Crowley, Huh, Larson, Simpson, and Wang in 2024.

#### Theorem A
Let $\mathcal{M}$ be a matroid with lattice of flats $\mathcal{L}$ of rank $r+1$, and $\mathcal{G}$ a building set that contains $\hat{1}$, the Chow ring 
```math
    \mathcal{A}(\mathcal{L}, \mathcal{G}) = \bigoplus_{k = 0}^r A^k
```
satisfy the following:

$\hspace{1cm}(1)$ (Poincarè duality) For every $k\le \frac{r}{2}$, there is a perfect $\mathbb{Z}$-bilinear pairing:
```math
    A^k \times A^{r-k} \longrightarrow \mathbb{Z}; \ 
    (a,b) \longmapsto \deg(a \cdot b)
```
that induces an isomorphism $A^{r-k} \simeq \text{Hom}_{\mathbb{Z}}(A^k, \mathbb{Z}).$

$\hspace{1cm}(2)$ (Hard Lefschetz) The Chow ring with real coefficients 
```math
    \mathcal{A}_{\mathbb{R}}(\mathcal{L}, \mathcal{G}) = \bigoplus_{k = 0}^r A^k_{\mathbb{R}}
```
contains a non-empty convex cone $\mathcal{K} \subset A^1_{\mathbb{R}}$ of Lefschetz elements such that $ \forall \omega \in \mathcal{K}$ the map $a \longmapsto a \cdot \omega^{r- 2k}$ is an $\mathbb{R}$-linear isomorphism:
```math
    A^k_{\mathbb{R}} \longrightarrow A^{r-k}_{\mathbb{R}}, \text{for } k \le \frac{r}{2}.
```
In particular the multiplication by $\omega$ is an injection:
```math
    A^k_{\mathbb{R}} \hookrightarrow A^{k+1}_{\mathbb{R}}, \text{for } k \le \frac{r}{2}.
```

$\hspace{1cm}(3)$ (Hodge-Riemann inequality) Each Lefschetz element $\omega$ define a quadratic form 
```math
    a \longmapsto (-1)^k \deg(a \cdot \omega^{r-2k} \cdot a)
```
on $A^k_{\mathbb{R}}$ that become positive definite upon restriction to the kernel of the map 
```math
    A^k_{\mathbb{R}} \longrightarrow A^{r-k+1}_{\mathbb{R}},
```
that sends $a \longmapsto a \cdot \omega^{r-2k+1}$.

In particular, the proof of the log-concavity conjecture follows by the Hodge-Riemann inequality in degree $k=1$.

Given the importance of these techniques it is interesting to study the Chow rings and building sets from which they depends.
Regarding building sets we report a 2024 work by Backman and Danner about the geometry of the family of building sets, in particular they proves that building sets ordered by inclusion form a supersolvable convex geometry.

In this thesis we focused primarily on a 2024 work by Angarone, Nathanson and Reiner where they studied how the Poincare duality and Hard Lefschetz properties interact with symmetries. More generally, a group action on a matroid $\mathcal{M}$ is a permutation of the elements that preserve the lattice $\mathcal{L}_{\mathcal{M}}$. They used a monomial base for the Chow ring provided by Feichtner and Yuzvinsky, referred as $FY$, and proved, under a certain assumptions for the G-action on $FY$ the existence of G-equivariant relations in the basis.

#### Theorem B
Let $\mathcal{M}$ be a simple matroid with lattice of flats $\mathcal{L}$, $\mathcal{G}$ a building set that contains $\hat{1}$. Let $G$ a group setwise stabilizing $\mathcal{G}$ acting on $\mathcal{M}$ as in Section 3.2. Then there exists:

$\hspace{1cm}(1)$ $G$-equivariant bijections $\pi : FY^k \longrightarrow FY^{r-k}$, for $k \le \frac{r}{2}$;

$\hspace{1cm}(2)$ $G$-equivariant injections $\lambda : FY^k \longrightarrow FY^{k+1}$, for $k < \frac{r}{2}$.


To prove this result they used symmetric chain decompositions of a poset. A symmetric chain in a ranked poset is a chain that is symmetric with respect to the middle degree of the poset. The idea is to decompose the $FY$ basis in a disjoint union of symmetric chains, ordered by divisibility, and to define the injections and isomorphisms as functions acting on the elements of the chains in the decomposition.

This thesis is divided into tree chapters. In the first one we firstly introduce lattices, matroids and define the action of a group on matroids. Then we define building and nested sets and we introduce a distance function for atomic lattices.

In Chapter 2 we define the Chow ring of a matroid and the action of the automorphism group of the matroid on the Chow ring. Then we describe a monomial basis of the Chow ring and we state some properties such as the Kahler package. We define the De Concini-Procesi wonderful models, and present their Chow rings.

In the last Chapter we introduce symmetric chains decomposition of a poset and prove the existence of it for the poset of divisors of a natural number.
Then we apply those tools proving the Theorem B. We conclude by showing that the technical condition on the group action is necessary.
