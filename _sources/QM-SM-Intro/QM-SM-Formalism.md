## Formalism of quantum statistical mechanics

(Also see Kardar 6.4 (Quantum microstates) and Kardar 6.5 (Quantum macrostates))

Thus far, we dove into quantum stat-mech using the replacement recepie

$$
Z=\sum_{n} e^{-\beta E_{n}}, \hat{H}\left|E_{n}\right\rangle=E_{n}\left|E_{n}\right\rangle
$$

This is correct, but its worth developing the general formalism.

Classically, we have a distribution over microstates " $\mu$ ", $p(\mu)$, with $\langle O\rangle=\sum_{\mu} p(\mu) O(\mu)$

The distribution $p(\mu)$ depends on ensemble,

$$
p(\mu)=\frac{1}{\Omega} \delta(H(\mu)-E), \qquad p(\mu)=\frac{1}{z} e^{-\beta H(\mu)} \text {, etc. }
$$

The quantum analog is the "density matrix"

$$
\begin{aligned}
& \hat{\rho}=\sum_{\alpha} p_{\alpha}|\alpha\rangle\langle\alpha|, \\
& \langle\hat{O}\rangle=\sum_{\alpha} p_{\alpha}\langle a|\hat{\theta}| \alpha\rangle \\
& \operatorname{Tr}(\hat{j})=1 \quad \sum_{\alpha} \rho_{\alpha}=1 \\
& =\operatorname{Tr}(\hat{\rho} \hat{O})
\end{aligned}
$$

The various eq. ensembles are then taken diagonal in $\hat{H}$ :

$$
\begin{aligned}
& \left.\hat{\rho}_{E}=\frac{1}{\Omega} \sum_{n} \delta\left(E_{n}-E\right)\left|E_{n}\right\rangle<E_{n} \right\rvert\, \\
& \hat{\rho}_{\beta}=\frac{1}{Z} \sum_{n} e^{-\beta E_{n}}\left|E_{n}\right\rangle\left\langle E_{n}\right| \\
& \hat{\rho}_{\beta, \mu}=\frac{1}{Q} \sum_{n} e^{-\beta\left(E_{n}-\mu N_{n}\right)}\left|E_{n}\right\rangle\left\langle E_{n}\right) \\
& \quad \tau \quad[\hat{H}, \hat{N}]=0
\end{aligned}
$$

N-conserved



QH analog of a distribution over mierostates is the "density matrix":

Consider a system being in QH micratate $\left|\psi_{\alpha}\right\rangle$ with probability $p_{\alpha}$. This can be summarized by the density matrix

$$
\hat{\rho} \equiv \sum_{\alpha} \rho_{\alpha}\left|p_{\alpha}\right\rangle\left\langle\psi_{\alpha}\right|, \quad \sum \rho_{\alpha}=1=\operatorname{Tr} (\hat{\rho})
$$

Expectation value

$$
\begin{aligned}
& \langle\hat{O}\rangle_{\hat{\rho}}=\sum_{\alpha} p_{\alpha}\left\langle\psi_{\alpha}|\hat{O}| \psi_{\alpha}\right\rangle \stackrel{(*)}{=} \operatorname{Tr}(\hat{O} \hat{\rho})
\end{aligned}
$$

To see (*), note that

$$
\operatorname{Tr}(\hat{O} \hat{\rho})=\sum_{\alpha_{1}}\langle\alpha|\hat{O} \hat{\rho}| \alpha)=\sum_{\alpha \beta}\langle\alpha|\hat{O}| \beta\rangle \underbrace{\langle\beta|\hat{\rho}| \alpha\rangle}_{=p_{\alpha}\delta_{\alpha, \beta}}
& =\sum_{\alpha} p_{\alpha}\langle\alpha|\hat{O}| \alpha\rangle
$$

$\hat{\rho}$ can be expanded in any orthogonal basis

$$
\hat{\rho}=\sum_{i, j} \rho_{i, j}|i\rangle\langle j| \;, \qquad \rho_{i j}=\langle i|\hat{\rho}| j\rangle
$$

