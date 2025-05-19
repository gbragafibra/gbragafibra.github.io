---
layout: default
title: "Collatz's Ant - alternative representation of collatz dynamics"
date: 2025-05-19
---

Preceding posts [here](https://gbragafibra.github.io/2025/01/08/collatz_ant2.html) and [here](https://gbragafibra.github.io/2025/05/18/collatz_ant3.html).

Consider the example of the landscape of $n = 10^{20} + 99$:

![](/gifs/landscape_1e20_99.png)

along with the development of its trajectory:

![](/gifs/collatz_ant_1e20_99.gif)

And this is what both the position (euclidean distance) and angle (rads) with respect to the origin look like over time:

![](/gifs/dist_1e20_99.png)

Let's us forget for a moment that we are talking about a different representation of collatz dynamics for each $n$, based on Langton's Ant.

Imagine you're given a set of landscapes (peek at [last post](https://gbragafibra.github.io/2025/05/18/collatz_ant3.html) for a variety of examples), along with the corresponding trajectories' development, and some plotting of distance and angles with respect to the origin over time. The only thing you have associated to each of these is the corresponding number $n$. You have purposefully forgotten anything to do with the collatz function itself. You see some systems which could presumably be modelled after random walks (majority of examples by needing to add some drift term). Additionally, you start noticing that a good chunk of these landscapes correspond to the same form, even if with minute differences. 

The question is:

- Could one explain the specificity of each landscape (as in the form produced), and how $n$ influences it, without relying on any contextualization with the collatz function?	

[Back](https://gbragafibra.github.io)
