---
layout: default
title: "Autopoietic Networks (a few more examples)"
date: 2025-05-27
---

This is a type of cellular automaton which was initially designed to simulate [autopoiesis](https://en.wikipedia.org/wiki/Autopoiesis). 

Here, a network of $N × N$ cells is initialized with a state and a corresponding gate associated to it. In the example below for instance, the cells in a small central square region have their state initialized to 1 (the rest of them to 0), but every cell in the network has a gate randomly sampled from a given set (examples below with `AND`, `OR` and `XOR`). After each iteration, each cell updates its state according to the gate allocated to it, and according to the neighbors' states (itself included) in a radius $r$. Additionally, each cell has a $\Phi$ value associated to it, that is increased by 1 if the cell's state remains the same over consecutive iterations, and is reset to 0 if not. On top of all of this, if a cell reaches $Φ = \epsilon$, its state is propagated to cells in the neighborhood. 

With $ε = 3$, $r = 2.5$, and gates `AND`, `OR`, `XOR`. 

![](/gifs/autopoietic_multiple2.gif)

These three following examples instead of using the previously mentioned gates, use `MAJORITY`, `MEAN`, `MAX` and `MIN` (`MAJORITY` takes the mean over the inputs which exceed the value $0.5$). Additionally, the cells in the square region have their state randomly initialized from $[0, 1]$. All three have $ε = 15$, $r = 2.2$, and a precision parameter $θ = 0.1$ for which the difference between consecutive iterations is to be compared to (if such difference is smaller than $\theta$, then $\Phi$ is increased).

Furthermore, these three examples also have some other restrictions. The state is not being propagated from the central cell to every other cell in the neighborhood.

In the first example, it's only propagated to cells in the corresponding neighborhood which also have $\Phi$ superior to that of the main cell.

![](/gifs/autopoietic_multiple_higher.gif)

In the second, such propagation only happens to the cells which have $\Phi$ equal to the main cell's.

![](/gifs/autopoietic_multiple_equal.gif)

And in this one, propagation is restricted to those which hold a lower $\Phi$.

![](/gifs/autopoietic_multiple_lower.gif)

The [messy repo](https://github.com/gbragafibra/autopoietic-nets) also includes various other examples, including ones for which gate propagation is also applied.

[Back](https://gbragafibra.github.io)
