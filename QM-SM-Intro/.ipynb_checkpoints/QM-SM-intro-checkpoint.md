## When does quantum mechanics make a difference?

Following Kardar, we'll motivate quantum statistical mechanics with some cases where classical mechanics gives incorrect answers or even diverges, before developing the general formalism.

#### Fluctuations of a Hydrogen atom

Consider the classical Hamiltonian of a hydrogen atom,

$$
H=\frac{p_{1}^{2}}{2 m_{e}}+\frac{p_{2}^{2}}{2 m_{p}}+V\left(r_{1}-r_{2}\right)
$$

What is $Z(T), F(T), E(T)$ etc?

We first transform to relative & center of mass coordinates, $\left(\vec{r}=\vec{r}_{1}-\vec{r}_{2}, \vec{p}\right)$ and $(\vec{R}\left.=\frac{1}{M}\left(m_{e} \vec{r}_{1}+m_{p} \vec{r}_{2}\right), \vec{P}\right)$, such that 

$$
H=\frac{P^{2}}{2 M}+\frac{p^{2}}{2 \mu}+V(\vec{r})\;,
$$

where $M=m_e+m_p$ and $\mu=m_e m_p/(m_e+m_p)$.

CM and relative motions decouple: $Z=Z_{\mathrm{cm}} \cdot Z_{r}$, where 

$$
\begin{aligned}
Z_{r} & =\int \frac{d^{3} p d^{3} r}{h^{3}} e^{-\beta\left(\frac{p^{2}}{2 \mu}+V(r)\right)} \\
& =\frac{1}{\lambda_mu^{3}} 4 \pi \int_{0}^{\infty} d r \cdot r^{2} e^{+\beta \frac{e^{2}}{4 \pi \epsilon_{0} r}}
\end{aligned}
$$


$$
\left(\lambda_\mu\equiv\sqrt{\frac{h^2\beta}{2\pi \mu }}\right)
$$

But, at short wave length, we get into trouble: $e^{r_{0} / r} \rightarrow \infty$ as $r \rightarrow 0$. 


Quantum mechanics offers a resolution through Heisenberg's uncertainty relationship,

$$
\Delta p \Delta r \geq h
$$

This leads to a discrete spectrum of energy levels:

$$
\hat{H}\left|E_{\alpha}\right\rangle=E_{\alpha}\left|E_{\alpha}^{\prime}\right\rangle
$$

So if we replace the classical expression 

$$
Z=\int \frac{d q d p}{h} e^{-\beta H(q, p)} 
$$

by


$$
\boxed{ Z=\sum_{\alpha} e^{-\beta E_{\alpha}}}
$$ (qm-partition-function)

we obtain a well-defined quantum mechanical partition function. The following examples serve to show that this approach recovers classical results in the $T \rightarrow \infty$ limit.

We will later (~2 lectures from now) see how {eq}`qm-partition-function` arises from a more formal approach to quantum statistical mechanics.

Note that, in {eq}`qm-partition-function`, we sum over all measurable quantum states $\alpha$, which become the equivalent of micro states in classical stat mech.


#### Dilute Polyatomic Gasses

Consider a gas of tightly bound molecules. The Hamiltonian within each molecule is 

$$
H=\sum_{i=1}^{n} \frac{p_{i}^{2}}{2 m}+V\left(q_{1}, \cdots, q_{n}\right)
$$

where $n$ is the number of atoms in the molecule.

We have taken $m_{i}=m$ after scaling $q_{i}$ by $\sqrt{m_i/m}$ and $p_{i}$ by $\sqrt{m/m_i}$ (preserving phase space measure $dq*dp$). If $Z_1$ is the partition function for one molecule, a gas of $\mathrm{N}$-molecules gives $Z(N)=\frac{Z_1^{N}}{N !}$, ignoring inter-molecule interactions. For $Z_1$, we get

$$
Z_1=\int \prod_{i=1}^n\frac{d^{3} q_{i} d^{3} \rho_{i}}{h^{3 }} e^{-\beta\left(H_{kin}+V( \vec q )\right)}
$$

(Note no $\frac{1}{n !}$ if the molecule is composed of different types of atoms.)

The scale of the interaction potential $V$ is the Rydberg:

$$
R_{y} \sim 13.6 \mathrm{eV}
$$

