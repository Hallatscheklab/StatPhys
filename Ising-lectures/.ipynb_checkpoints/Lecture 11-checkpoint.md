Lecture ll: Interacting Spins:

Copyright Michael Zaletel, Phys 211, UC Berkeley Physics 2021 $O D$ no phases $D=\infty I \sin g$ IDIsing

$$
\begin{aligned}
Z(\beta, M) & =\sum_{\left\{\sigma_{i}\right\}} e^{-\beta\left(-B \Sigma \sigma_{i}\right)} \\
& =\left(1+e^{\beta B}\right)^{N}
\end{aligned}
$$

Because no interactions, $N$-spin problem is simply additive:

$$
F=-k B T N \ln \left(1+e^{\beta B}\right)
$$

Whole is not greater than sum of parts.

Further more, $F(T, M)$ is analytic function; no cusps/kinks/singularities. since observables are obtained from derivatives, e.g. $\left\langle\sigma_{i}\right\rangle=\cdot \frac{1}{N} \partial B F$, everything behaves smoothly: no phase transitions.

This is true for any model with a finite \# of states; if $\mathcal{H}[S ; J]$ is analytic in J, then then

$$
Z(\beta, J)=\sum_{s=1}^{|s|} e^{-\beta H[s ; J]}
$$

is. However, with interactions + T. D.L., this need not be the case: the whole is greater than the sum of its parts, "more is different" (P. Anderson)

Generic interacting spin systems cannot be solved exactly:

$$
Z(\beta)=\sum_{\{\sigma\}} e^{-\beta Z[\sigma]}
$$

involves $2^{v}$ terms in the sum! we will learn approximations + numerical approaches. However, there are som

All-to-all Using Model