Note that not all $\rho_{i j}$ are valid density matrices.
Requirements:

(1) $\operatorname{Tr}(\hat{\rho})=1$

(2) $\hat{\rho}^{+}=\sum_{\alpha} p_{\alpha}^{*}\left(\left|\psi_{\alpha}\right\rangle\left\langle\psi_{\alpha}\right|\right)^{*}=\hat{\rho} $. (Hermitian) 

(3) For any $|v\rangle$,

$$
\begin{gathered}
\langle v|\hat{\rho}| v\rangle=\sum_{\alpha} p_{\alpha}\left\langle v \mid \psi_{\alpha}\right\rangle\left\langle\psi_{\alpha} \mid v\right\rangle \\
=\sum_{\alpha} p_{\alpha}\left|\left\langle v \mid \psi_{\alpha}\right\rangle\right|^{2} \geqslant 0
\end{gathered}
$$

I.e. $\hat{\rho}$ is "positive semi-definite"



In a general basis, the density matrix typically has the following structure: 

![](https://cdn.mathpix.com/cropped/2024_04_17_46da8704ff73657c50ccg-04.jpg?height=853&width=1816&top_left_y=1854&top_left_x=139)

By positive semi-definiteness and the definition of the d.m.s., we have 

$$
0 \leq \rho_{i i} \leq 1, \sum \rho_{i i}=1 .
$$

So the "populations"look like probabilities. However, this is basis dependent!

For example, for a single spin, we can convert matrix from the up-down basis to the left- right basis, we obtain

$$
\frac{1}{2}\left[\begin{array}{ll}
|\uparrow\rangle & |\downarrow\rangle \\
\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2}
\end{array}\right] \leftrightarrow\left[\begin{array}{cc}
|\rightarrow\rangle & |\leftarrow\rangle \\
1 & 0 \\
c & 0
\end{array}\right]
$$

There is always a special basis in which coherence part vanishes, e.g.

$$
\hat{\rho}=\operatorname{diag}\left(p_{i}\right) .
$$

We will mostly assume that this basis is time -independent, so we can heuristically work with population $p_{i}$.

$$
\operatorname{Tr}[A, B]=A_{i j} B_{j i}-B_{i j} \cdot A_{j i}=0 \text {. finite ! } \quad \mid \quad \underbrace{}_{-i \hbar}\langle\psi|=\langle\psi| \hat{H}
$$

### Dynamics:

Exercise: Show that the Schrödinger equation 

$$i\hbar \partial_{t}|\varphi\rangle=\hat{H}|\psi\rangle$$

implies the von Neumann equation

$$i \hbar \partial_{t} \hat{\rho}=[\hat{H}, \hat{\rho}]$$


So

$$
i\hbar \partial_{t} \sum_{i} \rho_{i, i}=i \hbar \partial_{t}(\operatorname{Tr}(\hat{\rho}))=\operatorname{Tr}([\hat{H}, \hat{\rho}])=0 \text {. }
$$

(since $\operatorname{Tr}([A, B])=0$ )

Thus, $\operatorname{Tr}(\hat{\rho})=1$ is respected under unitarian time evolution.

