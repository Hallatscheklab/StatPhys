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


Note that the self-interaction terms ($i=j$) merely contribute a constant and, therefore, have no effect on the behavior of the model. These terms could be explicitely taken out of the Hamiltonian, but we keep them for notational simplicity. 

#### Key question
Defining $m \equiv \frac{1}{N} \sum_{i=1}^{N} \sigma_{i}$ what is $\langle m\rangle(\beta, J, \beta)$ as $N \longrightarrow \infty$ ?

We will find that, in the thermodynamic limit $N\to \infty$, the all-to-all Ising model exhibits a phase transition. Below a certain critical temperature, the magnitization assumes a finite value, whose sign can be flipped by an infinitesimal amounts of the magnetic field.

```{note} **Versatility of the Ising model**
All-to-all Ising models, where each spin interacts with every other spin in the system, have applications far beyond the study of magnetism. These models are used in various fields to study systems characterized by complex interactions among their components. E.g.

1. **Neural Networks and Neuroscience**: In computational neuroscience, the Ising model is used to describe the statistical properties of networks of neurons. It helps in understanding how the collective behavior of neurons can give rise to complex phenomena like memory, learning, and pattern recognition.

2. **Optimization Problems**: The Ising model has been applied to solve complex optimization problems, where the goal is to find the minimum of a function over a large space of possible solutions. This includes tasks like the traveling salesman problem, job scheduling, and portfolio optimization. Quantum annealing and classical annealing techniques often use Ising models to represent these problems.

3. **Social Dynamics**: In sociology, the Ising model is employed to study opinion dynamics within societies. It can model how individual opinions (spins) influence each other, leading to the emergence of consensus or polarization within groups.

4. **Financial Markets**: The Ising model has been used to understand the complex dynamics of financial markets, including how individual decisions can lead to collective phenomena like bubbles and crashes. It helps in studying the correlation and volatility clustering observed in market data.

5. **Protein Folding**: In biophysics, the Ising model is applied to understand protein folding, where the folding process can be thought of as spins finding their lowest energy configuration. This analogy helps in exploring the energy landscape of proteins and predicting their stable structures.

6. **Ecological and Evolutionary Dynamics**: The model is used to study species distribution and interaction in ecosystems, as well as evolutionary dynamics where species or traits compete for dominance.

7. **Materials Science**: Beyond traditional magnetism, the Ising model aids in studying the behavior of other condensed matter systems, like alloys and superconductors, where it helps in understanding phase transitions and critical phenomena.

8. **Quantum Computing**: The Ising model is central to the design of quantum algorithms and the operation of quantum computers, especially in quantum annealing and simulation of quantum systems.

9. **Epidemiology**: In modeling the spread of diseases, the Ising model can represent the state of individuals (susceptible, infected, recovered) and their interactions, helping to understand and predict outbreaks.
```




#### Analysis: 
$\langle m\rangle \equiv \frac{1}{N} \sum\left\langle\sigma_{i}\right\rangle$ follows from the partition function $Z=\sum_{\{\sigma\}} e^{-\beta H\{\sigma\}}=e^{-\beta F}$ via differentiation, $\langle m\rangle=-\frac{1}{N} \partial_{B} F$.

To compute $Z$, rewrite the Hamiltonian as

$$
\begin{aligned}
H[\sigma] & =-\frac{J}{2 N} \sum_{i, j=1}^{N} \sigma_{i} \sigma_{j}-\sum_{i=1}^{N} B \sigma_{i} \\
= & \left.N-\frac{J}{2} [m(\sigma)]^2-B m(\sigma)\right] .
\end{aligned}
$$

So, the energy of a microstate only depends on the magnetization $m(\sigma)$.

We can therefore decompose

$$
Z=\sum_{\sigma} e^{-\beta H[\sigma]}=\sum_{m} \Omega(m) e^{-\beta H[m]}
$$

where $\Omega(m)$ is the density of states with magnetization $m$.

Since $N_{+}=\frac{N+M}{2}; N_-=\frac{N-M}{2}$,

$$
\Omega(M)=\frac{N !}{N_{+} ! N_{-} !}=e^{S(M)}
$$

Recall from our analysis of coin flipping, that this is exactly the number of states with $M$ more heads than tails in $N$ trials. Employing Stirling's formula, the entropy takes the form

$$
s(m)=\frac{\ln \Omega(m)}{N}=-\left[\frac{1+m}{2} \ln \frac{1+m}{2}+\frac{1+m}{2} \ln \left(\frac{1-m}{2}\right)\right.
$$

which is the same expression we found for  coin flipping in {eq}`entropy-coin-flipping`. 

So, 
 
$$
Z(\beta, J, B)=\int_{-1}^{1} d m e^{-\beta N\left[-\frac{J}2 m^2- B m - \frac{s(m)}\beta\right]}= e^{-\beta f(m)}
$$

where $f(m)=e(m)-T s(m)=-\frac{J}2 m^2- B m-Ts(m)$ is the free energy density conditional on magnetization.

Thus, depending on $\beta J$, the net $f(m)$ looks

![](https://cdn.mathpix.com/cropped/2024_02_16_819a36779a8388cf6552g-06.jpg?height=400&width=966&top_left_y=663&top_left_x=1018)


As $N \rightarrow \infty$ (TDL), sum is dominated by minima $f(m)=f(\bar{m})+\frac{1}{2} f^{\prime \prime}(m)(m-\bar{m})^{2}$

$$
\begin{aligned}
Z & =\int d m e^{-\beta N\left[f(\bar{m})+\frac{1}{2} f^{\prime \prime}(m)(m-\bar{m})^{2}\right]} \\
& =e^{-\beta N f(\bar{m})} \frac{1}{\sqrt{2 \pi \beta N / f^{\prime \prime}(\bar{m})}} \\
F & =-k_{B} T \ln Z=N f(\bar{m})+O(\log (N))
\end{aligned}
$$

So, problem reduces to determining minima $f(\bar{m})$. To facilitate, assume $m \ll 1$, where

$$
\begin{gathered}
s(m)=\ln (2)-\frac{m^{2}}{2}-\frac{m^{4}}{12}+O\left(m^{6}\right) \\
\Rightarrow f(m)=-k_{B} T \ln (2)-B m+m^{2} \frac{k_{B} T-J}{2}+m^{4} \frac{k_{B} T}{12} .
\end{gathered}
$$


Let's consider case $B=0$ :

$\bar{m}$ depends crucially on sign of

$$
\begin{aligned}
& k_{B} T-J>0: f(\bar{m}) \text{ is a single well; one minimum } \bar{m}=0 \\
& k_{B} T-J<0: f(\bar{m}) \text{ is a symmetrical double well; two minima at } \bar{m}= \pm \sqrt{3\left(\frac{J}{k_{B}T}-1\right)}\;.
\end{aligned}
$$

Which minimum is attained depends on sign (B), even for infinitesimal $B$ !






(more analysis next HW)

The previous model is physically un realistic because it had all-to-all coupling; in our universe d.a.f. are arranged in space and interact locally. To this end:



