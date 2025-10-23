---
layout: default
title: "Collatz Automata"
date: 2025-10-23
---

> Check the [gist](https://gist.github.com/gbragafibra/2c75367423472a741aae74ab8c634762) with the corresponding script.

Consider an almost empty tape with a single marked cell as the initial state, such that the following collatz function is applied to a starting $n$:

$$
f(n) = \begin{cases}
n/2 & \text{if} \quad n \equiv 0 \quad (\text{mod}\, 2) \\
(3n + 1)/2 & \text{if} \quad n \equiv 1 \quad (\text{mod}\, 2) \\
\end{cases}
$$

and depending on the parity of $n$ either [Rule 30](https://en.wikipedia.org/wiki/Rule_30) or another rule is applied during that step (e.g. if $n$ even Rule30 is applied, else Rule18 is applied). This is the example for $n = 10^{30}$ with (Rule30, Rule18):

![](/gifs/col_aut_1e30_r30,18.png)

### Other examples

- $n = 10^{30}$, (Rule30, Rule244):

![](/gifs/col_aut_1e30_r30,244.png)

- $n = 10^{30}$, (Rule30, Rule202):

![](/gifs/col_aut_1e30_r30,202.png)

- $n = 10^{30} - 2$, (Rule30, Rule104):

![](/gifs/col_aut_1e30-2_r30,104.png)

- $n = 10^{30} - 3$, (Rule30, Rule246):

![](/gifs/col_aut_1e30-3_r30,246.png)

- $n = 10^{30} - 4$, (Rule30, Rule202):

![](/gifs/col_aut_1e30-4_r30,202.png)

- $n = 10^{30}$, (Rule30, Rule76):

![](/gifs/col_aut_1e30_r30,76.png)

- $n = 10^{30}$, (Rule30, Rule104):

![](/gifs/col_aut_1e30_r30,104.png)

- $n = 10^{30}$, (Rule30, Rule144):

![](/gifs/col_aut_1e30_r30,144.png)

- $n = 10^{30}$, (Rule30, Rule156):

![](/gifs/col_aut_1e30_r30,156.png)

- $n = 10^{30}$, (Rule30, Rule170):

![](/gifs/col_aut_1e30_r30,170.png)









[Back](https://gbragafibra.github.io)