For time-independent Hamiltonian, we have $\psi(t)=\hat{U}(t) \psi(0)$ with $
\hat{U}=e^{-i \hat{H} t(\hbar} $ and so 


$$
\hat{\rho}(t)=\hat{U}(t) \hat{\rho}_{0} \hat{U}^{+} (t)
$$

( For a unitarian evolution in a open systan, one obtaines the so-called Lindblad quation which has aspects of a Masters equation)



### Density matrices in equilbrium.

The various equilibrium ensembles are then taken to be diagonal in the $\hat{H}$ basis:

$$
\begin{aligned}
& \hat{\rho}_{E}=\frac{1}{\Omega} \sum_{n} \delta\left(E_{n}-E\right)\left|E_{n}\right\rangle\left\langle E_{n}\right| \\
& \hat{\rho}_{\beta}=\frac{1}{Z} \sum_{n} e^{-\beta E_{n}}\left|E_{n}\right\rangle\left\langle E_{n}\right| \\
& \hat{\rho}_{\beta, \mu}=\frac{1}{Q} \sum_{n} e^{-\beta\left(E_{n}-\mu N_{n}\right)} \left|E_{n}\right\rangle\left\langle E_{n}\right\rangle
\end{aligned}
$$

(Note that $[\hat{H}, \hat{N}]=0$). The density matrices can be conveniently summarized as operator expressions, eg.

$$
\hat{\rho}_{\beta}=\frac{1}{Z} e^{-\beta \hat{H}}, \quad Z=\operatorname{Tr}\left(e^{-\beta \hat{H}}\right)
$$

This points to an interesting observation: with

$$
\beta=\frac{1}{K_{B} T} \rightarrow i t / A, \quad e^{-\beta \hat{H}} \rightarrow e^{-i t \hat{H} / h}=\text { Time Evolution! }
$$

Thus the thermal density matrix is formally equivalent to "imaginary time evolution",

$$
\hat{\rho}_{\beta}=\frac{1}{Z} \hat{U}(t=-i \beta)
$$

This mathematical coincidence (??) gives rise to a number of technical tricks (Wick rotation | Euclidean path integral) important to quantum field and many body theory.



For an ensemble like $\hat{H}-\mu \hat{N}$, where $[\hat{H}, \hat{N}]=0$, it is easy to show that 

$$
\begin{aligned}
& \langle E\rangle=\langle\hat{H}\rangle=\frac{1}{Z} \partial_{(-\beta)} \operatorname{Tr}\left(e^{-\beta \hat{H}}\right) \\
& =\frac{1}{Z} \partial_{-\beta} Z=-\partial_{\beta} \ln (Z)
\end{aligned}
$$

Note that $Z$ is just a number (as in classical stat mech) in contrast to $\hat{H}$  and  $\hat{\rho}$.

So, fortunately, all our thermo results like $F=-\frac{1}{\beta} \ln (Z), \mu=-\frac{\partial F}{\partial N}$, etc and Maxwell's relations / thermodynamic inequalities are unchanged by quantum effects. It's just harder to compute $Z$ because we need eigenspectrom $\hat{H} \longrightarrow E_{n}$, which is itself hard!

## The Many-Body Hilbert space

The sum $\sum_{n} e^{-\beta E_{n}}\left|E_{n}\right\rangle\left\langle E_{n}\right|$ runs over the Hilbert space $\left|E_{n}\right\rangle \in \mathcal{H}$, so its worth understanding the structure of $\mathcal{H}$ in a many-body system. 3 common cases:

(1) Spins / quits $|\uparrow \uparrow \downarrow \uparrow \cdots\rangle$

(2) Bosons $\left.\psi\left(x_{1}, x_{2}\right)=\psi\left(x_{2}, x_{1}\right)\right\}$ 1st/2nd

(3) Fermions $\left.\psi\left(x_{1}, x_{2}\right)=-\psi\left(x_{2}, x_{1}\right)\right\}$ quantization

We start with (1) amd some rudiments of quantum information- (2, 3) are covered in future lectures.

#### Spins 1 "qu-dits"

The Hilbert space of $s=1 / 2$ spin is

$$
\begin{aligned}
& H=\operatorname{span}\left(\{|\uparrow\rangle,|\downarrow\rangle \})=\mathbb{C}^{2}\right. \\
& |\psi\rangle=\psi_{\tau}|\lambda\rangle+\psi_{+}|\downarrow\rangle-\left(\begin{array}{l}
\psi_{\uparrow} \\
\psi_{\downarrow}
\end{array}\right)
\end{aligned}
$$

In quant-info, call it "qubit", $\{|0\rangle,|1\rangle\}$

Operators spanned by $2 \times 2$ Paulies $\sigma^{x / y / z}$, often denoted $X, Y, Z$ in quant-info.

For spin S,

$$
\begin{aligned}
\mathcal{H}= & \operatorname{span}\left(\{|m\rangle \}\right)=\mathbb{C}^{2 S+1} \\
& -S \leq m \leq S
\end{aligned}
$$

or "qudit", $d=2s+1$.

#### What about 2 spins? 

Now, 

$$H^{(2)}=\operatorname{span}(\{|\uparrow \uparrow\rangle,|\uparrow \downarrow\rangle,|\downarrow \uparrow\rangle,|\downarrow \downarrow\rangle\})\\
=\mathbb{C}^{2} \otimes \mathbb{C}^{2}=\mathbb{C}^{2*2=4}
$$

The 2-spin $\mathcal{H}^{(2)}=\mathcal{H}^{(1)} \otimes \mathcal{H}^{(1)}$ is a "tensor product",

$$
|\psi\rangle=\sum_{\sigma_{1}, \sigma_{2}=\tau / \downarrow} \psi_{\sigma_{1}} \sigma_{2}\left|\sigma_{1} \sigma_{2}\right\rangle=\left(\begin{array}{l}
\psi_{\uparrow \pi} \\
\psi_{\tau \downarrow} \\
\psi_{\downarrow \pi} \\
\psi_{\downarrow \downarrow}
\end{array}\right)
$$

We can extend to $N$-spins:

$$
\begin{aligned}
\mathcal{H}^{(N)} & =3 \operatorname{span}\left(\left\{| \sigma_{1}, \sigma_{2}, \cdots, \sigma_{N}>\right\}\right) \\
& =\mathbb{C}^{2} \otimes \mathbb{C}^{2} \otimes \mathbb{C}^{2} \otimes \cdots \\
& =\mathbb{C}^{2^{N}}
\end{aligned}
$$

Key: dimension of $\mathcal{H}^{(N)}=2^{N}$, NOT $2 * N$

So to encode a generic microstate

$$
|\psi\rangle=\sum_{\sigma_{1}, \sigma_{2} \ldots \sigma_{N}} \psi_{\sigma_{1}, \sigma_{2},\cdots} \mid\left\{\sigma\}\right\rangle
$$

we need $2^{N}$ complex numbers $\psi_{\{\sigma\}}$

Exponentially large in N!!

In contrast, a microstate of the classical Ising model, $\mu=\sigma_{1} \sigma_{2} \cdots \sigma_{N}$, requires $N$ classical bits. So your Monte-Carlo simulation of $20 \times 20=400$ spins needed $<1$ K B RAM. If we store quantum $\psi_{\{\sigma\}}$ using 128-bit precision floating point, need

$$
\begin{aligned}
128 \cdot 2^{400} & =3 \cdot 10^{122} \mathrm{bits} \\
& =3 \cdot 10^{112} \mathrm{~GB}
\end{aligned}
$$

So... simulating quantum w/ classical hard!

#### Many body operators

The tensor product structure also extends to operators:

$$
\begin{array}{r}
\hat{Z}_{i}\left|\sigma_{1}, \sigma_{2}, \cdots \sigma_{N}\right\rangle \equiv \sigma_{i}\left|\sigma_{1}, \cdots \sigma_{N}\right\rangle \\
\left(\hat{Z}_{i} \cdot \hat{Z}_{j}\right)\left|\sigma_{1}, \cdots, \sigma_{N}\right\rangle \equiv \sigma_{i} \cdot \sigma_{j}\left|\sigma_{1}, \cdots, \sigma_{N}\right\rangle
\end{array}
$$

Since $\hat{X}=\left[\begin{array}{ll}0 & 1 \\ 1 & 0\end{array}\right]$, with notation $\sigma\in\{1 ,-1\}$,

$$
\begin{aligned}
& \hat{X}|\sigma\rangle=|-\sigma\rangle \quad \text{("Bitflip")} \\
& \hat{X}_{1}\left|\sigma_{1}, \sigma_{2}, \cdots \sigma_{N}\right\rangle=\left|-\sigma_{1}, \sigma_{2}, \cdots\right\rangle
\end{aligned}
$$

