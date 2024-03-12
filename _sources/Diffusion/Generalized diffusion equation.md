## Brownian Motion as a Free Energy minimizing process



Consider a suspension of a large nr of ideal, non-interacting beads (friction coefficient $\xi=6 \pi \eta_{s}^{\sigma}$ ):

$c(x, t)=$ Particle density @ $\{x,t\}$.

Goal: Construct a phenomenological model for the dynamics $c(x, t)$ that generates the equilibrium distribution $ \longrightarrow C_{e q}(t) \sim e^{-\frac{U(x)}{v_{B} T}}$ long-term. ,

We will see: This Brownian Dynamics continuously

lowers the Free Energy.

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-03.jpg?height=340&width=1866&top_left_y=358&top_left_x=102)

The probability current $j(x, t)$ (=ur of particles passing through $x$ per uniting) results from

i) deterministic motion $\dot{f}_{\text {jet }}=c \cdot \bar{v}=-\frac{c}{\xi} \partial_{x} u$

ii) random motion $j_{\text {shah }}=-D \frac{\partial C}{\partial x} \quad$ Pick's law

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-03.jpg?height=482&width=1582&top_left_y=1503&top_left_x=472)

$$
\begin{aligned}
\text { i) }+ \text { ii }) \Rightarrow \quad j & =c \cdot V_{f l} \text { with } \\
V_{f l} & =-\xi^{-1} \partial_{x}(\underbrace{u+D \xi \ln (c)}_{=\mu(x)})=-\xi^{-1} 2 x \mu .
\end{aligned}
$$

local chemical potential of non-interacting particles.

$$
\begin{equation*}
\Rightarrow \quad \frac{\partial c}{\partial t}=\frac{\partial}{\partial x}\left(C \frac{\partial y}{\xi}\right)=\frac{\partial}{\partial x} \frac{1}{\xi}\left(D \xi \frac{\partial c}{\partial x}+C \frac{\partial u}{\partial x}\right) \tag{1}
\end{equation*}
$$

with $\mu(x)=k_{B} T \ln (c)+U$

Equilibrium $(t \rightarrow \infty)$ :
Sualuclacoski Equation (also called Fokker -Planck or Generalized Diffusion Eq.4)

$$
\begin{aligned}
& \frac{\partial c}{\partial t}=-\partial_{x j} \longrightarrow 0 \quad \text { fin } t \rightarrow \infty \\
\Rightarrow & j=\text { cons. } \stackrel{!}{=} 0 \quad(\text { refer } j(x \rightarrow \pm \infty)=0) \\
= & -\frac{c}{\xi} 2 x \mu \Rightarrow \mu=U+D \xi \log \left(c_{1}\right)=\text { canst. } \\
\Rightarrow & C_{\text {eq }} \propto \exp \left(-\frac{U(x)}{D \xi}\right) \stackrel{!}{\alpha} \exp \left(-\frac{U(x)}{k_{B} T}\right)
\end{aligned}
$$

(Since it has bo be the Bottemane distribution)

$$
=0 \sqrt{D=\frac{k_{i n} T}{\sum_{1}}}
$$

Stakes-

Einstein Relation

velocity

fluctuations dissipation

$$
\left\langle\Delta x^{2}(t)\right\rangle=2 D t
$$

(R) Friction coefficient of

Typical proteins have $R \approx 2$ nm

$$
\Rightarrow D_{\text {protein }} \approx 100 \frac{\mathrm{mm}^{2}}{\mathrm{~s}}
$$

a ball of radius $R: \xi=6 \pi \eta R$. Cf. bacteria, $D_{\text {bc }} \approx 0,5 \frac{\mathrm{m}^{2}}{\mathrm{~s}}$

Notes from (1):

$$
j \propto \frac{\partial \mu(x)}{\partial x},
$$

where $\mu(x) \equiv U(x)+k_{B} T \ln (c)$ is our good dd chemical potential!

Thus $j=0$ if $\mu=$ canst.

三 good ald condition for themody manic equilibrium.
This sugsests a generalization: Smoluchask:

$$
\begin{gathered}
\partial_{+} \psi\left(\left\{x_{i}\right\}_{i}\right)=-\partial_{i} j_{i} \\
j_{i}=-\psi \sum_{j} H_{i j} F_{j} F_{j}=-\partial_{j}\left(U+k_{\beta} T \ln (\psi)\right)
\end{gathered}
$$

$\Rightarrow$ Browiem mation of interacting degrees of freedou, e.y.

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-06.jpg?height=399&width=947&top_left_y=1256&top_left_x=712)

freely jointed chain = micdel of a plexible polquer.

Free Energy Minimization:

Proposition! The functional tigre-dep

$$
F[c]=\int d x c(x, t) \cdot \mu(x) \frac{1}{\Gamma}\langle u\rangle-T S ;
$$

is monotonously decreasing $\delta S=-h_{B}\langle\log c\rangle$;

$$
\frac{d F}{d t}=\int d x\left[\mu \frac{\partial c}{\partial t}+G \frac{\partial u}{\partial t}\right]
$$

