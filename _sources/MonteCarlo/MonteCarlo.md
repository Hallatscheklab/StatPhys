## Monte Carlo and the Metropolis Algorithm

For general $H$, it is not easy to compute

$$
\langle \mathcal{O}\rangle=\frac{1}{Z} \sum_{\mu} \mathcal{O}(\mu) e^{-\beta H(\mu)}
$$

exactly. Except in special cases (1D, non-interacting, exactly solvable), either approximate (variational/perturbative) or numerical approaches needed.

Monte Carlo is a general method for computing $\sum_{\mu} f_{\mu}$ where $\mu \in$ really big space. Applicable not just to statistical physics but alos in biology, finance, complex systems etc. (cite)

In a general setting, $\sum_\mu f_{\mu}$ may not have an underlying probabilistic interpretation; for example we might be trying to evaluate an oscillatory integral in a high-dim space $\mu \in \mathbb{R}^{n}$

$$
\underbrace{\int_{0}^{1} d x_{1} d x_{2} \cdots d x_{n}}_{\sum_{\mu}} \underbrace{f\left(x_{1}, \cdots x_{n}\right)}_{f_{\mu}}
$$

### Importance sampling

In this general setting, the first step is to introduce an "importance" weight $0<p_{\mu}<1, \sum_{N} p_{\mu}=1$. A natural choice is $p_{\mu}=\frac{\left|f_{\mu}\right|}{\sum\left|f_{\mu}\right|}$, which places a higher weight at summands that are large. We can then trivially rewrite

$$
\sum_{\mu} f_{\mu}=\sum p_{\mu} \cdot \overbrace{\left(\frac{f_{\mu}}{p_{\mu}}\right)}^{\mathcal{O}_{\mu}}=\langle\mathcal{O}\rangle_{p}
$$

In statistical mechanics, the natural choice is the Boltzmann distribution: $p_{\mu}=\frac{e^{-\beta H_{\mu}}}{z}$

Since the entropy $S\propto N$ is extensive in the number $N$ of degrees of freedom, which can be very large (e.g. $N \sim 10^{23}$), the number $\Omega=e^{S/k_B}$ of all possible microstates is often *huge*. It is, therefore, way too slow to explicitly sum $\sum_{\mu=1}^{\Omega} p_{\mu} \mathcal{O}_{\mu}$.

However, rare ("unimportant") events $p_{\mu} \ll 1$ don't contribute much, so we shouldn't spend much time on them. This suggest we can estimate $\langle \mathcal{O}\rangle p$ by sampling from $p_\mu$.

All this means is that we repeatedly roll an $\Omega$-sided die weighted by $p_{\mu}$. This generates a sequence of samples $\mu_{1}, \mu_{2}, \cdots \mu_{m}$ where $M \ll \Omega$. Our estimate is then

$$
\langle \mathcal{O}\rangle_{p} \approx \frac{1}{M} \sum_{i=1}^{M} \mathcal{O}_{\mu_{i}}
$$

and $\lim _{M \rightarrow \infty} \frac{1}{M} \sum_{i=1}^{M} \mathcal{O}_{\mu_i}=\langle\mathcal{O}\rangle_p$ guaranteed.

For finite $M$, there will be some error in our estimate of $\langle \mathcal{O}\rangle_p$ because we may have made some atypical rolls of the die. The typical deviation between $\langle \mathcal{O}\rangle_p$ and $\frac{1}{M} \sum_{i=1}^{M} \mathcal{O}_{\mu_i}$ is (central limit theorem)

$$
\Delta \mathcal{O}=\frac{1}{\sqrt{M}} \sqrt{\left\langle(O-\langle O\rangle)^{2}\right\rangle}
$$

So the Monte-Carlo accuracy scales as

$$
\epsilon=\frac{\text{var}{(\mathcal{O})}}{\sqrt{M}} \;.
$$

In most cases of interest, $\text{var}{(\mathcal{O})}$ is bounded as the size of the space $\Omega \rightarrow \infty$. For example, in the Ising model $\Omega=2^{N}$, but $\left\langle m^{2}\right\rangle \equiv N^{-1}\sum_i \sigma_i$ is independent of $N$.  

To obtain accuracy $\epsilon$, we need $M_{\epsilon}=\frac{\left\langle \mathcal{O}^{2}\right\rangle}{\epsilon^{2}}$ samples, which will thus be vastly less than a full sum $\sum_{\mu=1}^{\Omega} p_{\mu} \mathcal{O}_{\mu}$ over all $\Omega$ states.