The $\hat{Z}_{i}, \hat{X}_{i}$ are $2^{N} \times 2^{N}$ matrices:

Ex: for $N=2, \quad$ Hilbert space$=\{|1,1\rangle, \mid 1,-1\rangle,|-1,1\rangle,|-1,-1\rangle\}$

$$
\begin{array}{ll}
\hat{Z}_{1}=\left[\begin{array}{llll}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{array}\right] & \hat{Z}_{2}=\left[\begin{array}{llll}
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1
\end{array}\right] \\ \\
\hat{X}_{1}=\left[\begin{array}{llll}
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0
\end{array}\right] & \hat{X}_{2}=\left[\begin{array}{llll}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0
\end{array}\right]
\end{array}
$$

Generic $2^{N} \times 2^{N}$ operators can be built up by adding / multiplying $\hat{Z}_{i}, \hat{X}_{i}$.

Ex: Transverse - Field Ising model

$$
\begin{aligned}
& \hat{H}_{T F I} \sum_{i=1}^{N}\left[-J \hat{Z}_{i} \cdot \hat{Z}_{i+1}-g \hat{X}_{i}\right] \\
& \hat{m}=\frac{1}{N} \sum_{i} \hat{Z}_{i} \quad \text { (magnetization) }
\end{aligned}
$$

Typical question: 

Given $\hat{\rho}_{\beta}=e^{-\beta \hat{H} T F I} / Z$, what's $\operatorname{Tr}\left(\hat{m} \hat{\rho}_{\beta}\right)$ ?

Not easy, because to obtain $\hat{\rho}_\beta$ we need to diagonalize $2^{N} \times 2^{N}$ matrix $\hat{H}_{T F I}$ ! The biggest computations of this form can handle $N \sim 20$ or so (see  discussions of "quantum supremacy")

#### Reduced Density matrices / Entanglement

In classical probability theory, a distribution over two random variables, $\mu=\{\mu_{1}, \mu_{2}\}, \quad p\left(\mu_{1}, \mu_{2}\right)$, allows us to define a marginal distribution over
one:

$$
p_{1}\left(\mu_{1}\right) \equiv \sum_{\mu_{2}} p\left(\mu_{1}, \mu_{2}\right)
$$

If we only care about observables $O_{1}\left(\mu_{1}\right) \quad\left(\right.$ rather than $\left.O\left(\mu_{1}, \mu_{2}\right)\right)$

$$
\begin{aligned}
\left\langle O_{1}\right\rangle & =\sum_{\mu_{1}, \mu_{2}} O_{1}\left(\mu_{1}\right) p\left(\mu_{1}, \mu_{2}\right) \\
& =\sum_{\mu_{1}} O_{1}\left(\mu_{1}\right) p\left(\mu_{1}\right)
\end{aligned}
$$

So, the marginal $p_{1}$ is sufficient to recover $\left\langle O_{1}\right\rangle$.
Note that, in general,

$$
\rho\left(\mu_{1}, \mu_{2}\right) \neq \rho_{1}\left(\mu_{1}\right) \cdot \rho_{2}\left(\mu_{2}\right)
$$

For example, 

$$
\rho(\{\sigma \})=\frac{1}{Z} e^{-\beta \sum_{i} \sigma_{i} \cdot \sigma_{i+1}} 
$$

does not factorize.

In contrast, for 

$$
\rho(\sigma)=\frac{1}{Z} e^{-\beta \sum_{i} h \sigma_{i}}\\
=\frac{1}{Z} \prod_{i} e^{-\beta h \sigma_{i}} \\
=\rho_{1}\left(\sigma_{1}\right) \rho_{2}\left(\sigma_{2}\right) \ldots
$$

$p\left(\mu_{1}, \mu_{2}\right) \neq p_{1}\left(\mu_{1}\right) \cdot p_{2}\left(\mu_{2}\right)$ implies $\mu_{1}, \mu_{2}$ are "correlated", and $\left\langle O_{1} O_{2}\right\rangle \neq\left\langle O_{1}\right\rangle\left\langle O_{2}\right\rangle$.

