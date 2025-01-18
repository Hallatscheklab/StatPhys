Entropy

Previously, $S \equiv \ln [\underbrace{\# \text { of configurations }}_{\Omega}](*)$

Example: given $N_{+}, \Omega\left(N_{+}\right)=\left(\begin{array}{c}N \\ N_{+}\end{array}\right)=\frac{N !}{N_{+} N_{-}}$

$$
\text { or } S\left(N_{+}\right)=N_{+} \ln N_{+} / N+N_{-} \ln N_{-} / N
$$

$(*)$ is appropriate if all configurations are equally likely, which is the case if we fix $N_{+}$

In general/ $N_{+}$is nat fixed but itself a random variable $\rightarrow p_{S}(S) d S=p\left(N_{+}\right) d N_{+} s\left(N_{+}\right)$.

But in the themadyn. limit, we know

$$
\begin{aligned}
& \text { But in the hermann. } \\
& \begin{array}{c}
N_{+} \rightarrow\left\langle N_{+}\right\rangle=p N, N_{-}=\left\langle N_{r}\right\rangle=q N . \\
\Rightarrow S=-N \cdot(p \ln p+q \ln q) .
\end{array}
\end{aligned}
$$

$\Rightarrow$ In thermadyn. limit $(N \rightarrow \infty)$, we can only observe typical" configurations $\left(N_{+}=p N ; N_{-}=q N\right)$; there are $e^{S}$ of them and all of them are equally likely $\left(p^{p^{N}} \cdot q^{q^{N}}\right.$ )

Generalization

Consider a dice whIM faces.

$$
\text { Face } i \longrightarrow p_{i}
$$

Thermodynamic limit, $N \rightarrow \infty ;$

Face i share up exactly Np times.

$$
\begin{aligned}
& =F D^{\prime}=\# \operatorname{con}\left(i g{ }^{\prime}{ }^{\prime}=\frac{N !}{\left(N p_{1}\right) !\left(N p_{2}\right) ! \ldots\left(W p_{n}\right) !}\right. \\
& S=\log _{z}(\Omega)=N[\log (N)-I]-\sum_{i}\left(N p_{i}\right)\left[\log N p_{i}-1\right] \\
& =-N \sum_{i=1} p_{i} \log p_{i} \cdot\left(^{*}\right)
\end{aligned}
$$

In physics, $(t)$ is "Entropy of mixing" Me components. (also closely related to Gibbs entropy).

Information entropy

Shannon realized: \# of configurations given what we know is lack of knowledge about specific microstate.

Ex: - N coin flips and we know Nt.

$\Rightarrow$ microstate is ane of $e^{S\left(N_{+}\right)}$states.
- If we don't know N+N+ is not fixed?

$\Rightarrow e^{S}$ typical microstates, $S=-N \sum_{i} p_{i} \log p_{i}$

![](https://cdn.mathpix.com/cropped/2024_01_19_b6c94b34fcab4495da5bg-3.jpg?height=289&width=1311&top_left_y=1059&top_left_x=715)

Consequences:

Suppose we end up measuring the microblete, Suppose we end up measuring
how many bits do we need to
store this information?

For $N \rightarrow \infty$, simply enumerate only the $e^{S}$ typical microstates, all having came probes. This needs $\log _{2}\left(e^{s}\right)=S \cdot \log _{2}(e)$ bits. (not a proof; but work because of CLT $\rightarrow$ measure concentration.)

To simplify notation Shannon introduced the information entropy

$$
\mathbb{S}(\{p\})=-\left\langle\log p_{i}\right\rangle=-\sum_{i} p_{i} \log p_{i}
$$

for any distribution $p_{i}$.

$\rightarrow$ represents average bits per bits needed to encode a long message of words $i=1 . . M$ drawn from $p$.

Note: $S=\log (M)$ if $p_{i}=$ cont. $=\frac{1}{M} \quad$ "naivecucodiny"
- But $S<\log (M)$ for any non- uniform $p \cdot d$.
- code rate $S$ can be achieved by encoding symbol i by codeword of length $-\log \left(p_{i}\right)$ (problem: discreteness)

$\rightarrow$ compline ns symbols. $n \gg 1$. $I\left[\left\{p_{i}\right\}\right]=\ln _{2} M-S: \begin{aligned} & \text { Information content } \\ & \text { of the } p d f .\end{aligned}$

Estimation:

Suppose we want to estimate a distribution of $X$ and that we have some

partial information, eng. $\langle x\rangle=\sum_{i} p_{i} x_{i}$ or $\operatorname{var}(X)$, but not $\left\{p_{i}\right\}$.

Then: Least biased pod. is the one that maximises $S$ given constraints. $\rightarrow$ May En approad.

Example:
i) $\langle F(x)\rangle=\sum_{i} p_{i} F\left(x_{i}\right)$ given

ii) $\langle 1\rangle=\sum_{i} p_{i}=1$ always to ne.

$=D$ Maximize $S=-\sum_{i} p_{i}$ In $p_{i}$ subbed to constrains $\left.i, i i\right)$

