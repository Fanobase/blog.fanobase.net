+++
title = "ZL62 labels"
date = 2026-11-11
authors = ["Pieter Belmans"]
description = "A short introduction to the ZL62 labels used for zero-locus presentations in the type A database."
+++

In the [type A database](https://type-a.fanobase.net/), each zero-locus presentation has a **ZL62 label**.
This is short for [*ZeroLocus62*](https://zl62.homogeneous.tools), and it is a compact way to specify a zero locus.

Some presentations involve products of several flag varieties and long direct sums of bundles.
We need a reliable way to pass these constructions between our computational tools, attach results to the right presentation, and share examples with others.
A ZL62 label records the construction in one string that can be decoded without consulting our database.

Below, we illustrate these labels using [Küchle's list, introduced in our first Fano Tuesday post]({{< relref "fano-tuesday-fanobase-origin-story.md" >}}).

## A quick introduction
A label has the form `ambient.bundle`:

* The part before the dot describes the ambient variety, which can be a product of partial flag varieties.
* The part after it describes the vector bundle whose section defines the zero locus.

For example, `40.G` describes a quintic threefold: a degree-five hypersurface in $\mathbb P^4$.

The "62" in the name __ZeroLocus62__
refers to the characters used: the digits `0`–`9`, upper-case letters `A`–`Z`, and lower-case letters `a`–`z`.
The labels are short and easy to use in URLs, filenames, and database searches.
Upper- and lower-case letters are different, so case matters when copying a label.

The format puts bundle summands and ambient factors in a standard order, so reordering them gives the same label.
Several ZL62 labels can encode the same family of Fano fourfolds when it has different zero-locus presentations.
We will see an interesting instance of this phenomenon in the examples at the end of this post!

You can paste a label into the [online decoder](https://zl62.homogeneous.tools/) to see the construction, or use the ZL62 search field in the [type A database](https://type-a.fanobase.net/).
For more details, see the [ZeroLocus62 website](https://zl62.homogeneous.tools/).
There is a [very detailed and boring technical specification](https://zl62.homogeneous.tools/specification/) that has all the details.
See also the [original announcement](https://homogeneous.tools/blog/2026/08/16/zerolocus62/).

## Küchle's list

Here are the Grassmannian presentations in [Küchle's original list](https://doi.org/10.1007/BF02571923), with their ZL62 labels.
Each description specifies a bundle whose general section cuts out the fourfold in the indicated Grassmannian.
We write $\mathcal U$ for the tautological subbundle of rank $k$ on $\mathrm{Gr}(k,n)$, $\mathcal Q$ for the quotient bundle of rank $n-k$, and $\mathcal O(1)=\det(\mathcal U^\vee)$ for the Plücker line bundle.
Parentheses denote twists by this line bundle, so $\mathcal F(t)=\mathcal F\otimes\mathcal O(t)$.
The ZL62 labels link to the corresponding presentations in Fanobase.

| Küchle's label | Description | ZL62 label |
| --- | --- | --- |
| (b1) | $\mathcal O(1)\oplus\mathcal O(3)$ on $\mathrm{Gr}(2,5)$ | [`41.19`](https://type-a.fanobase.net/family/1-15-9-a?presentation=41.19) |
| (b2) | $\mathcal O(2)^{\oplus 2}$ on $\mathrm{Gr}(2,5)$ | [`41.55`](https://type-a.fanobase.net/family/1-20-10-a?presentation=41.55) |
| (b3) | $(\bigwedge^3\mathcal Q^\vee)(2)$ on $\mathrm{Gr}(2,6)$ | [`51.f`](https://type-a.fanobase.net/family/1-42-15-a?presentation=51.f) |
| (b4) | $\operatorname{Sym}^2\mathcal U^\vee\oplus\mathcal O(2)$ on $\mathrm{Gr}(2,6)$ | [`51.65`](https://type-a.fanobase.net/family/2-40-15-c?presentation=51.65) |
| (b5) | $\mathcal U^\vee(1)\oplus\mathcal O(1)^{\oplus 2}$ on $\mathrm{Gr}(2,6)$ | [`51.11Z`](https://type-a.fanobase.net/family/1-33-13-a?presentation=51.11Z) |
| (b6) | $\mathcal O(1)^{\oplus 3}\oplus\mathcal O(2)$ on $\mathrm{Gr}(2,6)$ | [`51.1116`](https://type-a.fanobase.net/family/1-28-12-a?presentation=51.1116) |
| (b7) | $\mathcal O(1)^{\oplus 6}$ on $\mathrm{Gr}(2,7)$ | [`601.111111`](https://type-a.fanobase.net/family/1-42-15-a?presentation=601.111111) |
| (b8) | $\operatorname{Sym}^2\mathcal U^\vee\oplus\mathcal O(1)^{\oplus 3}$ on $\mathrm{Gr}(2,7)$ | [`601.1116`](https://type-a.fanobase.net/family/1-56-18-a?presentation=601.1116) |
| (b9) | $(\operatorname{Sym}^2\mathcal U^\vee)^{\oplus 2}$ on $\mathrm{Gr}(2,7)$ | [`601.66`](https://type-a.fanobase.net/family/8-80-21-a?presentation=601.66) |
| (b10) | $\mathcal Q^\vee(1)\oplus\mathcal O(2)$ on $\mathrm{Gr}(2,7)$ | [`601.27`](https://type-a.fanobase.net/family/1-36-14-a?presentation=601.27) |
| (b11) | $\mathcal Q^\vee(1)\oplus\mathcal O(1)^{\oplus 2}$ on $\mathrm{Gr}(2,8)$ | [`701.211`](https://type-a.fanobase.net/family/1-57-18-a?presentation=701.211) |
| (c1) | $\mathcal O(1)^{\oplus 5}$ on $\mathrm{Gr}(3,6)$ | [`53.22222`](https://type-a.fanobase.net/family/1-42-15-b?presentation=53.22222) |
| (c2) | $\bigwedge^2\mathcal U^\vee\oplus\mathcal O(1)\oplus\mathcal O(2)$ on $\mathrm{Gr}(3,6)$ | [`53.271`](https://type-a.fanobase.net/family/1-32-13-a?presentation=53.271) |
| (c3) | $(\mathcal Q^\vee(1))^{\oplus 2}$ on $\mathrm{Gr}(3,7)$ | [`603.33`](https://type-a.fanobase.net/family/1-72-21-a?presentation=603.33) |
| (c4) | $\operatorname{Sym}^2\mathcal U^\vee\oplus\mathcal O(1)^{\oplus 2}$ on $\mathrm{Gr}(3,7)$ | [`603.226`](https://type-a.fanobase.net/family/1-128-33-a?presentation=603.226) |
| (c5) | $\bigwedge^2\mathcal U^\vee\oplus\mathcal Q^\vee(1)\oplus\mathcal O(1)$ on $\mathrm{Gr}(3,7)$ | [`603.321`](https://type-a.fanobase.net/family/1-66-20-a?presentation=603.321) |
| (c6) | $(\bigwedge^2\mathcal U^\vee)^{\oplus 2}\oplus\mathcal O(1)^{\oplus 2}$ on $\mathrm{Gr}(3,7)$ | [`603.2211`](https://type-a.fanobase.net/family/1-61-19-a?presentation=603.2211) |
| (c7) | $(\bigwedge^2\mathcal Q^\vee)(1)\oplus\mathcal O(1)$ on $\mathrm{Gr}(3,8)$ | [`703.42`](https://type-a.fanobase.net/family/2-102-27-a?presentation=703.42) |
| (d1) | $\operatorname{Sym}^2\mathcal U^\vee\oplus\mathcal O(1)^{\oplus 2}$ on $\mathrm{Gr}(4,8)$ | [`707.337`](https://type-a.fanobase.net/family/1-128-33-a?presentation=707.337) |
| (d2) | $\operatorname{Sym}^2\mathcal U^\vee\oplus\bigwedge^2\mathcal U^\vee$ on $\mathrm{Gr}(4,9)$ | [`807.18`](https://type-a.fanobase.net/family/4-384-81-c?presentation=807.18) |
| (d3) | $(\bigwedge^2\mathcal U^\vee)^{\oplus 2}\oplus\mathcal O(1)$ on $\mathrm{Gr}(5,10)$ | [`90F.411`](https://type-a.fanobase.net/family/5-120-31-a?presentation=90F.411) |

Cases (c4) and (d2) have index greater than one, while (d1) is disconnected.
They are included here to retain the original numbering and presentations.
Cases (b3) and (b7) describe isomorphic fourfolds, but their different Grassmannian presentations have different ZL62 labels.
This identification was proved by Laurent Manivel in [*On Fano manifolds of Picard number one*](https://arxiv.org/abs/1502.00475).

I hope you are convinced that having an unambiguous and efficient (and copy-pastable) way of describing zero loci is a useful thing to have!
Maybe it is even worth using in your next paper on zero loci?
