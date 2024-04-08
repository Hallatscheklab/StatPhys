Brownian Motion as a Free Energy, minimizing process

non-interacting

Consider a suspension of a large nr of "ideal beads:

![](https://cdn.mathpix.com/cropped/2024_03_07_73f8625918f18547e48dg-01.jpg?height=929&width=1683&top_left_y=700&top_left_x=259)

(friction coefficient $\xi=6 \pi \eta_{s}{ }^{\sigma}$ )

$c(x, t)=$ Particle density @ $x_{1}+$.

Goal: Construct a phenomendegical model

for the dynamics $c(x, t) \longrightarrow C_{e q}(t) \sim e^{-\frac{u(x)}{v_{B} T}}$,

We will see: This Brownian Dynamics continuously

lower the Free Energy.

![](https://cdn.mathpix.com/cropped/2024_03_07_73f8625918f18547e48dg-02.jpg?height=340&width=1866&top_left_y=358&top_left_x=102)

The probability current $j(x, t)$ (=ur of particles passing through $x$ per uniting) results from

i) deterministic motion $\dot{j}_{\text {bet }}=c \cdot \bar{v}=-\frac{c}{\xi} \partial_{x} u$

ii) random motion $j_{\text {shah }}=-D \frac{\partial c}{\partial x} \quad$ Pick's law

![](https://cdn.mathpix.com/cropped/2024_03_07_73f8625918f18547e48dg-02.jpg?height=478&width=1569&top_left_y=1510&top_left_x=468)
i) $+i i)=0 \quad j=C \cdot V_{f l}$ with

$$
V_{f l}=-\xi^{-1} \partial_{\equiv}(\underbrace{u+D \xi \ln (c)}_{\equiv \mu(x)})=-\xi^{-1} \partial_{x} \mu .
$$

local chemical potential of non-interacting particles

$$
\begin{equation*}
\Rightarrow \frac{\partial c}{\partial t}=\frac{\partial}{\partial x}\left(C \frac{\partial \mu}{\xi}\right)=\frac{\partial}{\partial x} \frac{1}{\xi}\left(D \xi \frac{\partial c}{\partial x}+C \frac{\partial u}{\partial x}\right) \tag{1}
\end{equation*}
$$

with $\mu(x)=k_{B} T \ln (c)+U$

Equilibrium $(t \rightarrow \infty)$ :

Sualuclacoski Equation

(also called Fokker-Planck or Generalized Diffusion Eq. )

$$
\begin{aligned}
& \frac{\partial c}{\partial t}=-\partial x j \longrightarrow 0 \quad \text { fin } t \rightarrow \infty \\
= & j=\text { cons } \stackrel{!}{=} 0 \quad(\text { deepen } j(x \rightarrow \pm \infty)=0) \\
= & -\frac{c}{\xi} 2 x \mu=0 \mu=U+D \xi \log (G)=\text { canst. } \\
\Rightarrow & C_{\text {eq }} \propto \exp \left(-\frac{U(x)}{D \xi}\right) ! \stackrel{ }{\alpha} \exp \left(-\frac{U(x)}{t_{B}}\right)
\end{aligned}
$$

(Since it las bo be the Boltzmann distribution)

$=0 D=\frac{R_{i 0} T}{\sum_{D}} \quad$ Einstein Relation

velocity

fluctuations dissipation

$$
\left\langle\Delta x^{2}(t)\right\rangle=2 D t
$$

(R) Friction coefficient of Typical proteins have $R \approx 2$ um a ball of radius $R: \xi=6 \pi \eta R . \quad \begin{aligned} & \Rightarrow D_{\text {pate ic }} \approx 100 \frac{\mathrm{mm}^{2}}{\mathrm{~s}} \\ & \text { C.facterie, } D_{\text {be c }} \approx 0,5 \frac{\mathrm{m}^{2}}{\mathrm{~s}}\end{aligned}$

Notes from (1):

$$
j \propto \frac{\partial \mu(x)}{\partial x},
$$

where $\mu(x) \equiv U(x)+k_{B} T \ln (c)$ is our good dd chemical potential!

Thus $j=0$ if $\mu=$ canst.

$\equiv$ good old condition for themody nomic equilibrium.

Free Energy Minimization:

Proposition: The functional

$$
F[c]=\int d x c(x, f) \cdot \mu(x)=\langle u\rangle-T S
$$

is monotonously decreasing $\delta=-l_{B}\langle\log c\rangle$.
Europe.

$$
\frac{d F}{d t}=\int d x\left[\mu \frac{\partial c}{\partial t}+c \frac{\partial u}{\partial t}\right]
$$

(1), parielle bet