(1) parielle int

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-07.jpg?height=470&width=1741&top_left_y=1137&top_left_x=334)

$\angle O$ culess $\mu=$ const $\Rightarrow \quad C=C_{\text {eq. }}$.

Nbles:

- Dynamice is time ineverible cames forn coase-srainis (sce next Tue)

Recap: Generalized diffusion eau (in ID)

$$
\partial_{+} c(x, t)=-\partial_{x j}
$$

current $f(x, t)=-\frac{G \cdot \partial_{x} \mu}{\xi}$

local chemical potential $\mu(x, t)=U(x, t)-\xi_{B} T \log (c)$

Flow is driven by gradients in chem. pot.

Einstein Relation: $D=\frac{k_{B} T}{\xi}$

Basic solution of the diffusion eau.

$$
\begin{equation*}
U=0 \Rightarrow \frac{\partial c(x, t)}{\partial t}=D \partial_{x}^{2} c\left(x_{t} t\right) \tag{1}
\end{equation*}
$$

Assume point-like initial conditions: $C(x, 0)=\delta(x)$ standard deviation. Fourier transform of eq.n (1):

$$
\begin{array}{r}
c(x, t)=\int_{-\infty}^{\infty} \frac{d q}{2 \pi} e^{-i q x} c(q, t) \\
\sim(1) \Rightarrow \frac{\partial c(q, t)}{\partial t}=-D q^{2} c(q, t) .
\end{array}
$$

Now, this is an ordinary differential eq (in contrast to the partial diff. eau. (1))

The solution is

$$
c(q, t)=C(q, 0) e^{-D_{q}^{2} t}
$$

$c(a, c)$ follows from Fearer transforming (2):

$$
\begin{aligned}
& c(q, 0)=\int_{-\infty}^{\infty} d x e^{i q x} c(x, t) \\
&=\int_{-\infty}^{\infty} d x e^{i q x} d(x)=1 \\
& \Rightarrow c(q, t)=e^{-D q^{2} t}
\end{aligned}
$$

Foamier back transform:

$$
\begin{aligned}
& c(x, t)=\int_{-\infty}^{\infty} \frac{d q}{2 \pi} c(q, f) e^{-i q x}= \\
& =\int_{-\infty}^{\infty} \frac{d q}{2 \pi} e^{-D_{q}^{2} t-i q x}
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-10.jpg?height=342&width=1153&top_left_y=2019&top_left_x=454)

$$
\begin{aligned}
& =e^{-\frac{x^{2}}{4 D t} \frac{1}{2 \pi \sqrt{D t}}} \underbrace{\int_{-\infty}^{\infty} d Q e^{-Q^{2}}}_{\sqrt{\pi}}
\end{aligned}
$$

$$
\Rightarrow \begin{aligned}
& c(x, t)=\frac{e^{-\frac{x^{2}}{4 D t}}}{\sqrt{4 \pi D t}}=\frac{e^{-\frac{x^{2}}{2 \sigma_{t}^{2}}}}{\sqrt{2 \pi \sigma_{t}^{2}}}(3) \\
& \text { with } \sigma_{t}^{2} \equiv\left\langle(x(t)-x(\theta))^{2}\right\rangle=2 D t
\end{aligned}
$$

N.B.: This is a Green's function solution,

The solution to any initial condition

can be found by convolution with (3).

N.B: In our examples (so far), all particles are mon-interacting.

$$
\Longrightarrow c(x, t)=N \cdot p(x, t)
$$

with $p(x, t)$ being the probability of a single particle to be at $x, t$.

Applications of the Diffusion equ

Recap:- D=coust II no external force.

Let's pat in numbers:

i) Nerve Cell

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-13.jpg?height=442&width=1282&top_left_y=678&top_left_x=410)

Is diffusion fast enough to transport vesicles?

$$
\begin{aligned}
& D=0,5 \mathrm{~m}^{2} / \mathrm{s}=\frac{k T}{6 \pi \eta R_{+}} ; \\
& \frac{\left\langle x^{2}\right\rangle}{2 D}=t=12 \text { days! }
\end{aligned}
$$

$\Rightarrow$ Nerve cells heed active Aranspat?

ii) E. coli:

$$
\text { RAP; } R=2,5 \mathrm{um}
$$

$$
D \approx 100 \text { prom } 2 / 5
$$

1 m

$$
t=\frac{R^{2}}{2 D} \approx 2 \mathrm{~ms}
$$

$\Rightarrow$ diffusion is fast enough!

Application: Diffusion sets fundamental limits to Rates of biological aud chemical reactions.

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-14.jpg?height=1044&width=1499&top_left_y=541&top_left_x=610)

How many ligands capthesed per sec?

Use diffusion eau. to model tree ligands:

ss. $0=\partial_{+} c \Rightarrow \quad \partial_{r} c_{s}=\frac{\text { cons. }}{r^{2}}$ for $r>R$

$$
c_{s}(r)=\frac{-A}{r}+B=-\frac{A}{r}+c_{\theta} \Rightarrow c_{\varsigma}(\infty)=\varepsilon
$$

