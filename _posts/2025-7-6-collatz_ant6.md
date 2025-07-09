---
layout: default
title: "Self-Cleaning Ants"
date: 2025-07-06
---

> Correction (July 09, 2025): Updates on how $\tau$	was being computed through the count of frames (e.g. as in the following [script](https://github.com/gbragafibra/collatz-ant/blob/main/collatz_ant_score.py)). Now corrected to `τ = len(frames) - 1`, not counting initial empty frame. Along with a few minor tweaks and additions. 

Relevant preceding posts [here](https://gbragafibra.github.io/2025/01/08/collatz_ant2.html), [here](https://gbragafibra.github.io/2025/05/18/collatz_ant3.html) and [here](https://gbragafibra.github.io/2025/07/06/collatz_ant5.html).

Consider again a score function $\Sigma(n)$ which for a given $n$, outputs the number of 1's (or marked states) left by the ant on the landscape at the end of the run. A self-cleaning ant (in a similar manner to the use of the term [self-cleaning Turing machines](https://nickdrozd.github.io/2021/07/11/self-cleaning-turing-machine.html)) is one for which $\Sigma(n) = 0$. Unlike Turing machines, for which the symbols left on the corresponding tape affect the dynamics, dictating state-transition, here the dynamics of the ant are purely dictated by the collatz function for the corresponding $n$. The landscape is a by-product of such.

Anyways. $1704$ is an example of a self-cleaning ant, with a stopping time of $τ = 16$. Represented next is the corresponding landscape:

![](/gifs/collatz_ant_sc1704.gif)

One would perhaps wonder if these self-cleaning ants are rare or not, and what their distribution is. Well from $n = 2$ to $n = 10^{6}$, we have the following (and with respective stopping times):

- Powers of 2 marked with *

|$n$|$τ_{n}$|
|---|---|
|256*|8|
|1704|16|
|1813|16|
|2009|24|
|10880|16|
|12056|24|
|65536*|16|
|72808|24|
|72817|24|
|77136|24|
|85717|32|
|91744|32|
|101581|40|
|436224|24|
|436904|24|
|464128|24|
|464213|24|
|465568|24|
|504712|32|
|514304|32|
|514389|32|
|548400|32|
|548557|32|
|586561|40|
|609488|40|
|609745|40|
|785605|56|

A mere 27 self-cleaning ants from a set of one million ants? And also only two of these are powers of 2. For a (trivial) self-cleaning ant, which would inherently be a power of 2, we would need two full rotations of the ant. The first one to mark the states, and the second to delete them. Consider the first example of a trivial self-cleaning ant, $n = 256$:

![](/gifs/collatz_ant_sc256.gif) 

In fact, the trivial self-cleaning ants would be easy to predict and would be given by $n = 2^{8k},\, k ∈ \mathbb{N}$. With $k = 1$ we have $n = 256$, with $k = 2$ we have the other self-cleaning ant we see $n = 65536$, with $k = 3$ we would have $n = 16777216$, and so on.

For the non-trivial ones, presumably there isn't such an easy pattern. We can of course group these self-cleaning ants (trivial ones included) by their corresponding stopping times $τ$ according to a parameter $j ∈ \mathbb{N}$, such that $τ = 8j$.

It's important to note that this doesn't mean that the corresponding landscapes are going to be the same. Take into account some of the examples for which $τ = 40$ with $j = 5$:

| $n = 586561$ | $n = 609488$ | $n = 609745$ |
|-----------|-----------|-----------|
| ![](/gifs/collatz_ant_ex1.gif) | ![](/gifs/collatz_ant_ex2.gif) | ![](/gifs/collatz_ant_ex3.gif) |

Additionally, one might think that these self-cleaning ants are going to behave pretty much like the example shown above of $n = 1704$, but these can start showing some interesting behaviour. Consider $n = 785605$:

![](/gifs/collatz_ant_sc785605.gif)

[Back](https://gbragafibra.github.io)
