#### Entropy

Previously, $S \equiv \ln [\underbrace{\# \text { of configurations }}_{\Omega}](*)$

Example: given $N_{+}, \Omega\left(N_{+}\right)=\left(\begin{array}{c}N \\ N_{+}\end{array}\right)=\frac{N !}{N_{+} N_{-}}$

$$
\text { or } S\left(N_{+}\right)=N_{+} \ln N_{+} / N+N_{-} \ln N_{-} / N
$$

$(*)$ is appropriate if all configurations are equally likely, which is the case if we fix $N_{+}$

In general $N_+$ is not fixed but itself a random variable $\rightarrow P_{S}(S) d S=P\left(N_{+}\right) d N_{+} $.

But in the thermodynamic limit, we know

$$
\begin{aligned}
& \begin{array}{c}
N_{+} \rightarrow\left\langle N_{+}\right\rangle=p N, N_{-}=\left\langle N_{r}\right\rangle=q N . \\
\Rightarrow S=-N \cdot(p \ln p+q \ln q) .
\end{array}
\end{aligned}
$$

$\Rightarrow$ In the thermodynamic limit $(N \rightarrow \infty)$, we can only observe "typical" configurations $\left(N_{+}=p N ; N_{-}=q N\right)$; there are $e^{S}$ of them and all of them are equally likely $P({\sigma_i})=p^{N} \cdot q^{N}$ )

These observations are easily generalized to a dice with M faces. If rolling the dice results in face $i$ with probability $p_{i}$, we expect face $i$ to show up exactly $N p_i$ times in the thermodynamic limit, $N \rightarrow \infty$. The number of typical configurations is therefore

$$
\begin{aligned}
\Omega & \equiv\text{nr. of config's}=\frac{N !}{\left(N p_{1}\right) !\left(N p_{2}\right) ! \ldots\left(N p_{n}\right) !} \\
& S\equiv \log_{2}(\Omega)=N[\log (N)-1]-\sum_{i}\left(N p_{i}\right)\left[\log N p_{i}-1\right] \\
& =-N \sum_{i=1} p_{i} \log_2 p_{i}.\left({*}\right)
\end{aligned}
$$

In physics, $(*)$ arises as the entropy change when $M$ components are mixed together. It is therefore called "entropy of mixing" (also closely related to Gibbs entropy).

#### Information entropy

Shannon realized that the number of possible configurations consistent with our macroscopic constraints can be viewed as a *lack of knowledge* about the current microstate.

Examples: 

- Suppose we flip coin $N$ times and we know $N_+$. Then, the actual microstate is one of $e^{S\left(N_{+}\right)}$ micro-states.
- If we don't know $N_+$, respectively $N_+$ is not fixed? $\Rightarrow e^{S}$ typical microstates, $S=-N \sum_{i} p_{i} \log p_{i}$. For a coin: $S=-N (p \log p +q \log q)$.


##### Consequences:

Suppose we end up measuring the micro-state, how many bits do we need to store this information?

For $N \rightarrow \infty$, simply enumerate only the $e^{S}$ typical microstates, all having came probabilities. This needs $\log _{2}\left(e^{s}\right)=S \cdot \log _{2}(e)$ bits. (of course, this is not a proof, but it works because of CLT induced measure concentration.)

To simplify notation Shannon introduced the information entropy, which for any probability distribution $p_{i}$, is defined as

$$
s(\{p\})=-\left\langle\log p_{i}\right\rangle=-\sum_{i} p_{i} \log p_{i} \;.
$$

$s(\{p\})$ represents the average bits per word needed to encode a long message of words $i=1 \ldots M$ drawn form $p$.

Note: 
- $s=\log (M)$ if $p_{i}=$ cont. $=\frac{1}{M} \quad$ "naive encoding"
- But $s<\log (M)$ for any non-uniform probability distribution.
- $I\left[\left\{p_{i}\right\}\right]=\log_{2} (M)-S$ measures information content of the pdf.

#### Estimation:

Suppose we want to estimate a distribution of $X$, about which we have some partial information, e.g. we know the value of $\langle X\rangle=\sum_{i} p_{i} X_{i}$ or $\operatorname{var}(X)$, but not $\left\{p_{i}\right\}$.

Then: Least biased probability distribution.is the one that maximises $s$ given constraints. This is called the MaxEnt approach.

Example: 

Find MaxEnt distribution under the constraint of a given fixed calue $\phi$ of $\langle F(x)\rangle=\sum_{i} p_{i} F\left(x_{i}\right)$. We always have to ensure the constraint that the probability distribution sums up to one, $\langle 1\rangle=\sum_{i} p_{i}=1$ always to ne.

To maximize the entropy $s=-\sum_{i} p_{i} \log p_{i}$ subject to both constraint, we use two Lagrange multipliers $\alpha, \beta$ and maximize

$$
\begin{aligned}
S^{*}\left(\alpha, \beta,\left\{p_{i}\right\}\right) & =-\sum_{i} p_{i} \ln p_{i}-\alpha\left(\sum_{i} p_{i}-1\right)- \\
& -\beta\left(\sum_{i} p_{i} F\left(x_{i}\right)-f\right)
\end{aligned}
$$

$$
\begin{aligned}
\frac{\delta S^{*}}{\partial p_{i}} & =-\ln p_{i}^{*}-1-\alpha-\beta F\left(x_{i}\right) \\
& \Rightarrow p_{i}^{*}=e^{-\left(1+\alpha+\beta F\left(x_{i}\right)\right.}=\frac{1}{Z} e^{-\beta F\left(x_{i}\right)}\;
\end{aligned}
$$

which is familiar from the Boltzmann distrib.

$$
\left(\beta=\frac{1}{k_{B} T} ; F=\text { Enasy }\right)
$$

$\Rightarrow$ Boltzmann = Max-Ent subject to $\langle H\rangle=E$.

Note: 
- This does not mean $p$ **is** $p^{*}$. Multiple $\{p_i\}$ may give the same $\langle F(x)\rangle$
- One can add further constaints and update in light of extra knouledge.

$$
\rightarrow p_{i} \propto e^{-\beta F_{1}(x)-\gamma F_{2}(x)-\ldots}
$$
- How does this compare to Bayes?