However: we encounter a problem. For $p_{\mu}=\frac{e^{-\beta H_{\mu}}}{Z}$, how do we efficiently roll a $\Omega$-sided die? Worse, we don't actually know the probabilities because we cannot compute the normalization constant

$$
Z=\sum_{N=1}^{N} e^{-\beta H_{N}} \;,
$$

aka the partition function. Getting around this problem is where the genius of Metropolis et al. '53 (cite) comes in. They discovered a way to sample from $p_{\mu}=\frac{e^{-\beta E_{\mu}}}{Z}$ without knowing $Z$ !

The idea is to invent some fictions dynamics $\mu_{t} \rightarrow \mu_{t+1}$ so that $\quad\left\{\mu_{1}, \mu_{2}, \mu_{3}, \ldots\right\}$ visits state $\mu$ with frequency $p_\mu$. Of course in stat-mech, we could choose $r=\{q, p\}$ to evolve under $\vec{F}=m \vec{a}$ with a reservoir, which by ergodic hypothesis would produce $p_\mu$. But (as your HW demonstrates) this is expensive/slow. Instead we introduce some simpler/fake dynamics in the form of a "Markov chain". 

A "Markov chain" is a set of transition rates $O<M_{\mu^{\prime} \mu}<1$ under which the probability dist. evolves as 

$$
p_{\mu^{\prime}}(t+1)=\sum_{N} M_{\mu^{\prime} \mu} p_{\mu}(t)
$$ (master-eq)

with $\sum_{\mu^{\prime}} M_{\mu^{\prime} \mu}=1$. $M_{\mu^{\prime} \mu}=P\left(\mu^{\prime} \mid \mu\right)$ is the conditional probability for transition $\mu \longrightarrow \mu^{\prime}$ at each step. 

At long times, the distribution equilibrates to

$$
p_{\mu}(t=\infty)=\lim _{t \rightarrow \infty}\left(M^{t}\right) p_{\mu}(0) \equiv \pi_{\mu}
$$

where $M \cdot \pi_{\mu}=\pi_{\mu}$.

We are not going to keep track of the full distribution $p_{\mu}(t)$ ($\Omega$ is huge). Instead, we want to sample from it, $\left\{\mu_{1}, \mu_{2}, \cdots\right\}$.

To implement the Markov process represented by the above master equation {eq}`master-eq`, we pick at each time step a new state $\mu_{t+1}$ given $\mu_t$ by rolling a die biased on the conditional probability $P\left(\mu_{t+1} \mid \mu_{t}\right)=M_{\mu_{t+1}\mu_t} $. As you repeat, you build up $\left\{\mu_{1}, \mu_{2}, \cdots, \mu_{T}\right\}$ which is distributed at $\pi_{\mu}$ as $T \rightarrow \infty$.

So the question is now how to pick $M_{\mu^\prime\mu}$ so that $\pi_{\mu}=\frac{1}{Z} e^{-\beta H_{\mu}}$.

Suppose $M$ satisfies

