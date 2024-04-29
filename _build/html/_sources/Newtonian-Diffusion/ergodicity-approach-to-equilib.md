Lecture 3: Ergodicity and the approach to $E q$.

Copyright Michael zaletel 2021

- Liouville's theorem
- QM density matrices
- Master equations
- H- theorem

So far, we've discussed probability in distriguteral. In stat -mech the relevant physical system: over micro-states of

Microstates:

$\frac{\text { Classical Particles: }}{\text { (Phase Space) }}\left\{\vec{q}_{1}, \vec{q}_{2}, \cdots \vec{q}_{N}, \vec{p}_{1}, \vec{\rho}_{2} \cdots \vec{p}_{N}\right\}$

$$
\int P\left(\vec{q}_{i}, \vec{p}_{i}, t\right) \prod_{i} d^{3} q_{i} d^{3} p_{i}=1
$$

The target space need not, be $\mathbb{R}^{3 N}$

for example in a spin-system, $\vec{q} \sim \vec{s},|\vec{s}|^{\prime}=1$.

Averages of observables:

$$
\left\langle\vec{q}_{i}\right\rangle=\int P(\{q, p\}) \underset{N}{\vec{q}_{i}} d V
$$

Density: $<n(\vec{r}))=\int P(\{q, p\}) \underbrace{\sum_{i=1}^{N} \delta^{3}(\vec{r}-\vec{q} ;)}_{n(\vec{r})} d V$

Density-density correlation function

$$
\begin{gathered}
\left\langle n\left(\vec{r}_{1}\right) n\left(\vec{r}_{2}\right)\right)=\int p(\{q, p\}) \sum_{i, j} \delta^{(s)}\left(\vec{r}_{1}-\vec{q}_{i}\right) \delta\left(\vec{r}_{2}-\vec{q}_{j}\right) d V \\
E=\int P(\{q, p\}) H(\{q, p\}) d V
\end{gathered}
$$

$c+c$.

QM:

$$
|\psi\rangle=\sum_{i} c_{i}|i\rangle
$$

To describe a probability distribution
over $Q M$ states
$\left\{p_{\alpha},|\psi a\rangle\right\}$

$$
\begin{aligned}
\hat{\rho} & =\sum_{\alpha} p_{\alpha}\left|\psi_{\alpha}\right\rangle\left\langle\psi_{\alpha}\right|, \quad \sum p_{\alpha}=1=\operatorname{Tr}(\hat{\rho}) \\
\langle\hat{O}\rangle_{\hat{\rho}} & =\sum_{\alpha} p_{\alpha}\left\langle\psi_{\alpha}|\hat{\cup}| \psi_{\alpha}\right\rangle \\
& =\operatorname{Tr}(\hat{O} \hat{\rho})
\end{aligned}
$$

$\hat{\rho}_{\text {basis: }}$ ban be expanded in orthoganal

$$
\hat{\rho}=\sum_{i, j} \rho_{i, j}|i\rangle<j \mid
$$

Note that not all $\rho i, j$ are valid D.M.

(1) $\operatorname{Tr}(\hat{\rho})=1$

(2) $\left(\hat{\rho}^{+}\right)=\sum_{\alpha} \rho_{\alpha}^{*}\left(\left|\psi_{\alpha}\right\rangle\left\langle\psi_{\alpha}\right|\right)^{+}=\hat{\rho} \quad$ (Hermitian)

(3) For any $|v\rangle$,

$$
\begin{aligned}
\langle v|\tilde{\rho}| v\rangle & =\sum_{\alpha} p_{\alpha}\left\langle v\left(\psi_{\alpha}\right)\left\langle\psi_{\alpha} \mid v\right\rangle\right. \\
& =\sum_{\alpha} p_{\alpha}\left|\left\langle v \mid \psi_{\alpha}\right\rangle\right|^{2} \geq 0
\end{aligned}
$$

$\hat{\rho}$ is "positive semi-definite"

$$
\text { PS. } D \longleftrightarrow \operatorname{spec}(\hat{\rho}) \geq 0
$$

In general basis,

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-04.jpg?height=539&width=1426&top_left_y=292&top_left_x=295)

By P.S.D, $\quad 0 \leqslant p_{i, i} \leq 1, \quad \sum p_{i, i}=1$

So populations look like probabilities.

However, this is basis dependent!

