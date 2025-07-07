---
layout: default
title: "Self-Cleaning Ants"
date: 2025-07-06
---

Relevant preceding posts [here](https://gbragafibra.github.io/2025/01/08/collatz_ant2.html), [here](https://gbragafibra.github.io/2025/05/18/collatz_ant3.html) and [here](https://gbragafibra.github.io/2025/07/06/collatz_ant5.html).

Consider again a score function $\Sigma(n)$ which for a given $n$, outputs the number of 1's (or marked states) left by the ant on the landscape at the end of the run. A self-cleaning ant (in a similar manner to the use of the term [self-cleaning Turing machines](https://nickdrozd.github.io/2021/07/11/self-cleaning-turing-machine.html)) is one for which $\Sigma(n) = 0$. Unlike Turing machines, for which the symbols left on the corresponding tape affect the dynamics, dictating state-transition, here the dynamics of the ant are purely dictated by the collatz function for the corresponding $n$. The landscape is a by-product of such.

Anyways. $1704$ is an example of a self-cleaning ant, with a stopping time of $τ = 17$. Represented next is the corresponding landscape:

![](/gifs/collatz_ant_sc1704.gif)

One would perhaps wonder if these self-cleaning ants are rare or not, and what their distribution is. Well from $n = 2$ to $n = 10^{6}$, we have the following (and with respective stopping times):

- Powers of 2 marked with *

|$n$|$τ_{n}$|
|---|---|
|256*|9|
|1704|17|
|1813|17|
|2009|25|
|10880|17|
|12056|25|
|65536*|17|
|72808|25|
|72817|25|
|77136|25|
|85717|33|
|91744|33|
|101581|41|
|436224|25|
|436904|25|
|464128|25|
|464213|25|
|465568|25|
|504712|33|
|514304|33|
|514389|33|
|548400|33|
|548557|33|
|586561|41|
|609488|41|
|609745|41|
|785605|57|

A mere 27 self-cleaning ants from a set of one million ants? And also only two of these are powers of 2. For a (trivial) self-cleaning ant, which would inherently be a power of 2, we would need two full rotations of the ant. The first one to mark the states, and the second to delete them. Consider the first example of a trivial self-cleaning ant, $n = 256$:

![](/gifs/collatz_ant_sc256.gif) 

In fact, the trivial self-cleaning ants would be easy to predict and would be given by $n = 2^{8k},\, k ∈ \mathbb{N}$. With $k = 1$ we have $n = 256$, with $k = 2$ we have the other self-cleaning ant we see $n = 65536$, with $k = 3$ we would have $n = 16777216$, and so on.

For the non-trivial ones, presumably there isn't such an easy pattern.

Additionally, one might think that these self-cleaning ants are going to behave pretty much like the example shown above of $n = 1704$, but these can start showing some interesting behaviour. Consider $n = 785605$:

![](/gifs/collatz_ant_sc785605.gif)

[Back](https://gbragafibra.github.io)
