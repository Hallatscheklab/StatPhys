Continuous state space:

Fokker-Planck Equation

Let $X(t) \in \mathbb{R}$ be a stochastic process continuous in time and space.

The master equation reads

$$
\begin{equation*}
\partial_{t} p(x, f)=\int d x^{\prime}\left[w\left(x \mid x^{\prime}\right) p\left(x^{\prime}, t\right)-w\left(x^{\prime} \mid x\right) p(x, t)\right] \tag{1}
\end{equation*}
$$

1 integra- differential eq'n: hard fo solve

Simplification passible if only short jumps are highly likely. (goes bock to Einstein 1905)

$$
\begin{equation*}
t(\xi ; x) \equiv w(x+\zeta ; x) \tag{2}
\end{equation*}
$$

... is sharply peaked in the first variable ("clepsiza") but any slow ty varying in the second variable ("position")

Tee.

$$
f(\xi ; x)=g_{x} \delta_{\xi, 1}^{1}+v_{x}^{2} \delta_{g,-1}
$$

Use $t(\xi, x)$ to rewrite $M E$

$$
\begin{aligned}
& \partial_{t} p(x, t)=\int d f[t(\underbrace{t\left(-\xi_{;} x+\xi\right) p(x+\xi, t)}-t\left(\varphi_{;} x\right) p(x, t)] \\
& \xi \rightarrow-\xi_{\text {in }} 1 \text { term: } t\left(\xi_{;} x-\xi\right) p\left(x-\xi_{1} t\right)
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_03_07_ce5626f1ad9767cc6b8dg-2.jpg?height=416&width=1070&top_left_y=2039&top_left_x=775)

$$
\partial_{+} p(x, t)=\int d \varphi \sum_{l=1}^{\infty} \frac{(-y)}{l !} \frac{\partial^{l}}{\partial x^{l}}[t(\varphi ; x) p(x, t)] \text { (3) }
$$

(note the cancellation in the loo term)

With the jump moments

$$
\alpha_{e}(x, t) \equiv \int d f f^{l} f(f ; x),
$$

(3) can be written as

$$
\begin{array}{r}
\partial_{+p}(x, y)=\sum_{l=1}^{\infty} \frac{(-1)^{l}}{l !} \frac{\partial^{l}}{\partial x^{l}}\left[\alpha_{l}(x, t) p(x, t)\right] \\
\text { Kramers-Moyal expansion }
\end{array}
$$

Expansions are not necessarily useful:

(i) Sane jump moments may be $\infty$.

$\longrightarrow$ useless /il defined

(ii) all enoments finite but series clos notstop.

$\longrightarrow$ work with orivinaleq,

or truncate (adhoe)

(iv) all moments finite and non -vanishing for $0 \leq C \leq v<\infty$.

The Paula therm then says $r=2$

$$
\begin{aligned}
& \partial p(x, t)=-\partial_{x}\left(\alpha_{1}(x, t) p(x, t)\right)+\frac{1}{2} Q^{2}\left[\alpha_{2}(x, t) p(x, t)\right] \\
& \text { Fokker - Hank equation }
\end{aligned}
$$

U. B: Paula theorem.

$$
\begin{aligned}
& \left|\alpha_{n+m}(x)\right|=\left|\int d f g^{n+m}+(y, x)\right| \\
& \left.\left.\frac{\leq}{4} \right\rvert\, \int d\right\}\left.^{2 n} f^{2 n} t(y, x)\right|^{\frac{1}{2}} \cdot\left|\int d \xi^{2 m} t(y, x)\right|^{\frac{1}{2}}
\end{aligned}
$$

Schwartz inequality:

$$
\Rightarrow\left|\alpha_{n+m}(x)\right| \leq\left|\alpha_{2 n}(x)\right|^{1 / 2}\left|\alpha_{2 m}(x)\right|^{1 / 2} .
$$

For $n=r-1$ and $m=1$ we get

$$
\left|\alpha_{\gamma}(x)\right| \leq\left(\left|\alpha_{2 \gamma-2}(x)\right|\left|\alpha_{2}(x)\right|\right)^{1 / 2}
$$

For $\left|\alpha_{N}\right|>0$, we need $2 \gamma-2 \leq \tau$ (otherwise $\alpha_{2 r-2}=0$ by assumption)

$$
\Rightarrow \nabla \leq 2
$$

Ex: Poisson process

$$
\begin{array}{r}
t(\delta ; x)=v \delta_{y+a} . \\
=0 \alpha_{l}=v a l>\theta \forall b
\end{array}
$$

$\Rightarrow$ KM does not truncate.

Now, limit $a \rightarrow 0, v \rightarrow \infty$ so that $r a=v=$ cont.

$$
\begin{aligned}
& \Rightarrow \partial_{t p}(x, t)=-v \partial_{x} p(x, t) \\
& \Rightarrow p(x, t)=p_{0}(x-v t) \ldots
\end{aligned}
$$

approximation not useful $\Rightarrow$ all stochastic effete

Random walk

$$
\begin{aligned}
t\left(y_{1} x\right) & =\varepsilon \delta_{y_{1}}+\varepsilon \delta_{y_{1}-1} \\
\Rightarrow \alpha_{1}(x) & =0 \\
\alpha_{2}(x) & =2 \varepsilon a^{2} \\
\alpha_{u}(x) & =\varepsilon a^{4} \text { (u even) }
\end{aligned}
$$

$$
\alpha_{n}(x)=0 \quad \text { (node) }
$$

$=0$ KM expansion still does not terminate.

BUT the re is a useful scaling limit

$a \rightarrow 0$
$\varepsilon \rightarrow \infty$ such that $D=\varepsilon a^{2}$ finite.

$\rightarrow \alpha_{n>2} \rightarrow 0$ and

$$
\partial_{p} p(x, t)=D \partial_{x} \partial_{p}(x, t)
$$

for $p(x, 0)=\delta(x)$, we finds

$$
p(x, t)=\frac{1}{\sqrt{4 \pi D t}} \exp \left(-\frac{x^{2}}{4 D t}\right)
$$

via a Fourier transform.

![](https://cdn.mathpix.com/cropped/2024_03_07_ce5626f1ad9767cc6b8dg-7.jpg?height=402&width=939&top_left_y=2104&top_left_x=494)

