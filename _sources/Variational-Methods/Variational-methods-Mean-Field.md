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

showing that the difference between the approximate and true free energy is proportional to the "KL" divergence 

$$
S_{K L}(P \| Q)= \sum P_{i} \ln \left(\frac{P_{i}}{Q_{i}}\right) \geq 0
$$

which is non-negative (see Shannon entropy lecture, eq. {eq}`KL-div`).

It is convenient to parameterize $\rho(g)$  as a Boltzmann distribution corresponding to a fictitious Hamiltonian $H_g$,

$$
\rho(g) \equiv \frac{1}{Z_{g}} e^{-\beta H_{g}}\;.
$$

Consider, for example, the generalized Ising Hamiltonian 

$$H=-J \sum_{\langle i, j\rangle} \sigma_{i} \sigma_{j}$$ 

where the notation $\langle i, j\rangle$ indicates that sites $i$ and $j$ are in contact (i.e. they are nearest neighbors) and each pair is only counted once. We might then choose $H_{g}=-g \sum_{i} \sigma_{i}$, where $g$ is a parameter we will adjust. In terms of $H_g$, we have

$$
F[\rho(g)]=\sum_{\mu} \frac{e^{-\beta H_{g}(\mu)}}{Z_{g}}\left(H(\mu)+\frac{1}{\beta} \ln \left(\frac{e^{-\beta H_{g}(\mu)}}{Z_{g}}\right)\right)
$$

Defining $\quad e^{-\beta F_{g}}=Z_{g}= \sum_{\mu} e^{-\beta H_{g}(\mu)}\quad\left(F_{g} \neq F[p(g)) !\right)$, we have 

$$
F[\rho(g)]=\langle H\rangle_{g}-\left\langle H_{g}\right\rangle_{g}+F_{g}
$$

The lower bound

$$
F[p(g)]-F_{0}=F_{g}-F_{0}+\langle H\rangle_{g}-\left\langle H_{g}\right)_{g} \geq 0
$$

is called the "Gibbs's inequality". It can be rewritten as

$$
\begin{aligned}
-\frac{1}{\beta}\left(\ln \left(Z_{g}\right)-\right. & \ln (Z))+\langle H\rangle_{g}-\left\langle H_{g}\right\rangle_{g} \geqslant 0 \\
& \ln (Z) \geqslant \ln (Z_g)+\beta\left(\langle H_g\rangle_{g}-\langle H\rangle_{g}\right)
\end{aligned}
$$

Let's try this for

$$
\begin{aligned}
H & =-J \sum_{\langle i, j\rangle} \sigma_{i} \sigma_{j}, \\
H_{g} & =-g \sum_{i}^{N} \sigma_{i}, \quad \text { "Mean field " }
\end{aligned}
$$

We need to compute $Z_{g},\left\langle H_{g}\right\rangle_{g},\langle H\rangle_{g}$

$$
\begin{aligned}
& Z_{g}=\left(e^{\beta g}+e^{-\beta g}\right)^{N}=[2 \cosh (\beta g)]^{N}\equiv z_g^N \\
& F_{g}=-\frac{1}{\beta} N \ln[2 \cosh (\beta g)] \\
& \left\langle H_{g}\right\rangle=-g\left \langle \sum_{i} \sigma_{i}\right\rangle_{g}
\end{aligned}
$$

which depends on the mean magnetization $m_g$ under the fictitious Hamiltonian, 

$$
m_{g}\equiv \langle \sigma_i \rangle_g= N^{-1}\left \langle \sum_{j} \sigma_{j}\right\rangle_{g}=(Ng)^{-1}\partial_{\beta} \ln \left(Z_{g}\right)=\tanh (\beta g)\;.
$$

And crucially, because under $\rho_{g}$ the different spins are uncorrelated,

$$
\begin{aligned}
& \rho_{g}\left(\sigma_{1}, \sigma_{2}, \ldots\right)=\rho_{g}\left(\sigma_{1}\right) \rho_{g}\left(\sigma_{2}\right) \ldots \\
&=\prod_{i}\underbrace{\left(\frac{e^{-\beta g \sigma_{i}}}{z_g}\right)}_{\rho_{g}\left(\sigma_{i}\right)} 
\end{aligned}
$$