![](https://cdn.mathpix.com/cropped/2024_02_16_8ad99d9eac551204c94bg-03.jpg?height=325&width=395&top_left_y=1119&top_left_x=231)

$$
\therefore
$$

Consider $N$-spins $\sigma_{1}, \sigma_{2}, \ldots$ interacting through all-to-all ferromagnetic interaction:

$$
\mathcal{H}[\sigma]=-\frac{J}{2 N} \sum_{i, j=1}^{N} \sigma_{i} \sigma_{j}-\sum_{i=1}^{N} B \sigma_{i}
$$

Iso prefers $\uparrow \uparrow+\downarrow \downarrow$ us $\uparrow \downarrow, \downarrow \uparrow$

Defining $m \equiv \frac{1}{N} \sum_{i=1}^{N} \sigma_{i}$ what

is $\langle m\rangle(\beta, J, B)$ as $N \rightarrow \infty^{2}$ If we can compute $Z=\sum_{\{\sigma\}} e^{-\beta H[\sigma]}=e^{-\beta F}$

$$
m=-\frac{1}{N} \partial_{B} F
$$

To do so, note we can write

$$
\begin{aligned}
\mathcal{H}[\sigma] & =-\frac{J}{2 N} \sum_{i, j=1}^{N} \sigma_{i} \sigma_{j}-\sum_{i=1}^{N} B \sigma_{i} \\
& =N\left[-\frac{J}{2} m^{2}[\sigma]-B m[\sigma]\right]
\end{aligned}
$$

So $E$ depends only on $M=N \cdot m[\sigma]$. We can then decompose

$$
Z=\sum_{\sigma} e^{-\beta H[\sigma]}=\sum_{M} \Omega(M) e^{-\beta \mathcal{H}[M]}
$$

$\tau$ \# of $\{\sigma\}$ with $M$.

Since $N_{\uparrow}=\frac{N}{2}+\frac{\mu}{2}, N_{\nu}=\frac{N}{2}-\frac{M}{2}$

$$
\begin{aligned}
& \Omega(M)=\left(\begin{array}{c}
N \\
\frac{N}{2}+\frac{M}{2}
\end{array}\right)=\frac{N !}{\left(\frac{N+M}{2}\right) !\left(\frac{N-M}{2}\right) !} \\
\approx & e^{N \ln (N)-\left(\frac{N+M}{2}\right) \ln \left(\frac{N+M}{2}\right)-\left(\frac{N-M}{2}\right) \ln \left(\frac{N-M}{2}\right)} \\
= & e^{N\left[\ln (2)-\frac{1+m}{2} \ln (1+M)+\frac{1-m}{2} \ln (1-m)\right]} \\
\equiv & e^{N(m)} f^{\ln (2)}
\end{aligned}
$$

So

![](https://cdn.mathpix.com/cropped/2024_02_16_8ad99d9eac551204c94bg-05.jpg?height=354&width=1831&top_left_y=152&top_left_x=111)

The H-part looks like this:

$s(m)$

Depending on $\beta J$, net $f(m)$ either or $\sim$. As $N \rightarrow \infty$, sum is dominated by minima $f(\bar{m})$

$$
\begin{aligned}
f(m) & =f(\bar{m})+\frac{1}{2} f^{\prime \prime}(\bar{m})(m-\bar{m})^{2}+\cdots \\
Z & =\int d m e^{-\beta N\left(f(\bar{m})+\frac{1}{2} f^{\prime \prime}(\bar{m})(m-\bar{m})^{2}\right)} \\
& =e^{-\beta N f(\bar{m}) \cdot \frac{1}{\sqrt{2 \pi \beta N / f^{\prime \prime}}}} \\
F & =N f(\bar{m})+O(\log (N))
\end{aligned}
$$

So problem reduces to determining minima $f(\bar{m})$. To facilitate, assume $m \ll 1$, where

$$
s(m)=\ln (2)-\frac{m^{2}}{2}-\frac{m^{4}}{12}+O\left(m^{6}\right)
$$

$$
\begin{aligned}
f(m) & =-\frac{J}{2} m^{2}-B m+k_{B} T\left(\frac{m^{2}}{2}+\frac{m^{4}}{12}-\ln (2)\right)+\cdots \\
& =-k_{B} T \ln (2)-B m+\frac{\left(k_{B} T-J\right)}{2} m^{2}+\frac{k_{B} T}{12} m^{4}
\end{aligned}
$$

Let's consider case $B=0 . \bar{m}$ depends crucially on sign of $K_{B} T-J$ :

$$
\begin{aligned}
& K_{B} T-J>0: f=\bigcup^{\prime} \quad \bar{m}=0 \\
& K_{B} T-J<0: f=\sqrt{m}= \pm \sqrt{3\left(\frac{J}{K_{B} T}-1\right)}
\end{aligned}
$$

Which minima depend on sign $(B)$, even for
in finitesmal $B$.

Non-analytic behavior: a spontaneous symmetry breaking phase transition!

In HW you'll analyze further.

The previous model is physically unrealistic be cause it had all-to-all coupling; in our universe d.o.f are arranged in space and interact locally. To this end:

10 Ising Model

$$
\begin{aligned}
& \ldots \widehat{\phi}_{i=-1}^{m} \phi_{i=0}^{m} \phi_{i=1}^{m} \cdots_{0}^{m} \ldots \\
& H[\sigma]=-J \sum_{i} \sigma_{i} \cdot \sigma_{i+1}-B \sum_{i} \sigma_{i}
\end{aligned}
$$

For $T=0$, there are two lowest

![](https://cdn.mathpix.com/cropped/2024_02_16_8ad99d9eac551204c94bg-07.jpg?height=129&width=2025&top_left_y=1158&top_left_x=77)

The interesting question is whether in ID this "order" survives to finite $T_{c}$, as for all-to-all, or is immediately destroyed for $T>0$. In ID, it turns out the latter (not so in D22!), but weill still find some effect of interaction "J" such as "thermal correlation length" $\xi=e^{2 J / K_{B} T}$

The ID model (unlike 3D!) can still be solved exactly using the "transfer matrix" method. I'll lsthandle $B=0$ for simplicity

$$
Z=\sum_{\sigma_{i}} \prod_{i} e^{\beta J \sigma_{i} \sigma_{i r}}
$$

Define a $2 \times 2$ matrix $T_{\sigma}, \sigma^{\prime}=e^{\beta J \sigma \sigma^{\prime}}$

$$
T=\left[\begin{array}{ll}
e^{\beta J} & e^{-\beta J} \\
e^{-\beta J} & e^{\beta J}
\end{array}\right]=\sigma^{\sigma} \sigma^{\prime}
$$

Then $Z=\sum_{\sigma_{1}, \sigma_{2}, \ldots} T_{\sigma_{1} \sigma_{2}} T_{\sigma_{2} \sigma_{3}} T_{\sigma_{4} \sigma_{5}} \ldots$

This is just matrix multiplication!

with $B \neq 0$, group as

$$
\begin{aligned}
& T_{\sigma_{i} \sigma_{i+1}}=e^{\beta\left(J \sigma_{i} \sigma_{i+1}+\frac{B}{2} \sigma_{i}+\frac{B}{2} \sigma_{i+1}\right)} \\
& T=\left[\begin{array}{cc}
e^{\beta(J+B)} & e^{-\beta J} \\
e^{-\beta J} & e^{\beta(J-B)}
\end{array}\right]
\end{aligned}
$$

On a periodic ring of length $N$ (egg. $\sigma_{N}$ talks with $\left.\sigma_{1}\right)$

$$
Z_{N}=\operatorname{Tr}\left[T^{N}\right]
$$

If $\operatorname{eig}(T)=\left\{\lambda_{+}, \lambda_{-}\right\}$,

$$
Z_{N}=\left(\lambda_{+}\right)^{N}+\left(\lambda_{-}\right)^{N}
$$

For $B=0$,

$$
\begin{aligned}
T= & {\left[\begin{array}{cc}
e^{\beta J} & e^{-\beta J} \\
e^{-\beta J} & e^{\beta J}
\end{array}\right]=e^{\beta J} \mathbb{I}+e^{-\beta J} \tilde{\sigma}^{x} } \\
\lambda+1- & =e^{\beta J} \pm e^{-\beta J}
\end{aligned}
$$

Note $\frac{\lambda-}{\lambda+}=\tanh (\beta J)<1$

So $\lim _{N \rightarrow \infty} Z_{N}=\lambda_{+}^{N}\left(1+\left(\frac{\lambda_{-}}{\lambda_{+}}\right)^{N}\right) \rightarrow \lambda_{+}^{N}$

$$
F=-K_{B} T N \ln (2 \cosh (\beta J))+\theta(1)
$$

Note that $F(T)$ is manifestly analytic in $T$, unlike all-tosall. In HW you will explicitly verify $x=-\left.\partial_{B}^{2} F(T, B)\right|_{B=0}$ is regular for all $T$ : no phase transition

$$
\begin{aligned}
F & =-K_{B} T N \ln \left(e^{\beta J}+e^{-\beta J}\right) \\
& =-K_{B} T N \ln \left(e^{\beta J}\left(1+e^{-2 \beta J}\right)\right) \\
(\beta J \gg 1) & \approx-K_{B} T N\left(\beta J+e^{-2 \beta J}+O\left(e^{-4 \beta J}\right)\right) \\
& =N\left(-J-K_{B} T e^{-2 \beta J}\right)=E-T S
\end{aligned}
$$

Note $E[\uparrow \uparrow \uparrow \ldots]=-N J$ so the first part is the $T \rightarrow 0$ Egg. The $e^{-2 J / K_{B} T}$ can be understood as excitations above G.S.:

...aq+ $\uparrow \downarrow \downarrow \downarrow \downarrow \downarrow \ldots$

"Domain wall"

Each domain wall costs $\Delta=2 \mathrm{~J}$ energy, so finite- $T$ corrections come from $e^{-2 \Delta / K B T}$

The entropy density $S=\frac{1}{N} \partial_{T} F$

$A+T / J \rightarrow 0$

$$
S=\partial_{T} K_{B} T e^{-\Delta / K_{B} T}=K_{B}\left(1+\frac{\Delta}{K_{B} T}\right) e^{-\Delta / K_{B} T}
$$

The energy density is $\partial_{\beta}(\beta F)$

For low- $T$,

$$
\begin{aligned}
& \frac{E}{N}=-J\left(1-2 e^{-2 J / K_{B} T}+\cdots\right) \\
& E=E_{g S}+N \cdot \underbrace{(2 J)}_{\Delta_{D W}} \underbrace{e^{-2 J / K_{B} T}}_{D W \cdot \text { density }}+\cdots
\end{aligned}
$$

Thermal correlation length " $\xi$ "

Let's compute $m=\left\langle\sigma_{i}\right\rangle$ and the correlation function

$$
c(r) \equiv\left\langle\sigma_{r} \sigma_{0}\right\rangle
$$

When $B=0, \quad T>0$, it is easy to see $\langle\sigma\rangle=0$ by symmetry:

$$
\begin{aligned}
\left\langle\sigma_{i}\right\rangle & =\frac{1}{Z} \sum_{\{\sigma\}} \sigma_{i} e^{-\beta H[\sigma]} \\
H(\sigma] & =-J \sum_{i} \sigma_{i} \sigma_{i+1}
\end{aligned}
$$

Defining the $\mathbb{Z}_{2}$ "Ising symmetry"

$$
g: \sigma_{i} \longrightarrow-\sigma_{i}
$$

we see $H(-\sigma]=H[\sigma]$ if $B=0$.

So when computing $\sum_{\sigma} \rho_{\sigma} O(\sigma)$, configurations $\sigma,-\sigma$ have equal weight, so $\langle\sigma\rangle=0$.

of course the same logic applies for the all-to-all case, where $I$ said $\langle\sigma\rangle= \pm \bar{m} \neq 0$ for $K_{B} T<J$.

The issue is order of limits for $B, N$ For all-to-all,

$$
\begin{aligned}
& \lim _{N \rightarrow \infty}\left(\lim _{B \rightarrow 0^{+}} m(B, N)\right)=0 \\
& \lim _{B \rightarrow 0^{+}}\left(\lim _{N \rightarrow \infty} m(B, N)\right)=\bar{m} \neq 0 \text { for } T<T_{C}
\end{aligned}
$$

In HW you will also analyze this from Prov of susceptibility $X=\partial_{B} m(B)$

This is possible because $\frac{F}{N}(T, B, N)$ is non-analytic in $T, B$ as $N \rightarrow \infty$.

For ID, $\frac{1}{N} F(T, B)$ is analytic and the two -limits commute.

A physical picture can be obtained from $C(r)=\left\langle\sigma_{r} \sigma_{0}\right\rangle$

For $K_{B} T \ll J$, there is a density $n_{\text {ow }}=e^{-\Delta / K_{B} T^{\prime}} \quad$ D.W. $>$

![](https://cdn.mathpix.com/cropped/2024_02_16_8ad99d9eac551204c94bg-14.jpg?height=243&width=2017&top_left_y=632&top_left_x=81)

The typical size of domains is thus $\xi=\left\langle l_{n}\right\rangle=\frac{1}{n_{D w}}=e^{\Delta / K_{B} T}$

If we measure $\left\langle\sigma_{r} \sigma_{0}\right\rangle$ for $r \ll \xi$, we get +1 because in same domain. But for $r \gg \xi$, there is random - of D.W. in between (Poisson), so $\left\langle\sigma_{r} \sigma_{0}\right\rangle \rightarrow 0$. This suggest something like

$$
\left\langle\sigma_{r} \sigma_{0}\right\rangle \sim e^{-r / \xi}
$$

We can show this analytically via T.M.

$$
\left\langle\sigma_{0} \sigma\right\rangle=\frac{\sum_{\xi \sigma_{1}} \cdots T_{\sigma_{1} \sigma_{0}} \sigma_{0} T_{\sigma_{0} \sigma_{1}} T_{\sigma_{1} \sigma_{2} \cdots T_{\sigma_{1} \sigma_{r}}\left|\sigma_{r}\right| T_{\sigma_{r}} \sigma_{r+1} \mid}^{Z}}{Z}
$$

Viewing $\hat{\sigma}^{2}=\left(\begin{array}{cc}1 & 0 \\ 0 & -1\end{array}\right)$

$$
C(r)=\frac{\operatorname{Tr}\left(\hat{\sigma}^{2} T^{r} \hat{\sigma}^{2} T^{N-r}\right)}{\operatorname{Tr}\left(T^{N}\right)}
$$

We can compute via cigensystem of

$$
\begin{aligned}
& T=e^{\beta J} \mathbb{1}+e^{-\beta J} \hat{\sigma}^{x} \\
& 1+\rangle=\frac{1}{\sqrt{2}}\left(\begin{array}{c}
1 \\
1
\end{array}\right) \quad \lambda_{+}=2 \cosh (\beta J) \\
& 1-\rangle=\frac{1}{\sqrt{2}}\left(\begin{array}{c}
1 \\
-1
\end{array}\right) \quad \lambda_{-}=2 \sinh (\beta J) \\
& T^{r}=\sum_{\alpha= \pm}|\alpha\rangle\langle\alpha| \lambda_{\alpha}^{r} \\
& \left\langle\beta\left|\sigma^{2}\right| \alpha\right\rangle\left\langle\alpha\left|\sigma^{2}\right| \beta\right\rangle \lambda_{\alpha}^{r} \lambda_{\beta}^{N-r}
\end{aligned}
$$

For $N \rightarrow \infty$, this is dominated by $\beta=t$, and $\left\langle\alpha\left|\sigma^{2}\right|+\right\rangle \Rightarrow \alpha=-$. So

$$
c(r)=\frac{\lambda_{-}^{r} \lambda_{+}^{N-r}}{\lambda_{+}^{N}}=\left(\frac{\lambda_{-}}{\lambda_{+}}\right)^{r}
$$

So we indeed find

$$
c(r)=e^{-r / \xi} \quad \frac{1}{\xi} \equiv \ln \left(\frac{\lambda_{+}}{\lambda_{-}}\right)
$$

Since $\frac{\lambda_{t}}{\lambda_{-}}=\tanh (\beta J)$, as $\beta J \rightarrow \infty$

$$
\begin{aligned}
\ln \left(\frac{\lambda_{+}}{\lambda_{-}}\right) & =\ln \left(\frac{1+e^{-2 \beta J}}{1-e^{-2 \beta J}}\right) \\
& =\ln \left(1+2 e^{-2 \beta J}\right) \\
& \simeq 2 e^{-2 \beta J .}
\end{aligned}
$$

So $\xi=\frac{1}{2} e^{\Delta / K_{B} T}, \Delta=2 J$

Agrees with hand-waving argument!

Absence of symmetry breaking in Equilibrium.

Consider a system with $m-$ competing orders, eeg. for Ising $m=2$ with T^ or w 2 . But this could be more general, like water/gas $e+c$.

In ID with local interactions a domain wall between two phases costs some finite energy " $\Delta$ " Phase 1 $\overbrace{}^{+\Delta}$ Phase 2 ...

At finite-T, there will thus be a density $n_{D W} \sim e^{-\Delta / k_{B} T}$ of them. Since they are far apart, they don't interact, and just randomly move around like a free gas.

This means for $T>0$ there are always bubbles, and $C(r) \sim e^{-r / \xi}$ : no true order in ID/ no phase transitions.

For $D>1$ domain walls: are extended

since energy not bounded by $\Delta$, argument doesn't apply!

