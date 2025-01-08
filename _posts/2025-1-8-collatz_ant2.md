---
layout: default
title: "Collatz's Ant and similarity of collatz sequences"
date: 2025-01-08
---

This is a brief continuation of a previous [post](https://gbragafibra.github.io/2024/12/21/collatz_ant.html) ([Repo](https://github.com/gbragafibra/collatz-ant)), which introduced such visualization for collatz sequences based on [Langton's Ant](https://en.wikipedia.org/wiki/Langton%27s_ant).

Collatz's Ant is based on the [collatz function](https://en.wikipedia.org/wiki/Collatz_conjecture):

$$
f(n) = \begin{cases}
n/2 & \text{if} \quad n \equiv 0 \quad (\text{mod}\, 2) \\
3n + 1 & \text{if} \quad n \equiv 1 \quad (\text{mod}\, 2) \\
\end{cases}
$$

and additionally, if $n \equiv 0 \, (\text{mod}\, 2)$ the ant turns 90º clockwise, else the ant turns 90º counter-clockwise. On both accounts, the state of the cell is flipped and the ant moves forward one unit. This is repeated until $n = 1$. An example of such is present in the following animation:


![](/gifs/collatz_ant1.gif)

Example of consecutive trajectories from $n = 10^{40}$ to $n = 10^{40} + 20$.

![](/gifs/collatz_ant40.gif)

And although this representation is interesting, the flipping of state can eventually lead to ambiguous scenarios<span class="footnote" data-footnote="Although this particular case isn't an example of that.">1</span> where trajectories seem similar to each other through omission.

Given that, the following picture corresponds to the ant's landscape (final snapshot) without state flipping for the same trajectories, along with respective stopping times. This is done by merely adding a $+1$ count to each coordinate the ant has been through<span class="footnote" data-footnote="The color scheme intensity is relative to the stopping time of each corresponding trajectory.">2</span>.

![](/gifs/collatz_ant_attractor40.png)

### Some other examples

The first 100 numbers from $n = 2$ to $n = 102$.

![](/gifs/collatz_ant_attractor2-102.png)

From $n = 10^{9}$ to $n = 10^{9} + 100$.

![](/gifs/collatz_ant_attractor9.png)

From $n = 10^{20}$ to $n = 10^{20} + 100$.
<a name="ref-1"></a>

![](/gifs/collatz_ant_attractor20.png)

From $n = 10^{200}$ to $n = 10^{200} + 10$.

![](/gifs/collatz_ant_attractor200.png)

### Some interesting things

- Very similar landscapes have the same stopping time (or similar ones)<span class="footnote" data-footnote="Due to converging to the same sub-trajectory.">3</span>, but the inverse isn't true. An example of the inverse not being true, is present in [this comparison between](#ref-1) $n = 10^{20} + 1$ (1st row, 2nd col) and $n = 10^{20} + 16$ (4th row, 2nd col), both with stopping times 532.

If we check the similarity between both of these trajectories:

```python
import numpy as np
import mpmath

def collatz_seq(n):
    seq = []
    while n != 1:
        seq.append(n)
        if n % 2 == 0:
        	n /= 2
        else:
        	n = 3*n + 1
    return seq

mpmath.mp.dps = 22
n1 = mpmath.mpf("1e20") + 1
n2 = mpmath.mpf("1e20") + 16
len(np.intersect1d(collatz_seq(n1), collatz_seq(n2)))
```
```text
Output: 142
```
If the same is done between $n = 10^{20} + 16$ and $n = 10^{20} + 20$, which have similar landscapes and the same stopping time, we get:
```text
Output: 527
```

- Furthermore, if we now look at an example of sub-trajectories converging, in this case with a difference of 5 steps between each, we can see that the landscapes are pretty similar to each other, but for the rotation (which seems to overall be of 90º)<span class="footnote" data-footnote="Or any combination of direction changes in those 5 extra steps which adds to such angle.">3</span>. This is of course the product of the early re-orientation of the ant given those 5 extra steps.

Example with $n = 18750000000000000004$ and $n = 10^{20} + 16$, the former being found after 5 reduction steps of the latter.

![](/gifs/collatz_ant_attractor_rotation.png)

Now with a difference of 100 steps, the landscapes still seem very similar but for a rotation of 180º.

![](/gifs/collatz_ant_attractor_rotation100.png)

With a difference of 200 steps, the landscapes start losing some detail relative to each other.

![](/gifs/collatz_ant_attractor_rotation200.png)

And with 300 steps, only a few larger-scale characteristics are now common between the two landscapes.

![](/gifs/collatz_ant_attractor_rotation300.png)

[Back](https://gbragafibra.github.io)
