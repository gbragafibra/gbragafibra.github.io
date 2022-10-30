---
author:
- '<span style="font-variant:small-caps;">Gonçalo Braga</span>'
bibliography:
- 'References\_final.bib'
title: '<span style="font-variant:small-caps;">Can you tell an aged cell?</span>'
...

------------------------------------------------------------------------

Main considerations
===================

Given a system with current state $i$, such system would have
corresponding energetic content given by $$E_{i} \simeq m_{i}c^{2}$$
where $m_{i}$ and $c$ represent the mass of the system in such state and
the speed of light, respectively. Furthermore, accounting for
Bremermann’s limit @aharonov1961time@lloyd2000ultimate, we will have the
maximum number of logical operations per $\Delta t$, in computing
systems, or the maximum number of state transitions[^1], based on
$E_{i}$. If we set $\Delta t = 1$ second, we then have the maximum
number of state transitions allowed per second, as
$$N_{max} = \frac{2E_{i}}{\pi\hbar}$$

\[Consideration 2\] Given the following state transition
$i \rightarrow j$ with elapsing time
$\Delta \tau = \tau_{j} - \tau_{i}$, over temperature $T$, we would have
the following metrics
$$\Delta S(\pi_{ij}) = \frac{\Delta Q_{j} - \Delta Q_{i}}{T} = \frac{\Delta Q_{ij}}{T}$$
$$\label{Equation 4}
\Delta \pi_{ij} = \frac{1}{T}\bigintssss_{\tau_{i}}^{\tau_{j}}\lvert\Delta Q_{\tau} - \langle \Delta Q \rangle_{\Delta \tau}\rvert \, d\tau$$
or[^2] $$\label{Equation 5}
\Delta \pi_{ij} = \frac{1}{T}\left\langle \sum_{k = 1}^{n} A_{k} \right\rangle$$
$$\bullet \,\langle \Delta Q \rangle_{\Delta \tau}\, \textrm{being an attractor point characteristic of the said system.}\footnote{Although this attractor point doesn't need to be constant, and in fact varies given respective inputs into the system.}$$

with illustration given in Fig.\[Figure 1\]. There’s some discussion
about these metrics in Appendix \[App A\].

\[smooth, xmin=0, xmax=23, ymin=0, ymax=7, width = 15cm, axis lines =
left, xlabel = $\tau$ (a.u.), ylabel = $\Delta Q (J)$, clip = false, \]
+\[color = black, mark = o\]coordinates <span> ( 0, 5.2 ) ( 1, 2.3 ) (
2, 5 ) ( 3, 2 ) ( 4, 5.4 ) ( 5, 1.9 ) ( 6, 4.7 ) ( 7, 2.3 ) ( 8, 5.2 ) (
9, 1.8 ) ( 10, 5 ) ( 11, 2.1 ) ( 12, 5.3 ) ( 13, 2.5 ) ( 14, 5.4 ) ( 15,
2 ) ( 16, 5.2 ) ( 17, 1.9 ) ( 18, 5.1 ) ( 19, 2.2 ) ( 20, 5.3 ) ( 21,
2.3 ) </span>;

node\[right,
pos=1\]<span>$\langle \Delta Q \rangle_{\Delta \tau}$</span>;

\(1) at (0.1,6.2)<span>1</span>; (2) at (0.55,5.2)<span>2</span>; (3) at
(1.1,6.4)<span>3</span>; (4) at (1.7,5.2)<span>4</span>; (5) at
(2.3,6.4)<span>5</span>; (6) at (2.9,5.2)<span>6</span>; (7) at
(3.5,6.4)<span>7</span>; (8) at (4.1,5.2)<span>8</span>; (9) at
(4.7,6.4)<span>9</span>; (10) at (5.25,5.2)<span>10</span>; (11) at
(5.82,6.4)<span>11</span>; (12) at (6.37,5.2)<span>12</span>; (13) at
(7,6.4)<span>13</span>; (14) at (7.6,5.4)<span>14</span>; (15) at
(8.15,6.4)<span>15</span>; (16) at (8.75,5.2)<span>16</span>; (17) at
(9.35,6.4)<span>17</span>; (18) at (9.9,5.2)<span>18</span>; (19) at
(10.5,6.4)<span>19</span>; (20) at (11.1,5.2)<span>20</span>; (21) at
(11.7,6.4)<span>21</span>; (22) at (12.4,5.2)<span>22</span>;

\(i) at (0, 8.47); (I) at (1.2, 9.5)<span>state $i$</span>; (I) to (i);
(j) at (12.2, 3.7); (J) at (11.4, 2)<span>state $j$</span>; (J) to (j);

(legend) at (6,
11)<span>$\Delta S(\pi_{ij}) = \dfrac{\Delta Q_{j} - \Delta Q_{i}}{T}$
$\Delta \pi_{ij} = \frac{1}{T}\left\langle \sum_{k = 1}^{22} A_{k} \right\rangle$</span>;

Given the metrics introduced in consideration \[Consideration 2\], we
can add an error-rate, $\epsilon$, representing how much change occured
from state $i$ to $j$, as
$$\epsilon \propto \frac{\lvert\Delta S(\pi_{\Delta \tau})\rvert + \Delta \pi_{\Delta \tau}}{\langle \Delta Q \rangle_{\Delta \tau}\times\frac{1}{T}}$$
where
$\langle \Delta Q \rangle_{\Delta \tau}\times\frac{1}{T} = \langle \Delta S \rangle_{\Delta \tau}$
can be viewed as the entropic cost of maintaining the respective
attractor point. Employing Bremermann’s limit again, we can also have
the maximum amount of state transitions per second allowed over the
value $\langle \Delta Q \rangle_{\Delta \tau}$[^3], as
$$N = \frac{2\langle \Delta Q \rangle_{\Delta \tau}}{\pi\hbar}$$ and
another metric relating $N_{max}$ and $N$, as $$\label{Equation 8}
\Theta = \frac{N_{max} - N}{N_{max}}$$ indicating how much heat a
certain system releases, given its energy content.

Regarding the change of energetic content of such a system after a
transition $i \rightarrow j$, we would have
$$\Delta E = E(\chi) - \Delta Q_{\Delta \tau}$$ where $E(\chi)$
represents the energetic content of an input set $\chi$. Taking this
into account, we can then have a general model of computation such as
the following one

\[Figure 2\]

\[node distance = 5cm\] (i)\[state\] <span>$i$</span>; (input)\[state,
\] \[above left of = i\] <span>$E(\chi)$</span>; (transform)\[state,
rectangle\] at (5,0) <span>Transform</span>; (i+1)\[state\] at (10,0)
<span>$j$</span>; (output)\[state\] \[above left of = i+1\]
<span>$\Delta Q_{\Delta \tau} \geq k_{B}T\ln2$ $^{\dagger}$</span>; (i)
to (transform); (transform) to (i+1); (input) to (i); (transform) to
(output); (i) to (i+1); (i+1) to\[“$\Delta \tau$”\] (i);

These priorly mentioned metrics might be used to separate systems, not
according to what categories we might find easier to distinguish
between, but according to their heat oscillation dynamics[^4].

Multi-scale selection and aging
===============================

Why do *Pogonomyrmex owyheei* ant queens live about 30 years
@holldobler1990ants, while the worker-caste counterpart lives on average
a year, and the drone-caste a few days? And this tendency seems to hold
over majority of eusocial insects. Regardless of the caste each ant
belongs to, they have the same genome. However, they will have
differences in epigenetic modulation, which will end up leading to
differences in phenotypes[^5]. There seem to be transitions between
castes, for example between worker and queen status, accounted by a
small number of different transcription factors @gospocic2021kr.
However, are these transitions accounted totally by epigenetic
differences, or does there need to be a constant input, in terms social
interactions between ants, at an emergent scale on the colony level,
“checking every time” the status of the colony?

Furthermore, lets account for scaling metabolic rates with the general
tendency, with some exceptions, of larger organisms having a lower
mass-specific power outage than smaller organisms @west2002allometric
[@glazier2015body].

These are just two examples of problems that can’t be accounted with a
single scale consideration, as higher-scale constraints limit
development of lower-scale dynamics and vice-versa. Also, it starts to
seem tricky to identify what’s the evolutionary advantage behind some of
these mechanisms and tendencies, if we only consider a single scale at a
time, as with that type of approach we will see *natural selection*
going through low fitness points before converging to high fitness ones,
almost optimizing for “long-term consideration”.

The fundamental problem here at hand seems to be; how do smaller scale
components optimize for, and “find” a reliable path to an increase of
collective fitness, at a bigger scale? Afterall, we are made of
components (organs and communities of cells), and those components are
also made of components (cells), with those being made of further
smaller scale components (metabolic circuits, genetic circuits, etc).
And you can also take into account the bigger scale counterpart, and
view us as components of bigger networks. This is briefly illustrated in
Fig.\[Figure 3\].

\[scale=0.85,every node/.style=<span>minimum size=1cm</span>,on grid\]

\[ yshift=-240, every node/.append
style=<span>yslant=<span>0.5</span>,xslant=<span>-0.6</span></span>,
yslant=<span>0.5</span>,xslant=<span>-0.6</span>\] (0,0) rectangle
(7,7); (1) at (4,4);\] ; (2) at (2.2,1);\] ; (3) at (6,6.2);\] ; (4) at
(2,4.5);\] ; (5) at (1,3);\] ; (6) at (3.4,3.3);\] ; (more) at
(-0.2,-1);\] ;

