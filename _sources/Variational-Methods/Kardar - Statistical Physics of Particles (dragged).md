# 5 <br> Interacting particles 

### 5.1 The cumulant expansion

The examples studied in the previous chapter involve non-interacting particles. It is precisely the lack of interactions that renders these problems exactly solvable. Interactions, however, are responsible for the wealth of interesting materials and phases observed in nature. We would thus like to understand the role of interactions amongst particles, and learn how to treat them in statistical mechanics. For a general Hamiltonian,

$$
\begin{equation*}
\mathcal{H}_{N}=\sum_{i=1}^{N} \frac{\vec{p}_{i}^{2}}{2 m}+\mathcal{U}\left(\vec{q}_{1}, \cdots, \vec{q}_{N}\right) 
\end{equation*}
$$

the partition function can be written as

$$
\begin{align*}
Z(T, V, N) & =\frac{1}{N !} \int \prod_{i=1}^{N}\left(\frac{\mathrm{d}^{3} \vec{p}_{i} \mathrm{~d}^{3} \vec{q}_{i}}{h^{3}}\right) \exp \left[-\beta \sum_{i} \frac{\vec{p}_{i}{ }^{2}}{2 m}\right] \exp \left[-\beta \mathcal{U}\left(\vec{q}_{1}, \cdots, \vec{q}_{N}\right)\right] \\
& \left.=Z_{0}(T, V, N) \exp \left[-\beta \mathcal{U}\left(\vec{q}_{1}, \cdots, \vec{q}_{N}\right)\right]\right\rangle^{0}
\end{align*}
$$

where $Z_{0}(T, V, N)=\left(V / \lambda^{3}\right)^{N} / N$ ! is the partition function of the ideal gas (Eq. (4.73)), and $\langle\mathcal{O}\rangle^{0}$ denotes the expectation value of $\mathcal{O}$ computed with the probability distribution of the non-interacting system. In terms of the cumulants of the random variable $\mathcal{U}$, Eq. (5.2) can be recast as

$$
\begin{equation*}
\ln Z=\ln Z_{0}+\sum_{\ell=1}^{\infty} \frac{(-\beta)^{\ell}}{\ell !}\left\langle\left. U^{\ell}\right|_{c} ^{0}\right. \tag{5.3}
\end{equation*}
$$

The cumulants are related to the moments by the relations in Section 2.2. Since $\mathcal{U}$ depends only on $\left\{\vec{q}_{i}\right\}$, which are uniformly and independently distributed within the box of volume $V$, the moments are given by

$$
\begin{equation*}
\left\langle\mathcal{U}^{\ell}\right\rangle^{0}=\int\left(\prod_{i=1}^{N} \frac{\mathrm{d}^{3} \vec{q}_{i}}{V}\right) \mathcal{(}\left(\vec{q}_{1}, \cdots, \vec{q}_{N}\right)^{\ell} \tag{5.4}
\end{equation*}
$$

Various expectation values can also be calculated perturbatively, from

$$
\begin{align*}
\langle\mathcal{O}\rangle & =\frac{1}{Z} \frac{1}{N !} \int \prod_{i=1}^{N}\left(\frac{\mathrm{d}^{3} \vec{p}_{i} \mathrm{~d}^{3} \vec{q}_{i}}{h^{3}}\right) \exp \left[-\beta \sum_{i} \frac{\vec{p}_{i}^{2}}{2 m}\right] \exp \left[-\beta \mathcal{U}\left(\vec{q}_{1}, \cdots, \vec{q}_{N}\right)\right] \times \mathcal{O}  \tag{5.5}\\
& =\frac{\langle\mathcal{O} \exp [-\beta \mathcal{U}]\rangle^{0}}{\langle\exp [-\beta \mathcal{U}]\rangle^{0}}=\left.\mathrm{i} \frac{\partial}{\partial k} \ln \langle\exp [-\mathrm{i} k \mathcal{O}-\beta \mathcal{U}]\rangle^{0}\right|_{k=0} .
\end{align*}
$$

The final expectation value generates the joint cumulants of the random variables $\mathcal{O}$ and $\mathcal{U}$, as

$$
\begin{equation*}
\ln \langle\exp [-\mathrm{i} k \mathcal{O}-\beta \mathcal{U}]\rangle^{0} \equiv \sum_{\ell, \ell^{\prime}=1}^{\infty} \frac{(-\mathrm{i} k)^{\ell^{\prime}}}{\ell^{\prime} !} \frac{(-\beta)^{\ell}}{\ell !}\left\langle\mathcal{O}^{\ell^{\prime}} * \mathcal{U}^{\ell}\right\rangle_{c}^{0} \tag{5.6}
\end{equation*}
$$

in terms of which ${ }^{1}$

$$
\begin{equation*}
\langle\mathcal{O}\rangle=\sum_{\ell=0}^{\infty} \frac{(-\beta)^{\ell}}{\ell !}\left\langle\mathcal{O} * \mathcal{U}^{\ell}\right\rangle_{c}^{0} \tag{5.7}
\end{equation*}
$$

The simplest system for treating interactions is again the dilute gas. As discussed in chapter 3 , for a weakly interacting gas we can specialize to

$$
\begin{equation*}
\mathcal{U}\left(\vec{q}_{1}, \cdots, \vec{q}_{N}\right)=\sum_{i<j} \mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right) \tag{5.8}
\end{equation*}
$$