$$
M_{\mu^{\prime} \mu} \pi_{\mu}=M_{\mu \mu^{\prime}} \pi_{\mu'}
$$

for any two $\mu, \mu^{\prime}$ ("detailed balance").

We have 

$$
\left(M \cdot \pi\right)_{\mu^{\prime}}=\sum_{\mu} M_{\mu^{\prime} \mu} \pi_{\mu}=\sum_{\mu} M_{\mu \mu^{\prime}} \pi_{\mu^{\prime}}=\pi_{\mu^{\prime}}
$$

So, any arbitrary distribution $\pi_\mu$ can be generated by a Markov process where the transition rates satisfy the detailed balance condition corresponding to $\pi_\mu$, 


$$
\frac{M_{\mu^{\prime} \mu}}{M_{\mu \mu^{\prime}}}=\frac{\pi_{\mu^{\prime}}}{\pi_{\mu}}=e^{-\beta\left(E_{\mu^{\prime}}-E_{\mu}\right)} \;.
$$

The key simplification is that $Z$ cancels in these transition rate ratios - the RHS is easily computable.

There are many choices which satisfy detailed balance; the simplest is the Metropolis rule.

#### Metropolis Rule

Let's focus on a spin system $\mu={\sigma_{1},\sigma_{2}, \cdots \sigma_{N}}$ for notational simplicity (the original paper focusses on $\mu=\left\{\vec{q}_{i}, \vec{p}_{i}\right\})$

(1) Randomly pick one of the $N$ spins " $\sigma_{i}$ "

(2) Consider a "trial" configuration $\{\sigma\}^{\prime}$ obtained by taking current $\left\{\sigma\}_{t}\right.$ and flipping only $\sigma_{i} \rightarrow-\sigma_{i}$

E.g., for $\{\sigma\}_{t}=\uparrow \uparrow \downarrow \uparrow$ and $\{\sigma'\}=\uparrow \downarrow \downarrow \uparrow$.


(3) Compute the energy change

$$
\Delta E=H\left[\left\{\sigma^{\prime}\right\}\right]-\mathcal{H}\left[\{\sigma\}_{t}\right]
$$

Note that because $\mathcal{H}$ is local, this can be done only by looking at the spins near $\sigma_{i}$ ; we don't need to compute the full energy!

(4) Generate a random number $0<q<i$.

If $ q<e^{-\beta \Delta E}$ : **Accept** the move. $\left\{\sigma 3_{t+1}=\{\sigma\}^{\prime}\right.$

Otherwise, if $q>e^{-\beta \Delta E}$ : **Reject** the move: $\{\sigma\}_{t+1}=\{\sigma\}_{t}$

Note that if $\Delta E<0, e^{-\beta \Delta E}>1$, we always accept the rule.

Let's check: is $\frac{M_{\mu^{\prime} \mu}}{M_{\mu \mu^{\prime}}}=e^{-\beta\left(E_{\mu^{\prime}}-E_{\mu}\right)}$?

If $\Delta E=E_{\mu}-E_{\mu}<0$, then

$$
\begin{aligned}
& M_{\mu^{\prime} \mu}=1, \quad M_{\mu \mu^{\prime}}=e^{+\beta \Delta E} \\
& \longrightarrow \frac{M_{\mu^{\prime}\mu}}{M_{\mu \mu^{\prime}}}=e^{-\beta \Delta E}
\end{aligned}
$$

If $\Delta E>0$

$$
\begin{aligned}
& M_{\mu^{\prime} \mu}=e^{-\beta \Delta E}, \quad M_{\mu \mu^{\prime}}=1 \\
& \longrightarrow \frac{M_{\mu^{\prime} \mu}}{M_{\mu \mu^{\prime}}}=e^{-\beta \Delta E}
\end{aligned}
$$

Thus, $M_{\mu'\mu}$ indeed satisfies detailed balance w.r.t. $\pi_\mu$. 

We throw this into a for-loop, generating thousands of samples

$$
\left\{\mu_{1}, \mu_{2}, \mu_{3}, \cdots, \mu_{M}\right\}
$$

As we go along, we accumulate measurements

$$
\langle \mathcal{O} \rangle\approxM^{-1}\sum_{t=1}^{M} \mathcal{O}\left(\mu_{t}\right)
$$

for any relevant observables.

#### Numerical Considerations

(1) "Burn in". Given an initial state, a MC chain relaxes to eq. value over time " $\tau$ "

$$
M^{t} p(t=0)=\pi+O\left(e^{-t / \tau}\right)
$$

$\tau$ is determined by the eigenspectrum of $M$. It is a good idea to throw-out the first $\sim \tau$ measurements to account for this:

$$
\begin{aligned}
\langle \mathcal{O}\rangle=\frac{1}{\mu-T} & \sum_{t=T}^{M} \mathcal{O}\left(\mu_{t}\right) \\
& \tau \text { "burn-in" time }
\end{aligned}
$$

In practice you done know the relaxation time a priori, so $T$ determined by various heuristics.

(2) Error Bars + auto-correlation

For a finite number of samples " $M$ ",

$$
\begin{aligned}
& \langle \mathcal{O}\rangle=\frac{1}{M} \sum_{t=1}^{M} \mathcal{O}\left(\mu_{t}\right)+\epsilon 
\end{aligned}
$$

The error $\epsilon$ is given by 

$$
\epsilon=\frac{\text{var}(\mathcal{O})}{\sqrt{M}} \\
\text{var}(\mathcal{O})=\frac{1}{M} \sum_{t=1}^{M} \mathcal{O}^{2}\left(\mu_{t}\right)-\langle\mathcal{O}\rangle^{2}
$$

if each a sample $\mu_{t}$ is generated by an indepedent roll of an $N$-sided die. However, if $\mu_{t}$ is generated by a Markov chain this generates a correlation between samples

$$
\langle \mathcal{O}_{t}\mathcal{O}_{t+\tau} \rangle\sim e^{t/\tau}
$$

where $\tau$ is "auto-correlation" rime. Very roughly speaking this gives

$$
\epsilon=\frac{\text{var}(\mathcal{O})}{\sqrt{M/\tau}}\;.
$$