we obtain for the $\rho_g$ averaged energy


$$
\langle H\rangle_{g}=-J \sum_{\langle i, j\rangle}\left\langle\sigma_{i} \sigma_{j}\right\rangle_{g}=-J \sum_{\langle i, j\rangle}\left\langle\sigma_{i}\right\rangle_{g}\left\langle\sigma_{j}\right\rangle_{g}\\
=-J \sum_{\langle i, j\rangle} m_g^2=-J \sum_{\langle i, j\rangle} \tanh ^{2}(\beta g)=\frac{N \zeta}2 \tanh ^{2}(\beta g)
$$

where $\zeta$ is the number of nearest neighbors each spin has - the so-called coordination number.

Putting it all together

$$
\begin{aligned}
& F[p(g)]=\langle H\rangle_{g}-\langle H_g\rangle_{g}+F_{g} \\
& =-J \frac{N \zeta}{2} m_{g}^{2}+N g m_{g}-\frac{1}{\beta} N \ln [2 \cosh (\beta g)]  
\end{aligned}
$$

Now, finally, we minimize ($m_{g}^{\prime}=\partial_{g} m_{g}$):


$$
\begin{aligned}
& \partial_{g} F[\rho(g)]=N\partial_{g} \left[-J \frac{\zeta}{2} m_{g}^{2}+g m_{g}-\frac{1}{\beta} \ln (\cosh (\beta g))\right] \\
&=N\left[-J \zeta m_{g} m_{g}^{\prime}+g m_{g}^{\prime}+m_{g}-m_{g}\right]=0 \\
& g=J \zeta \cdot m_{g}=J \cdot \zeta \cdot \tanh (\beta g) \\
& \text { "self-consistency" }
\end{aligned}
$$

This has a simple physical interpretation: in $H=-J\sum_{\langle i, j\rangle} \sigma_{i} \sigma_{j}$, each $\sigma_{i}$ sees "on average" a field $J \zeta \langle \sigma_i\rangle_g=J \zeta m_g$ induced by its neighors - suggesting $H\approx -J \zeta m_g\sum_i \sigma_i$. Since $H_{g}=-g \sum_i \sigma_{i}$, the condition is $g=J \zeta m_g$.

We can solve $g=J \zeta \tanh (\beta g)$ analytically for small $g$ :

$$
g=J \zeta \beta g\left(1-\frac{1}{3}(\beta g)^{2}\right)+\cdots
$$

Solution $1: g=0 . \longrightarrow m_{g}=0$

But for $T \zeta \beta>1$,

$$
1=J \zeta \beta\left(1-\frac{1}{3}(\beta g)^{2}\right)
$$

Solution 2: $\beta g= \pm \sqrt{3\left(1-\frac{1}{J \zeta \beta}\right)}$

$$
m_{g}= \pm \sqrt{3\left(1-\frac{1}{J \zeta \beta}\right)}
$$

For $J \zeta \beta>1$, it can be verified this is lower-F solution: symmetry breaking!

Graphical Solution

$$
g=J \zeta \tanh (\beta g)
$$

Is this variational approximatition good? It knows about the lattice and dimensions $D=1,2,3$ only through coordination number $\zeta$. e.g., for square lattice $\quad z=2 D $

But we know that the exact solution of 1D Ising model does not have symmetry breaking: the variational result is bad in 1D. On the other hand, if $(D, z) \rightarrow \infty$, you can verify $F[\rho(g)]$ is identical to the exact result of the all-to-all model: it is good in large $D$ and large $\zeta$.

For $D=2,3$, the accuracy is intermediate; it correctly predicts symmetry breaking  but doesn't get $T_{c}$ or $m \sim\left|T-T_{c}\right|^{\beta}$ quantitatively right.

Was the physical interpretation of $g=J \zeta \langle\sigma\rangle$ a coincidence? No. Consider general

$$
\begin{aligned}
H_{g} & =\sum_{i} g_{i} \cdot O_{i} \\
F(p(g)] & =\langle H\rangle_{g}-\left\langle H_{g}\right\rangle_{j}+F_{g}
\end{aligned}
$$

We know $\partial g_{i} F_{g}=\left\langle O_{i}\right\rangle$. So


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

