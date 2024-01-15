LI Coin flipping

Agenda:
- microctates us macros.
- emerging collective behavior
- universality (CLT)
- entropy us energy
- probability recap

Reading:
- Atovas, Ch.
- Kardar, Ch. 2

## Coin flipping  $N$ times

We will use the simple example of the repeated flipping a generally biased coin (outcome Heads or Tails) a warm-up excercise to illustrate key concepts in statistical physics. 

Coin flipping in many context:
- spatial configuration of magnetic moments: spin up or down
- time series of left- or right steps in a random walk or a polymer (1D freely jointed chain)

We assume that the coin is flipped $N$ times (~"volume" of spin chain) and describe the outcome of the coin flip $i$ as $\sigma_{i} \in\{-1,+1\}$.

$P\left(\sigma_{i}\right)=\left\{\begin{array}{l}p \;, \quad\sigma=1 \\ q=1-p\;, \quad \sigma=-1\end{array}\right.$ 

$\left(P\left(\sigma_{i}\right)=p \cdot \delta_{i 1}+q \delta_{i 0} \quad\right.$ sometimes useful. $)$

Since coin flips are uncorrelated (by assumption), the probability of observing a particular configuration is given by
$$
\begin{aligned}
P\left(\sigma_{1}, \sigma_{2}, \ldots\right) & = \prod_{j} P\left(\sigma_{j}\right) \\
& \text { (uncorrelated spins) }
\end{aligned}
$$

*Question:* Compare
\begin{aligned}
& A=\{++--+++-+-+++---+++-+-++-+\} \\
& B=\{++++++++++++++++++++++++++\} \\
& C=\{+-+-+-+-+-+-+-+-+-+-+-+-+-\}
\end{aligned}



If $p=q=\frac{1}{2}, P(A)=P(B)=P(C)$. So, why does $B$ (and $C$?) look exceptional?

### Coarse-graining

In the realm of statistical physics, the concept of **coarse-graining** plays a pivotal role in understanding the transition from microscopic to macroscopic descriptions. The entire configuration of a system, denoted by $\{\sigma\} = \left\{\sigma_{1}, \sigma_{2}, \ldots\right\}$, represents the **micro-state**. The set of all micro-states encompasses all possible configurations at the most fundamental level.


But, usually, we cannot directly observe all degrees of freedom of a microstate. Instead, we measure certain observables that have the same value for many microstates. For example, we typically cannot measure all spins in a magnet but just a sum over all spins. In a magnet, for instance, we care about the magnetization, $$X \equiv \sum_{j=1}^{N} \sigma_{j}\;,$$
which is the difference $X=N_+-N_-$ between up- and down-spins. (Likewise, when we stare at a coin flip series of 1's and 0's our brains tend to quickly notice if there's a mismatch between 1's and 0's.) 

Since $\{\sigma\} \rightarrow X$ is a many-to-one mapping, we call $X$ a macroscopic observable. By fixing the value of $X$, we effectively define what is known as a **macro-state**.

A typical objective in statistical physics is to transition from the probability distribution of micro-states, $P(\{\sigma\})$, to that of macro-states, $P(X)$. What generically happens during this transition is a fundamental aspect that we will explore now,  using coin flipping.

The probability of $X$ is naturally represented as a product of the number $\binom{N}{N_+}$ of possible microstates (aka microscopic configurations) and the probability $p^{N_{+}}q^{N_{-}}$ to observe anyone of the microstates. We thus obtain the binomial distribution
$$
P(X)=P(N_+,N_+)=\underbrace{\frac{N!}{N_{+}! N_{-}!}}_{\equiv e^{S(X)}} \quad \underbrace{p^{N_{+}}q^{N_{-}}}_{\equiv e^{-E(X)}}
$$
$$
P(X)= e^{S(X)}e^{-E(X)}
$$
Here, we introduced $S(X)$ as the log of the microstates $E(X)$ as the log-probability of the microstates. Up to pre-factors, these quantities are **entropy** and **energy** in statistical physics. They always compete with one another ....  


$$
\begin{aligned}
& S=\ln (N !)-\ln \left(N_{+} !\right)-\ln \left(N_{-} !\right)
\end{aligned}
$$

Stirling: $\ln N !=N(\ln N-1)+O(\ln N)$

$$
S \approx-N\left(\frac{1+x}{2} \ln \left(\frac{1+x}{2}\right)+\frac{1-x}{2} \ln \left(\frac{1-x}{2}\right)\right)
$$

Where we introduced the specific magnetization $x=X/N$. 

Notice that, for large $N$, the entropy $S\propto N$ has a very simple, linear dependence on $N$. Macroscopic observables that grow linearly with the system size are called **extensive**. These are in contrast to **intensive** quanitites, which approach a constant in the thermodynamic limit of large systems, for example $x=X/N$ which is bounded between -1 and 1. 



There are more configurations for $x \approx 0$ than $X \approx N$

$$
\begin{aligned}
E(x) & =-\ln \left(p^{N_{+}} q^{N_{-}}\right)=-N_{+} \ln (p)-N_{-} \ln (q) \\
& =-N\left[\frac{1+x}{2} \ln p+\frac{1-x}{2} \ln q\right] \\
& =-\frac{N}{2}\left[\ln (p q)+x \ln \frac{p}{q}\right]
\end{aligned}
$$

"Low energy" higher probab.

$\langle x\rangle$ is set by competition between $S(x)$ and $E(x)$

Taylor expanding $S(x)-E(x)$ to $O\left[(x-\langle x\rangle)^{2}\right]$

$$
P(x) \approx C e^{-N\left[\frac{1}{2} \frac{(x-(x))^{2}}{4 P q}+O\left(\frac{1}{N}\right)\right]}
$$

So, as $N \rightarrow \infty$

Deterministic behavior emerges from $N \rightarrow \infty$ limit.



#### Warm-Up: Calculation of Expectation Value


But first a warm-up: 

Expectation value

$$
\begin{aligned}
\langle x\rangle & =\sum_{\{\sigma\}} P(\{\sigma\}) x(\{\sigma\})= \\
& =\sum_{\{\sigma\}}\left[\prod_{j} P\left(\sigma_{j}\right)\right]\left[\sum_{i} \sigma_{i}\right] \\
& =\sum_{j} \sum_{\sigma_{j}} P\left(\sigma_{j}\right) \cdot \sigma_{j} \\
& =\sum_{j}(p-q)=N(p-q)
\end{aligned}
$$

$\langle X\rangle \propto N$ is "**extensive**".

Also define specific magnetisation $\langle x\rangle \equiv \frac{\langle X\rangle}{N}=p-q$ is "**intensive**". 

Of course, a particular realization will (usually!) not have $x=\langle x\rangle$. 


One measure of spread is variance

$$
\operatorname{var}(x) \equiv\langle\underbrace{(x-\langle x\rangle)^{2}}_{\equiv \Delta x^2}\rangle=\left\langle x^{2}\right\rangle-\langle x\rangle^{2} .
$$

To compute $\left\langle x^{2} \right\rangle$
:


$$
\begin{aligned}
& \left\langle x^{2}\right\rangle=\sum_{\{\sigma\}} P(\{\sigma\}) x^{2}(\{\sigma\}) \\
& =\sum_{\{ \sigma \}} P(\{\sigma\}) \sum_{i, j} \sigma_{i} \cdot \sigma_{j}=\sum_{i, j}\left\langle\sigma_{i} \sigma_{j}\right\rangle \\
& i=j: \sigma_{i} \cdot \sigma_{i}=1 \text {, so }\left\langle\sigma_{i} \cdot \sigma_{i}\right\rangle=1
\end{aligned}
$$

if j: $\left\langle\sigma_{i} \sigma_{j}\right\rangle=\left\langle\sigma_{i}\right\rangle\left\langle\sigma_{i}\right\rangle=(p-q)^{2}$

So $\left\langle x^{2}\right\rangle=N+N(N-1)(p-q)^{2}$
v. $\langle x\rangle^{2}=N^{2}(p-q)^{2}$

$$
\begin{aligned}
\left\langle x^{2}\right\rangle-\langle x\rangle^{2} & =N\left(1-(p-q)^{2}\right) . \\
\operatorname{var}(x) & =4 \mathrm{Npq} .
\end{aligned}
$$

Note: $\quad \Delta x \sim \sqrt{N} 4 \mathrm{pq}$

$$
\langle x\rangle-N(p-q)
$$

so, as $N \rightarrow \infty, \frac{\Delta x}{\langle x\rangle} \rightarrow 0(p \neq q)$

The $\sqrt{N^{\prime}}$ is $N$ scaling is a general consequence of the C.L.T. we provelater.

So for, we have computed

$$
\langle x\rangle,\left\langle x^{2}\right\rangle
$$

but instructive to compute