\(1) to (2); (4) to (3); (5) to (6); (5) to (3); (1) to (5); (6) to (2);
(1) to (6); (3) to (2); (1) to (4); (4) to (6); (2) to (5); (3) to (1);
(4) to (5); (4) to (2); (uset\_1) at (1.7,0.5)<span>Network
$\eta + 1$</span>;

; (0.5,6.5) node\[right, scale=.7\] <span><span>Scale
$n + 1$</span></span>;

(-1,-6) to (-4,0.8); (-0.5,-5.8) to (5.8,0.8);

\[ yshift=-120, every node/.append
style=<span>yslant=<span>0.5</span>,xslant=<span>-0.6</span></span>,
yslant=<span>0.5</span>,xslant=<span>-0.6</span>\] (0,0) rectangle
(7,7); (0,0) rectangle (7,7);

\(1) at (3.7,3);\] ; (2) at (3.7,5);\] ; (3) at (6,2);\] ; (4) at
(1,5);\] ; (5) at (4.3,6);\] ; (6) at (2,3.3);\] ; (1) to (2); (4) to
(3); (5) to (6); (5) to (3); (1) to (5); (6) to (2); (1) to (6); (3) to
(2); (1) to (4); (4) to (6); (2) to (5); (3) to (1); (4) to (5); (4) to
(2); (0.5,6.5) node\[right, scale=.7\] <span><span>Scale
$n$</span></span>; (uset\_1) at (1.4,0.5)<span>Network $\eta$</span>;