$$
\frac{1}{2}\left[\begin{array}{cc}
|\uparrow\rangle & |\downarrow\rangle \\
\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2}
\end{array}\right] \longleftrightarrow\left[\begin{array}{ll}
|\rightarrow\rangle & \mid \longleftrightarrow \\
1 & 0 \\
0 & 0
\end{array}\right]
$$

There is always a special basis in which coherence $=0$, egg.

$$
\hat{\rho}=\operatorname{diag}\left(\rho_{i}\right)
$$

For the purpose of this week well assume this basis is time -independent, so we can heuristically just work with population $p_{i}$. of course full case is richer.

Conservation of probability and Liouville's Th.

In QM, $\quad \partial_{t}|\psi\rangle=-i \hat{H}|\psi\rangle$

$$
\left[\begin{array}{l}
\hat{\rho}=\sum p_{\alpha}\left|\psi_{\alpha}\right\rangle\left\langle\psi_{\alpha}\right| \\
\partial_{t} \hat{\rho}=-i[\hat{H}, \hat{\rho}]
\end{array}\right.
$$

So $\begin{aligned} \partial_{t} \sum_{i} p_{i, i}=\partial_{t}(\operatorname{Tr}(\hat{\rho})) & =-i \operatorname{Tr}([\hat{H}, \hat{\rho}]) \\ & =0\end{aligned}$

$$
(\operatorname{Tr}([A, B])=0
$$

$$
=0
$$

So $\operatorname{Tr}(\hat{\rho})=1$ is respected under time-evol.

How does this work in C.M.?

Liouville's Theorem

Classically,

$$
\begin{aligned}
& \partial_{t} q_{i}=\frac{\partial H}{\partial p_{i}} \quad \text { (Ham. Eq) } \\
& \partial_{t} p_{i}=-\frac{\partial H}{\partial q_{i}}
\end{aligned}
$$

What does this imply for $\partial_{t} P(\{q, p\}, t)$ ?

Consider the evolution of a small volume $\Delta V \longrightarrow \Delta V^{\prime}$

$$
(q, p) \longrightarrow\left(q^{\prime}, p^{\prime}\right)
$$

We know $P(q, p, t) \cdot \Delta V=P\left(q^{\prime}, p^{\prime}, t+d t\right) \cdot \Delta V^{\prime}$

We have $q^{\prime}=q+\dot{q} d t, \quad p^{\prime}=p+\dot{p} d t$

But what is $\Delta V^{\prime}$ ?

Claim: $\Delta V^{\prime}=\Delta V$

for Hamiltonian.

Like incompressible fluid!

$$
P(q, p, t)=P\left(q^{\prime}, p^{\prime}, t^{\prime}\right)
$$

Proof $\quad \Delta V=\Delta V^{\prime}$

Let's consider a general diff-eq.

$$
\begin{aligned}
& \partial_{t} x_{i}=\varphi_{i}(\vec{x}) \\
& \quad\left(\partial_{t} \vec{x}=\vec{\varphi}(\vec{x})\right)
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-07.jpg?height=350&width=1004&top_left_y=355&top_left_x=292)

$$
\begin{aligned}
& \vec{x} \longrightarrow \vec{x}+d_{t} \cdot \vec{\varphi}(x) \\
& \left.\vec{x}+\vec{\Delta}_{i} \rightarrow\left(\vec{x}+\vec{\Delta}_{i}\right)+d_{t} \quad \vec{\varphi}(\vec{x}+\vec{\Delta} ;)\right) \\
& \approx\left(\vec{x}+\vec{\Delta}_{i}\right)+d t\left(\vec{\varphi}(\vec{x})+\frac{\partial \vec{\varphi}^{\prime}}{\partial \vec{x}} \cdot \vec{\Delta}_{i}\right)
\end{aligned}
$$

So

$$
\begin{aligned}
& \vec{\Delta}_{i}^{\prime}=\vec{\Delta}_{i}+d_{t} \frac{\partial \vec{\varphi}}{\partial \vec{x}} \cdot \vec{\Delta}_{i} \\
& \Delta^{\prime}=\left(\mathbb{1}+d t \frac{\partial \varphi}{\partial x}\right) \cdot \stackrel{\rightharpoonup}{\Delta} \\
& \text { « Jacobian }
\end{aligned}
$$

