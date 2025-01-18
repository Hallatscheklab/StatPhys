
### Entropy + Information.

In the previous discussion we defined

$$
\begin{aligned}
e^{S} & =\# \text { of configurations }=\Omega \\
S & =\ln \Omega
\end{aligned}
$$

This is appropriate when all configurations are equally likely, $p_{i}=\frac{1}{\Omega}$.

More generally, we define Shannon Entropy

$$
\begin{aligned}
& S(\{p\}) \equiv-\sum_{i} p_{i} \ln p_{i}=-\langle\ln p_{i}\rangle \\
& \left(\text{"nats"}; \quad \ln n \rightarrow \log 2\quad  \text{"bits"}\right)
\end{aligned}
$$

$p_{i}=\frac{1}{\Omega}$ is a special case however.

Where does this come from?

Shannon gave an operational meaning to $S$ in terms of "information" and the resources required to communicate an ensemble of messages drawn from $p_i$. Note if $p_{i}=\frac{1}{\Omega}=\frac{1}{2^{N}}$,

$$
S=\log _{2}\left(2^{N}\right)=N .
$$

Here $S$ is obviously the number of bits required to encode the message.

But suppose instead we have a set of messages $\{i\}=\Omega$ which occur with probability pi. You can think of $\Omega$ as spanning 8-byte intervals of text, for example, with $p_{i} \neq 2^{-64}$ because some character combinations are more frequent

We then send a long sequence of $M_{i} \in \Omega$ over a (lossless) digital channel, If you allow for encoding of the messages, what is the minimal bit rate required per message?

$$
\left\{M_{1}, M_{2}, M_{3}, \cdots\right\}
$$

![](https://cdn.mathpix.com/cropped/2024_01_16_964940924692a65476a3g-10.jpg?height=359&width=572&top_left_y=1475&top_left_x=253)

encode

Shannon proved it is $S\left(p_{i}\right) \leq \log _{2}(\mid \Omega)$

Heuristic arguement following Kardar

In the limit of many (N) messages, we expect message "i" will be communicated

$$
N_{i}=N \cdot p_{i} \text { times. Define a "typical" }
$$

$\left\{M_{1}, M_{2}, \cdots\right\}$ to be one which satisfies this exactly. There are still many of them because of the orderings:

$$
\begin{aligned}
g & \equiv\left(\begin{array}{l}
N \\
N_{1}
\end{array}\right) \cdot\left(\begin{array}{c}
N-N_{1} \\
N_{2}
\end{array}\right) \cdot\left(\begin{array}{c}
N-N_{1}-N_{2} \\
N_{3}
\end{array}\right) \cdots \\
& =\frac{(N !)^{N}}{\left(N_{1} !\right)\left(N_{2} !\right)\left(N_{3} !\right) \cdots}
\end{aligned}
$$

Now $\operatorname{lng}=N \ln (N !)-\sum \ln \left(N_{i} !\right)$

$$
\begin{aligned}
& \approx N\left(N \ln N-N-\sum N_{i} \ln N_{i}-N_{i}\right) \\
& =N\left(N \ln N-N \sum p_{i} \ln \left(p_{i} N\right)\right) \\
& =-N S\left(p_{i}\right)
\end{aligned}
$$

So if we simply enumerate only the g "typical" messages we achieve the desired rate, of course this isn't proof; need to analyze deviations from typicality. I4 works because of C.L.T./ measure concentration, as we saw for $\Delta x$.

Max - en.

Often in life we encounter situations where we know some thing, but not everything

For example, suppose we know some average property " $x$ " of distribution,

$$
\bar{x}=\sum_{i} p_{i} x(i) \text {, but not }\left\{p_{i}\right\} \text {. }
$$

A humble guess for $p_{i}$ is to maximize $S\left(p_{i}\right)$ subject to $\bar{x}$ (and normalization) Without $\bar{x}, \quad i+$ is easy to see $p_{i}=\frac{1}{\Omega}$ maximizes S. With $\bar{x}$, "objective" is

$$
\begin{aligned}
S^{*} & =-\sum p_{i} \ln p_{i}-\lambda_{0}\left(\sum p_{i}-1\right)-\lambda_{1}\left(\sum p_{i} x_{i}-\bar{x}\right) \\
\frac{\delta s^{*}}{\delta p_{i}} & =-\ln p_{i}-1-\lambda_{0}-\lambda_{1} x_{i} \\
& \rightarrow p_{i}^{*}=e^{-\left(1+\lambda_{0}+\lambda_{1} x_{i}\right)}=\frac{1}{z} e^{-\lambda_{1} x_{i}}
\end{aligned}
$$

We then adjust $\lambda_{0}, \lambda_{1}$ so as to satisfy constraints. This form is of course familiar from $p_{i}=\frac{1}{z} e^{-\beta E_{i}}$ : Boltzmann $=$ max $-e n+$ subject to $\langle H\rangle=E$.

Note that this does not mean \{pis is $p_{i}^{*}$. Multiple $\left\{p_{i}\right\}$ may give same $\langle x\rangle$ (see Arovas). In principle one can continue give more observables: $\langle x\rangle,\langle y\rangle,\langle z\rangle \ldots$

$$
\begin{gathered}
\hookrightarrow \quad p_{i} \propto e^{-\lambda_{1} x_{i}-\lambda_{2} Y_{i}} \ldots \\
x=\sum_{i} \sigma_{i}
\end{gathered}
$$

For example, perhaps $\gamma=\sum_{i} \sigma_{i} \cdot \sigma_{i+1}$

$$
\rho_{i} \sim e^{-\lambda \cdot \sum_{1} \sigma_{i}-\lambda_{2} \sum_{i} \sigma_{i} \cdot \sigma_{i+1}}
$$

Interesting question: Max-ent and Bayes Theorem are both ways of updating a model as additional info comes in. What is the relation between them?