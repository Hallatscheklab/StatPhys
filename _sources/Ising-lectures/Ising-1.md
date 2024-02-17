## Statistical mechanics with interactions - Ising models 

Thus far, we have developed statistical mechanics as a theoretical framework and applied it to noninteracting systems (e.g. ideal gasses or the paramagnet) or small interacting systems (e.g. just a few spin degrees of freedom). We have left out interacting systems that are large. Why? 

Consider a system of $N$ Ising spins, i.e. $N$ degrees of freedom (d.o.f.) ${\sigma_1, \sigma_2, \dots}$ where each d.o.f. has two possible states, $\{+1,-1\}$. The partition function then involves summing over $2^N$ microstates. With arbitrary interactions (i.e. Hamiltonians), this can be done for small $N$, where we can simply enumerate all possible states. But to be able to compute the partition function analytically for large $N$ requires us to somehow organize the summation in a way that makes it tractable. 

To see why non-interacting systems are tractable, recall the partition function of a paramagnet ($N$ non-interacting Ising spins in a magnetic field $B$),

$$
\begin{aligned}
Z(\beta, M) & =\sum_{\left\{\sigma_{i}\right\}} e^{-\beta\left(-B \Sigma \sigma_{i}\right)} \\
& =\left(1+e^{\beta B}\right)^{N} \;.
\end{aligned}
$$

The factorization of the partition function factorized implies an additive free energy

$$
F=-k_{B} T N \ln \left(1+e^{\beta B}\right) \;.
$$

For non-interacting systems, we can simply "divide and conquer": Analyze a small subsystem, in which we can enumerate all possible states, and obtain the large system as the sum of independent subsystems. ("Whole is not greater than sum of parts.")


Also, $F(T, B)$ is an analytic function without any cusps, kinks or singularities. Since observables are obtained from derivatives, eg. $\left\langle\sigma_{i}\right\rangle=\frac{1}{N} \partial_B F$, everything behaves smoothly: no phase transitions.

This is true for any model with a finite number of microstates $s=1,\dots, \Omega$: If $H[s ; J]$ is analytic in the external force $J$, then 

$$
Z(\beta, J)=\sum_{s=1}^{\Omega} e^{-\beta H[s ; J]}
$$

is. However, with (i) interactions and (ii) thermodynamic limit, this need not be the case: the whole is greater than the sum of its parts, "more is different" (P. Anderson).

However, those intriguing, large, interacting systems generally cannot be solved exactly. We will explore approximations and numerical methods to tackle them. Nonetheless, there are certain cases that can be solved exactly, offering valuable insights. For example, the ...


### All-to-all Ising model

Consider $N$ Ising spins $\left\{\sigma_{1}, \ldots, \sigma_{N}\right\}$, $\sigma_{i} \in\{-1,+1\}$ with Hamiltonian

$$
H[\sigma]=-\frac{J}{2 N} \sum_{i, j=1} \sigma_{i} \sigma_{j}-\sum_{i=1}^{N} B \sigma_{i}
$$

The familiar second term describes the effect of an external magnetic field $B$. The first (non-linear) term describes ferromagnetic interactions: $J>0$ prefers $\uparrow \uparrow$ and $\downarrow \downarrow$ over $\downarrow \uparrow, \uparrow \downarrow$. The sum runs over all pairs of spins, i.e. the interactions are all-to-all,

![all-to-all](../figures/all-to-all.png)


Note that the self-interaction terms ($i=j$) merely contribute a constant and, therefore, have no effect on the behavior of the model. These terms could be taken out, but we keep them for notational simplicty. 

Defining $m \equiv \frac{1}{N} \sum_{i=1}^{N} \sigma_{i}$ what is $\langle m\rangle(\beta, J, \beta)$ as $N \longrightarrow \infty$ ?

We will find that, in the thermodynamic limit $N\to \infty$, the all-to-all Ising model exhibits a phase transition. Below a certain critical temperature, the magnitization assumes a finite value, whose sign can be flipped by an infinitesimal amounts of the magnetic field.

