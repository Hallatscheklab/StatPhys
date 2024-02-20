## Variational Method

Recall that in quantum mechanics, the ground state can be defined variationally as

$$
E_{0}=\min _{\psi} \frac{\langle\psi|\hat{H}| \psi\rangle}{\langle\psi \mid \psi\rangle}
$$

To obtain exact result, the minumum is taken over full Hilbert space, but we can obtain upper bound on ED by a fewparameter anstatz $\quad\left|g_{1,}, g_{2}, \cdots\right\rangle,\left(e_{\text {.g. }, ~}|g\rangle=e^{-\frac{1}{2} g r^{2}}\right)$

![](https://cdn.mathpix.com/cropped/2024_02_19_ae34ced50d3894eb01a7g-02.jpg?height=199&width=1359&top_left_y=1108&top_left_x=148)

The $|g\rangle$ obtained in this way is in this sense the "best" approximation to $\left|E_{0}\right\rangle$ in the Hilbert subspace $\mid \{ g\} \rangle$.

We can do something similar in statistical physics.


Given $T, H$, we define the free-energy of an *arbitrary* distribution $\rho$ by

$$
\begin{aligned}
F[\rho] & \equiv \sum \rho_{\mu}\left(H[\mu]+T \ln \left(\rho_{\mu}\right)\right) \\
& =\langle H\rangle_\rho-T S[\rho]
\end{aligned}
$$

where we've used the Gibbs entropy

$$
S[\rho]=-\sum_{\mu} \rho_{\mu} \log \left(\rho_{\mu}\right)
$$


Recall that $\rho_{\beta}=\frac{1}{Z_{\beta}} e^{-\beta H}=e^{-\beta (H-F_0)}$ minimizes $F$ :

$$
F[\rho] \geq F\left[\rho_{\beta}\right] \equiv F_{0}
$$

(Because $\rho_\beta$ maximizes the Gibbs entropy subject to $\langle E\rangle$)

Given a few-parameter ansatz $\rho_{\mu}(g)$, we can then define our best approximation as

$$
\min_{g} F[\rho(g)]>F_{0}
$$ (min-criterion)

and use $\rho(g)$ to compute approximate observables.

Note that there is a simple way to see that {eq}`min-criterion`is true. Using $\rho_{\beta}=e^{-\beta (H-F_0)}$, we can write

$$
\beta\left(F[\rho(g)]-F_{0}\right)=\beta\left[\langle H\rangle_{\rho(g)}-F_{0}\right]-S[\rho(g)]/k_B =\langle \ln(\rho(g))\rangle_{\rho(g)}-\langle \ln(\rho(g))\rangle_{\rho(g)}=S_{KL}\left(\rho(g) \| \rho_{\beta}\right)
$$

showing that the difference between the fake and true free energy is proportional to the "KL" divergence 

$$
S_{K L}(P \| Q)= \sum P_{i} \ln \left(\frac{P_{i}}{Q_{i}}\right) \geq 0
$$

which is non-negative (see Shannon entropy lecture, eq. {eq}`KL-div`).

A convenient way to parameterize $\rho(g)$ is via a fictitious Hamiltonian " $\mathrm{Hg}$ "

$$
p(g) \equiv \frac{1}{z_{g}} e^{-\beta H_{g}}
$$

For example, if $H=-J \sum_{r i, j\rangle} \sigma_{i} \sigma_{j}$, we might choose $H_{g}=-g \sum_{i} \sigma_{i}$, where " $g$ " is a parameter well adjust. In terms

$$
\text { of } F[\rho(g)]=\sum_{\mu} \frac{e^{-\beta H_{g}(\mu)}}{Z_{g}}\left(H(\mu)+\frac{1}{\beta} \ln \left(\frac{e^{-\beta H_{g}(\mu)}}{Z_{g}}\right)\right)
$$

Defining $\quad e^{-\beta F_{g}}=Z_{g} \quad\left(F_{g} \neq F[p(g)) !\right)$

$$
F[p(g)]=\langle H\rangle_{g}-\left\langle H_{g}\right\rangle_{g}+F_{g}
$$

The lower-loound

$$
F[p(g)]-F_{0}=F_{g}-F_{0}+\langle H\rangle_{g}-\left\langle H_{g}\right)_{g} \geq 0
$$

is called the "Gibbs's inequality". It can be rewritten as

$$
\begin{aligned}
-\frac{1}{\beta}\left(\ln \left(Z_{g}\right)-\right. & \ln (z))+\langle H\rangle_{g}-\left\langle H_{g}\right\rangle_{g} 20 \\
& \ln (Z) \geqslant \ln (Z g)+\beta\left(\langle H g\rangle_{g}-\langle H\rangle_{g}\right)
\end{aligned}
$$

Let's try this for

$$
\begin{aligned}
H & =-J \sum_{r i, j\rangle} \sigma_{i} \sigma_{j}, \\
H_{g} & =-g \sum_{i}^{N} \sigma_{i}, \quad \text { "Mra n-field" }
\end{aligned}
$$

We need to compute $Z_{g},\left\langle H_{j}\right\rangle_{g},\langle H\rangle_{g}$

$$
\begin{aligned}
& Z_{g}=\left(e^{\beta g}+e^{-\beta g}\right)^{N}=[2 \cosh (\beta g)]^{N} \\
& F_{g}=-\frac{1}{\beta} N \ln \cosh (\beta g) \\
& \left.\left\langle H_{g}\right\rangle=-g<\sum_{i} \sigma_{i}\right)_{g}
\end{aligned}
$$

We know $\left.-g<\sum_{i} \sigma_{i}\right)_{g}=-\partial_{\beta} \ln \left(Z_{g}\right)$

$$
=-N g \underbrace{\tanh (\beta g)}_{\equiv m_{g}}
$$

And crucially, because $\rho_{g}$ is uncorrelated,

$$
\begin{aligned}
& \rho_{g}\left(\sigma_{1}, \sigma_{2}, \cdots\right)=\rho_{g}\left(\sigma_{1}\right) \rho_{g}\left(\sigma_{2}\right) \cdots \\
&=\prod_{i}(\underbrace{e^{-\beta g \sigma_{i}}}_{p_{i}\left(\sigma_{i}\right)}) \\
&\langle H\rangle_{g}=-J \sum_{\langle i, j\rangle}\left\langle\sigma_{i} \sigma_{j}\right\rangle_{g}=-J \sum_{\langle i, j\rangle}\left\langle\sigma_{i}\right\rangle_{g}\left\langle\sigma_{j}\right\rangle_{g}
\end{aligned}
$$

$=-J \sum_{\langle i, j\rangle} \tanh ^{2}(\beta g) \quad$ uncorrelated

Potting it all together

$$
\begin{aligned}
& F[p(g)]=\langle H\rangle_{g}-\langle H g\rangle_{g}+F_{g} \\
& =-J \frac{N \tau^{2}}{2} m_{g}^{2}+N g m_{g}-\frac{1}{\beta} N \ln 2 \cosh (\beta g) \\
& m_{g} \equiv \tanh (\beta g) \quad \partial_{g} m_{g}=m_{g}^{\prime}
\end{aligned}
$$

Now finally we minimize:

(First order condition)

$$
\begin{aligned}
& \partial_{g} F[\rho(g)]=\partial_{g} N\left[-J \frac{z}{2} m_{g}^{2}+g m_{g}-\frac{1}{\beta} \ln (\cosh (\beta g))\right] \\
&=N\left[-J z m_{g} m_{g}^{\prime}+g m_{g}^{\prime}+m_{g}-m_{g}\right]=0 \\
& g=J z \cdot m_{g}=J \cdot z \cdot \tanh (\beta g) \\
& \text { "del f-consistency" }
\end{aligned}
$$

This has simple physical interpretation: in - J $\sum_{\langle i, j\rangle} \sigma_{i} \sigma_{j}$, each $\sigma_{i}$ sees "on average" a field $J \cdot Z^{*}$ neighors.

a field $J \cdot Z \cdot\langle\sigma\rangle$. Since $H_{g}=-g \sum \sigma_{i}$, condition is $g=J \cdot z\langle\sigma\rangle_{j}$.

We can solve $g=J z \cdot \tanh (\beta g)$ analytically for small $g$ :

$$
g=J_{2} \beta g\left(1-\frac{1}{3}(\beta g)^{2}\right)+\cdots
$$

Solution $1: g=0 . \longrightarrow\langle\sigma\rangle_{g}=0$

But for $T z \beta>1$,

$$
1=J 2 \cdot \beta\left(1-\frac{1}{3}(\beta g)^{2}\right)
$$

Solution 2: $\beta g= \pm \sqrt{3\left(1-\frac{1}{J z \beta}\right)}$

$$
\langle\sigma\rangle_{g}= \pm \sqrt{3\left(1-\frac{1}{J_{2} \beta}\right)}
$$

For $J_{z} \beta>1$, it can be verified this is lower-F solution: symmetry breaking!

Graphical Solution

$$
g=J z \cdot \tanh (\beta g)
$$

Is this variational approximatition good? It knows about lattice/ dim $D=1,2,3$ only through coordinatition \# $z$. eeg., for square lattice $\quad z=2 \cdot D \quad \& z=2$

But we know exact solution of ID Ising model does not have S.B: variational result is bad in CD. On the other. $h$ and, if $(D, z) \rightarrow \infty$, you can verify $F[\rho(g)]$ is identical to the exact result of the all-to-all model: it is good in large $D / z$.

For $D=2,3$, the accuracy is intermediate; it correctly predicts S.B.

but doesn't get $T_{c}$ or $m \sim\left|T-T_{c}\right|^{\beta}$ quantitatively right.

Was the physical interpretation of $g=J z<\sigma)$ a coincidence? No. Consider general

$$
\begin{aligned}
H_{g} & =\sum_{i} g_{i} \cdot O_{i} \\
F(p(g)] & =\langle H\rangle_{g}-\left\langle H_{g}\right\rangle_{j}+F_{g}
\end{aligned}
$$

We know $\partial g_{i} F_{g}=\left\langle O_{i}\right\rangle$. So

cancel

$$
\begin{aligned}
\partial_{g_{i}} F[p(g)] & =\partial_{g}\langle H\rangle_{g}-\partial_{g}\left\langle g_{i} \theta_{i}\right\rangle_{g}+\partial_{g} F_{g} \\
& =\sum_{\mu}\left(\partial_{g} p_{\mu}\right)\left(H(\mu)-H_{g}(\mu)\right)=0
\end{aligned}
$$

This means we need $H(\mu) \sim H_{g}(\mu)$ when projected onto the tangent plane of variations $\delta p$. It is illuminating to work through if

$$
\mu=\mu_{1} \otimes \mu_{2} \otimes \cdots, \quad H_{g}=\sum g_{i} \vartheta\left(\mu_{i}\right)
$$

