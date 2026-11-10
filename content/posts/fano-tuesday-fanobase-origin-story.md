+++
title = "Fano Tuesday: the origin story for Fanobase"
date = "2026-11-09"
draft = false
authors = ["Enrico Fatighenti"]
description = "Fano Tuesday: the origin story for Fanobase"
+++

Welcome to **Fano Tuesday**, a series of blog posts where we highlight some of the features of our database
and put into the spotlight some interesting examples that might be lost in the wilderness.

In this first blog post of the series, we start with a bit of a historical perspective.
Suppose you want to understand what Fano varieties should look like in dimension four.
The first strategy that comes to mind would probably be to look for complete intersections in projective spaces.
It is a very easy exercise in combinatorics to show that there are only a handful of them,
from $\mathbb P^4$ itself to a codimension-four complete intersection of quadrics in $\mathbb P^8$.
But what about other examples?

## Inside Grassmannians
Well, suppose that you are aware of [Mukai's work on K3 surfaces and prime Fano threefolds](https://doi.org/10.1073/pnas.86.9.3000).
Then you will soon realize that a fruitful way of writing down examples
would be to start from a homogeneous variety and take a bunch of linear sections.
But simply using linear sections (or more generally, complete intersections)
is not enough to enumerate all of them.

Consider, for example, the case of [$V_{22}$](https://fanography.info/1-10/):
you need a net of skew-symmetric forms $\langle\lambda_1,\lambda_2,\lambda_3\rangle\subset\bigwedge^2 V_7^\vee$
and consider the locus of three-dimensional subspaces of $V_7$ that are isotropic for all of them.
In other words, this is the zero locus of a global section of
three copies of the vector bundle $\bigwedge^2\mathcal{U}^\vee$ on $\mathrm{Gr}(3,7)$,
with $\mathcal{U}^\vee$ the dual of the tautological bundle.
So some other very interesting cases can be found.

You will quickly realize that the search for isolated examples
can be turned into a finite, combinatorial search: start from a Grassmannian $\mathrm{Gr}(k,n)$
and consider a homogeneous, completely reducible, globally generated vector bundle $\mathcal E$,
with the properties that $-\mathrm{K}_{\mathrm{Gr}(k,n)}-\det(\mathcal E)$ is ample
and the corresponding zero locus is of dimension four and *index* one.

## Küchle's list
This is exactly what Küchle did in his [paper](https://doi.org/10.1007/BF02571923) (*On Fano 4-folds of index 1 and homogeneous vector bundles over Grassmannians*, 1995). In fact, the search is combinatorial: an irreducible homogeneous bundle can be written in terms of Schur functors applied to the tautological and quotient bundles, and its rank and first Chern class can be determined using standard formulae from the corresponding partitions.

As a result, besides the complete intersections in $\mathbb P^n$, Küchle found 18 cases:
five as complete intersections in $\mathrm{Gr}(k,n)$
and thirteen using higher-rank homogeneous vector bundles.
Well, except that, two decades later, our very own *Laurent Manivel* managed to show that two cases are in fact the same!
The varieties of types [(b3)](https://type-a.fanobase.net/family/1-42-15-a) and [(b7)](https://type-a.fanobase.net/family/1-42-15-a) are isomorphic, as he proved in [*On Fano manifolds of Picard number one*](https://doi.org/10.1007/s00209-015-1523-7). So the thirteen non-split presentations give twelve further families, alongside the five Grassmannian complete intersections.

Küchle's results have been a nice source of inspiration for many beautiful results in algebraic geometry. As an example, the fourfold of type [(b9)](https://type-a.fanobase.net/family/8-80-21-a), of Picard rank eight, was studied by [Cinzia Casagrande](https://arxiv.org/abs/1410.3087): it can be obtained from the blow-up of $\mathbb P^4$ at seven points by performing 22 antiflips. The fourfold of type (c5) has been a major source of inspiration because of its potential connection to hyperkähler geometry, and its geometry has been studied by Sasha Kuznetsov in [this very nice paper](https://doi.org/10.1007/s00209-016-1707-9). And they continue to inspire [beautiful](https://arxiv.org/abs/1609.02695) [new](https://doi.org/10.1007/s00209-018-2163-5) [geometry](https://arxiv.org/abs/2609.09310) [in](https://doi.org/10.1007/s13163-021-00401-2) [many](https://doi.org/10.5802/AIF.3761) [different](https://doi.org/10.1070/IM2015v079n04ABEH002758) [directions](https://doi.org/10.1007/s00209-016-1707-9).

## Küchle's list in Fanobase

Of course, all Küchle fourfolds can be found in [our type-A database](https://type-a.fanobase.net/).
Here they are, using Küchle's original numbering, with links to the corresponding families:

- **(b):** [(b1)](https://type-a.fanobase.net/family/1-15-9-a), [(b2)](https://type-a.fanobase.net/family/1-20-10-a), [(b3)](https://type-a.fanobase.net/family/1-42-15-a), [(b4)](https://type-a.fanobase.net/family/2-40-15-c), [(b5)](https://type-a.fanobase.net/family/1-33-13-a), [(b6)](https://type-a.fanobase.net/family/1-28-12-a), [(b7)](https://type-a.fanobase.net/family/1-42-15-a), [(b8)](https://type-a.fanobase.net/family/1-56-18-a), [(b9)](https://type-a.fanobase.net/family/8-80-21-a), [(b10)](https://type-a.fanobase.net/family/1-36-14-a), [(b11)](https://type-a.fanobase.net/family/1-57-18-a).
- **(c):** [(c1)](https://type-a.fanobase.net/family/1-42-15-b), [(c2)](https://type-a.fanobase.net/family/1-32-13-a), [(c3)](https://type-a.fanobase.net/family/1-72-21-a), [(c5)](https://type-a.fanobase.net/family/1-66-20-a), [(c6)](https://type-a.fanobase.net/family/1-61-19-a), [(c7)](https://type-a.fanobase.net/family/2-102-27-a).
- **(d):** [(d3)](https://type-a.fanobase.net/family/5-120-31-a).

Attention: Strictly speaking, Küchle's original list contains 21 cases, but three of them are discarded: (c4) and (d2) have index greater than one, while (d1) is disconnected. But what about these three cases? Well, they are not lost either! Both [(c4)](https://type-a.fanobase.net/family/1-128-33-a) and [(d1)](https://type-a.fanobase.net/family/1-128-33-a) lead to complete intersections of three quadrics in $\mathbb P^7$ (although (d1) gives two disjoint copies), while [(d2)](https://type-a.fanobase.net/family/4-384-81-c) turns out to be $(\mathbb P^1)^4$.

You will possibly have noticed that the positivity condition imposed by Küchle is exactly the *strongly Fano* condition that we use in our search. His work inspired us to write [our paper](https://doi.org/10.5802/AIF.3761), inspired us to build [this database](https://type-a.fanobase.net/), and will keep on inspiring us! And for a close-up look at some nice new geometric examples? You'll have to wait until next Tuesday!

