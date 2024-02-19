

The previous model is physically un realistic because it had all-to-all coupling; in our universe d.a.f. are arranged in space and interact locally. To this end:

1 losing Model

$$
\begin{aligned}
& \ldots \hat{\phi}_{i=1} \phi_{i=c} \phi_{i=1} \hat{\phi}_{i=2} \\
& H[\sigma]=-J \sum_{i} \sigma_{i} \sigma_{i+1}-B \sum_{i} \sigma_{i}
\end{aligned}
$$

For $T=0$, two lowest $E$ stake:. $1 \uparrow \uparrow_{n, \ldots} \ldots \downarrow \downarrow \downarrow \ldots$

The interesting question is whether this a de survives for $T>0$, ie., whether spins are carreletted over the entire lattice. (lon grange correlations) If se, we expect phase transition at finite T. Terns out: no phase bansition

It turns oct, correlations $\xi=e^{\frac{2 f}{k_{B} T}}$

ID model (nike 3D!) can be solved exactly using "transfer matrix" method. First, consider $B=0$.

$$
Z=\sum_{\{\sigma\}} \prod_{i} e^{\beta J \sigma_{i} \sigma_{i+1}}
$$

Define $2 \times 2$ matrix $T_{\sigma, \sigma^{\prime}}=e \beta J \sigma \sigma^{\prime}$

$$
T=\left[\begin{array}{cc}
e^{\beta J} & e^{-\beta J} \\
e^{-\beta J} & e^{\beta J}
\end{array}\right]=\sigma T \sigma^{\prime}
$$