Now $\Delta V=$ vol of parallel piped $(\{\vec{\Delta} ; \xi)$

$$
=\operatorname{Det}\left[\begin{array}{lll}
\vec{\Delta}_{1} & \vec{\Delta}_{2} & \cdots
\end{array}\right]
$$

How do we figure out $\Delta v^{\prime}=\left|\Delta^{\prime}\right|$ ? Useful
formula:

$$
\operatorname{Det}(M)=e^{\operatorname{Tr} \ln (M)}
$$

Proof: If $\operatorname{spec}(M)=m_{i}, \operatorname{Det}(M)=\prod_{i} m_{i}$

So

$$
\begin{aligned}
\ln (\operatorname{Det}(M)) & =\ln \left(\Pi m_{i}\right)=\sum_{i}^{1} \ln \left(m_{i}\right) \\
& =\operatorname{Tr}(\ln (M))
\end{aligned}
$$

Deft $M=e^{\operatorname{Tr}(\ln (M))}$

Now $\quad M=\vec{\Delta}_{i}=\left(\mathbb{I}+d t \frac{\partial \varphi}{\partial x}\right) \Delta$

$$
\begin{gathered}
\ln \left(\left(\mathbb{1}+d_{t} \frac{\partial \varphi}{\partial x}\right) \cdot \Delta\right)= \\
\ln \left(\left(\mathbb{1}+d_{t} \frac{\partial \varphi}{\partial x}\right)\right)+\ln (\Delta) \\
\Delta V^{\prime}=e^{\operatorname{Tr}\left(\ln \left(\mathbb{1}+d_{t} \frac{\partial \varphi}{\partial x}\right)\right)} \cdot \Delta V \\
\Delta V^{\prime}=e^{\ln \left(\operatorname{Tr} \frac{\partial \varphi}{\partial x}\right)} \Delta V
\end{gathered}
$$

Trace of Jacobian $\frac{\partial y}{\partial x}$ determines expansion factor.

Hamiltonian: $\quad \dot{q}_{i}=\overbrace{\frac{\partial H}{\partial \rho_{i}}}^{\varphi_{1, i}} \quad \dot{\rho}_{i}=\overbrace{-\frac{\partial H}{\partial q_{i}}}^{\varphi_{2, i}}$

$$
\operatorname{Tr}\left(\frac{\partial q}{\partial x}\right)=\sum_{i} \frac{\partial \dot{q}_{i}}{\partial q_{i}}+\frac{\partial \dot{p}_{i}}{\partial p_{i}}=\sum_{i} \frac{\partial^{2} H}{\partial q_{i} \partial p_{i}}-\frac{\partial^{2} H}{\partial p_{i} \partial q_{i}}=\gamma
$$

$$
\Delta V^{\prime}=\Delta V
$$

Since $\quad \Delta V^{\prime}=\Delta V^{\prime}$

$$
\begin{aligned}
P(q, p, t) & =P\left(q^{\prime}, p^{\prime}, t+d t\right) \\
& =P(q+d t \dot{q}, p+d t \dot{p}, t+d t \\
& =P(q, p, t)+\left(\frac{\partial P}{\partial q} \dot{q}+\frac{\partial P}{\partial p} \dot{p}+\frac{\partial P}{\partial t}\right) d t \\
\frac{\partial P}{\partial t} & =-\left(\frac{\partial P}{\partial q} \dot{q}+\frac{\partial P}{\partial p} \dot{p}\right] \\
& =\left[\frac{\partial P}{\partial p} \frac{\partial H}{\partial q}-\frac{\partial P}{\partial q} \frac{\partial H}{\partial p}\right\} \\
& =\{H, P\}
\end{aligned}
$$

"Poisson Bracket": For general $A(q, p)$,

$$
\{A, B\} \equiv \sum_{i} \frac{\partial A}{\partial q_{i}} \frac{\partial B}{\partial p_{i}}-\frac{\partial A}{\partial p_{i}} \frac{\partial B}{\partial q_{i}}
$$

QM $\longrightarrow$ Classical

$-i b[\hat{A}, \hat{B}] \longrightarrow\{A, B\}$

$$
\partial_{t} \hat{\rho}=-i \hbar[H, \hat{\rho}] \longrightarrow \partial_{t} P=\{H, P\}
$$

Suppose system starts somewhere in box $\Delta V$, with $P=\frac{1}{\Delta V}$

When dynamics are chaotic, $\Delta V$ evolves like droplet in an incompressible turbulent fluid, distorting into fine tendrils (subject to E-conservation)

In principle, $P(\{q, p\}, t)$ develops a very fine fractal structure with rapid variations between $0 / 1$. However, physically we are interested in observables like $\left\langle\vec{q}_{i}\right\rangle$ which vary smoothly with phase space, or we make measurements at slightly different times. This will effectively make $P(\{q, p\})$ indistinguishable from a "smeared out" (coarse-grained) version.

Arovas presents nice way of

Break up phase-space into cubes of volume $\quad \Delta V=(2 \pi k)^{N} \quad[\Delta q \cdot \Delta p]=J \cdot s=[h]$

We can then coarse grain

$$
P(\{q, p\}) \rightarrow P_{i}
$$

To obtain coarse-grained

$\partial_{t} P_{i}$, note that microscopic trajectories flow between cells. Let

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-11.jpg?height=336&width=558&top_left_y=1191&top_left_x=323)

$$
W_{j i}=\text { rate at }
$$

which points in $i$

$(w>0)$$\rightarrow j$

So $\partial_{t} P_{i}=\underbrace{\sum_{j \neq i} W_{i j} P_{j}}_{\text {in }}-\underbrace{\sum_{j \neq i} W_{j i} P_{i}}_{\text {out }}$

This is a "continuou s-time Markov process" (HW: discrete time)

$$
\partial_{t} \sum_{i} P_{i}=\sum_{i \neq j} W_{i j} P_{j}-\sum_{i \neq j} W_{j i} P_{i}=0
$$

We can rewrite $\partial_{\tau} P_{i}=-\Pi_{i j} P_{j}$

$$
P(t)=e^{-\Gamma t} P(0)
$$

$\operatorname{Prob-cons} \Rightarrow \sum_{i} \Gamma_{i j}=0$. This implies

I has an eigen value of $0,\left(\begin{array}{l}1 \\ 1 \\ i\end{array}\right)^{\top} I=0$

Thus there is right eigenvector,

$$
I \cdot p^{e q}=0 \Rightarrow e^{-t I} \cdot p^{e q}=p^{e q}
$$

This is a fixed point / "steady state" It is not neccesarily unique for example if Wij has disconnected cliques, each will have a per independently

$W_{i j}:$

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-12.jpg?height=333&width=776&top_left_y=1466&top_left_x=886)

