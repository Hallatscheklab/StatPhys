ling models

![](https://cdn.mathpix.com/cropped/2024_02_18_d4a93dd939ac97dd8d1dg-01.jpg?height=1153&width=2055&top_left_y=235&top_left_x=42)

ID $\quad H=-\gamma \sum_{i=1}^{N} \sigma_{i} \sigma_{i+1}-B \sum_{i} \sigma_{i}$

Order destroyed by domain walls for any finis temperature

$$
\uparrow \uparrow \uparrow \Uparrow \downarrow \downarrow \downarrow \downarrow \downarrow
$$

di. costs energy $\Delta=Z J$

Boltzmann: $\operatorname{pr}[d-\omega \mid$ specificite $]=\frac{e^{-\beta \Delta}}{e^{-\beta \Delta}+1} \equiv P d \omega$.

$$
\begin{aligned}
& \beta J \gg 1 \Rightarrow p_{d \omega} \approx e^{-\beta \Delta} \\
& \beta J \ll 1 \Rightarrow P_{d, w} \approx \frac{1}{2}
\end{aligned}
$$

$\Rightarrow$ Gas of d.w.s with only hard-core interaction (Tonks gus) and davity

$$
\begin{aligned}
& \text { TDL } N_{d . w}=P d . w \cdot N, P_{d \omega} \ll l . \\
& \Rightarrow \text { dencity of d.w. } \rho=e^{-\beta \Delta}
\end{aligned}
$$

correlaticn funetion

$$
\begin{aligned}
& \left\langle\sigma_{0} \sigma_{r}\right\rangle=\left\{\begin{array}{l}
+1, \text { even ur. of d.w betw. Oandr } \\
-1, \text { odd ur. }
\end{array}\right. \\
& =\sum_{m=0}^{T} p_{m}(-1)^{m}
\end{aligned}
$$

$P_{m}=$ Binomial distrib. with $m$ success in $r$ trials if succ. proba. $=$ plw. .

$$
\begin{aligned}
\left\langle\sigma_{0} \sigma_{r}\right\rangle & =\sum_{m=0}^{r}\left(\begin{array}{l}
r \\
m
\end{array}\right) p^{m}(1-p)^{\tau-m} \cdot(-1)^{m} \\
& =(1-2 p)^{r} w \cdot p=\frac{e^{-\beta \Delta}}{e^{-\beta \Delta}+1}
\end{aligned}
$$

$$
\left\langle\sigma_{0} \sigma_{r}\right\rangle=\exp [r \ln (1-2 p)]=e^{-\frac{r}{\xi}},
$$

where the correlation length $\xi$ is given by

$$
\xi=\frac{1}{|\ln (1-2 p)|} \simeq \frac{1}{p \ll 1} \simeq \frac{e^{\beta \Delta}}{2}
$$

$\Rightarrow-\xi$ is typical domain size

$-\lim _{r \rightarrow \infty}\left\langle\sigma_{0} \sigma_{r}\right\rangle=0 \quad \forall T>0$

$\Rightarrow \quad N a$ long range order

always in paramapueticphase Na phase transitions!

Full solution

IDmadel (unlike 3D!) can be solved exactly using "transfer matrix method! First consider $B=0$

$$
\begin{equation*}
z=\sum_{\{\sigma\}} \prod_{B \text { lactor }}^{\prod_{i=1}^{N} e^{\beta J \sigma_{i} \sigma_{i+1}}} \tag{*}
\end{equation*}
$$

Deline $2 \times 2$ matrix $T_{\sigma \sigma_{1}}=e^{\beta J \sigma \sigma^{\prime}}$

$$
\begin{aligned}
& T=\left[\begin{array}{ll}
e^{\beta \gamma} & e^{-\beta z} \\
e^{-\beta z} & e^{\beta J}
\end{array}\right] \\
& Z=\sum_{\sigma_{1}} \sum_{\sigma_{2}} \cdots \sigma_{N} T_{\sigma_{1} \sigma_{2}} \cdot T_{\sigma_{2} \sigma_{3}} T_{3} \sigma_{4}
\end{aligned}
$$

Boltzmann fector

This sum is just matrix multiplic.!

Next, with $B \neq 0$

![](https://cdn.mathpix.com/cropped/2024_02_18_d4a93dd939ac97dd8d1dg-04.jpg?height=554&width=1513&top_left_y=1762&top_left_x=448)

Nsites with perindic b.c. (i.e.ering)

$$
Z_{N}=\left(T^{N}\right)_{11}+\left(T^{N}\right)_{22}=\operatorname{Tr}\left(T^{N}\right)
$$

Powers of a matrix are simple in terms of eigen vols and-rectors:

For $\beta=0, \lambda_{ \pm}=e^{\beta \gamma} \pm e^{-\beta J}$

$[$ from $(T-\lambda 11) \underline{x}=0$

$\operatorname{det}(T-\lambda 11)=0]$

Nate $\left.\frac{\lambda_{-}}{\lambda_{+}}=\tanh (\beta \gamma)<1 \quad \forall \beta\right\rangle$

So $\lim _{N \rightarrow \infty} z_{N}=\underbrace{\lambda_{+}^{N}\left(1+\left(\frac{\lambda_{-}}{\lambda_{+}}\right)^{N}\right)}_{\underbrace{}_{T}\left(T^{N}\right)} \rightarrow \lambda_{+}^{N}$

$$
F=-k_{B} T N \ln (2 \cosh (37))+o(1)
$$

Note: $F(T)$ is analytic in $T$, unlike all-bo-all $H W$ checks $x=-\left.\partial_{B}^{2} F(T, B)\right|_{B=0}=\frac{\partial(m)}{\partial B}$ regular $\forall T$.

Entropy density

$$
S=\frac{1}{N} \partial_{T} F
$$

$\ln (2)$

smooth fets/no ph.tansitions

Correlation $f c t: C(r) \equiv\left\langle\sigma_{0} \sigma_{r}\right\rangle$

$$
\left\langle\sigma_{0} \sigma_{r}\right\rangle=\frac{\sum_{i \sigma j} \ldots T_{\sigma_{0, \sigma_{0}}} \sigma_{0} T_{\sigma_{0} \sigma_{1}} \cdots \cdot \sigma_{x-1} \sigma_{r} \sigma_{j} T_{\sigma_{i} \sigma_{1}}}{z}
$$

Introducing $\hat{\sigma}^{z} \equiv\left(\begin{array}{cc}1 & 0 \\ 0 & -1\end{array}\right)$, we can write this as a matrix product

![](https://cdn.mathpix.com/cropped/2024_02_18_d4a93dd939ac97dd8d1dg-06.jpg?height=425&width=1469&top_left_y=2003&top_left_x=496)

Introduce eigensystem of $T$

$$
|+\rangle=\frac{1}{\sqrt{2}}\left(\begin{array}{l}
1 \\
1
\end{array}\right) ; \lambda_{t}=2 \cosh (\beta \gamma)
$$

$$
\begin{gathered}
1 \rightarrow=\frac{1}{\sqrt{2}}\left(\begin{array}{c}
1 \\
-1
\end{array}\right) ; \lambda_{-}=2 \sinh (\beta \gamma) \\
T^{\gamma}=\sum_{\alpha= \pm}|\alpha\rangle\langle\alpha| \lambda_{\alpha}^{\gamma} \\
C(\gamma)=\sum_{\alpha \beta \beta}\left\langle\beta\left|\hat{\sigma}^{z}\right| \alpha\right\rangle\left\langle\alpha\left|\hat{\sigma}^{z}\right| \beta\right\rangle \lambda_{\alpha}^{\gamma} \lambda_{\beta}^{N-\gamma}
\end{gathered}
$$

dominated by $\beta=+$ and $\left\langle\alpha\left|\beta^{z}\right|+\right\rangle \neq 0$

requires $\alpha=-$

So, $C(r)=\frac{\lambda_{-}^{r} \lambda_{+}^{N-r}}{\lambda_{+}^{N}}=\left(\frac{\lambda_{-}}{\lambda_{+}}\right)^{r}$

$$
=e^{-r / \xi} \text { with } \frac{1}{\xi} \equiv \ln \left(\frac{\lambda_{+}}{\lambda_{-}}\right) \text {. }
$$

Since $\frac{\lambda_{t}}{\lambda_{-}}=\tanh [\beta]=1-2 \frac{\underbrace{e^{-\beta \gamma}}_{P d . \omega .}}{\underbrace{\beta \gamma}+e^{-\beta \gamma}}$

$\Rightarrow$ same corrleurfh as found before.

Phase transition for $D>1$ ?

Recap essence of IDsituation:

In ID, long-range order can be destroyed by defects that cost a finite amount of energy.

Same argument in 2D?

For D>1, domain walls are extended

$\Rightarrow$ to destroy order

d. wis need to

be large $\Rightarrow$

energy cost is not bounded by finite

value $\Rightarrow I D$ argument canal be applied.

In 2D, a dew. is a ID object,

which cast $\Delta E=27 \cdot l$ where

$$
l=\text { loupth of d.w. }
$$

In ID, any finite density "olw of di.w.s destrons order at the ecale $\xi \sim \frac{1}{u_{d} \omega_{1}}$.

But in 2D, a fuile densits of sunall d.w.s dresuit abstroy as dor

![](https://cdn.mathpix.com/cropped/2024_02_18_d4a93dd939ac97dd8d1dg-09.jpg?height=792&width=1765&top_left_y=1021&top_left_x=290)

What matters is the size of the d.ws

![](https://cdn.mathpix.com/cropped/2024_02_18_d4a93dd939ac97dd8d1dg-09.jpg?height=676&width=818&top_left_y=2007&top_left_x=235)

Cnder olestrayed if size $\ell \sim L$ becnure favorable

So, the question is how

$$
\begin{aligned}
& \Delta F(l)=\text { bree energy change indlaced } \\
& \text { by } d . w \cdot s \text { of size } l= \\
&=\underbrace{27 l}_{\substack{\text { energetic } \\
\text { cost }}}-T S(l)
\end{aligned}
$$

In ID, the only source of $S$ was Whet dew. is: $S \sim \operatorname{lu}(L)$ for l.d.w. But in 2D, the are many ways to make a wall of birth $l$ :
![](https://cdn.mathpix.com/cropped/2024_02_18_d4a93dd939ac97dd8d1dg-10.jpg?height=374&width=1762&top_left_y=1732&top_left_x=261)

Counting $S(l)$ exactly is a tricky combinatorial probkun. But all we need, for $l>1, S(l) \cong S_{0} l$
(extensive)

To see why, let $\Omega\left(l, x_{0}, x_{1}\right)$ denote \# of ways string of berth $l$ connects $x_{0}, x_{1}$ :

![](https://cdn.mathpix.com/cropped/2024_02_18_d4a93dd939ac97dd8d1dg-11.jpg?height=373&width=1140&top_left_y=625&top_left_x=551)

Clearly

$$
\begin{aligned}
& \Omega\left(l_{A}+l_{B}, x_{0}, x_{2}\right) \geqslant \Omega\left(l_{A}, x_{0}, x_{1}\right) \Omega\left(l_{B}, x_{1}, x_{2}\right) \\
& S\left(l_{A}+l_{B}, x_{0}, x_{2}\right) \geqslant S\left(l_{A}, x_{0}, x_{1}\right)+S\left(l_{B}, x_{1}, x_{2}\right)
\end{aligned}
$$

Fix $x_{1}-x_{0}=\frac{e}{\alpha}$ these inequalities imply $S(l) \simeq S_{0} \cdot l$ or faster growing.

But faster than extensive nat possible.

So,

$$
\begin{aligned}
\Delta F & =2 J \ell-T s_{0} \ell \\
& =\ell\left(2 J-T s_{0}\right)
\end{aligned}
$$

Key result: For $T<\frac{27}{S_{0}}$, largel d.w.S

$\Rightarrow$ oretered plase Far $T>\frac{27}{S o}$, large ld.wis disarderel

