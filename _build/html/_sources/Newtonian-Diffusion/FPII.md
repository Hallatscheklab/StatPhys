![](https://cdn.mathpix.com/cropped/2024_03_07_98bf12f770d7dd841a69g-1.jpg?height=155&width=945&top_left_y=223&top_left_x=525)

General properties of the FPE:

The FPE has the form of a continuity equation

$$
\begin{gathered}
\partial_{+} p(x, t)=-\partial_{x} j(x, t) \text { where } \\
j(x)=\alpha_{1}(x, t) p(x, t)-\frac{1}{2} q_{t}\left[\alpha_{2}(x) p(x, t)\right]
\end{gathered}
$$

is the probability current at $(x, y)$

Ie.: Probability is locally conserved

\$\$

\$\$

$\frac{\text { Boundary conditions: }}{\text { Suppose: } x \in[a, b]}$

- Reflectingber $f^{\prime}(a, t)=j(b, 1)=0 \Rightarrow \int_{a}^{b} d x p(x, t)=$ cons.
- Absorbing bc: $p(a, t)=p(b, t)=0=0 \int_{a}^{b} d x p(x, t)$ decays. 1 a particle may get trapped at the boundary

or if $x=$ papulationsize $=0 x=0$ is absorbing.

$\frac{\text { Infinite systems: }}{\text { (usually ) }} \lim _{x \rightarrow \pm \infty} p(x, t)=\lim _{x \rightarrow \pm \infty} a_{x} p(x, t)=0$

$\Rightarrow$ system is normalizable \& well-behaved.

I many other boundary conditions (mixed /reactive).

Station any processes: $\partial_{+} p=0 \Rightarrow j(x, t)=$ cont.

Reflective b. cs:

$$
0=j(x, t)=\alpha_{1}(x) p_{s t}(x)-\frac{1}{2} \partial_{x}\left[\alpha_{2}(x) p_{s t}(x)\right]
$$

... integrate (by separation of variables) to give

$$
p_{s t}(x) \propto \frac{1}{\alpha_{2}(x)} \exp \left[2 \int^{x} d x^{\prime} \frac{\alpha_{1}\left(x^{\prime}\right)}{\alpha_{2}\left(x^{\prime}\right)}\right]
$$

Example:

- Brownian particle in a potential $U(x)$. Homogeneous fluid: $\alpha_{2}(x)=$ cons $=2 D$

Force en particle $=-\partial_{x} U(x)$

$\Rightarrow$ overdaurped velocity $=-\frac{\partial_{x} u(x) !}{y}=\alpha_{1}(x)$

where $y=$ friction coefficient.

$=6 \pi \eta R$ for a sphere of radius $R$.

$\Rightarrow p_{\delta t}(x) \alpha \exp \left[-\frac{U(x)}{\mathcal{G} D}\right]$

$\triangle$ Bolt z mann distribution

only if

$D=\frac{k_{B} T}{f} \left\lvert\, \begin{aligned} & \text { EINSTEIN } \\ & \text { RELATION } \\ & \text { connects 2 macroscopic } \\ & \text { coefficients ( } D, y)\end{aligned}\right.$ to the molecular world" $\left(t_{B} T\right)$.

- Brownian particle in a harmonic potential, $U(x)=\frac{1}{2} k x^{2}=$

Oronstein - Uhlenbeck process.

$$
\partial_{p}(x, f)=\partial_{x}\left[\frac{k}{q} \times p\right]+D \partial_{x}^{2} p=(1)
$$

Expectation: $\langle x(t)\rangle=\int d x \cdot x p(x, t)$.

$$
\partial_{t}(x\rangle=\int d x \partial_{x}\left[\frac{k}{g} x p+D \partial_{x}\right]_{-\frac{k}{q} t} x
$$

$$
-\frac{k}{\xi} t
$$

In fact (1) can be solved exactly,

$$
P(x, t)=\frac{1}{\sqrt{2 \pi \sigma^{2}(t)}} e^{-\frac{[x-\bar{x}(f)]^{2}}{2 \sigma^{2}(t)}}
$$

with $\sigma^{2}=2 D+$, wa 2) Meteleol of cherackistics

Backward -FP equation.

The propagator $G(x,+\mid \xi, z)$ not all satisfies the FP eqn,

$$
\partial_{+} G=-\partial_{x}\left(\alpha_{1} G\right)+\frac{1}{2} \partial_{x}^{2}\left(\alpha_{2} G\right)
$$

but also an equivalentbackwardequ

$$
\partial_{\tau} G=+\alpha_{1}(\xi) \partial_{\xi} G+\frac{1}{2} \alpha_{2}(\xi) \partial_{\xi}^{2} G,
$$

where the derivatives act on the initial conditions.

BE offer easier to use with absorbing

Proof: boundary conditions

$$
G(x,+\mid \xi, \tau-\delta \tau)=\int d g G\left(x,+\mid \xi_{1} \tau\right) G\left(y_{\tau} \tau \mid \xi_{1} \tau-\delta \tau\right)
$$

$$
\begin{aligned}
& G\left(\xi_{1} \tau \mid \xi, \tau-\delta \tau\right) \stackrel{\text { Telor }}{=} G\left(y_{1} \tau-\delta \tau \mid \xi, \tau-\delta \tau\right) \\
& +\delta \tau\left[-\partial_{y}\left(\alpha_{1} G\right)+\partial_{y}^{2}\left(\alpha_{2} G\right)\right] \\
& +O\left(\delta \tau^{2}\right)
\end{aligned}
$$

$\mathcal{F}(*)$, using partial intepation

$$
\begin{aligned}
& \operatorname{and} G(y, \tau-\delta \tau \mid \xi, \tau-\delta \tau) \equiv \delta(y-\xi)
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_03_07_98bf12f770d7dd841a69g-6.jpg?height=279&width=1632&top_left_y=1575&top_left_x=254)

$$
\begin{aligned}
& +\frac{1}{2} \int d \varphi_{\alpha_{2}}(\xi) \partial_{y}^{2} G\left(x_{1}+1 y_{1}\right) \delta(\xi-\xi)
\end{aligned}
$$