![](https://cdn.mathpix.com/cropped/2024_03_07_73f8625918f18547e48dg-05.jpg?height=470&width=1733&top_left_y=1137&top_left_x=338)

$\angle 0$ coles $\mu=$ cont $\Rightarrow \quad C=C_{\text {eq. }}$.

Noes:

$$
\begin{aligned}
& F[C]=\int d x c\left(x_{1}\right) \mu(x)=\left(\int d x c(x f) \cdot(d(x))+k_{B} T \cdot \int d x c(x, t) \log c\right. \\
& =\langle u\rangle-T S ; S=-\log \langle\log c\rangle \\
& \text { Entropy }
\end{aligned}
$$

Time-depundent Free Energy

Basic solution of the diflusion eq.u.:

$$
\begin{equation*}
U=0 \Rightarrow \quad \frac{\partial C(x, t)}{\partial t}=D \partial_{x}^{2} C(x, t) \tag{1}
\end{equation*}
$$

Assume peiat-like initial conditions

$$
\begin{equation*}
c(x, f)=\delta(x) \tag{2}
\end{equation*}
$$

Fomier trafa of $(1)$ :

$$
\begin{aligned}
& c\left(x_{1} t\right)=\int_{-\infty}^{\infty} \frac{d q}{2 \pi} e^{-i q x} c(q, t) \\
\Delta(1) \Rightarrow & \frac{\partial c(q, t)}{\partial t}=-D q^{2} c(q, t) .
\end{aligned}
$$

Nbw, this is an ordinary differential eq.n.

(in contrest to the partial diff.eq.u. (1))

The colution is

$$
C(q, t)=C(q, 0) e^{-D q^{2} t}
$$

$c(a, c)$ follows from Fearer transforming (2):

$$
\begin{aligned}
& c(q, 0)=\int_{-\infty}^{\infty} d x e^{i q x} c(x, t) \\
&=\int_{-\infty}^{\infty} d x e^{i q x} d(x)=1 \\
& \Rightarrow c(q, t)=e^{-D_{q}^{2} t}
\end{aligned}
$$

Fourier back trans form:

$$
\begin{aligned}
& c(x, t)=\int_{-\infty}^{\infty} \frac{d q}{2 \pi} c(q, t) e^{-i q x}= \\
& =\int_{-\infty}^{\infty} \frac{d q}{2 \pi} e^{-D_{q}^{2} t-i q x} \\
& =\int \frac{d q}{2 \pi} e^{-(\underbrace{}_{\equiv Q}(\underbrace{\sqrt{D T} q}-\frac{i x}{2 \sqrt{D t}})^{2}-\frac{x^{2}}{4 D t}}
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_03_07_73f8625918f18547e48dg-07.jpg?height=387&width=746&top_left_y=2121&top_left_x=571)

$$
\Rightarrow \begin{align*}
& c(x, t)=\frac{e^{-\frac{x^{2}}{4 D t}}}{\sqrt{4 \pi D t}}=\frac{e^{-\frac{x^{2}}{2 \sigma_{t}^{2}}}}{\sqrt{2 \pi \sigma_{t}^{2}}}  \tag{3}\\
& \text { with } \sigma_{t}^{2} \equiv\left\langle(x(t)-x(\theta))^{2}\right\rangle=2 D t
\end{align*}
$$

N. B.: This is a Green's function solution,

The solution to any initial condition can be found by convolution with .(3).

N.B: In our examples (sofar), all particles are man-interacting.

$$
\Longrightarrow c(x, t)=N \cdot p(x, t)
$$

with $p(x, t)$ being the probability of a simple particle to be at $x, t$.

Applications of the Diffusion eau

Recap: D=const II no external fore.

Let's pat in numbers:

i) Nerve Cell

![](https://cdn.mathpix.com/cropped/2024_03_07_73f8625918f18547e48dg-10.jpg?height=437&width=1282&top_left_y=676&top_left_x=410)

Is diffusion fast enough to transport vesicles?

$$
\begin{aligned}
& D=0,5 \mathrm{~m}^{2} / \mathrm{s}=\frac{k T}{6 \pi \eta R_{+}} ; \\
& \frac{\left\langle x^{2}\right\rangle}{2 D}=t=12 \text { days! }
\end{aligned}
$$

$\Rightarrow$ Nerve cells heed active Aranspat

ii) Ec ali

$$
\text { RAP; } R=2,5 \mathrm{um}
$$

$$
D \approx 100 \text { prom } 2 / 5
$$

lpn

$$
t=\frac{R^{2}}{2 D} \approx 2 \mathrm{~ms}
$$

$\Rightarrow$ diffusion is fast enough!

