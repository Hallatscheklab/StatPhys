## Variational treatment of a gas and the van der Waals equation of state

Our approximate treatment of a hard-sphere gas took only the "excluded volume" repulsion

$$
V^{N} \rightarrow(V-\Omega N / 2)^{N}
$$

But neutral molecules interact through an attractive $U(r) \approx-4 \epsilon\left(\frac{\sigma}{r}\right)^{6}$ as $r \rightarrow \infty$, with short-range repulsion. Why? The charged constituents of a molecule can polarize:

![](https://cdn.mathpix.com/cropped/2024_02_19_12ee2a2d42e4a6485d42g-02.jpg?height=299&width=709&top_left_y=1365&top_left_x=1208)

Since a dipole generates $\widetilde{E} \sim \frac{d}{r^{3}}$, and $H \ni-\vec{E} \cdot \vec{d}$,

$$
H \ni \frac{d_{1} d_{2}}{r^{3}}
$$

We can then treat this in quantum perturbation theory for a rotationally-symmetric molecule. In ground state, $\langle\vec{d}\rangle=0$ so to first order $\Delta E=0$. If $\Delta=E_{1}-E_{0}$ is gap, and second order perturbation theory gives

$$
\Delta E=-\frac{\mid\langle 1|\hat{v}| 0\rangle^{2}}{\Delta}
$$

Since $V \sim \frac{d_{1} d_{2}}{r^{3}}, \quad \Delta E \sim-\frac{1}{r^{6}}$

The completion between attraction, repulsion, and entropy leads to the presence of complex phase diagrams:

![](https://cdn.mathpix.com/cropped/2024_02_19_12ee2a2d42e4a6485d42g-03.jpg?height=750&width=1045&top_left_y=1435&top_left_x=615)

Mean-field treatment

$$
H=\sum_{i} \frac{\rho^{2}}{2 m}+\frac{1}{2} \sum_{i \neq j} v\left(r_{i}-r_{j}\right)
$$

$$
v(r)=\left\{\begin{array}{l}
\infty, \quad r<r_{0} \\
-u_{0}\left(\frac{r_{0}}{r}\right)^{6}, r>r_{0}
\end{array}\right.
$$

$$
\begin{aligned}
& Z(N, T, V)=\frac{1}{N !}\left(\frac{1}{\lambda_{T}}\right)^{N} \cdot \int_{V} d^{D} r_{i} e^{-\frac{\beta}{2} \sum V\left(r_{i}-r_{j}\right)} \\
& \Omega(\mu, T, V)=\operatorname{Tr}\left(e^{-\beta(H-\mu N)}\right)=\sum_{N} e^{\beta \mu N} Z(N, T, V)
\end{aligned}
$$

(explain why $\Omega$-ensemble convenient)

$N$ is like the "B" of Ising model, while $N$ jumps like m.

Variational ansate:

$$
\rho_{N} \alpha e^{-\beta \sum_{i=1}^{N} \frac{p^{2}}{2 m}}:\left|r_{i}-r_{j}\right| s r_{0}
$$

where $N$ is our variational parameter

If we treat $\left|r_{i}-r_{j}\right|>r_{0}$ constraint via lon-n excluded volume approximation,

$$
\begin{aligned}
Z(N, T, V) & =\frac{(V-N \Omega / 2)^{N}}{N ! \lambda_{T}^{3 N}} \\
\ln \frac{1}{N !} & =e^{N\left[\ln \left(\frac{1}{N}\right)+1\right] \quad(\text { stirling) }} \\
Z(N, T, V) & =e^{N\left[\ln \left(\frac{V / N-\Omega / 2}{\lambda^{3} T}\right)+1\right]} \\
Q(N, T, V) & =\sum_{N} Z\left(N^{\prime}, T, V\right) e^{\beta N^{\prime} N}
\end{aligned}
$$

But by our ansate, only $N^{\prime}=N$ contributes:

$$
Q_{N}(\mu, T, v)=e^{N\left[\ln \left(\frac{v / N-\Omega / 2}{\lambda^{3} T}\right)+\beta \mu+1\right] .}
$$

We can then apply Gibbs

$$
\ln Q \geq \ln (Q N)+\beta<H_{N}-\digamma_{\text {ansatr }}^{a c}
$$

$$
\begin{gathered}
\ln (Q) \geqslant \ln \left(Q_{N}\right)+\beta\left\langle H_{N}-H\right\rangle_{N} \\
H_{N}-H=-\frac{1}{2} \sum_{i \neq j}^{\text {ansate }} v\left(r_{i}-r_{j}\right) \quad\left(\left|r_{i}-r_{j}\right|>r_{0}\right)
\end{gathered}
$$

Fortunately, is is easy to compute $\left\langle v\left(r_{i}-r_{j}\right)\right)_{\bar{u}}$ because in $<7_{N}$ particles are uncorrelated outside $r_{0}$ :

$$
\begin{aligned}
\left\langle V\left(r_{i}-r_{j}\right)\right)_{N} & =\frac{\int_{r \rightarrow r_{0}} d r v(r)}{V} \equiv & -\frac{U}{V} \\
{[U] } & =J \cdot m^{D} \quad & \quad \sim<0
\end{aligned}
$$

For $V(r)=-v_{0}\left(\frac{r_{0}}{r}\right)^{\alpha}$ for example,

$$
S_{D} \int_{r_{0}}^{\infty} r^{D-1-\alpha} d r=\left.S_{D} \frac{r^{D-\alpha}}{D-\alpha}\right|_{r_{0}} ^{R}, \alpha>D
$$

$$
\begin{aligned}
U & =U_{0} r_{0}^{\alpha} S_{D}\left(\frac{0-r_{0}^{D-\alpha}}{D-\alpha}\right) \\
& =U_{0} \frac{S_{D}}{\alpha-D} r_{0}^{D}
\end{aligned}
$$

So

$$
\begin{aligned}
\left.<\frac{1}{2} \sum_{i \neq j} V\left(r_{i}-r_{j}\right)\right) & =-\frac{u}{V} \frac{N(N-1)}{2} \\
& =\frac{-U \cdot N^{2}}{V}=-U N \frac{n}{2} \quad(N \rightarrow \infty)
\end{aligned}
$$