(-3.45,4) to (-2.2,-0.32); (6.5,4) to (-1.8,-0.35);

\[ yshift=0, every node/.append
style=<span>yslant=<span>0.5</span>,xslant=<span>-0.6</span></span>,
yslant=<span>0.5</span>,xslant=<span>-0.6</span>\] (0,0) rectangle
(7,7); (0,0) rectangle (7,7); (1) at (4,5.6);\] ; (2) at (6,2);\] ; (3)
at (0.5,1);\] ; (4) at (4,3);\] ; (5) at (2.1,5);\] ; (6) at (3,3.3);\]
; (1) to (2); (4) to (3); (5) to (6); (5) to (3); (1) to (5); (6) to
(2); (1) to (6); (3) to (2); (1) to (4); (4) to (6); (2) to (5); (3) to
(1); (4) to (5); (4) to (2); (uset\_1) at (1.8,0.5)<span>Network
$\eta - 1$</span>; ; (more) at (4,8.2);\] ; (0.5,6.5) node\[right,
scale=.7\] <span><span>Scale $n - 1$</span></span>;

With this in mind, how do you a have a reliable transition from smaller
scale systems, optimizing for individual fitness, to larger scale ones,
optimizing for collective fitness?[^6]

On another note, while you have, for example, some general summaries of
what aging entails @lopez2013hallmarks [@gladyshev2016aging], I think we
can approach aging as the general breakdown of the interactions between
components with the respective repercussions between scales, and the
following reversal for the optimization of individual fitness.

