+++
title = "Fano Tuesday: Blowing up a point"
date = 2026-11-24
draft = false
authors = ["Francesco Denisi"]
description = "Which varieties remain Fano after blowing up a point, and which fourfolds in this classification appear in Fanobase?"
+++

Welcome to *Fano Tuesday*, a series of posts spotlighting features of our database and examples that might otherwise get lost in the wilderness.

In algebraic geometry, we like blowing up varieties.
But what is the simplest thing we can blow up?
A point, of course!
Now, suppose we start with a Fano variety and blow up a point.
Will the resulting variety still be Fano?
Well, not necessarily.
But what if we turn the question around?
If the blow-up at a point is Fano, must the original variety have been Fano too?
In general, blowing down a Fano variety [does not necessarily give us another Fano variety](https://doi.org/10.1007/s10711-004-1816-1).
However, when it comes to blowing up a single point, the story has a happy ending: the Fano property does descend.

## The classification

Requiring the blow-up of a smooth projective variety at a point to be Fano imposes strong restrictions on the original variety, as shown by [Bonavero, Campana and Wiśniewski](https://doi.org/10.1016/S1631-073X(02)02284-7).

**Theorem (Bonavero–Campana–Wiśniewski).**
*Let $X$ be a smooth complex projective variety of dimension $n\geq 3$, and let $p\in X$.
Then $\operatorname{Bl}_p X$ is Fano if and only if one of the following holds:*

1. *$X\cong\mathbb P^n$, with $p$ arbitrary;*
2. *$X\cong Q^n$, a smooth quadric, with $p$ arbitrary;*
3. *$X\cong V_d:=\operatorname{Bl}_Y\mathbb P^n$, where $Y\subset\mathbb P^n$ is a smooth codimension-two subvariety of degree $1\leq d\leq n$, contained in a hyperplane $H$, and $p$ maps to a point of $\mathbb P^n\setminus H$ under the blow-down.*

Thus, in dimension four, we are interested in $\mathbb P^4$, $Q^4$, and $V_d$ for $d=1,\ldots,4$, together with their blow-ups at points in the positions prescribed by the theorem.

## The fourfolds in Fanobase

Which of these varieties appear in [our database](https://type-a.fanobase.net/)?
Comparing numerical invariants leaves four candidates among the varieties *before* the point blow-up.
All of them have a strongly Fano presentation in our database:

| Variety | Database ID |
| --- | --- |
| $\mathbb P^4$ | [1-625-126-a](https://type-a.fanobase.net/family/1-625-126-a) |
| $Q^4$ | [1-512-105-a](https://type-a.fanobase.net/family/1-512-105-a) |
| $V_1=\operatorname{Bl}_{\mathbb P^2}\mathbb P^4$ | [2-512-105-b](https://type-a.fanobase.net/family/2-512-105-b) |
| $V_2=\operatorname{Bl}_{Q^2}\mathbb P^4$ | [2-431-90-a](https://type-a.fanobase.net/family/2-431-90-a) |

Blowing up a point in the prescribed position on $\mathbb P^4$, $Q^4$, $V_1$, and $V_2$ gives the following varieties, in the same order.
All four also have strongly Fano presentations in our database:

| Point blow-up | Database ID |
| --- | --- |
| $\operatorname{Bl}_p\mathbb P^4$ | [2-544-111-a](https://type-a.fanobase.net/family/2-544-111-a) |
| $\operatorname{Bl}_p Q^4$ | [2-431-90-a](https://type-a.fanobase.net/family/2-431-90-a) |
| $\operatorname{Bl}_{p\sqcup\mathbb P^2}\mathbb P^4$ | [3-431-90-b](https://type-a.fanobase.net/family/3-431-90-b) |
| $\operatorname{Bl}_{\lbrace q,r\rbrace}Q^4$ | [3-350-75-a](https://type-a.fanobase.net/family/3-350-75-a) |

The last row uses a second description of $V_2$: contracting the strict transform of $H$ gives $Q^4$, so $V_2\cong\operatorname{Bl}_q Q^4$.
The point $p$ maps to a second point $r$, and thus $\operatorname{Bl}_p V_2\cong\operatorname{Bl}_{\lbrace q,r\rbrace}Q^4$.
The line joining $q$ and $r$ is not contained in $Q^4$.
This is precisely the condition for the two-point blow-up to be Fano, as shown by [Bonavero, Campana and Wiśniewski](https://doi.org/10.1016/S1631-073X(02)02284-7).

## The missing cases

But what about the remaining cases $V_d=\operatorname{Bl}_{S_d}\mathbb P^4$ for $d=3,4$, and their point blow-ups?
Here $S_d$ is a smooth surface of degree $d$ in a hyperplane of $\mathbb P^4$.
These varieties are not recorded in the currently available database.

For every $d\geq 1$, regardless of whether $V_d$ is Fano, both $V_d$ and its blow-up at the prescribed point admit presentations as zero loci of sections of homogeneous, completely reducible bundles.
For $V_d$, such a presentation is given on $A=\mathbb P^9\times\mathbb P^4\times\mathbb P^4$:

<div>
\begin{equation}
\begin{aligned}
V_d &\cong \mathrm{Z}_A(\mathcal F),\\
\mathcal F &= \mathcal Q_2(1,0,0)\oplus\mathcal Q_3(1,0,0)\oplus\mathcal Q_3(0,d,0)\oplus\mathcal O(1,0,0).
\end{aligned}
\end{equation}
</div>

Here $\mathcal Q_2$ and $\mathcal Q_3$ are the universal quotient bundles pulled back from the second and third factors, and the three entries in each twist refer to the three factors of $A$.

Unfortunately, this presentation does not satisfy the *strongly Fano* condition.
That condition requires $\omega_A^{-1}\otimes(\det\mathcal F)^{-1}$ to be ample on the ambient variety $A$ itself.
In this case,

<div>
\begin{equation}
\det\mathcal F=\mathcal O(9,4d+1,2),
\end{equation}
</div>

and hence

<div>
\begin{equation}
\omega_A^{-1}\otimes(\det\mathcal F)^{-1}
=\mathcal O(1,4-4d,3),
\end{equation}
</div>

which is not ample for any $d\geq 1$.
The analogous presentation of the point blow-up is not strongly Fano either.

On the other hand, both $V_3$ and $V_4$, and their respective blow-ups at points in the position prescribed by the theorem, admit strongly Fano presentations as zero loci of sections of homogeneous vector bundles that are **not completely reducible**.
Why can't we have both complete reducibility and the strongly Fano condition?
We'll return to this question in a future Fano Tuesday!
In the meantime, take a look at the examples already appearing on [our website](https://type-a.fanobase.net/).