Simple physical interpretation: each particle sees $-U \cdot n$ on average from other particles (mean-field)

$\left.\ln Q-\geq \ln (N)+\beta<H_{N}-H\right\rangle_{N}=$

$$
\begin{aligned}
& N\left[\ln \left(\frac{v / N-\Omega / 2}{\lambda^{3} T}\right)+\beta \mu+1\right]+\beta \cup \frac{N^{2}}{2 V} \\
& \frac{\ln Q}{V} \geq \underbrace{n\left[\ln \left(\frac{v / N-\Omega / 2}{\lambda^{3} T}\right)+\beta \mu+1\right]+\beta \cup \frac{n^{2}}{2}}_{\psi[n]}
\end{aligned}
$$

4

Now maximize 4 w.r. $n$ : depending on $\beta, N$, can be two minima (gas +liquid)

Note $-\frac{1}{\beta} \ln Q=\Omega=E-T S-\mu N$

$$
\begin{aligned}
& =(T S+\rho \omega-P V)-(T S+\rho N) \\
& =-P V
\end{aligned}
$$

So $\beta P \approx \max _{n} \psi[n]$

Origin of Vd:

$$
\begin{aligned}
& \psi[n]=n\left[\ln \left(\frac{n^{-1}-\Omega / 2}{\lambda^{3} T}\right) \cdot \beta \mu+1\right]+\beta \cup \frac{n^{2}}{2} \\
& \beta P=\max _{n} \psi[n]
\end{aligned}
$$

Maximize:

$$
\partial_{n} \psi=\ln \left(\frac{n^{-1}-\Omega / 2}{\lambda^{3}}\right)+\beta \mu+1+\beta u n-\frac{1}{1-n \Omega / 2}
$$

$$
\beta \mu=-1-\beta u n-\ln \left(\frac{n^{-1}-n / 2}{\lambda^{3}}\right)+\frac{1}{1-n \Omega / 2}
$$

This can admit multiple solutions

substituting back into $\psi[n]$,

$$
\begin{aligned}
p= & \beta^{-1} \psi[n]=K_{B} T n \frac{1}{1-n \Omega / 2}-u n^{2} / 2 \\
& \left(P+u n^{2} / 2\right)=K_{B} T \frac{N}{V-N \Omega / 2}
\end{aligned}
$$

$$
\begin{aligned}
& \left(P+u n^{2} / 2\right)(V-N \Omega / 2)=N K_{B} T \\
& \left(P+a n^{2}\right)(V-b N)=N K_{B} T \quad E_{q} .
\end{aligned}
$$

We see the two phenomenological coefficients $a$, b of Vd have their origin in M.F. treatment of long-range attraction (a) and short-distance repulsion (b).

$$
\begin{aligned}
\partial_{n} \psi & =0 \\
\beta(\mu+u n) & =\ln \left(\frac{n \lambda^{3}}{1-n \Omega / 2}\right)+\frac{n \Omega / 2}{1-n \Omega / 2}
\end{aligned}
$$

Interpretation: effect of long-range interaction is to shift $\mu \rightarrow \mu+$ un do to the average attraction un experienced by each particle (mean-field)

$$
\psi=n\left[\ln \left(\frac{n^{-1}-\Omega / 2}{\lambda^{3} T}\right)+\beta \mu+1\right]+\beta \cup \frac{n^{2}}{2}
$$

Choose units with $\beta=1, \Omega / 2=1$, and shift $\mu$ :

$$
4=n \ln \left(n^{-1}-1\right)+u \frac{n^{2}}{2}+\left(\bar{\mu}+\frac{3}{2}-\frac{u}{3}-\ln 2\right) n
$$

Clearly two maxima $\longrightarrow 1$ minima. So need region

$$
\partial_{n}^{2} \psi=u-\frac{1}{n(1-n)^{2}} \geq 0
$$

Best case: $n=\frac{1}{3} \Rightarrow U \leq \frac{27}{4} \equiv U_{c}$

For $U>U_{c}, \quad \psi$ develops two maxima

at $n_{g}<n_{l}$

Below $T_{c}$,

Maxwell Construction / Coexistence

If we work in contact with particle reservoir ( $\mu$-ensemble), then $n(\mu)$ jumps below $T_{c}: n_{n g} \mathfrak{f}^{n} \longrightarrow_{N}$.

But what if we put $n=\frac{N}{V}$ particks in a box for fixed $N$ with $n_{g}<n<h_{l}$ ? Intuitively, we know: it will phase separate:

![](https://cdn.mathpix.com/cropped/2024_02_19_12ee2a2d42e4a6485d42g-11.jpg?height=504&width=603&top_left_y=1118&top_left_x=522)

$$
\begin{aligned}
& V=V_{g}+V_{l} \\
& N=N_{g}+N_{l} \\
& N=n_{g} \cdot V_{g}+n_{l} V_{l} \\
& n=n_{g} \cdot \frac{V_{g}}{V}+n_{l} \frac{V_{l}}{V}
\end{aligned}
$$