where $\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right)$ is a pairwise interaction between particles. The first correction in Eq. (5.3) is

$$
\begin{align*}
\langle\mathcal{U}\rangle_{c}^{0} & =\sum_{i<j} \int \frac{\mathrm{d}^{3} \vec{q}_{i}}{V} \frac{\mathrm{d}^{3} \vec{q}_{j}}{V} \mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right)  \tag{5.9}\\
& =\frac{N(N-1)}{2 V} \int \mathrm{d}^{3} \vec{q} \mathcal{V}(\vec{q})
\end{align*}
$$

The final result is obtained by performing the integrals over the relative and center of mass coordinates of $\vec{q}_{i}$ and $\vec{q}_{j}$ separately. (Each of the $N(N-1) / 2$ pairs makes an identical contribution.)

The second-order correction,

$$
\begin{equation*}
\left\langle\mathcal{U}^{2}\right\rangle_{c}^{0}=\sum_{i<j, k<l}\left[\left\langle\left.\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right) \mathcal{V}\left(\vec{q}_{k}-\vec{q}_{l}\right)\right|^{0}-\left\langle\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right)\right\rangle^{0}\left\langle\mathcal{V}\left(\vec{q}_{k}-\vec{q}_{l}\right)\right\rangle^{0}\right],\right. \tag{5.10}
\end{equation*}
$$

is the sum of $[N(N-1) / 2]^{2}$ terms that can be grouped as follows:

(i) There is no contribution from terms in which the four indices $\{i, j, k, l\}$ are different. This is because the different $\left\{\vec{q}_{i}\right\}$ are independently distributed, and $\left\langle\left.\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right) \mathcal{V}\left(\vec{q}_{k}-\vec{q}_{l}\right)\right|^{0}\right.$ equals $\left\langle\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right)\right\rangle^{0}\left\langle\mathcal{V}\left(\vec{q}_{k}-\vec{q}_{l}\right)\right\rangle^{0}$.

(ii) There is one common index between the two pairs, for example, $\{(i, j),(i, l)\}$. By changing coordinates to $\vec{q}_{i j}=\vec{q}_{i}-\vec{q}_{j}$ and $\vec{q}_{i l}=\vec{q}_{i}-\vec{q}_{l}$, it again follows that $\left\langle\left.\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right) \mathcal{V}\left(\vec{q}_{i}-\vec{q}_{l}\right)\right|^{0}\right.$ equals $\left\langle\left.\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{j}\right)\right|^{0}\left\langle\left.\mathcal{V}\left(\vec{q}_{i}-\vec{q}_{l}\right)\right|^{0}\right.\right.$. The vanishing of these

1 While this compact notation is convenient, it may be confusing. The joint cumulants are defined through Eq. (5.6), and for example $\left\langle 1 * \mathcal{U}^{\ell}\right\rangle_{c}=0\left(\neq\left\langle\mathcal{U}^{\ell}\right\rangle_{c}\right)$, while $\left\langle 1 * \mathcal{U}^{0}\right\rangle_{c}=1$ !