$\Rightarrow$ Use Lagrange multipliers $\alpha, \beta$ and maximize

$$
\begin{aligned}
S^{*}\left(\alpha, \beta,\left\{p_{i}\right\}\right) & =-\sum_{i} p_{i} \ln p_{i}-\alpha\left(\sum_{i} p_{i}-1\right)- \\
& -\beta\left(\sum_{i} p_{i} F\left(x_{i}\right)-f\right)
\end{aligned}
$$

$$
\begin{aligned}
\frac{\delta S^{*}}{\partial p_{i}} & =-\ln p_{i}^{*}-1-\alpha-\beta F\left(x_{i}\right) \\
& \Rightarrow p_{i}^{*}=e^{-\left(1+\alpha+\beta F\left(x_{i}\right)\right.}-\frac{1}{z} e^{-\beta F\left(x_{i}\right)}
\end{aligned}
$$

familiar from Boltzmann distrib.

$$
\left(\beta=\frac{1}{k_{B} T} ; F=\text { Enasy }\right)
$$

$\Rightarrow$ Bettemann = max-ent subiect $x\langle(1)=t$

Nate: this akes nat urau $p$ is $p^{*}$.

Hultiple \}isi\} mang give same $\langle F(x)\rangle$
- cuccons ardd funther constaints/updecte in lidd of extra knouledge.

$$
\rightarrow p_{i} \propto e^{-\beta F_{1}(x)-\gamma F_{2}(x)-\ldots}
$$
- How does His compare to Bayes?

Relative entropy II mutual information

- Suppose $\operatorname{Pr}\left[X=x_{i}\right]=p_{i}$ but we think it's from $q_{i}$ and use correspondingly sized cede words

$$
\begin{array}{r}
\Rightarrow L(N)=-N \sum_{i} p_{i} \log q_{i} \text { and } \\
\frac{L-L_{\text {min }}}{N}=\sum_{i} p_{i} \log \left(\frac{p_{i}}{q_{i}}\right)=D_{K L}(\vec{p} \| \vec{q})
\end{array}
$$

KL (Rullback-Leibler) divergence.

Suppose we obtain samples $\left\{X_{i}\right\}$ and want to decide whetter they are drawn from $\vec{p}$ or $\vec{q}$;

$$
\begin{gathered}
\log \left[\frac{P(\text { samples } \mid \vec{p})}{P(\text { samples } \mid \vec{q})}\right]=\sum_{i} n\left(x_{i}\right) \log 2\left(\frac{p_{i}}{q_{i}}\right) \\
\longrightarrow N \sum_{i} p_{i} \log \left(\frac{p_{i}}{q_{i}}\right)=N D_{k L}(\vec{p} \| \vec{q})
\end{gathered}
$$
$\Rightarrow$ We need $\gtrsim D_{K L}^{-1}(\vec{p} \| \vec{q})$ samples to distinguish between $\vec{p}$ and $\vec{q}$.

Mutual information

$S(X) \cong$ lack of knowledge about $X$.

Suppose we measure $Y$, correlated with $X_{0}$ ¿ By how much does our lack of knowledge?

$$
\begin{gathered}
=\int_{\text {entropy before }}(X)^{S} \begin{array}{l}
S(X \mid Y)= \\
\text { expected } \\
\text { entropy after }
\end{array} \\
=-\sum_{x} P_{X}(x) \log P_{X}(x)+\sum_{Y} P_{Y}(y) \sum_{x} P_{X}(x) \log P(x \mid y) \\
=\sum_{x, y} P(x, y) \log \left[\frac{P(y \mid x)}{P_{x}(x)}\right] \\
=\sum_{x, y} P(x, y) \log \left[\frac{P(x, y)}{P_{x}(x) P_{y}(y)}\right]=J(x ; y)
\end{gathered}
$$

The mutual information appears in baric models of information flow:

![](https://cdn.mathpix.com/cropped/2024_01_19_b6c94b34fcab4495da5bg-9.jpg?height=899&width=2093&top_left_y=297&top_left_x=0)

$\approx$ maximal rate of in formation transmission