Take into account the following figure from @lipsitz1992loss

![**Representation of heart rate (beats per minute).** Comparison
between a younger and an older subject. <span
data-label="Figure 4"></span>](Complexity_data_aging)

We notice that the average heart rate seems to be the same for both
cases. The maximum and minimum values of heart rate seem to also be the
same for both cases. However, you do notice a difference in the
frequency of oscillation around the average heart rate value. I would
presume this difference can be accounted by the competency of the
components forming the network, and therefore the capacity of the
components and the network to respond to inputs with reasonable
reliability and precision. We can perhaps correlate robustness, of a
given system, and its complexity, in this case regarding the heart rate
signal. Given that the younger system responds in a faster manner
relative to the older one. This type of response depends perhaps on the
type of input, for example, demand of cell communities in the body for
nutrients, oxygen, or other blood factors. Nonetheless, a faster
response, is for the major part better, making the given system more
robust to any input. As parts of this system become less reliable, by
accumulating errors genome wise, faulty cellular machinery or by
accumulation of interfering metabolites, that might translate to
cellular mechanisms inefficiency and a general loss of cellular
communication capabilities, any type of coordination mechanism gets less
effective. As in this case, a slower response seems to be apparent in
the latter case, as oscillations in heart rate are not as frequent. We
can see the heart rate measure as another coarse-grained metric, and if
we take the speculative step of presuming that $\Delta Q$ values would
follow the same tendency, we can see that
$\epsilon_{\textrm{old}} > \epsilon_{\textrm{young}}$, as by the
following definition of error-rate $$\label{Equation 10}
\epsilon = \frac{\lvert\Delta S(\pi_{\Delta \tau})\rvert + \Delta \pi_{\Delta \tau}}{\langle \Delta Q \rangle_{\Delta \tau}\times\frac{1}{T}}$$
where $\Delta \pi_{\Delta \tau}$ is given by
$$\Delta \pi_{\Delta \tau} = \frac{1}{T}\left\langle \sum_{k = 1}^{n} A_{k} \right\rangle$$
Given this example the difference in $\epsilon$ between both cases, can
be accounted solely by $\Delta \pi_{\Delta \tau}$.
Old($\Delta \pi_{\Delta \tau}$) $>$ Young($\Delta \pi_{\Delta \tau}$),
can probably be accounted either by a smaller amount of components
(cells) in the respective networks, or by a deficiency in accuracy and
longer response times to given inputs, in the older system. Or as it is
more likely, by a combination of both. Furthermore, it would be
inherently easier to allocate metabolic strain, and behind it
error-propagation, if you have a bigger amount of components in the
respective network. That presumably happens, in old age, where organ
failure starts to emerge, as cells are pushed to their upper metabolic
capacity, and can’t function reliably and precisely.

Coming back to scaling metabolic rates, if we take into account the
measure given in Eq.\[Equation 8\], and if we apply to the general
tendency, we would see $\Theta \rightarrow 1$ as we converge to larger
organisms. I would presume this is the case, as larger scale organisms,
would be constituted by more robust networks composed by a higher amount
of components, and so by the definition of error-rate given in
Eq.\[Equation 10\], are allowed bigger error-rates[^7] (given that
$\langle \Delta Q \rangle_{\Delta \tau}$ would be comparatively smaller,
accounting for mass-specificity, than the smaller organism counterpart),
considering their ability to better allocate error-propagation through
their bigger networks.

####  {#section .unnumbered}

Extension of incompleteness theorems by account of evolutionary constraints
===========================================================================

Understanding Nature is very much not a “spectator-like-sport”. In
accordance with Fig.\[Figure 5\], the perception that a given system $i$
can have of an universal set $\mathcal{S}$ representing reality, is
inherently limited by the types of constraints applied to it. Majority,
if not all, of our deductions about reality, are formulated in a logical
and axiomatic basis, and these formal systems and their foundations are
inherently restricted by the evolutionary adaptations such a system, the
one forming these axiomatic foundations, is subjected to. Such
evolutionary adaptations don’t necessarily optimize for *understanding
of Nature*, but for whatever characteristics that promote a reproductive
prime stage[^8], in general.