i) Perfect absorber limit: $c_{s}(R)=0$.

$$
\Rightarrow c_{S}(r)=c_{0}\left(1-\frac{R}{r}\right) .
$$

particle current $j(R)=|\vec{j}(\vec{R})|=D \partial_{r} c(r, t)=\frac{D c}{R_{c} R}$

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-15.jpg?height=644&width=1874&top_left_y=709&top_left_x=235)

per area.

total flux of captured particles

$$
\phi=j(R) \cdot 4 \pi R^{2}=\frac{4 \pi D c_{0} R}{\left[\frac{L^{2}}{s} \cdot \frac{1}{L^{3}} \cdot L=\frac{1}{S}\right]}
$$

ii) Finite abruption rate: $\phi=4 \pi R^{2}(R) \stackrel{\#}{=} M k_{0} \cdot c(R)(2)$

$$
\begin{aligned}
& \text { (1): } j(R)=-D \partial_{r} C C_{n=R}=-\frac{A}{R^{2}} D \\
& \curvearrowright(2): 4 \pi A D=\mu k_{g u}\left(-\frac{A}{R}+C_{0}\right)
\end{aligned}
$$

$$
\begin{aligned}
A & =\frac{C_{0} M k_{\text {an }}}{4 \pi D+\frac{M k_{\text {an }}}{R}} \\
C(R) & =C_{0}\left[1-\frac{M k_{\text {on }}}{4 \pi D R+M k_{\text {on }}}\right] \\
& =\frac{C_{e}}{1+\frac{M k_{\text {an }}}{4 \pi D R}}=\left\{\begin{array}{l}
C_{0}, \frac{M \pi R}{4 \pi R} \\
0, \frac{M k_{\text {an }}}{4 \pi R} \longrightarrow \infty
\end{array}\right.
\end{aligned}
$$

How many receptors for haft max. rate?

$$
\begin{aligned}
& j(k)=\frac{D A}{R^{2}}=\frac{C_{0} 4 k_{\text {au }} D / R}{4 \pi D R+M h_{\text {an }}}=\text { half max ? } \\
& 4 \pi D R=M k \\
& M=\frac{4 \pi D R}{k_{\text {au }}} \\
& k=10 \mu \mathrm{m} \\
& D=100 \frac{\mu^{2}}{\mathrm{~s}} \\
& k_{a_{1}}=10 \frac{1}{\mu H \cdot S}
\end{aligned}
$$

$\Rightarrow M \approx 10^{5}$ receptor (egg. insulin

on cell membrane (receptors in fat cells)

Ara $\approx$ ko qum ${ }^{2}$

$$
\Rightarrow \text { mean spacing } \approx \sqrt{\frac{\text { area }}{M}}=\frac{1}{10} m_{m}={ }^{109 n m}
$$

Com pare w/ protein radius $\sim 5 \mathrm{um}$.

Universal bound on chemical reaction rates

Keg question 1

3 How fast is $A+B \xrightarrow{k} C$

If it is limited by $A-B$ collision rates?

ie. each A-B collision leads to one $G$.

$\Rightarrow k=c_{A}-k_{A \in B}$, where

where $\tilde{k}_{A+B}$ is the rate at which

a focal A particle is hit by $B$ particles.

![](https://cdn.mathpix.com/cropped/2024_03_11_f0ae63d09b92115db638g-17.jpg?height=889&width=2029&top_left_y=1894&top_left_x=81)

Since $x_{A}-x_{B}$ diffuses w/ trice the diffusion constant, we have

$$
\begin{align*}
& \text { \# collisions of } \\
& \frac{\text { on focal A }}{\operatorname{tim} e}=4 \pi(2 D)(2 R) C_{B}=\widetilde{k}_{A \in B} \\
& \Rightarrow \frac{\partial C_{C}}{\partial t}=k_{\text {diff }} C_{A} \cdot C_{B} \quad(1) \tag{1}
\end{align*}
$$

where $k_{\text {diff }}=16 \pi D R=16 \pi R \frac{k_{B} T}{60 \eta k}=\frac{8 k_{B} T}{3 \eta}$

$$
\approx 7 \cdot 109 \frac{1}{M \cdot s}
$$

Nates:

- Most enzymes are 100-1000 times slaver

$\Rightarrow$ the require more than I collisions to form a product.

-... could be modeled by assuming a finite absorption rate.

- Relation to Michaelis-Menten kinetics:

$\underset{\text { Rate of product }}{\text { formation }}=k_{\text {max }}[E] \frac{[S]}{K_{M}+[S]} \xrightarrow{\underbrace{}_{\text {enzyme }} \frac{[S] \rightarrow 0}{k_{\text {max }}}[E][S]}$

compare $w / e q$. (1) $\Rightarrow$

efficiency

The enzyme "ficirncy" is bounded by kdifg

$$
\left[\frac{k_{\max }}{k_{M}}\right]=\frac{1}{\text { Concentration } \cdot \text { time }}
$$

