Lecture 4) Ergodicity, ETH, and the micro-canonical ensemble.

Ergodic Theorem.

In discussion thus far, we took approach

Microscopic Eq. of. Mot: Deterministic reversible/ volume preserving

Coarse training

![](https://cdn.mathpix.com/cropped/2024_03_07_178f123016aebc3c0419g-02.jpg?height=210&width=203&top_left_y=641&top_left_x=1479)

Coarse grained Eq. of Motion: Stochastic/

$$
\begin{aligned}
& \partial_{t} P_{i}=-I_{i j} P_{j} \quad \text { non-reversible } \\
& P_{i}(t \rightarrow \infty)=P_{i}^{e q}
\end{aligned}
$$

Thus, at long-times, behaviour of coarse -grained olos'ervadle $\theta_{i}$ governed

$$
\langle\theta(t)\rangle \rightarrow \sum_{i} \theta_{i} p_{i}^{e q}=\langle\theta\rangle_{\text {eq }} .
$$

However, this discussion was heuristic, and necessarily approximate, as the master eq. $\partial_{t} P=-I P$ breaks the time-reversal symmetry of the underlying dynamics. A more mathematically sound approach is ergodic theory.

Let $X$ denote microscopic state space, and for $A C X, \mu(A)$ to "volume" (measure) of A. Eng., for phase space,

$$
N(A)=\int_{A} \underbrace{\prod_{i} d^{3} q_{i} \pi d^{3} q_{j}}_{d \mu}=\int_{A} d \mu
$$

A (reversible) time evolution is a map

$$
\begin{aligned}
T^{t}: X & \rightarrow X \\
T^{t_{1}} \cdot T^{t_{2}} & =T^{t_{1}+t_{2}}
\end{aligned}
$$

e.g. evolving for time "t" under $H$. $t \ni \mathbb{R}^{+}, \mathbb{Z}^{+}$for real/ discrete time.

Def: map is "measure preserving"

$$
\text { if } \quad \mu(A)=\mu\left(T^{t}(A)\right)
$$

for all $A, t$. By Liouville's theorem, $H$ is measure -preserving.

Def: Measure-preserving $(X, \mu, T)$ is "ergodic" if

$$
T^{t}(A)=A \Rightarrow A=\{0\} \text { or } X
$$

Example: suppose $\quad x=\{(p, q)\} \in[0,1]^{2}$

![](https://cdn.mathpix.com/cropped/2024_03_07_178f123016aebc3c0419g-04.jpg?height=428&width=443&top_left_y=192&top_left_x=528)

$\operatorname{Map}$ 1: $T^{\prime}: \left.(q, p) \rightarrow\left(q+\frac{1}{2}, p\right) \bmod \right\rvert\,$

Then for $A=\overrightarrow{0}, T^{\prime}(A)=A$

$\Rightarrow$ not ergodic

$\operatorname{Map}$ 2: $\quad T^{\prime}:(q, p) \rightarrow(q+\underbrace{\left.\frac{e}{3}, \beta\right) \bmod 1}_{\text {irrational }}$

Then for

$$
A=\square \begin{array}{ll} 
& T^{t}(A)=\Delta \\
\Rightarrow \text { not ergodic }
\end{array}
$$

$\operatorname{Map}$ 3: $\quad T^{\prime}(q, p) \rightarrow\left(q+\frac{e}{3}, p+\frac{\pi}{4}\right) \bmod$

Ergodic. You can try to construct invariant space

$$
A=\bigcup_{\tau=0}^{\infty} T^{n}\left(x_{0}\right)
$$

However, the irrationality of the shifts causes trajectories to "fill up" space, so $A=\lim _{N \rightarrow \infty} \bigcup_{t=0}^{N} T^{t}\left(x_{0}\right)=X$

Ergodic Theorem. For reasonable functions $f$ on $X$, ergodicity implies

$$
\lim _{N \rightarrow \infty} \frac{1}{N} \sum_{t=0}^{N} f\left(T^{n} \cdot x_{0}\right)=\frac{1}{N(x)} \int_{x} f d \mu
$$

(or $\left.\quad \frac{1}{N} \int_{t=0}^{N} f\left(T^{t} x_{0}\right) d t\right)$

for "almostall" $x_{0} \in X$. Lexceptions measure 01 .

$"$

Average over time $\longleftrightarrow$ average over microstates"

So if measurements coarse grain over $\frac{\text { time }}{P(x)}=\frac{1}{\mu(x)}$ we can use

$$
\overline{P^{e q}(x)}=\frac{1}{\mu(x)}
$$

It is interesting to note there are two distinct

(1) Averaged over time, $f \rightarrow \frac{1}{\mu(x)} \int f(x) d y$

(2) At fixed time $t \gg 0$, any initial distribution will spread out in $X$,

![](https://cdn.mathpix.com/cropped/2024_03_07_178f123016aebc3c0419g-06.jpg?height=395&width=2005&top_left_y=962&top_left_x=61)

so if $f(x)$ varies "smoothly" in $x$, $\lim _{t \rightarrow \infty} \int_{X} P(t, x) f(x) d \mu \rightarrow \int_{x} \frac{1}{\operatorname{vol}(x)} f(x) d \nu$

e.g. $\quad P(t \rightarrow \infty) \rightarrow \frac{1}{\operatorname{vol}(x)}$

Ergodicity $\Rightarrow 1$, but not 2 .

Indeed, $\quad T:(q, p) \longrightarrow\left(q+q_{0}, p+p_{0}\right)$ is ergodic for irrational shifts, but

![](https://cdn.mathpix.com/cropped/2024_03_07_178f123016aebc3c0419g-06.jpg?height=294&width=954&top_left_y=2368&top_left_x=583)

The mathematical property implying (2) is "mixing".

$$
\lim _{t \rightarrow \infty} N\left(T^{t}(A) \cup B\right)=\mu(A) \mu(B)
$$

Why? If $T^{t}(A)$ "spreads out" evenly in space,

![](https://cdn.mathpix.com/cropped/2024_03_07_178f123016aebc3c0419g-07.jpg?height=303&width=706&top_left_y=691&top_left_x=888)

then since $\mu\left(T^{+}(A)\right)=\mu(A)$, the volume of $T^{*}(A)$ which intersects $B$ should be proportional to $\mu(B)$ irrespective of where $B$ is.

Mixing is stronger than ergodicity; chaotic systems are mixing.

Application of Ergodic theory to C.M.: the microcanonical ensemble,

Are H's equations ergodic on phase space $\mathbb{R}^{6 N}$ ? No! Energy is conserved, so there are invariant subsets $\Sigma_{E} \in$ Phase-Space

$$
\text { sit. } T^{t}\left(\Sigma_{E}\right)=\Sigma_{E}
$$

However, if we restrict space to an energy shell $\sum E$, with measure

![](https://cdn.mathpix.com/cropped/2024_03_07_178f123016aebc3c0419g-08.jpg?height=307&width=600&top_left_y=1169&top_left_x=590)

$D(E) \cdot d \Sigma_{E} \equiv \begin{aligned} & \text { surface element } \\ & \end{aligned}(E-H(q, p)) d N$

where $D(E) \equiv \int \delta(E-H) d N$

so that $\int_{\Sigma_{E}} d \Sigma_{E}=1$,

the dynamics still preserve measured $\Sigma_{E}$

"Ergodic hypothesis": many- body systems are ergodic on $\sum_{E}$.

So, Knowing $E$, coarse-grained behaviour governed by

$$
\langle f\rangle_{E} \equiv \int_{\Sigma_{E}} f d \Sigma_{E}
$$

We can think of this as just a particularly simple $p^{e q}$,

$$
P_{E}(\xi q, p \xi) d V=\frac{1}{D(E)} \delta(E-H(q, p))
$$

equidisributed on energy shell. The "micro canonical ensemble".

There are fine-tuned counter examples: "integrable system".

Also not always true if tuned to a critical point (Istorder P.T.)

Quantum case: ETH.

For generic initial state

$$
\begin{gathered}
(\psi\rangle=\sum\left(C_{\alpha}\left|E_{\alpha}\right\rangle\right. \\
\left.\hat{\rho}(t)=\mid \psi(t))<\psi(t)\left|=\sum_{\alpha, \beta} c_{\alpha}^{*} c_{\beta} e^{-i\left(E_{\alpha}-E_{\beta}\right) t}\right| E_{\alpha}\right)\left\langle E_{\beta}\right|
\end{gathered}
$$

Since $\lim _{T \rightarrow \infty} \frac{1}{T} f e^{-i\left(E_{K}-E_{\beta}\right) t}=\delta \alpha \beta$

$$
\begin{gathered}
\left.\left.\frac{1}{T} \int \hat{\rho}(t) d t \rightarrow \sum_{\alpha}\left|C_{\alpha}\right|^{2} \right\rvert\, E_{\alpha}\right)\left\langle E_{\beta}\right| \\
\frac{1}{T} \int\langle\hat{A} \hat{\rho}(t)\rangle=\sum_{\alpha}\left|C_{\alpha}\right|^{2}\left\langle E_{\alpha}|\hat{A}| E_{\alpha}\right\rangle \\
\langle\hat{A}\rangle_{\{c\}} \equiv \sum_{\alpha}\left|C_{\alpha}\right|^{2} A_{\alpha \alpha}
\end{gathered}
$$

If $\quad\left|C_{x}\right| \neq 0$ only in infinitesimal window $E_{\alpha} \in[E, E+\Delta E]$, we

expect

$$
\langle\widehat{A}\rangle_{E}=\frac{\sum_{E_{\alpha} \sim E} A_{\alpha \alpha}}{\sum_{E_{2} \sim E} \cdot 1}
$$

If microcanonical expectation is correct irrespective of detailed local, this suggests
equality term-by-term:

$$
\begin{aligned}
& E T H: \\
& \left\langle E_{\alpha}|\hat{A}| E_{\alpha}\right\rangle=\underset{\substack{\left(E_{\alpha} \sim E\right)}}{ } A_{\alpha \alpha}=\langle\hat{A}\rangle_{E}=\frac{\sum_{E_{\alpha} \sim E} A_{\alpha \alpha}}{\sum_{E_{2} \sim E} \cdot 1}
\end{aligned}
$$

for local observables $\widehat{A}$.

obviously not true if we pick $\widehat{A}$ complicated, egg. $\hat{A}=\left|E_{\alpha}\right\rangle\left\langle E_{\alpha}\right|$ !

