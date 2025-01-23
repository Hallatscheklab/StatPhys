Warmups:

(1) Hicrascepic law are lime reversible $\Rightarrow$ In equilibrium:

rate of $A \rightarrow B=$ rate of $B \rightarrow A$

(Only initial cold. can break time ne. spume)

Detail balance:

$$
\begin{gathered}
p(A \rightarrow B)=p(B \rightarrow A) \\
p(A \rightarrow B \mid A) \cdot p(A)=p(B \rightarrow A \mid B) p(B)
\end{gathered}
$$

![](https://cdn.mathpix.com/cropped/2024_02_07_4bb257c57f906ba929a2g-02.jpg?height=908&width=2548&top_left_y=12&top_left_x=191)

![](https://cdn.mathpix.com/cropped/2024_02_07_4bb257c57f906ba929a2g-02.jpg?height=283&width=1732&top_left_y=791&top_left_x=191)

(2)

$$
\begin{aligned}
& P_{\lambda}(E)=\frac{e^{-\beta(E)}}{z}=e^{-\beta(E-F(\lambda))} \\
& F=k_{B}+\ln (z)=\beta^{-1} \ln (z)
\end{aligned}
$$

Non equilibrium Fluctuation Theorems es (Crooks \& Jarzyuski)

Setup: $\quad x(t)=$ microstate of the polymer

![](https://cdn.mathpix.com/cropped/2024_02_07_4bb257c57f906ba929a2g-03.jpg?height=741&width=1541&top_left_y=633&top_left_x=150)

System $=$ polymer + ideal spring

Reservoir = surrounding fluid

Goal: Measure $F\left(\lambda_{f} T\right)-F\left(\lambda_{i} T\right)$

using finite time protocols $\Lambda=\{\lambda(t)\}$

$\begin{array}{ll}t_{i} & t_{f}\end{array}$

Key: External force does nat perform any work in intervals with $\lambda(t)=$ canst. !

Thus, $\frac{P\left(x_{t}^{+} \rightarrow x_{t+1}^{-} \mid \lambda_{t, t+1}, x_{t}^{+}\right)}{P\left(x_{t+1}^{-} \rightarrow x_{t}^{+} \mid \lambda_{t, t+1}, x_{t+1}^{-}\right)}=e^{-\beta Q_{t, t+1}}$ whey $Q_{t, 1+1}$ : heat added to the sicken in $(t, t+1)$

Assumption: Sunup in $\lambda$ dies nd affect $\underline{x}=x_{t}^{-}=x_{+}^{+} \forall t$. - makes sense for polymer + spring.

Generalizing (1), we thus obtain

$$
\begin{aligned}
& \frac{P\left(X \mid \Lambda_{i} x_{i}\right)}{P\left(\tilde{X} \mid \tilde{\Lambda}, x_{f}\right)}=e^{-\beta Q(2)} \\
& \text { Where } X=\left\{x_{i}, x_{1}, x_{2}, \ldots x_{f}\right\} \\
& \text { (time reversed) } \widetilde{X}=\left\{x_{f,} x_{N-11} x_{N-21} . . x_{i}\right\} \\
& \Delta=\left\{\begin{array}{c}
\left.\lambda_{C} \lambda_{i}, \lambda_{1}, \ldots \lambda_{g}\right\}_{3} \\
\sim
\end{array}\right. \\
& \vec{\Lambda}=\left\{\lambda_{f}, \ldots . \lambda_{i}\right\}
\end{aligned}
$$

$$
\begin{aligned}
& \frac{P(x \mid \Lambda)}{P(\tilde{x} \mid \tilde{\Delta})}=\frac{P\left(x \mid \Delta_{1} x_{i}\right) P\left(x_{i} \mid \lambda_{i}\right)}{P\left(\tilde{x} \mid \tilde{\Delta}, x_{f}\right) P\left(x_{j} \mid \lambda_{j}\right)}= \\
& \text { (2) } e^{-\beta C} \frac{P\left(x_{i} \mid \lambda_{i}\right)}{P\left(x_{f} \mid \lambda_{j}\right)}=e^{-\beta Q} \frac{e^{-\beta\left(E_{i}-F_{i}\right)}}{e^{-\beta\left(E_{f}-F_{f}\right)}} \\
& =e^{-\beta(\underbrace{Q-\Delta E}_{-\Delta W}+\Delta F)}=e^{-\beta(\Delta F-W)}(3)
\end{aligned}
$$

Crooks theorem ('Co)

$$
\begin{array}{r}
P(+W \mid \Delta)=\int D X \delta(W-w) P(X \mid \Delta) \\
\stackrel{(3)}{=} \int D \tilde{X} \delta(W+w) P(\tilde{x} \mid \pi) \cdot \\
\cdot e^{-\beta(\Delta F-W)} \\
e^{-\beta(\Delta F-W) P(-W \mid \pi)} \\
\frac{P(+W \mid \Delta)}{P(-W \mid \Delta)}=e^{-\beta(\Delta F-W)} \text { Creeks } \\
\text { Theorem }
\end{array}
$$

From Crooks, we get Jariynski easily

$$
\begin{aligned}
& \left\langle e^{-\beta \omega}\right\rangle_{\Delta}=\int d \omega P(+\omega \mid \Delta) e^{-\beta \omega} \\
& \quad \stackrel{(4)}{=} \int d \omega P(-\omega \mid \tilde{\Delta}) e^{-\beta \omega-\beta(\Delta F-\omega W)} \\
& =e^{-\beta \Delta F} \sqrt{d \omega \Gamma P(-\omega \mid \tilde{\Delta})} \\
& \left\langle e^{-\beta \omega)}\right\rangle_{\Delta}=e^{-\beta \Delta F} \text { Jarzushi } \\
& 1998
\end{aligned}
$$

Jensens in equality $\left\langle e^{-x}\right\rangle \geqslant e^{-\langle x\rangle}$

$$
\begin{aligned}
& \Rightarrow \\
& \left.e^{-\beta(\omega)} \leqslant C e^{-\beta \omega}\right\rangle_{1}=e^{-\beta \Delta F} \\
& \langle w\rangle \geqslant \Delta F \\
& \left\langle\Delta s^{\tan t}\right\rangle \geq 0
\end{aligned}
$$

$$
d E=\left.\frac{\partial E}{\partial \lambda}\right|_{x} d \lambda+\left.\frac{\partial E}{\partial x}\right|_{\lambda} \cdot d x
$$

internal state