I would presume that some inconsistencies, and paradoxes[^9] emerge as a
result of there not being strong evolutionary pressures based on the
“opposition” between “two ways of thinking” when accounting to a
paradox, where the successful solving of this “opposition” (leading to a
survival of the individual in a precarious situation) would promote the
propagation of the respective molecular and cellular dynamics, for
example regarding the neural dynamics of the corresponding individual,
into the next generation. In essence, the paradox is solved and would no
longer be apparent to next generations.

And I don’t think I’m necessarily missing that the whole premise of
understanding reality (as in scientific endeavours), was and is based on
this notion; that we are not spectators. However, I would think that
this notion should be way more present in our minds when trying to
understand Nature. That we have evolutionary constraints, and limits
will emerge on our formal and deductive systems[^10]. On these limits,
“inconsistencies” will appear.[^11]

\[scale=1.1,every node/.style=<span>minimum size=1cm</span>,on grid\]

\[ yshift=-120, every node/.append
style=<span>yslant=<span>0.5</span>,xslant=<span>-0.6</span></span>,
yslant=<span>0.5</span>,xslant=<span>-0.6</span>\] (0,0) rectangle
(7,7);

(circle1) at (3.7,3)<span>Perception of the\
universal set $\mathcal{S}$\
by system $i$\
(Set $s_{i}$)</span>;\] (uset\_1) at (1.5,0.5)<span>Universal set
$\mathcal{S}$</span>; (0.5,6.5) node\[right, scale=.7\]
<span><span>Perception Level</span></span>;

(3.8,4) to (3.8,-0.32); (.8,2.4) to (.8,-1.8);

\[ yshift=0, every node/.append
style=<span>yslant=<span>0.5</span>,xslant=<span>-0.6</span></span>,
yslant=<span>0.5</span>,xslant=<span>-0.6</span>\] (0,0) rectangle
(7,7); (0,0) rectangle (7,7); (circle1) at (3.7,3)<span>Constraints of
the system $i$</span>;\] (uset\_1) at (1.5,0.5)<span>Universal set
$\mathcal{S}$</span>; (0.5,6.5) node\[right, scale=.7\]
<span><span>Constraint Level</span></span>;

####  {#section-1 .unnumbered}

