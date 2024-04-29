Lecture 12

- Existence of phase transitions in $D \geq 2$
- Interacting gasses:
-Tanks
- Excluded Volume
- Viral Expansion

The Existence of phase transitions in 20

In ID, starting from g.s. $\uparrow \uparrow \uparrow \ldots$, the change in free-energy to add IDW is

$$
\begin{aligned}
\Delta F & =\Delta E-T \Delta S \\
= & (2 J)-k_{B} T \ln (L) \curvearrowleft \text { system size }
\end{aligned}
$$

So for $L>e^{2 J / K_{B} T}$, $\Delta F<0$, and hence D.W.s always destroy order beyond $\xi \sim e^{2 \pi / k_{B} T}$

What about 2D?

In 2D, D.W.S are ID objects:

![](https://cdn.mathpix.com/cropped/2024_02_16_622e679a6d467a0c4e40g-02.jpg?height=566&width=727&top_left_y=1678&top_left_x=641)

A domain wall of length $l$ costs

$$
\Delta E=2 \mathrm{Jl}
$$

In ID, any finite density $n_{D w}$ of domains walls destroys order at scale $\xi \sim 1 / n_{\text {ow }}$

But in 2D, a finite density on small D.W.S doesn't destroy order:

![](https://cdn.mathpix.com/cropped/2024_02_16_622e679a6d467a0c4e40g-03.jpg?height=498&width=610&top_left_y=642&top_left_x=528)

still majority IIII!

What matters is the size $l$ of the D.W.S

![](https://cdn.mathpix.com/cropped/2024_02_16_622e679a6d467a0c4e40g-03.jpg?height=557&width=639&top_left_y=1494&top_left_x=804)

$$
V=L \cdot L
$$

Order is destroyed if D.W.S of size $l \sim L$ become favorable.

So the question is how

$$
\Delta F(l)=2 J l-T S(l)
$$

behaves.

In $I D$ the only source of th $^{S}$ was
where ${ }^{\text {the }}$ is: $\ln (L)$.

But in 2D, there are many ways to make wall of length $l$ !

$$
l=12: \square,
$$

![](https://cdn.mathpix.com/cropped/2024_02_16_622e679a6d467a0c4e40g-04.jpg?height=247&width=895&top_left_y=525&top_left_x=889)

Counting $S(l)$ exactly is tricky combinatorial problem. But all we really need to know is that for $l \geqslant 1$, $s(l) \propto$ so .l (extensive)

To see why, let $\Omega\left(l, x_{0}, x_{1}\right)$ denote \# of way string of length $l$ connects $x_{0}, x_{i}$.

![](https://cdn.mathpix.com/cropped/2024_02_16_622e679a6d467a0c4e40g-04.jpg?height=233&width=513&top_left_y=1559&top_left_x=722)

Clearly

$$
\begin{aligned}
& \Omega\left(l_{A}+l_{B}, x_{0}, x_{2}\right) \geq \Omega\left(l_{A}, x_{0}, x_{1}\right) \Omega\left(l_{B}, x_{1}, x_{2}\right) \\
& S\left(l_{A}+l_{B}, x_{0}, x_{2}\right) \geqslant S\left(l_{A}, x_{0}, x_{1}\right)+S\left(l_{B}, x_{1}, x_{2}\right)
\end{aligned}
$$

If we fix $l=\alpha \cdot\left|x_{i}-x_{j}\right|$, this requires $s(l) \propto s_{0} \cdot l$

So

$$
\begin{aligned}
\Delta F & \approx 2 J l-T s_{0} l \\
& =l\left(2 J-T S_{0}\right)
\end{aligned}
$$

Key result: for $T<2 \mathrm{~J} /$ so, large- l Dow. forbidden! ordered

for $T>2 \mathrm{~J} / \mathrm{so}$,

larger D.W favored: disordered. Remarkably, the $2 D$ I sing model admits
exact solution (onstage nl and indeed finds $k_{B} T_{C}=\frac{2 J}{\sinh ^{-1}(1)} \approx J \cdot 2.26 \cdots$

Similar to our all-to-all problem, but locality gives nontrivial fractal structure at $T_{c}, w i+h$

$$
{ }_{m}^{+h} \propto\left|T-T_{c}\right|^{1 / 8}
$$

Te described by $2 D^{\prime \prime}$ conformal field theory" (Phys 212)

Interacting Gasses

Let's return to

$$
\begin{aligned}
& H=\sum_{i} \frac{p_{i}^{2}}{2 m i}+\frac{1}{2} \sum_{i \neq j} V\left(q_{i}-q_{j}\right) \\
& Z(J, N, V)=\frac{1}{N !} \overbrace{\left[\frac{d_{p}^{D}}{(2 \pi+)^{D}} e^{-\beta \frac{p^{2}}{2 m}}\right]^{N}}^{\lambda^{-D N}, \lambda=\sqrt{2 \pi h^{2} \beta / m}} \\
& \times \underbrace{\left(\prod_{i} \int_{V} d_{i} q_{i}\right) e^{-\frac{\beta}{2} \sum_{i<j} V\left(q_{i}-q_{j}\right)}}_{Q_{N}(T, V)} \\
& =\frac{1}{N !} \frac{1}{\lambda^{-D N}} Q_{N}
\end{aligned}
$$

For $\quad v=0, \quad Q_{N}=v^{N} \quad \ln (N !)$

$$
\begin{aligned}
& F=-K_{B} T \ln (Z)=-K_{B} T N\left(\ln \left(\frac{V}{\lambda^{D}}\right)-\ln \left(\frac{N}{e}\right)\right) \\
& P=-\left.\frac{\partial F}{\partial V}\right|_{N, T}=\frac{N K_{B} T}{V}, \quad P V=N K_{B} T
\end{aligned}
$$

But with interactions, $Q_{N} \neq V^{N}$. This "configuration integral" cant be exactly computed in general. Need:

$\checkmark$ - numeric (molecular dynamics/

(see text) - perturbation theory in $N / V$ (Mayer Cluster expansion)

$\checkmark$ - mean field theory

$\checkmark$ - variational approximations:
$F[P] \leqslant F\left[P_{\beta}\right]$

Before diving in, an exactly solvable warmup

ID Tank's Gas

![](https://cdn.mathpix.com/cropped/2024_02_16_622e679a6d467a0c4e40g-08.jpg?height=237&width=1305&top_left_y=103&top_left_x=234)

Gas of hard ID "spheres" of diameter a; $\quad V\left(q_{i}-q_{j}\right)= \begin{cases}0 & \text { if }\left|q_{i}-q_{j}\right|>a \\ \infty & \text { otherwise }\end{cases}$

$Q_{N}=$ non-overlapping configurations

W.L.O.G., restrict $q_{i} s q_{i+1}-a$, then $\times N$ ! for permutations

For $q_{1}: V_{1}\left(q_{2}\right) \equiv \int_{0}^{q_{2}-a} d q_{1}=q_{2}-a$

$$
\begin{aligned}
q_{1}+q_{2}: v_{2}\left(q_{3}\right) & \equiv \int_{a}^{q_{3}-a} d q_{2} \cdot v_{1}\left(q_{2}\right) \\
& =\frac{1}{2}\left(q_{3}-2 a\right)^{2} \\
\longrightarrow v_{n}\left(q_{n+1}\right) & =\frac{1}{n !}\left(q_{n+1}-n \cdot a\right)^{n}
\end{aligned}
$$

Finally, $\quad V_{N}=\int_{(N-1) a}^{L-a} d q_{N} V_{N-1}\left(q_{N}\right)$

$$
=\frac{1}{N !}(L-N a)^{N}
$$

So $Q_{N}=(L-N a)^{N}=L^{N}(1-n \cdot a)^{N}$

$$
\begin{aligned}
& F=F_{\text {free }}-K_{B} T \ln \left(\frac{Q_{N}}{L^{N}}\right) \\
& =F_{\text {free }}-K_{B} T N \ln \left(1-\frac{N}{V} \cdot a\right) \quad(V=L) \\
& P=-\frac{\partial F}{\partial V}=P_{\text {free }}+K_{B} T \frac{n^{2} \cdot a}{1-n \cdot a} \\
& =K_{B} T\left(n+\frac{n^{2} a}{1-n a}\right) \\
& =K_{B} T \frac{n}{1-n a} \\
& P \cdot(1-n a)=K_{B} T \cdot n \text { on } \\
& P(V-\underbrace{N a})=N K_{B} T \\
& \text { Ns/2 "excluded volume" }
\end{aligned}
$$

$$
P=\frac{N K_{B} T}{V-N_{a}}
$$

The "excluded volume" effect extends more generally, but in approximate sense. Consider for example hard spheres of volume $\Omega=\frac{4}{3} \pi r^{2}$

$$
Q_{N} \approx \frac{1}{N !} V \cdot(V-\Omega) \cdot(V-2 \Omega) \cdot(V-(N-1) \Omega)
$$

This is approximate because of jamming

....... The excluded volume for

(1) (2) 3 once 1,2 placed is not strictly additive if 1,2 are close. If $N \Omega \ll V$, this interaction is rare, so approximation ok in dilute limit.

$$
\text { Now } \begin{aligned}
& \prod_{n=1}^{N}(V-(N-n) \Omega)=e^{\sum \ln (V-(N-n) \Omega)} \\
& \approx e^{N \ln \left(V-\frac{N}{2} \Omega\right)}+V\left(\left(\frac{N \Omega}{V}\right)^{2}\right)
\end{aligned}
$$

So effectively $\quad V \longrightarrow V-\frac{N}{2} \Omega$

$$
\begin{array}{r}
P\left(V-\frac{N}{2} \Omega\right) \approx N K_{B} T \\
P=n K_{B} T \frac{1}{1-n \frac{\Omega}{2}}
\end{array}
$$

$$
\begin{aligned}
P & =n K_{B} T \frac{1}{1-n \frac{\Omega}{2}} \\
& =n K_{B}+\left(1+\frac{\Omega}{2} n+\left(\frac{\Omega}{2}\right)^{2} n^{2}+\cdots\right)
\end{aligned}
$$

This is an example of a "viral expansion"

$$
P=n K_{B} T\left(1+B_{2}(T) n+B_{3}(T) n^{2}+\cdots\right)
$$

As explained in the textbook, the $B_{n}(T)$ can be computed systematically via a diagrammatic perturbation theory. (Mayer Cluster Expansion)

I find the result rather technical, so next lecture we will instead consider variational approach ( MFT.

