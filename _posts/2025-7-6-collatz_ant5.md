---
layout: default
title: "Collatz's Ant and Σ(n)"
date: 2025-07-06
---

Relevant preceding posts [here](https://gbragafibra.github.io/2025/01/08/collatz_ant2.html) and [here](https://gbragafibra.github.io/2025/05/18/collatz_ant3.html).

Consider the corresponding ant's landscape development for $n = 500$:

![](/gifs/collatz_ant500.gif)

with the last frame being:

![](/gifs/collatz_ant_last500.png)

Let's also consider a score function $\Sigma(n)$ which returns the number of 1's (or marked states) left by the ant on the corresponding landscape (regarding the last frame). With the prior example, we would have $\Sigma(500) = 54$. We might also want to normalize this by the corresponding stopping time $\tau_{n}$ characteristic of the collatz function dynamics for a given $n$. As such, given $\tau_{500} = 111$, we would have $\frac{\Sigma(500)}{\tau_{500}} ≈ 0.49$.

Additionally, let's also consider some metrics relative to the ant's (euclidean) distance to the origin. Say $α$ is the maximum distance reached relative to the origin over the whole development of the landscape, and $γ$ is the distance from the origin at the last frame (so where the ant ends up). For $n = 500$, we would have the ratio $\frac{\gamma}{\alpha} ≈ 0.87$.

The following is a representation of such metrics for numbers from $n = 2$ to $n = 50000$:

![](/gifs/norma_score3.png)

[Back](https://gbragafibra.github.io)
