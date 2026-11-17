+++
title = "Fano Tuesday: The importance of being strongly Fano"
date = 2026-11-17
draft = false
authors = ["Enrico Fatighenti"]
description = "A Fano fourfold gives a strongly Fano presentation of the Mori-Mukai threefold 2-18."
+++

In this *second* installment of **Fano Tuesday**, we explore how a Fano fourfold can shed new light on the geometry of Fano threefolds.

Today, we start with the family [2-513-105-b](https://type-a.fanobase.net/family/2-513-105-b).
At first sight, there is nothing particularly remarkable about this Fano fourfold.
It has two rather simple descriptions:

- The projection to $\mathbb P^2$ realizes it as $Y\simeq\mathbb P_{\mathbb P^2}(\mathcal O(-1)^{\oplus 2}\oplus\mathcal O)$.
- The projection to $\mathrm{Gr}(2,5)$ is a small resolution of the projective cone over the Segre embedding of $\mathbb P^1\times\mathbb P^2$, contracting a copy of $\mathbb P^2$ to its vertex.

For the full geometry of these projections, see the [mini-article](https://type-a.fanobase.net/pdfs/2-513-105-b.pdf).

## Strongly Fano presentations

The interesting thing is that this rather innocent fourfold has led me to a new construction for Fano threefolds.
But first, a little background.

For the moment, in [FanoBase](https://type-a.fanobase.net/), we are collecting zero loci admitting a *strongly Fano* presentation.
By this we mean a presentation $X=\mathrm{Z}_A(\mathcal F)$ as the zero locus of a general section of a homogeneous vector bundle $\mathcal F$ on a product $A$ of homogeneous varieties, such that $\omega_A^\vee\otimes\det(\mathcal F)^\vee$ is ample **on the ambient variety $A$ itself**, before restricting to $X$.
There are several reasons for imposing this condition, mainly related to enumeration: we will expand on this in the future.

Notice that ample line bundles on products of flag varieties are very ample, so a strongly Fano presentation automatically implies that $\omega_X^\vee$ is very ample.
As it turns out, strongly Fano presentations are remarkably effective in low dimensions.

For example, in [De Biase–Fatighenti–Tanturri — *Fano 3-folds from homogeneous vector bundles over Grassmannians*](https://doi.org/10.1007/s13163-021-00401-2), we found that, among the **98 Mori–Mukai families with very ample anticanonical bundle**, 84 admit a strongly Fano presentation among the classical homogeneous models considered there.
The remaining 14 cases, in Mori–Mukai notation, are:

**[1-12](https://fanography.info/1-12/), [2-8](https://fanography.info/2-8/), [2-18](https://fanography.info/2-18/), [3-1](https://fanography.info/3-1/), [3-2](https://fanography.info/3-2/), [3-4](https://fanography.info/3-4/), [3-5](https://fanography.info/3-5/), [3-9](https://fanography.info/3-9/), [3-14](https://fanography.info/3-14/), [4-2](https://fanography.info/4-2/), [4-5](https://fanography.info/4-5/), [4-13](https://fanography.info/4-13/), [5-1](https://fanography.info/5-1/), [5-2](https://fanography.info/5-2/).**

Of course, this does not mean that these families cannot admit strongly Fano models.
It only means that the presentations considered in our paper do not satisfy the required positivity condition.
**Or, rather, this was the situation until today.**

## From fourfolds to threefolds

Thanks to our fourfold [2-513-105-b](https://type-a.fanobase.net/family/2-513-105-b), we can now add one more strongly Fano presentation *of a Fano threefold*, in a surprisingly simple way.
Consider the homogeneous description linked above and cut it with an additional general quadric of type $\mathcal O(0,2)$.
Under the projection to $\mathrm{Gr}(2,5)$, we are simply intersecting the cone over $\mathbb P^1\times\mathbb P^2$ with a quadric, which we may assume avoids the vertex of the cone.
Projecting from that vertex then gives a double cover $X\longrightarrow B=\mathbb P^1\times\mathbb P^2$.

But what about its branch divisor?
To compute it, we blow up the vertex of the cone, obtaining the projective bundle $\mathbb P_B(E)$, where $E=\mathcal O_B\oplus\mathcal O_B(-1,-1)$.
This does not change the double cover, since the quadric does not pass through the vertex.
The quadric defines a symmetric morphism $\varphi:E\longrightarrow E^\vee$, and the branch divisor is precisely the degeneracy locus $\mathrm{D}_1(\varphi)$, where $\varphi$ has rank at most one.

By the Thom–Porteous formula, its class is $[\mathrm{D}_1(\varphi)]=\mathrm{c}_1(E^\vee)-\mathrm{c}_1(E)=2h_1+2h_2$, where $h_1$ and $h_2$ are the pullbacks of the hyperplane classes from the two factors of $B$.
Hence the branch divisor has bidegree $(2,2)$.
And this is exactly the Mori–Mukai family **[2-18](https://fanography.info/2-18/)**: the double cover of $\mathbb P^1\times\mathbb P^2$ branched along a divisor of bidegree $(2,2)$.

Even better, the presentation we have just constructed is strongly Fano, as is easily checked.
So a very simple Fano fourfold from our database has provided a new strongly Fano presentation of a classical Fano threefold.

And what happens for the other 13 families?
Using a very similar argument, we can find a simple strongly Fano model for the threefold **[4-2](https://fanography.info/4-2/)**, where the bundle involved is completely reducible.
For some other families, it seems that we can find strongly Fano models, but we need to use bundles that are not completely reducible.

There is still work to be done to understand potential obstructions — stay tuned for that!
More generally, it would be very nice if our program in dimension four could also teach us something new about a classification we thought we already knew so well!
