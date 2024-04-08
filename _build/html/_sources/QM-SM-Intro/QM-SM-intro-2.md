## Gapless quantum matter: phonons + Debye model Coldstone's Theorem

#### Phonon + Debye model

Thus far, we've considered few d.o.f's, in which case the quantum Hamiltonian has a gap, e.g., $\Delta E=\hbar \omega$ or $\Delta E=\frac{\hbar^{2}}{I}$, which implies $C_V\sim e^{-\Delta E/(k_B T)}$.

A more interesting behaviour arises as $N \rightarrow \infty$ if the Hamiltonian is gapless. As an example of a gapless model, we will now discuss vibrations in a crystal.

Consider a crystal formed from regular array of atoms,

$$
\begin{gathered}
\vec{q}_{l, m, n}^{*}=l \vec{R}_{1}+m \vec{R}_{2}+n \vec{R}_{3} \\
l, m, n \in \mathbb{Z}
\end{gathered}
$$

![](https://cdn.mathpix.com/cropped/2024_03_30_5afcfb13a3ee84e64774g-02.jpg?height=425&width=593&top_left_y=818&top_left_x=1151)

$\vec{R}_{i}$ are "Bravais vectors"; for the cubic case, we have

$$
\vec{R}_{1}=a \hat{x} \quad \vec{R}_{2}=a \hat{y} \quad \vec{R}_{3}=a \hat{z}
$$

There are other possibilities such at hexagons, orthorombic, etc: 14 distinct Bravais lattices in 3D. There may also be multiple atoms in the unit cell. But here, we focus on  the simple cubic case.

The atoms are held in place $\vec{q}^{*}_{l, m, n}$ by various chemical/electrical forces. But their positions can fluctuate thermally and quantum mechanically, 

$$
\vec{q}_{l, m, n}=\vec{q}_{l, m, n}^{*}+ \vec{u}_{l, m, n} \;,
$$

where $\vec{u}_{l, m, n}$ is the displacement of atom $l, m, n$ from its equilibrium position.

It is convenient to label atom $l, m, n$ by it's equilibrium position $\vec{r} \equiv \vec{q}_{l, m, n}^{*}$ :

$$
\vec q_{\vec r}=\vec r+\vec u_{\vec r}
$$

 
The potential energy takes the general form

$$
V(\{\vec q_{\vec r}\})=V^*+\frac 12 \sum_{\vec r, \vec r', \alpha, \beta} \frac{\partial^2 V}{\partial q_{\alpha,r} \partial q_{\beta, r'}}u_{\alpha, r}u_{\beta, r'}
$$

where $\alpha, \beta$ are the 3-dimensional  vector indices ($\{x,y,z\}$) of the displacement vector. Also, we assume $|\vec{u}| \ll a$, valid for $T \rightarrow 0$ and mass $  \rightarrow \infty$ (since $\Delta v \Delta u \geq \hbar / $ mass ) outside this regime, crystal is melting! Note that $\left.\frac{\partial V}{\partial q}\right|_{q^{*}}=0$ at equilibrium.

We now make use of translation invariance: $\quad V\left(\left\{\vec{q}_{\vec{r}}+\vec{c}\right\}\right)=V\left(\left\{\vec{q}_{r}\right\}\right)$ which implies

$$
\frac{\partial^{2} V}{\partial q_{\alpha}(r) \partial q_{\beta}\left(r^{\prime}\right)} \equiv K_{\alpha \beta}\left(\vec{r}-\vec{r}^{\prime}\right)
$$

The total Hamiltonian is given by 

$$\hat{H}=V^{*}+\sum_{r} \frac{\vec{p}_{r}^{2}}{2 m}+\frac{1}{2} \sum_{r, r^{\prime}} u_{\alpha, r} K_{\alpha  \beta}\left(r-r^{\prime}\right) u_{\beta, r^{\prime}}
$$

where $\quad\left[p_{\alpha, r}, u_{\beta, r^{\prime}}\right]=-i \delta_{\alpha \beta} \delta_{r r^{\prime}}$

This allows us to use discrete Fourier transform to simplify $\tilde{H}$ :

$$
\begin{aligned}
& U_{\alpha}(\vec{k}) \equiv \frac{1}{\sqrt{N}} \int \sum_{\vec{r}} e^{-i \vec{k} \cdot \vec{r}} U_{\alpha, r} \\
& p_{\alpha}(\vec{k}) \equiv \frac{1}{\sqrt{N}} \sum_{\vec{r}} e^{-i \vec{k} \cdot \vec{r}} p_{\alpha, r} \\
& K_{\alpha \beta}(\vec{k}) \equiv \sum_{\vec{r}} e^{i \vec{k} \cdot \vec{r}} K_{\alpha, \beta}(\vec{r})
\end{aligned}
$$

For simplicity assume $K_{\alpha \beta}(\vec{k})=\delta_{\alpha \beta} \tilde{K}(\vec{k})$

$$
\hat{H}=\sum_{k}\left[\frac{\vec{p}(\vec{k}) \cdot \vec{\rho}(-\vec{k})}{2 m}+\frac{1}{2} \widetilde{K}(\vec{k}) \vec{u}(\vec{k}) \cdot \vec{u}(-\vec{k})\right]
$$

What discrete values do $\vec{k}$ take?

First recall $\vec{r}=a(l \hat{x}+m \hat{y}+n \hat{z})$

So $\quad e^{i \vec{k} \cdot \vec{r}}=e^{i\left(\vec{k}+\frac{2 \pi}{a} \hat{e}_{i}\right) \cdot \vec{r}}$ for $\hat{e}_{i}=\hat{x}, \hat{y}, \hat{z}$.

Thus $u_{\alpha}(\vec{k})=U_{\alpha}\left(\vec{k}+\frac{2 \pi}{a} \hat{e}_i\right)$ : periodic in k-space. This k-space torus is called the "Brillouin Zone" (BZ)

![](https://cdn.mathpix.com/cropped/2024_03_30_5afcfb13a3ee84e64774g-05.jpg?height=445&width=712&top_left_y=780&top_left_x=729)

Second, let's assume the system has periodic boundary condition in real space, $\vec{r} \sim \vec{r}+L \cdot \hat{e}_{i}$. This implies that we can only choose $\vec k$ vectors that satisfy

$$
\begin{aligned}
& e^{i \vec{k} \cdot \vec{r}}=e^{i \vec{k}(\vec{r}+L \cdot  \hat{e}_i)} \\
& \longrightarrow \quad \vec{k} \in \frac{2 \pi}{L} \cdot(i, j, k), \quad i, j, k \in \mathbb{Z} \\
& -\frac{L}{2} \leq i, j, k\leq\frac{L}{2}
\end{aligned}
$$

Together this gives, a one-to-one mapping between $(L/a)^{3}$ $\vec{r}$ points ti $(L/a)^{3}$ $\vec{k}$ points.

Finally, note that because $\vec{p}_{\vec{r}}$ and $\vec{u}_{\vec{r}}$ are real,

$$
\begin{gathered}
\vec u_{\alpha,\vec k}=\vec u_{\alpha,-\vec k}^{*} \quad \vec p_{\alpha, k}=\vec p_{\alpha,-\vec k}^{*}: \\
\hat{H}=V^{*}+\sum_{k}\left[\frac{|\vec{p}(\vec{k})|^{2}}{2 m}+\frac{1}{2} \tilde{K}(\vec{k})|\vec{u}(\vec{k})|^{2}\right]
\end{gathered}
$$

We see problem decouples in K-space: $3 N=3 L^{3} \quad$ indepedent harmonic oscillators with frequency $\omega(\vec{k})=\sqrt{\frac{\widetilde{K}(\vec{k})}{m}}$

These oscillations correspond to waves in the positions of atoms:


![](https://cdn.mathpix.com/cropped/2024_03_30_5afcfb13a3ee84e64774g-06.jpg?height=430&width=1737&top_left_y=1436&top_left_x=140)

These are sound waves of the crystal. They travel at group velocity $\vec{v}_{\vec{k}}=\frac{\partial \omega(\vec{k})}{\partial \vec{k}}$, which depends on the "dispersion relation" $\omega(\vec{k})$.


Quantum mechanically, we introduce $3 \mathrm{~N}$ raising / lowering operators $\hat a_{\alpha, k}^{+}, \hat a_{\alpha, k}$ with occupancy operator $\hat n_{\alpha, k}=a_{\alpha, k}^{+} a_{\alpha, k}$. With ansatz

$$
\begin{aligned}
& u_{\alpha, k}=\sqrt{\frac{b}{2 m \omega(k)}}\left(a_{k}^{+}+a_{-k}\right) \\
& p_{\alpha, k}=i \sqrt{\frac{k m \omega(k)}{2}}\left(a_{k}^{+}-a_{-k}\right) \\
& {\left[p_{k}, u_{-k}\right]=i \frac{\hbar}{2}(-1-1)=-i \hbar}
\end{aligned}
$$

we obtain

$$
\hat{H}=V^{*}+\sum_{k, \alpha} \hbar \omega_\alpha(\vec{k})\left(\hat{n}_{\alpha, \vec{k}}+\frac{1}{2}\right) \;.
$$

Just like electromagnetic waves (light) give rise to quantized photons (Q.E.D.), these quanta of sound waves are called "phonons." They are bosonic "quasiparticles" even though the underlying atoms may be fermions. Simple example of persistent theme in cond-mat / quantum many -body physics: emergence of lowenergy quasiparticle excitations distinct from constituent particles; they are "collective modes."

The Hilbert space is spanned by specifying the occupation of each of the $3 N \quad n_{\alpha, k}=0,1,2, \ldots$

$$
\left|\left\{n_{\alpha, k}\right\}\right\rangle=\left|0,3,1,2, \ldots\right\rangle
$$

The QM partition function is

$$
\begin{aligned}
Z & =\sum_{\left\{n_{\alpha, \vec k}\right\}} e^{-\beta H}=e^{-\beta E_{0}} \sum_{\left\{n_{\alpha, \vec k}\right\}} e^{-\beta\sum_{\vec k, \alpha} \hbar \omega(\vec{k})n_{\alpha, \vec{k}}} \\
& =e^{-\beta E_{0}} \prod_{\vec k,\alpha}\left(\sum_{n_{\alpha, \vec k}=0}^{\infty} e^{-\beta \hbar \omega_{\alpha}(\vec k)  n_{\alpha, \vec k}}\right) \\
& =e^{-\beta E_{0}} \prod_{\vec k,\alpha}\left(\frac{1}{1-e^{-\beta \hbar \omega_{\alpha}(\vec k)}}\right) \\
F & =-\frac{1}{\beta} \ln (Z)=E_{0}+\frac{1}{\beta} \sum_{\vec k,\alpha} \ln \left(1-e^{-\beta \hbar \omega_{\alpha}(\vec k)}\right)
\end{aligned}
$$

Important physical observables are

$$
\begin{aligned}
\langle E\rangle & =E_{0}+\sum_{\alpha, \vec k}\left\langle n_{\alpha, k}\right\rangle \hbar \omega_{\alpha}(k) \\
C & =\partial_{T}\langle E\rangle
\end{aligned}
$$

For a single QM d.o.f., we found $C \sim e^{-\Delta E / K_{B} T}$. We'll now see that this is not the case for phonons!

First we need

$$
\begin{aligned}
& \left\langle n_{\alpha, \vec k}\right\rangle=\frac{\sum_{n=0}^{\infty} n e^{-\beta \hbar \omega_{\alpha}(\vec k) n}}{\sum_{n=0}^{\infty} e^{-\beta \hbar  \omega_{\alpha}(\vec k) \cdot n}}=\frac{1}{e^{\beta \hbar \omega_{\alpha}(\vec k)}-1}
\end{aligned}
$$

This is the famous Bose-Einstein distribution.

$$
\begin{aligned}
& \langle E\rangle=E_{0}+\sum_{\alpha, \vec k}\left\langle n_{\alpha, \vec k}\right\rangle \hbar \omega_{\alpha}(\vec k) \\
& C=\partial_{T}\langle E\rangle=k_{B} \sum_{\alpha, \vec k} \frac{1}{\left(e^{\beta \hbar \omega_{\alpha}(\vec k)}-1\right)^{2}}\left(\frac{\hbar \omega_{\alpha}(\vec k)}{k_{B} T}\right)^{2}
\end{aligned}
$$

To proceed further, we need to know $\omega_{\alpha}(\vec k)$.

## Debye Model.

In general, the precise form of $\omega_{\alpha}(\vec k)$ depends on all the details of

$$
\text { chemistry } \longrightarrow V\left(\{\vec{q} \vec{r} \}) \rightarrow K_{\alpha \beta}(\vec{r}) .\right.
$$

However, one thing we know is $V(\{\vec{q} \vec{r}+\vec{c} \})=V(\{\vec{q} r\})$ because of translation invariance

Since $\vec{q} \vec{r}=\vec{r}+\vec{u} \vec{r}$, this implies $\vec{u}_{\vec{r}}=\vec{c}$ (a rigid shift of lattice) has $\Delta E=0$. This is precisely the $\vec{u}(\vec{k}=0)$ mode. So we know

$$
\tilde K_{\alpha \beta}(\vec{k}=0)=0
$$

Second, suppose $K_{\alpha \beta}(\vec{r})$ is local, meaning $K \rightarrow 0$ as $\vec{r} \rightarrow \infty$ exponentially quickly. The Fourier transform of a local function is analytic, so we can Taylor expand:

$$
\begin{aligned}
\tilde{K}(\vec{k})=0 & +\tilde{\kappa}_{\alpha} \cdot k_{\alpha}+\frac{1}{2} \tilde{\kappa}_{\alpha \beta} k_{\alpha} \cdot k_{\beta} \\
& +\frac{1}{3 !} \tilde{\kappa}_{\alpha \beta \gamma} k_{\alpha} k_{\beta} k_{\gamma}+\cdots
\end{aligned}
$$

With inversion symmetry, $K(\vec{r})=K(-\vec{r})$ so the odd-k terms vanish:

$$
\tilde{K}(\vec{k})=\frac{1}{2}  \tilde{\kappa}_{\alpha \beta} k_{\alpha}k_{\beta}+O\left(K^{+}\right)
$$

Finally, if system is isotropic, $x \sim y \sim z$,

$$
F(\vec{k})=B|\vec{k}|^{2}+O\left(k^{4}\right)
$$

So $\omega(\vec{k})=\sqrt{\frac{B k^{2}+\cdots}{m}}=v \cdot|\vec{k}|+O\left(k^{3}\right)$

where $v=\sqrt{B / m}=$ is the velocity of sound.

The approximation breaks down as $k \rightarrow \pi / a$.

Within this approximation,

$$
\langle E\rangle=E_{0}+\sum_{\alpha, \vec{k}} \frac{\hbar v \cdot k}{e^{\beta k v k}-1}
$$

Since $\vec{k}=\frac{2 \pi}{L }(i, j, k)$, we obtain in the limit $L \rightarrow \infty$

$$
\sum_{\vec{k}} \rightarrow\left(\frac{L \cdot a}{2 \pi}\right)^{3} \int_{B Z} d^{3} k
$$

So $\langle E\rangle \approx E_{0}+3 \cdot v \int_{B Z} \frac{d^{3} k}{(2 \pi)^{3}} \frac{\hbar v k}{e^{\beta \hbar  v k}-1}$

Since $B Z=[-\pi / a, \pi / a]^{3}$, this is hard integral. However, for

$$
\begin{gathered}
T \ll T_{D} \equiv \frac{\hbar v}{k_B} \cdot \frac{\pi}{a}, \\
\frac{1}{e^{\beta \hbar  v k}-1} \sim e^{-\beta \hbar v k} \ll 1 \text { for } k \sim \frac{\pi}{a} .
\end{gathered}
$$

The boundary of the $B Z$, which has energy $\quad E \sim \hbar v \cdot \frac{\pi}{a} \gg T$, does not contribute to integral. Thus to exponential accuracy in $T / T_{D}$ we can simply extend shape of $B Z \rightarrow \infty$

$$
\begin{aligned}
\langle E) & =E_{0}+3 V \int_{d^{3} k}^{(2 \pi)^{3}} \frac{\hbar v k}{e^{\beta \hbar v k}-1} \\
& =E_{0}+3 V \int_{0}^{\infty} d k \frac{4 \pi k^{2}}{(2 \pi)^{3}} \frac{\hbar v k}{e^{\beta \hbar v k}-1} \\
& =E_{0}+\frac{\pi^{2}}{10} \cdot V \cdot \frac{\left(k_{B} T\right)^{4}}{(\hbar v)^{3}} \\
\frac{C}{V} & =k_{B} \frac{2 \pi^{2}}{5}\left(\frac{k_{B} T}{\hbar v}\right)^{3}
\end{aligned}
$$

The key finding is $E \sim T^{4}$, and $C_v \sim T^{3}$, rather than $E, C \sim e^{-\Delta E / T}$. This is because the phonon are gapless: since $\hbar \omega(k) \sim k v \cdot k$, there are excitations with arbitrarily low energy. There is "no energy gap". In HEP language, phonon are massless,

$$
E(k)=k v k \longleftrightarrow E(p)=v \cdot p
$$

vs "mass gap" dispersion,

$$
E(p)=\sqrt{m_{0}^{2} v^{4}+p^{2} \cdot v^{2}}=m v^{2}+\frac{p^{2}}{2 m}
$$

The above illustrates a profound principle: low $-T$ behaviour depends on only a few "relevant" parameters (e.g., $v$ ) and not further details!

Relation to spontaneous symmetry breaking: "Goldstone modes."

Recall that for $T<T_{c}$, the Ising model spontaneously broke the time-reversal symmetry $E(\{\sigma\})=E(\{-\sigma\})$

The phonon model just discussed also has a symmetry: $E\left(\left\{q_{\vec{r}}\right\}\right)=E\left(\left\{\overrightarrow{q_{r}}+\vec{c}\right\}\right)$

This implies $\left\langle\vec{q}_{r}\right\rangle=\vec{r} $ spontaneously breaks translation symmetry!

[note $\left\langle\vec{q}_{r}\right\rangle=\vec{r}+\left\langle u_{\vec{r}}\right\rangle$, and

$$
\begin{aligned}
\left\langle u_{\vec{r}}\right\rangle & =\sum_{k} \frac{e^{i \vec{k} \cdot \vec{r}}}{\sqrt{N}} \sqrt{\frac{1}{2 m \omega_{k}}}\left\langle a_{k}^{+}+a_{-k}\right\rangle \\
& =0]
\end{aligned}
$$

(Caveat: in $D=2$, it's actually more subtle: "Mermin-Wagner" theorem $\Rightarrow$ no SSB of continuous symmetry. Covered in Physics 212)

The existence of translation symmetry is what allowed us to conclude $\hbar \omega(k=0)=0 \Rightarrow \omega(k) \sim v \cdot k \Longrightarrow$ gapless.

This is actually special case of more general result: Gold stone's Theorem

"A system with a spontaneously broken continuous global symmetry has a gapless mode (the Goldstone boson)

[Some subleties depending on Lorentz/ vs hon-relatavistic and internal vs spacetime symmetry?

The phonon (sound!) is the "Goldstone mode" for SSB of translation!