About entropic measures $\Delta S(\pi_{ij})$, $\Delta \pi_{ij}$ and $\langle \Delta S \rangle_{\Delta \tau}$ {#App A}
============================================================================================================

Given a certain system with current state $i$, $\pi_{i}$ will represent
the probability vector with corresponding state transition probabilities
from state $i$ to every other state that is accessible to the system,
such that $0 < P(i \rightarrow n) \leqslant 1$. $\pi_{i}$ is represented
in the following form $$\pi_{i} = 
\begin{bmatrix}
    P_{i \rightarrow i}  \\
    P_{i \rightarrow 1} \\
    P_{i \rightarrow 2} \\
    \vdots \\
    P_{i \rightarrow n}  
\end{bmatrix}$$ where $P_{i \rightarrow i}$ represents the probability
of the system not changing state after iteration time $\Delta \tau$. And
$P_{i \rightarrow n}$ represents the probability of the system changing
from state $i$ to $n$ after iteration time $\Delta \tau$. Furthermore,
we have $$\sum_{k = i}^{n} P_{i \rightarrow k } = 1$$ Lets now talk a
bit about the entropic measures $\Delta S(\pi_{ij})$, $\Delta \pi_{ij}$
and $\langle \Delta S \rangle_{\Delta \tau}$, considering the state
transition $i \rightarrow j$ with iteration time $\Delta \tau$.
$$\Delta S(\pi_{ij}) = S(\pi_{j}) - S(\pi_{i})$$ where $S(\pi_{n})$ will
be given by
$$S(\pi_{n}) = -k_{B}\sum_{k = n}^{N} P_{n \rightarrow k } \ln(P_{n \rightarrow k })$$
Taking that into account, $\Delta S(\pi_{ij})$ will give the entropic
cost to change from $\pi_{i}$ to $\pi_{j}$.

Regarding $\Delta \pi_{ij}$, if we take into account the following
probability vectors $$\pi_{i} = 
\begin{bmatrix}
    P_{i \rightarrow i}  \\
    P_{i \rightarrow 1} \\
    P_{i \rightarrow 2} \\
    \vdots \\
    P_{i \rightarrow n}  
\end{bmatrix}
\quad \quad \quad
\pi_{j} = 
\begin{bmatrix}
    P_{j \rightarrow j}  \\
    P_{j \rightarrow 1} \\
    P_{j \rightarrow 2} \\
    \vdots \\
    P_{j \rightarrow n}  
\end{bmatrix}$$ $\Delta P_{i}$ will represent the difference between
state transition probabilities with ending state $i$ (Ex:
$\Delta P_{1} = P_{j \rightarrow 1} - P_{i \rightarrow 1}$). Such that
$\Delta \pi_{ij}$ will be given by
$$\Delta \pi_{ij} = - k_{B} \sum_{k = i}^{n}\lvert\Delta P_{k}\rvert\ln\left(\lvert\Delta P_{k}\rvert\right)$$
Although, given this definition of $\Delta \pi_{ij}$ and the one given
in Eq.\[Equation 4\], I’m not sure the following equality
$$\frac{1}{T}\bigintssss_{\tau_{i}}^{\tau_{j}}\lvert\Delta Q_{\tau} - \langle \Delta Q \rangle_{\Delta \tau}\rvert \, d\tau = - k_{B} \sum_{k = i}^{n}\lvert\Delta P_{k}\rvert\ln\left(\lvert\Delta P_{k}\rvert\right)$$
holds true. Either way, $\Delta \pi_{ij}$ will give an idea of how much
a system oscillates around the attractor point given a certain state
transition. Furthermore, and with the objective of having the following
$$0 ~\leq \epsilon \leq 1$$ maintaining the same definition of
error-rate, $\epsilon$, as
$$\epsilon = \frac{\lvert\Delta S(\pi_{\Delta \tau})\rvert + \Delta \pi_{\Delta \tau}}{\langle \Delta Q \rangle_{\Delta \tau}\times\frac{1}{T}}$$
although here, as an equality, $\epsilon$ becomes presumably normalized,
if
$$\Delta \pi_{ij} = \frac{1}{T}\left\langle \sum_{k = 1}^{n} A_{k} \right\rangle$$
where $\left\langle \sum_{k = 1}^{n} A_{k} \right\rangle$, in accordance
with the illustration given in Fig.\[Figure 1\], gives the energetic
cost underlying the average area. And so, $\Delta \pi_{ij}$ ends up
representing the average entropic cost of an oscillation around the
respective attractor point of said system.\
Lastly, $\langle \Delta S \rangle_{\Delta \tau}$ will give you the
average entropic cost[^12] of maintaining the attractor point of such
system over iteration time $\Delta \tau$.

####  {#section-2 .unnumbered}

Comment about current approaches in molecular medicine
======================================================

Why are we, for the major part, trying to program a script in Python by
moving individual electrons, when it comes to solving health issues over
an organismic scale. We are stuck in the same situation as engineers
were when dealing with computing systems in the early 50’s. Once you
have competent components, perhaps better apptly called hardware here
(as cells are), you need to develop higher-level approaches[^13]. And
you don’t even need to develop them, better yet you need to find them.
As cells and biological systems in general, have been dealing with these
optimization problems long enough, that they have inherent higher-level
approaches “developed”. These would be under the umbrella of
communication mechanisms between smaller parts, that drive the increase
of collective fitness. Look at the example of bioelectricity.

You start wondering how pulling a single lever, as in the case of what
happens in modern molecular medicine, where you tackle if at most a few
“circuits” doesn’t lead the whole “grid” to where you want it to go
(resulting in expected and unexpected side-effects). Just imagine how
fragile and low-fitness these biological systems would need to be, that
a single-input intervention at the “hardware-level” would lead to a
drastic change at the emergent level.

This is obviously a very strong caricature, and is not intended to give
the impression that there aren’t any problems to solve at the
“hardware-level”. However, the same effort if not more should be put at
working with these competent units, as in cells and communities of
cells, to solve what is essentially a collective intelligence problem.
As in, how does selection allow smaller components to find the path to
an increase of collective fitness?

####  {#section-3 .unnumbered}

You should have a bigger range of perspectives. Why look at an object
from the same façade everytime, and assume it gives you the whole
picture, without considering the other sides of the object. It’s not
like a single perspective will give you all the explanatory power to
describe reality, if such a limit is even approachable. However, with a
bigger set of tools, you surely will have an easier time solving
problems that appear in front of you. Let go of the reductionist
approach when not needed, and realize that what we are trying to
understand is Nature itself, and that the fields we create to better
perceive separate branches of knowledge, don’t actually exist, and
should be trespassed with vigour.

[^1]: Between orthogonal states.

[^2]: See discussion in Appendix \[App A\].

[^3]: Although, we should perhaps see this value as the maximum decrease
    of the amount of state transitions allowed per second, as we have in
    fact a system in state $j$ with less energy than in state $i$, given
    the transition $i \rightarrow j$ and the corresponding
    $\Delta Q_{\Delta \tau}$. Ignoring the respective energetic content
    of the input layer, we have
    $E_{j} = E_{i} - \Delta Q_{\Delta \tau}$.

[^4]: We might simply refer to information dynamics of a respective
    system, and account for bit erasure, as depending on the scale of
    the system, such a metric as heat release might not be easy to
    measure, and another coarse-grained metric might need to suffice.

[^5]: Also we can account for some differences in longevity between
    castes, as in the type of behaviour they take in the colony. For
    example, queens would inherently be more protected in the nest, than
    the worker counterpart, given that this can account for difference
    in longevity between these castes. And if this is an advantageous
    strategy, it will tend to get selected (Although, we can perhaps
    state there is some correlation between this behaviour and the type
    of epigenetic modulation taken).

[^6]: It almost seems to be a general trend of some of these smaller
    scale systems to converge to a point where they optimize for
    collective fitness. As an example, two metabolic networks (A and B)
    with a common metabolite. If a certain input is applied to network
    A, network B will have some of its conversion rates changed. Or
    another example, consider two cells (C and D) which have multiple
    gap-junctions between them. If a certain external input is applied
    so that, lets say cell C has a fundamental change in the
    concentration of its cellular machinery, resulting in a major ion
    flux through the gap-junctions connecting cells C and D, there will
    be an inherent response by cell D, and in this sense can cell D
    really “perceive” itself as anything but the collective of cell C
    and D, and vice-versa? Any type of input will have repercussions in
    the opposite’s environment. In evolutionary game theoretic terms,
    it’s as if there isn’t only *cooperate* or *compete*, but
    *cooperate*, *compete* or *fuse*. A great essay about this
    @levin2020cognition.

[^7]: Although, we can presumably state every biological system would be
    bounded by the limits $[\epsilon_{min}; \epsilon_{max}]$, with
    respect to their heat release dynamics.

[^8]: Maybe such a selection tendency doesn’t hold at civilization
    selection levels, as in such a level, the priority might be for the
    *understanding of Nature*.

[^9]: As an example, Zeno’s paradoxes. Given two inital approaches
    (relying in continuity and discreteness at the same time), and
    taking logical steps, you end up running into oppositions.

[^10]: We obviously take into account experiments, and whether a
    corresponding theory has experimental evidence backing it up.
    However, we also intuit about how things happen, based on our formal
    systems, and we are inherently more likely to dismiss something and
    not consider it, if it doesn’t make logical sense. That’s why this
    notion, I believe, should way more present in our minds. So that
    when considering the borders of our formal systems, we don’t dismiss
    something on the basis of not making sense.

[^11]: In essence, for our case, the types of ”logic programmes” allowed
    to ”run” on our brains, are inherently constrained by the types of
    molecular and cellular mechanisms that were and are being selected
    for.

[^12]: As referred before, such value does not need to be constant, and
    usually isn’t.

[^13]: That is not to say that you can’t optimize existent hardware,
    with, in this case, new metabolic pathways and genetic circuits.