For a quantum system on $\mathcal{H}=\mathcal{H}_{1} \bigotimes\mathcal{H}_{2}$, there is an equivalent notion of marginal: the "Reduced Density Matrix"

Let $\operatorname{span}\left\{\left|i_{1}\right\rangle\right\}=H_{1}=\mathbb{C}^{D_{1}}$, $i_{1} =1, \cdots, D_{1}$ and $\operatorname{span}\left(\left\{\left|i_{2}\right\rangle\right\}\right)=H_{2}=\mathbb{C}^{D_{2}}$, $i_{2} =1, \cdots, D_{2}$
 
Then $\quad \mathcal{H}=\operatorname{span}\left(\left\{\left|i_{1}, i_{2}\right\rangle\right\}\right)=\mathbb{C}^{D_{1} \cdot D_{2}}$

A generic state is

$$
|\psi\rangle=\sum_{i_{1}, i_{2}} \psi_{i_{1}, i_{2}}\left|i_{1}, i_{2}\right\rangle \\
\hat{\rho}=\sum \rho_{\alpha} |\psi_{\alpha}\rangle\langle\psi_{\alpha}|=\sum \rho_{i_{1}, i_{2} ; j_{1}, j_{2}}| i_{1}, i_{2}\rangle\langle j_{1}, j_{2}|
$$

Consider an observable $\hat{O}=\hat{O} \otimes \hat{\mathbb{I}}$, which  only makes a measurement on subsystem ,'

$$
\hat{O}_{1}=\sum_{i_{1}, i_{2}, j_{1}} \hat{O}_{i_{1}, j_1}\left|i_{1}, i_{2}\right\rangle \left\langle j_{1}, i_{2}\right|
$$

For example, if we have 2 spins, $\mathcal{H}=\mathbb{C}^{2} \otimes C^{2}$, we might physically separate them to different regions of the lab, and then use Stern-Gerlach to measure only $\operatorname{spin} 1: \hat{G}=\hat{Z}_{1} \otimes \hat{\mathbb{1}}_{2}$

We have 

$$
\left\langle\hat{O}\right\rangle=\operatorname{Tr}\left(\hat{O} \hat{\rho}\right)\\
 =\sum O_{i_{1}, j_{1}}\left\langle j_{1}, i_{2}|\hat{\rho}| i_{1}, i_{2}\right\rangle \\
 =\sum_{i_{1}, i_{2}, j_{1}} O_{i_{1}, j_{1}} \rho_{j_{1}, i_{2} ; i_{1}, i_{2}}
$$

If we define the $D_{1} \times D_{1}$ matrix

$$
\rho_{j_{1} ; i_{1}}^{(1)}\equiv\sum_{i_{2}} \rho_{j, i_{2} ; i_{1}, i_{2}}
$$

and the corresponding operator

$$
\hat{\rho}^{(1)}=\sum \rho_{i_{1}, j,}^{(1)}\left|i_{1}\right\rangle\left\langle j_{1}\right| 
$$

we obtain

$$ \left\langle\hat{O}_{1}\right\rangle=\operatorname{Tr}\left(\hat{O}_{1} \hat{\rho}^{(1)}\right)
$$

So, the "partial trace" $\hat{\rho}^{(1)}=\operatorname{Tr}_{2}(\hat{\rho})$ is the quantum analog of marginal; called "reduced density matrix" for subsystem 1.

Ex: EPR state $|E P R\rangle=\frac{1}{\sqrt{2}}(|\uparrow \downarrow\rangle+|\downarrow \uparrow\rangle)$

$$
\begin{aligned}
\hat{\rho} & =|E P R\rangle\langle E P R| \quad \text { "Pure state" } \\
& =\frac{1}{2}(|\uparrow \downarrow \rangle+|\downarrow \uparrow\rangle)(|\uparrow \downarrow \rangle+|\downarrow \uparrow\rangle) \\
& =\frac{1}{2}\left[\begin{array}{llll}
0 & 0 & 0 & 0 \\
0 & 1 & 1 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 0
\end{array}\right] 
\end{aligned}
$$