Since $\frac{e V}{k B} \approx 1160 \mathrm{~K}$, for $T<1000 \mathrm{~K}$, the molecule is rigidly bound. This means that if $q_{i}^{*}$ is the lowest energy config of $V\left(q_{i}\right)$, then $u_{i} \equiv q_{i}-q_{i}^{*}$ will be "small". We can thus expand to second order:

$$
V\left(\left\{q_{i}\right\}\right)=V^*+\frac{1}{2} \sum_{i, j} \frac{\partial^{2} V}{\partial q_{i} \partial q_{j}} u_{i} \cdot u_{j}
$$

where $V^*=V\left(\left\{q_{i}^{*}\right\}\right)$ and $\left.\frac{\partial V}{\partial q}\right|_{q_{x}}=0$ at the ground state. Moreover, the stability of the ground state demands the matrix $\frac{\partial^{2} V}{\partial q_{i} \partial q_{j}}$ to be positive definite. It's also symmetric, so it can be diagonalized by a orthogonal matrix $O$:

$$
\frac{\partial^{2} V}{\partial q \partial q}=O^{\top} K O, \quad K=\operatorname{diag}\left(K_{s}\right)
$$

If we define

$$
\tilde u= O u \\
\tilde p= O p
$$

we get for the partition function

$$
\begin{aligned}
Z & =\int \prod_{i=1}^n\frac{d^{3} q_{i} d^{3} \rho_{i}}{h^{3 }} e^{-\beta\left(\frac{1}{2 m} p^\top \cdot p+V(\{ q_i \})\right.} \\
& \approx \int\prod_{i=1}^n \frac{d^{3} \tilde{u}_i d^{3} \tilde{p}_i}{h^{3 }} e^{-\beta\left(\frac{1}{2 m} \tilde{\rho}^\top \cdot \tilde{p}+V^{*}+\frac{1}{2} \tilde{u}^\top K \tilde{u}\right)}
\end{aligned}
$$

Note $d q d p=d \tilde{v} d \tilde{\rho}$ because $\mathcal{O}^{\top}O=1$. We integrate over $\tilde{\varphi}$ to get $\lambda^{-3 n}$, so
(if $K_s \neq 0$ )

$$
\begin{aligned}
Z & =\frac{1}{\lambda^{3 n}} \prod_{s} \int d \tilde{u}_{s} e^{-\beta \frac{K_{s}}{2} \tilde{u}_{s}^{2}}, \lambda=\sqrt{h^{2} \beta / (2\pi m)} \\
& =\frac{1}{\lambda^{3 n}} \prod_{s=1}^{3 n} \sqrt{2 \pi / \beta K_{s}}=\prod_{s=1}^{3 n} \sqrt{\frac{m}{K_{s} h^{2} \beta^{2}}} \\
E & =-\partial_{\beta} \ln (z)=-\partial_{\beta}\left(\sum_{s=1}^{3 n} \ln \left(\beta^{-1}\right)\right)=3 n k_{B} T
\end{aligned}
$$

We thus obtain the classical equipartion theorem: $E=\frac{1}{2} K_{B} T$ per quadratic d.o.f.

However, this was if $K_{s} \neq 0$. For $K_{s}=0$, $
\int d \tilde{u} e^{-\beta \cdot 0}=V: \text { no } \beta \text { - dependence. }\longrightarrow \text { no contribution to } E.$

So if there are $m$ modes with $K_{s}>0$,

$$
E=\frac{3 n+m}{2} k_{B} T
$$

The $r=3n-m$ zero modes come from symmetries: translations and rotations that leave the potential energy $V$ invariant. Center of mass translation contributes $3$ zero modes and rotation of the reference frame contributes $0$, $2$ or $3$ for a monoatomic, diatomic and a generic polymatic gas, respectively.



The heat capacity of the gas is thus

$$
C_{v}=\left.\frac{d E}{d T}\right|_{v}=\left(3 n-\frac{r}{2}\right) K_{B} / \text { molecule. }
$$

Key prediction: $C_{V}$ is T-independent

This is not what's seen in experiment:

![](https://cdn.mathpix.com/cropped/2024_03_19_23a706af92a350552302g-08.jpg?height=709&width=1045&top_left_y=207&top_left_x=578)

For $H_{2}$, for example, we have $n=2$ (diatomic molecule) and $r=3+2$ due to cm translation and 2 rotations. 

Prediction: $\quad C_V=6-\frac{5}{2}=\frac{7}{2}=\frac{\text{3 translations+2 rotations + 1 vibration}}{2}$

Instead, as 

$$
\begin{aligned}
& T \rightarrow 0, C_V\sim \frac{3}{2} k_B \quad \text{c.m. translation} \\
& T \rightarrow 500 \mathrm{k}, C_V \sim \frac{5}{2} \mathrm{k_B} \quad \text {c.m. translation, rotation } \\
& T \gg 1000 \mathrm{k}, C_V \sim \frac{7}{2} \mathrm{k_B} \quad \mathrm{CM}, \text { c.m. translation, rotation, vibration}
\end{aligned}
$$

Classical results are recovered only at $K_{B} T > e V$, degrees of freedom are "frozen out" at intermediate T. This effect comes from energy quantization.

#### Vibrational Modes

A diatomic molecule only has  $3 \cdot 2-5=1$ modes with $K_{s}>0$, corresponding to the vibration of the bond connecting the two atoms.

Let $q=x-x_{0}$ be the bond length extension ($x_0$ is the ground state length), 

$$
H_{\text {vib }}=\frac{p^{2}}{2 m}+\frac{K_s q^{2}}{2}=\frac{p^{2}}{2 m}+\frac{m \omega^{2}}{2} q^{2}
$$
where $\omega=\sqrt{K_s/m}$ is the classical vibration frequency.

Classically, we found

$$
\begin{aligned}
& Z=\frac{1}{\lambda} \sqrt{2 \pi / \beta K_s}=\sqrt{\frac{m}{K_s \hbar^{2} \beta^{2}}}=\frac{K_{B} T}{\hbar \omega}=\frac{1}{\beta \hbar \omega} \\
& E=\langle H\rangle=-\partial_\beta\ln(Z)=k_{B} T
\end{aligned}
$$

corresponding to two d.o.f.s.

In quantum mechanics, we have the energy eigenstates,

$$
\hat{H}|n\rangle=h \omega\left(n+\frac{1}{2}\right)|n\rangle, n=0,1,2, \cdots
$$

If we take

$$
\begin{aligned}
Z & =\sum_{n=0}^{\infty} e^{-\beta E_{n}}=e^{-\beta \hbar \omega / 2} \sum_{n=0}^{\infty}\left(e^{-\beta \hbar \omega}\right)^{n} \\
& =\frac{e^{-\beta \hbar \omega / 2}}{1-e^{-\beta \hbar \omega}}=\frac{1}{2 \sinh (\beta \hbar \omega / 2)}
\end{aligned}
$$

$$
Z=\frac{e^{-\beta \hbar \omega / 2}}{1-e^{-\beta \hbar \omega}}=\frac{1}{2 \sinh (\beta \hbar \omega / 2)}
$$

As $\quad T \rightarrow \infty$, $\beta \rightarrow 0$, we get the classical result, 

$$
\lim _{T \rightarrow \infty} Z=\frac{1}{\beta\hbar\omega}=Z_{\text {classical }}
$$

Note this required the $\int \frac{d q d p}{h}$ we've conventionally put in the classical phase-space integral. While it doesn't affect observables, it arises from the semiclassical principle!

```{note} One quantum state per $2 \pi$-t phase space volume

This can be seen from the Bohr-Sommerfeld condition 

$$
S=\int_{\partial S} p(q) \cdot d q=n \cdot k
$$

Note $\quad \int_{\partial } p d q=\int_{S} d p \wedge d q=$ Phase-volume

(Weyl-formula / Gutzwiller-Trace formula)
```


Since $\ln (Z)=\ln (2)-\ln (\sinh (\beta+\omega / 2))$, we get

$$
E=-\partial_\beta \ln Z=\frac{\hbar \omega}{2} \frac{\cosh (\beta+\omega / 2)}{\sinh (\beta+\omega / 2)}
$$

![](https://cdn.mathpix.com/cropped/2024_03_19_23a706af92a350552302g-11.jpg?height=783&width=1809&top_left_y=436&top_left_x=137)

$$
C_V=\partial_T E=k_{B}\left(\frac{k \omega}{k_{B} T}\right)^{2} \frac{e^{-\beta \hbar \omega}}{\left(1-e^{-\beta A \omega}\right)^{2}}
$$

```{note}
Note $\frac{C_V}{K_{B}} \sim\left(\frac{\hbar w}{K_{B} T}\right)^{2} e^{-\hbar \omega / K_{B} T}$ is exponentially small as $T \rightarrow 0$. This is a general feature of any model with a gap $\Delta E=\hbar \omega $ above ground state.
``` 

#### Rotations

![](https://cdn.mathpix.com/cropped/2024_03_19_23a706af92a350552302g-12.jpg?height=384&width=218&top_left_y=820&top_left_x=194)

The orientation of a diatomic molecule can be specified by $\theta, \varphi \quad\left(S_{2}\right)$

$$
\begin{aligned}
& L=\frac{I}{2}\left(\dot{\theta}^{2}+\sin ^{2} \theta \dot{\phi}^{2}\right) \\
& p_{\theta}=\frac{\delta L}{\delta \dot{\theta}}=I \dot{\theta} \quad \rho_{\phi}=\frac{\delta L}{\delta \dot{\phi}}=I \sin ^{2} \theta \dot{\phi} \\
& H=p \dot{q}-L=\frac{1}{2 I}\left(\rho_{\theta}^{2}+\frac{\rho_{\phi}^{2}}{\sin ^{2} \theta}\right)=\frac{\vec{L}^{2}}{2 I}
\end{aligned}
$$

(Same as particle on sphere)

Classically, we have

$$
\begin{aligned}
Z & =\frac{1}{h^{2}} \int_{0}^{\pi} \int_{0}^{2 \pi} d \theta d \phi \quad \iint d \rho_{\theta} d \rho_{\phi} e^{-\frac{\beta}{2 I}\left(\rho_{0}^{2}+\frac{\rho_{\phi}^{2}}{\sin ^{2} \theta}\right)} \\
& =\frac{1}{h^{2}} \int_{0}^{\pi} \int_{0}^{2 \pi} d \theta d \phi \quad \sqrt{2 \pi I / \beta} \sqrt{2 \pi I \sin ^{2} \theta / \beta} \\
& =\frac{2 \pi I}{\beta h^{2}} \int d \theta d \phi \sin \theta=\frac{2 \pi I}{\beta} \frac{4 \pi}{h^{2}}
\end{aligned}
$$

$$
\begin{array}{ccc}
\ln (Z) & \Rightarrow-\ln (\beta), & \text { so } \\
E & =k_{B} T, & C_V=k_{B}
\end{array}
$$

E.g., the energy corresponds to two degrees of freedom for $\rho_{\theta}, \rho_{\beta}$.

Quantum mechanically $H=\frac{\vec{L}^{2}}{2 I}$ but

$$
\left[L_{i}, L_{j}\right] \neq 0
$$

As usual, $\psi(\theta, \phi)=Y_{l, m}(\theta, \phi)$

with $\vec L^2=b^{2} l(l+1), \quad-l \leq m \leq l$

$$
\begin{aligned}
Z_1  & =\sum_{l=0}^{\infty} \sum_{| m | \leq l} e^{-\frac{\beta}{2 I} \hbar^{2} l(l+1)} \\
& =\sum_{l=0}^{\infty}(2 l+1) e^{-\frac{\beta}{2 I} \hbar^{2} l(l+1)}
\end{aligned}
$$

As $T \rightarrow \infty, \beta \rightarrow 0 \quad \sum_{l=0}^{\infty} \rightarrow \int_{0}^{\infty} d l=\int_0^{\infty} dy/(2l+1)$

$$
\begin{aligned}
\lim _{T \rightarrow \infty} Z & =\frac{T}{\theta_{r}}, \quad \theta_{r}=\frac{h^{2}}{2 I k_B} \\
& =Z_{c l}
\end{aligned}
$$

But as $T \rightarrow 0, \quad Z=1+3 e^{-2\theta_{r} / T}$, such that the specific heat has a steep dropoff as temperature goes to 0,

$$
E_{rot}=-\partial_\beta \ln(Z)\approx 6k_B\theta_r e^{-2\theta_{r} / T}
$$

$$
C_{rot}=\partial_T E_{rot}\approx 3k_B\left(\frac{2\theta_r}{T}\right)^2 e^{-2\theta_{r} / T}\;.
$$