But unique $p^{e q}$ is rather generic; for example always generic in finite state space.

If $p^{e q}$ is unique, we call the markov process "ergodic"

In $H W$, you prove $\operatorname{spec}(\Gamma)=\gamma_{i}$

satisfies $\operatorname{Re}\left(\gamma_{i}\right) \geqslant 0$ with $\gamma_{0}=0$

So at large times, $e^{-\Gamma t} \sim e^{-\gamma_{i} t} \Rightarrow$

$$
\lim _{t \rightarrow \infty} P(t)=\lim _{t \rightarrow \infty} e^{-\Gamma t} P(0)=P^{e q}+O\left(e^{-+\gamma_{1}}\right)
$$

System relaxes to equilibrium; rate
depends on spectrum $\gamma_{i}$.

Note partitioning into phase-space cubes is not the only type of coarse-graining possible. We can also coarse -grain from $N$-body $\Rightarrow 2$-bod,

$$
P\left(q_{1}, \cdots q_{N} ; p_{1}, \cdots p_{N}\right) \Rightarrow P_{1}(q, p)
$$

by integrating over all possible $N-1$
other particles, egg.

$$
P_{1}(q, p)=\frac{1}{N} \sum_{i} \int d V \delta\left(q_{i}-q\right) \delta\left(p_{i}-p\right) P(\{q, p\})
$$

This is the type of coarse-graining
relevant to BBGKY/ Bultmann Theorem of gasses, (Kadar che 3).

QM application: $\quad P_{i}=$ population of $\hat{\rho}$,

$$
W_{j \leftarrow i}=\frac{2 \pi}{A}|\langle i|\hat{v}| j\rangle|^{2} \rho_{\pi}\left(E_{j}\right)_{\text {DOS }}
$$

However, this is heuristic since it neglects coherence. Well do proper treatment later ("Lind bladian")
$\mathrm{H}$ - theorem

As $\quad P(t) \rightarrow p^{e q}(t)$, intuitively the system get's more "mixed up." Under certain assumptions, this approach can be proven monotonic. Our measure of mixing we call " $\mathcal{H}$ ".

$$
H=\sum P_{i} \ln \left(\frac{P_{i}}{P_{i}^{e q}}\right)=\sum P_{i} \ln \left(\frac{1}{P_{i}^{e q}}\right)-S^{\text {entropy }}[P]
$$

