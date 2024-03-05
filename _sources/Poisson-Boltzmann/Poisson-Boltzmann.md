## Charge screening by counter ions - plasmas



When we discussed our variational approach and mean field theory, the question came up what happens when the two-body potential energy decays slowly, like the eletrostatic potential $U= e^2/(4\pi r^{2})$? Then,

$$
\langle H\rangle_N\propto \int d^3r U(r)=4\pi \int_{r_0}^\infty r^2 U(r) dr = e^2 \int_{r_0}^\infty dr=\infty\;.
$$

Thus, the interactions are too strong to apply our previous mean field /variational approaches, which assumed we can approximate the true gas by a modified version of the ideal gas. 

Fortunately, there's another mean-field theory: Debye-Hückel.

But first, a quick ...


### Recap electrostatics

Gauß's law for electricity in differential form

$$
\nabla \cdot \mathbf{E}=\rho/(D\epsilon_0)
$$

where $\rho(\vec r)$ is the charge density and $D$ is the dielectric constant of the medium, assumed to be constant ($D\approx 80$ in water!).

In the absence of a magnetic field, the curl of the electric field vanishes, so that we can express the express $\mathbf{E}$ in terms of an electrical potential $V$, 

$$
\mathbf{E} = -\nabla V \;.
$$

Gauß's law thus turns into the Poisson equation

$$
\nabla^2 V=-\rho/(D\epsilon_0)\;.
$$

For discrete charges $q_i$,

$$
\rho=\sum_i q_i \delta(\vec r- \vec r_i) \;,
$$

We can express the total electrostatic interaction energy as

$$
U=\frac12 \int V(\vec r) \rho(\vec r)
$$















### Debye screening

Suppose there are two types of ions, $q_{\pm}=\pm z e$, where $z$ is the charge number and "+" refers to a cation and "-" to anion. Let's describe the ion density by $n_{\pm}$, which is on average $n_\infty$. For example, inside cells there are lots of sodium (Na+), potassium (K+), and chloride (Cl-) at around $n_\infty\sim 100 mM$ each. What happens if we introduce an extra charge at the origin?

**Intuitively:**

![Debye screening](../figures/Debye-screening.jpg)



How to describe the density $c(x)$ of charges and the electric potential $V(x)$?

What's the shape of the charge distribution? 

- The Boltzmann distribution dictates the density given the electrostatic potential 

$$c_{ \pm}(x)=e^{-\frac{ \pm z e V(x)}{k T}} \cdot c_{\infty}$$ (elec-potential)

- But the electric potential $V(x)$ depends on the density via the Poisson equation (in 1D):

$$\quad \partial_{x}^{2} V(x) \cong-\frac{\rho(x)}{\varepsilon_{0} D}=-\frac{c_{+}(x) z e-c_{-}(x) z e}{\varepsilon_{0} D}
$$ (poisson)

- {eq}`elec-potential` and {eq}`poisson` have to be solved self-consistently, which is hard in general.

But when $q V \ll K T$ (ie. assume $x \gg l_{\beta}$ ), we can expand: $c_{ \pm}=c_{\infty}\left(1 \mp \frac{z e V(x)}{k T}\right)$

$$
\partial_{x}^{2} V=\frac{2(z e)^{2} c_{\infty} V(x)}{\varepsilon_{0} D k T} 
$$

So, the electrical potential decays exponentially,

$$
V(x) \sim e^{-\frac{x}{\lambda_{D}}} 
$$

on a length scale called the Debye screening length,

$$
\lambda_{D}=\sqrt\frac{\epsilon_0 D k_BT}{2(ze)^2 c_\infty} \;.
$$

Ex: Inside biological physiological conditions, $\lambda_D\approx 0.8$ nm.


Boundary conditions @ $x=0$: $E \stackrel{!}{=} \frac{\sigma}{\varepsilon_{0} D}=-\frac{d V}{d x}$

$$
\begin{aligned}
& \Rightarrow V(x)=\frac{\sigma \lambda_{D}}{\varepsilon_{0} D} e^{-\frac{x}{\lambda_{D}}} \\
& g(x)=-\varepsilon_{0} D \partial_{x}^{2} V=-\frac{\sigma}{\lambda_{D}} e^{-\frac{x}{\lambda_{D}}}
\end{aligned}
$$

rem: our assumption $q V \gg k_{B} T$ works well for proteins

![](https://cdn.mathpix.com/cropped/2024_03_05_6d0b0833bad953ee6990g-3.jpg?height=299&width=1270&top_left_y=1232&top_left_x=536)

```{note} Significance of Debye screening:

For distances $>\lambda_D$, charges are not "felt" by others. This is essential to the "laws" of protein binding via non-covalent bonds:

![](https://cdn.mathpix.com/cropped/2024_03_05_6d0b0833bad953ee6990g-4.jpg?height=369&width=750&top_left_y=746&top_left_x=733)

- Binding requires complementary surface shapes and charge distributions.
- Even if complimentary charges get close, interaction potentials barely exceeds $k_BT$ (technically, because thermal fluctuations let charges fluctuate on a scale comparable to $\lambda_D$) $\Rightarrow$ need several electrostatic bonds.
- together, this implies that binding is highly specific
- Bulk structure and bulk charge distribution are  less critical to binding.
- caveat: The last decade has revealed that weak binding due to unspecific binding between intrinsically disordered proteins can generate protein condensates that form membrane-less droplet-like organelles -> hot/hyped field.
```