So

$$
\\
\hat{\rho}_{1} & =\left[\begin{array}{cc}
\frac{1}{2} & 0 \\
0 & \frac{1}{2}
\end{array}\right]
$$

Note $\hat{\rho}_{1}$ is mixed even though $\hat{\rho}$ is pure! So

$$
\left\langle X_{1}\right\rangle=\left\langle Y_{1}\right\rangle=\left\langle Z_{1}\right\rangle=0  
$$

even though $\left\langle Z_{1} Z_{2}\right\rangle=-1$.

The two EPR spins are correlated even though the system (as a whole) is in a definite (pure) state.

#### Entropy: 

$$\quad S=-\operatorname{Tr}(\hat{\rho} \ln (\hat{\rho}))$$

For $\hat{\rho}=\sum p_{\alpha}|\alpha\rangle\langle\alpha|, \quad\langle\alpha \mid \beta\rangle=\delta_{\alpha \beta}$.

$$
S=-\sum_\alpha p_{\alpha} \ln p_{\alpha}
$$

We call a state $\hat{\rho}$ "pure" if

$$
S[\hat{\rho}]=0 \Longleftrightarrow \hat{\rho}=|\psi\rangle\langle\psi|
$$

Otherwise, $\quad S[\hat{\rho}]>0 \Rightarrow \hat{\rho}$ "mixed

#### Entanglement: 
Let $\mathcal{H}=\mathcal{H}_{1} \otimes \mathcal{H}_{2}$, and $\quad|\psi\rangle \in \mathcal{H}$.

Clearly, $\hat{\rho}=|\psi\rangle\langle\psi|$ has $S[\hat{\rho}]=0$. 

However, the RDM $\hat{\rho}_{1}=\operatorname{Tr}_{2}(\hat{\rho})$ can be mixed. We call $S\left[\hat{\rho}_{1}\right]$ the "entanglement entropy".

Even though, the system is in a single fixed pure state $|\psi\rangle$, measurements between $1$ and $2$ are correlated:

$$
\left\langle O_{1} O_{2}\right\rangle \neq\left\langle O_{1}\right\rangle\left\langle O_{2}\right\rangle
$$

Our earlier example was $|\psi\rangle=|E P R\rangle$, where $\hat{\rho}_{1}=\text{diag}\left[\begin{array}{ll}1 / 2 & 1 / 2\end{array}\right] \rightarrow S=\ln (2)$ : one bit of entanglement.


```{note}
Check out recent colloquium by Matthew Fisher on phase transitions in entanglement entropy.
```


#### Measures of quantum information

Many but not all results of classical information theory transfer to the quantum case.

For $\quad H_{A} \otimes \mathcal{H}_{B}=\mathcal{H}_{A B}, \quad \hat{\rho}_{A}=\operatorname{Tr}_{B}\left(\hat{\rho}_{A B}\right)$,
one defines the "mutual information", which is a measure of total correlation

$$
I(A: B)=S\left[\hat{\rho}_{A}\right]+S\left[\hat{\rho}_{B}\right]-S\left[\hat{\rho}_{A B}\right] \geq 0
$$


$$
I(A: B)=0 \quad \Longleftrightarrow \hat{\rho}_{A B}=\hat{\rho}_{a} \otimes \hat{\rho}_{B}
$$


Important property:

$$
\begin{aligned}
& I(A: B C) \geq I(A: B) \\
& I(A: B C)-I(A: B)=S_{A}+S_{B C}-S_{A B C} \\
& -S_{A}-S_{B}+S_{A B} \\
& =S A B+S_{B C}-S_{A B C}-S_{B} \geq 0
\end{aligned}
$$

"[Strong subadditivity of quantum information](https://en.wikipedia.org/wiki/Strong_subadditivity_of_quantum_entropy)" - not easy to prove.

