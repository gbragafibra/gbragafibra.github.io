---
layout: default
title: "Collatz's Ant"
date: 2024-12-21
---

Collatz's Ant is a visualization for collatz sequences based on [Langton's Ant](https://en.wikipedia.org/wiki/Langton%27s_ant).

Additionally to what the [collatz function](https://en.wikipedia.org/wiki/Collatz_conjecture) is:

$$
f(n) = \begin{cases}
n/2 & \text{if} \quad n \equiv 0 \quad (\text{mod}\, 2) \\
3n + 1 & \text{if} \quad n \equiv 1 \quad (\text{mod}\, 2) \\
\end{cases}
$$

if $n \equiv 0 \, (\text{mod}\, 2)$ the ant turns 90º clockwise, else the ant turns 90º counter-clockwise. On both accounts, the state of the cell is flipped and the ant moves forward one unit. This is repeated until $n = 1$.

[Code and examples](https://github.com/gbragafibra/collatz-ant).

### Some examples

![](/gifs/collatz_ant1.gif)

![](/gifs/collatz_ant5.gif)

Example of consecutive trajectories from $n = 10^{30}$ to $n = 10^{30} + 20$.

![](/gifs/collatz_ant_grid.gif)

[Back](https://gbragafibra.github.io)
