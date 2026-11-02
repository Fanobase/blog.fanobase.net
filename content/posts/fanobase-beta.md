+++
title = "The beta release of type-A data"
date = 2026-11-02
draft = false
authors = ["Pieter Belmans", "Enrico Fatighenti"]
description = "Introducing Fanobase's type-A beta release: our legacy database, quantum periods, computational tools, and the next updates to the catalogue."
+++

Welcome to the beta version of [Fanobase](https://fanobase.net/)!
This post introduces the type A data available today, the computations behind it, and the updates planned for the next weeks.

> *Our aim is to collect all Fano fourfolds that can be constructed using homogeneous vector bundles, compute their invariants, and understand their birational geometry.
> The constructions we will use include zero loci of homogeneous vector bundles on homogeneous varieties of all Lie types, as well as classical and orbital degeneracy loci.*

We want to construct new examples, compare known families, and describe their birational models and the maps between them.
The goal is a navigable birational network for exploring Fano geography in dimension 4, similar to what [Fanography](https://fanography.info/) does in dimension 3.

## The legacy database

This beta release starts from what we call the *legacy database*.

Built by Marcello Bernardara, Enrico Fatighenti, Laurent Manivel, and Fabio Tanturri a few years ago, it collected Fano fourfolds realized as zero loci of homogeneous, globally generated, completely reducible vector bundles on products of homogeneous varieties of type A.
The search imposed an additional condition, which we called *strongly Fano*: if $X$ is cut out by a section of a vector bundle $E$ on $Y$, we require $\mathrm{K}_Y+\det(E)$ to be anti-ample on $Y$ itself.
This is stronger than requiring only that the zero locus $X$ be Fano, but it is a useful condition for enumeration.

Much of our work on the legacy database has been to identify presentations that describe the same variety.
We call these presentations *identified*.
Some identifications are immediate, such as replacing a line in $\mathbb P^2$ by $\mathbb P^1$.
Others reveal more geometry: think of the two models of the sextic del Pezzo surface as a linear section of $\mathbb P^2\times\mathbb P^2$ and as a divisor in $(\mathbb P^1)^3$.

Starting from more than 2,000 zero-locus presentations, we have chosen a single description for each equivalence class under our systematic identification rules, leaving 919 representative presentations.
We have then applied further, less systematic identification rules to group these representatives into 823 clusters for the beta release.
These clusters may still describe the same family, and we are working on further identifications between them.

## Quantum periods

The *quantum period* is a deformation invariant of Fano varieties.
We have computed it for each of our zero loci and found **652 distinct quantum periods** in the legacy database.
Of these, **58 quantum periods seem to be new compared with the lists available in the literature**.

This suggests that the legacy database contains **652 families of Fano fourfolds**.
Matching periods alone do not prove that two presentations belong to the same family, so this remains a conjectural family count.

Recent developments have made these quantum computations more accessible.
The [gwflags software](https://github.com/leonardofcavenaghi/atomicdecompositions) accompanies the paper [*On the atomic decomposition of complete intersection in flag varieties*](https://arxiv.org/abs/2609.21914) by Alexeev, Cavenaghi, Galindo, Georgiev, Katzarkov, and Martins.
It implements localization computations of Gromov–Witten invariants and quantum multiplication for flag varieties and their zero loci.
We use this work to compute the quantum data on the website, including quantum spectra alongside the periods.

## Invariants and birational geometry

For each of the 919 zero-locus presentations, we have set up a page for the information we compute.

The numerical data include Chern numbers, Hodge numbers, polyvector parallelograms, and Hilbert series, in addition to the quantum data described above.
These computations use Oscar's [IntersectionTheory](https://docs.oscar-system.org/stable/Experimental/IntersectionTheory/AbstractVarieties/), [PartialFlagVarieties.jl](https://github.com/HomogeneousTools/PartialFlagVarieties.jl) from [HomogeneousTools](https://homogeneous.tools/), and our internal Macaulay2 code.
IntersectionTheory provides intersection calculations and Chern numbers, while PartialFlagVarieties.jl handles sheaf cohomology and related invariants.

The beta release starts with detailed geometric descriptions for **116 families**.
We are adding descriptions of Mori cones and contractions, together with proofs and links to related entries.
The aim is to let you follow the maps between models and understand how each construction relates to the others.

## Next steps

Within the next weeks, we will release:

- Results from a more systematic search in type A, which is already uncovering interesting new cases beyond the legacy database.
- More geometric descriptions of catalogue entries, with supporting proofs.
- More birational links between entries, with descriptions of the maps and their constructions.

In later releases, we will extend the search beyond type A and add classical and orbital degeneracy loci and other constructions.

We will also release all the data in plain text format on Zenodo soon, so that it can be downloaded and used independently of the website.

The [type A catalogue](https://type-a.fanobase.net/) is available now.

What would you like to see?
Is anything not working for you?
Please get in touch at [info@fanobase.net](mailto:info@fanobase.net).