Incidentally this is called the "relative-entropy" or "Kullback-Leibler divergence" of $P$, Per,

$$
H=S_{k L}\left(P \| P^{e q}\right) \geq 0
$$

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-14.jpg?height=200&width=1694&top_left_y=1374&top_left_x=266)

Note if $p_{i}^{e q}=e^{-\beta E_{i}} / Z$

$$
\begin{aligned}
H & =\ln (Z)+\beta(\underbrace{\sum_{i} P_{i} E_{i}-\beta^{-1} S[P]}_{\langle E\rangle-T S=F[P]}) \\
& =\beta\left(F[P]-F\left[P^{e q}\right]\right) \geqslant 0
\end{aligned}
$$

The $\mathrm{H}$-theorem states that underacertain assumption, "detailed balance",

$$
\frac{\partial H}{\partial t} \leq 0
$$

Recall eq. condition $I \cdot p^{e q}=0$

$$
O=\sum_{j \neq i} W_{i j} P_{j}^{e q}-W_{j i} P_{i}^{e q} \quad \forall i
$$

Only need to be true after summing $j$.

"Detailed balance" is special property of $W_{i j}$ that it hold term-by-term:

$$
\begin{gathered}
W_{i j} p_{j}^{e q}-W_{j i} p_{i}^{e q}=0 \\
\qquad \frac{W_{i j}}{W_{j i}}=\frac{p_{i}^{e q}}{p_{j}^{e q}}
\end{gathered}
$$

It says that in eq, probability flows look like

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-15.jpg?height=403&width=750&top_left_y=1697&top_left_x=135)

rather than

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-15.jpg?height=436&width=536&top_left_y=1684&top_left_x=1505)

Satisfied, for example, by

$$
\begin{aligned}
& w_{i j}=\frac{2 \pi}{}|\langle i|v| j\rangle|^{2} \rho\left(E_{i}\right) \\
& \longrightarrow \frac{w_{i j}}{w_{j i}}=\frac{\rho\left(E_{i}\right)}{\rho\left(E_{j}\right)}
\end{aligned}
$$

$$
\begin{aligned}
\frac{d P}{d t}= & -\Gamma P \quad, \quad \Gamma_{i j}=0 \\
\frac{d H}{d t}= & \frac{d}{d t} \sum P_{i} \ln \left(\frac{P_{i}}{P_{i}^{e q}}\right)=-\sum_{i, j} \Gamma_{i j} P_{j} \ln \left(\frac{P_{i}}{P_{i}^{e q}}\right) \\
& +\sum_{i, j} P_{i} \frac{\Gamma_{i j} P_{j}}{P_{i}} \\
= & I_{0}\left(\sum_{i} \Gamma_{i j}=0\right) \\
= & -\sum_{i, j} \ln \left(\frac{P_{i}}{P_{i}^{e q}}\right) \Gamma_{i j} P_{j} \\
\frac{d H}{d t}= & -\sum_{i, j}\left(\Gamma_{i j} P_{j}^{e q}\right) \mu_{j}, \mu_{i}=\frac{P_{i}}{P_{i}^{e q}}
\end{aligned}
$$

Now note detailed balance implies

$$
\begin{aligned}
& W_{i j} p_{j}^{e q}=W_{j i} P_{i}^{e q} \\
& I_{i j} p_{j}^{e q}=\Gamma_{j i} p_{i}^{e q}
\end{aligned}
$$

This symmetrizes the expression under ir jj

$$
\frac{d H}{d t}=\frac{1}{2} \sum_{i, j}\left(\ln \left(\mu_{i}\right)-\ln \left(\mu_{j}\right)\right)\left(\Gamma_{i j} P_{j}^{e q}\right)\left(\mu_{i}-\mu_{j}\right)
$$

$i=j$ doesn't contribute, while for $i \neq j, \quad \Gamma_{i j} p_{j}^{e q} \leq 0$

![](https://cdn.mathpix.com/cropped/2024_03_07_d17e115a9bf9f64f18f8g-16.jpg?height=221&width=1788&top_left_y=2449&top_left_x=114)

$$
\begin{aligned}
& \text { So, term-by-term } \\
& \frac{d H}{d t} \leq 0
\end{aligned}
$$

$$
\text { Wi+h } \quad H=0 \quad \rightarrow \quad P_{i}=p_{i}^{\text {eq }}
$$