Then $z=\sum_{\left\{\sigma_{3}\right.} T_{\sigma_{1} \sigma_{2}} T_{\sigma_{2} \sigma_{3}} T_{\sigma_{4} \sigma_{5}} \cdot \cdots$

This is just matrix multiplication! Next, with $B \neq 0$

$$
\begin{aligned}
T_{\sigma_{i} \sigma_{i+1}} & =e^{\beta\left(J \sigma_{i} \sigma_{i+1}+\frac{B}{2} \sigma_{i}+\frac{B}{2} \sigma_{i+1}\right)} \\
& =\left[\begin{array}{cc}
e^{\beta(J+B)} & e^{-\beta J} \\
e^{-\beta J} & e^{\beta(J-B)}
\end{array}\right]
\end{aligned}
$$

$N$ sites with periodic boundary conditions (ie. a ring):

$$
Z_{N}=\left(T^{N}\right)_{11}+\left(T^{N}\right)_{22}=T_{N}\left(T^{N}\right)
$$

If $\operatorname{eig}(T)=\left\{\lambda_{+}, \lambda_{-}\right\}$,

$Z_{N}=\lambda_{+}^{N}+\lambda_{-}^{N} \Rightarrow$ larger Evil wins for $N>0$

For $B=0, \lambda_{ \pm}=e^{\beta J} \pm e^{-\beta J}$.

![](https://cdn.mathpix.com/cropped/2024_02_16_f7648d1deba1b235d1a3g-18.jpg?height=550&width=1706&top_left_y=774&top_left_x=246)

Wale $\frac{\lambda_{-}}{\lambda_{+}}=\tanh (\beta J)<1 \quad \forall \beta J$

So $\lim _{N \rightarrow \infty} z_{N}=\lambda_{+}^{N}\left(1+\left(\frac{\lambda_{\lambda}}{\lambda_{1}}\right)^{N}\right) \longrightarrow \lambda_{+}^{N}$.

$$
F=-k_{B} T N \ln (2 \cosh (B J))+o(1)
$$

Note: $F(T)$ is analytic in $T$, unlike all-to-all. $H W$ clucks $X=-\left.\partial_{B}^{2} F(T, B)\right|_{B=0}$ regular $\forall T$.

$\rightarrow$ no phase transition. $\rightarrow$ explain

Excitations intuitively.

$$
\begin{aligned}
& F=-k_{B} T N \ln \left(e^{\beta j}+e^{-\beta J}\right) \\
& =-k_{B} T N \ln \left(e^{\beta \gamma}\left(1+e^{-2 \beta \gamma}\right)\right)
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_02_16_f7648d1deba1b235d1a3g-19.jpg?height=444&width=2140&top_left_y=1632&top_left_x=378)
$e^{-2 \beta J}$ can be understood as excitations above ground state: $\quad \uparrow \uparrow \uparrow \uparrow \downarrow \downarrow \downarrow \downarrow \downarrow$ "Domain wall"

Each domain wall costs $\Delta=2$ J energy, so finite $T$ corrections come from $e^{-2 \Delta / k_{B} T}$.

Entropy density

Energy density

$S=\frac{1}{N} \partial_{T} \neq$

![](https://cdn.mathpix.com/cropped/2024_02_16_f7648d1deba1b235d1a3g-20.jpg?height=813&width=1340&top_left_y=1200&top_left_x=1298)

Absence of symmetry breaking in ID in equilibrium

Consider a system with m competing orders, eeg. Using $m=2$ with $\uparrow \uparrow$ or $\downarrow \downarrow$.

or liquid/gas.

In ID with local interactions, dew. costs finite every $A$.

$$
2 \xi \text { Phase } 132
$$

At finite $T$, there will thus be a density uphroe $e^{-\frac{\Delta}{V_{T}}}$ of them. Low $T \Rightarrow$ low $n \Rightarrow$ Dis far a past $\Rightarrow$ do not interact $\Rightarrow$ move around randomly, like a foe gas

This means for $T>0$ there are always "bubbles", and $C(r) \sim e^{-r / \xi}$ - no true order in ID/ no phase transitions.

For D>I, domain walls core extended. Since energy net bounded by $\Delta$, argument does not apply

![](https://cdn.mathpix.com/cropped/2024_02_16_f7648d1deba1b235d1a3g-22.jpg?height=800&width=1105&top_left_y=1289&top_left_x=635)

Thermal correlation tenth

Let's compute $m=\left\langle\sigma_{i}\right\rangle$ and correlation function $C(v) \equiv\left\langle\sigma_{r} \sigma_{0}\right\rangle$.

When $B=0, T\rangle 0:\langle\sigma\rangle=0$ by symmetry.

In fact $H[\sigma]=H[-\sigma]$ has $\mathbb{Z}_{2}$ ling symmetry. all spins flipped.

$$
\Rightarrow \sum_{\sigma} p_{\sigma} \sigma(\sigma)=\sum_{\sigma} p_{-\sigma} O(\sigma)=\sum_{\sigma} p_{\sigma} O(\sigma) .
$$

$\rightarrow$ all odd moments vanish.

In all-to-all case $\lim _{N \rightarrow \infty}$ and $\lim _{B \rightarrow 0} d o$ not com mute!

A physical picture can be obtained from $C(r)=\left\langle\sigma_{r} \sigma_{0}\right)$

For $K_{B} T \ll J$, there is a density $n_{\text {ow }}=e^{-\Delta / K_{B} T^{\prime}} \quad$ D.W. $>$ $\cdots \uparrow \uparrow \uparrow \uparrow \underbrace{\downarrow \downarrow \downarrow \downarrow}_{l .1} \underbrace{\uparrow \uparrow \uparrow \uparrow \uparrow \uparrow}_{l o} \underbrace{\downarrow \downarrow \downarrow}_{l .} \uparrow \uparrow$.

The typical size of domains is thus $\xi=\left\langle l_{n}\right\rangle=\frac{1}{n_{\text {ow }}}=e^{\Delta / K_{B} T}$

If we measure $\left\langle\sigma_{r} \sigma_{0}\right\rangle$ for $r \ll \xi$, we get +1 because in same domain. But for $r \gg \xi$, there is random - \# of D.W. in between (Poisson), so $\left\langle\sigma_{r} \sigma_{0}\right\rangle \rightarrow 0$. This suggest something like

$$
\left\langle\sigma_{r} \sigma_{0}\right\rangle \sim e^{-r / \xi}
$$

We can show this analytically via T.M.

$$
\left\langle\sigma_{0} \sigma_{\gamma}\right\rangle=\frac{\sum_{i \in 3} \ldots T_{\sigma_{1} \sigma_{0}}\left|\sigma_{0} T_{\sigma_{0} \sigma_{1}} \ldots T_{\sigma_{r-1} \sigma_{v}}\right| \sigma_{\gamma \gamma} T_{\sigma_{r} \sigma_{r+1}}}{z}
$$

Introducing $\hat{\sigma} \equiv\left(\begin{array}{cc}1 & 0 \\ 0 & -1\end{array}\right)$, we can write this as the matrix product

$$
C(r)=\frac{\operatorname{Tr}\left(\hat{\sigma}^{z} T^{r} \hat{\sigma}^{z} T^{N-r}\right)}{\operatorname{Tr}\left(T^{N}\right)}
$$

Introduce liger system of $T$ :

$$
\begin{aligned}
& |t\rangle=\frac{1}{\sqrt{2}}\left(\begin{array}{l}
1 \\
1
\end{array}\right) \quad \lambda_{+}=2 \cosh (\beta J) \\
& |-\rangle=\frac{1}{\sqrt{2}}\left(\begin{array}{c}
1 \\
-1
\end{array}\right) \quad \lambda_{-}=2 \sinh (\beta 7)
\end{aligned}
$$

$$
\begin{aligned}
& \Rightarrow T^{\gamma}=\sum_{\alpha= \pm}|\alpha\rangle\langle\alpha| \lambda_{\alpha}^{\gamma} \\
& \Rightarrow C(\gamma)=\sum_{\alpha, \beta}\left(\beta\left|\hat{\sigma}^{z}\right| \alpha\right)\left(\alpha\left|\hat{\sigma}^{z}\right| \beta\right\rangle \lambda_{\alpha}^{\gamma} \lambda_{\beta}^{N-\gamma}
\end{aligned}
$$

dominated by $\beta=+$. and $\left\langle\alpha\left|\sigma^{z}\right|+\right\rangle \neq 0$ requires $\alpha=-$. So,

$$
\begin{aligned}
& C(r)=\frac{\lambda_{-}^{r} \lambda_{+}^{N-r}}{\lambda_{t}^{N}}=\left(\frac{\lambda_{-}}{\lambda_{+}}\right)^{r} \\
\Rightarrow & C(r)=e^{-r / \xi} \text { with } \frac{1}{\frac{z}{z}} \equiv \ln \left(\frac{\lambda_{+}}{\lambda_{-}}\right) .
\end{aligned}
$$

Since $\frac{\lambda_{+}}{\lambda_{-}}=\tanh \beta J \quad \beta J \rightarrow \infty$ we get $\xi=\frac{1}{2} e^{\Delta / k_{B} T}, \Delta=27$