The above Ising model arises as an effective model in many contexts, eg. as a lattice model of particles where it describes 

1: gas

II': liquid.

Corks when we

have a divergent length scale -

near and order phase transition

Analysis: $\langle m\rangle \equiv \frac{1}{N} \sum\left\langle\sigma_{p}\right\rangle$ follows from partition fact $Z=\sum_{\{\sigma\}} e^{-\beta H\{\sigma\}}=e^{-\beta F}$ via differentiation, $\langle m\rangle=-\frac{1}{N} \partial_{B} F$.

To compute $Z$, note we can write

$$
\begin{aligned}
H[\sigma] & =-\frac{7}{2 N} \sum_{i, j=1}^{N} \sigma_{i} \sigma_{j}-\sum_{i=1}^{N} B \sigma_{i} \\
= & \left.N-\frac{J}{2} m^{2}[\sigma]-B m[\sigma]\right] .
\end{aligned}
$$

So, $H$ depends only on $M=N \cdot m[\sigma]$

We can then decompose

$$
Z=\sum_{\sigma} e^{-\beta H[\sigma]}=\sum_{m} \Omega(m) e^{-\beta H[m]}
$$

where $\Omega(m)$ is the density of states with magnetization $m$.

Since $N_{+}=\frac{N}{2}+\frac{M}{2}, N-\frac{N}{2}-\frac{M}{2}$,

$$
\Omega(M)=\frac{N !}{N_{+} ! N_{-} !}=e^{S(M)}
$$

Recall coin flipping w/ $M$ more Hs than $T_{s}$ :

$$
\begin{aligned}
& S(m)=\frac{\ln \Omega(m)}{N}=-\left[\frac{1+m}{2} \ln \frac{1+m}{2}+\frac{1+m}{2} \ln \left(\frac{1-m}{2}\right]\right. \\
& \text { So } \\
& Z(\beta, J, B)=\int_{-1}^{e(m)} d m e^{-\beta N} \underbrace{=f(m)}_{\left.-\frac{f}{2} m^{2}-B m-\frac{s(m)}{\beta}\right]}
\end{aligned}
$$

fromenty density

Thus, depending on $\beta y$, the net $f(m)$ looks


As $N \rightarrow \infty$, sum is dominated by minima $f(m)=f(\bar{m})+\frac{1}{2} f^{\prime \prime}(m)(m-\bar{m})^{2}+\ldots$ $z=\int \operatorname{dm} e^{-\beta N\left[f(\bar{m})+\frac{1}{2} f^{\prime \prime}(\bar{m})(m-\bar{m})^{2}\right]}$

$$
=e^{-\beta N f(\bar{m})} \frac{1}{\sqrt{2 \pi \beta N / f^{(1)}}}
$$

$$
F=N f(\bar{m})+O(\log (N))
$$

So problem reduces to determining minima $f(\bar{m})$. To facilitate, assume $m \ll 1$, where

$$
\begin{gathered}
S(m)=\ln (2)-\frac{m^{2}}{2}-\frac{m^{4}}{12}+C\left(m^{6}\right) \\
\Rightarrow f(m)=-k_{B} T \ln (2)-B m+m^{2} \frac{k_{B} T-f}{2}+m^{4} \frac{k_{B} T}{12} .
\end{gathered}
$$

Let's consider case $B=0$ :

$\bar{m}$ depends crucially on sign of $k_{B} T-\mathcal{Z}$

$$
\begin{aligned}
& k_{B} T-J>0 . f=0 \quad \bar{m}=0 \\
& k_{B} T-J<0: f=\square \bar{m}= \pm \sqrt{3\left(\frac{J}{k_{B} T}-1\right)}
\end{aligned}
$$

which minimum depends on sign (B),

(m) even for infinitesimal $B$ !

(more analysis next HW)

The previous model is physically un realistic because it had all-to-all coupling; in our universe d.a.f. are arranged in space and interact locally. To this end:



