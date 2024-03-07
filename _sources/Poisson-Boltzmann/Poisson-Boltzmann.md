## Debye-Hückel theory - charge screening 



When we discussed our variational approach and mean field theory, the question came up what happens when the two-body potential energy decays slowly, like the eletrostatic potential $U= e^2/(4\pi r)$? Then,

$$
\langle H\rangle_N\propto \int d^3r U(r)=4\pi \int_{r_0}^\infty r^2 U(r) dr = e^2 \int_{r_0}^\infty r dr=\infty\;.
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
$$ (interaction)















### Debye screening

Suppose there are two types of ions, $q_{\pm}=\pm z e$, where $z$ is the charge number and "+" refers to a cation and "-" to anion. Let's describe the ion density by $n_{\pm}=\langle \rho_{\pm}\rangle/q_{\pm}$, which we suppose is equal to $n_\infty$ for both ion types far from any perturbation. For example, inside cells there are lots of sodium (Na+), potassium (K+), and chloride (Cl-) at around $n_\infty\sim 100 mM$ each. What happens if we introduce an extra charge at the origin?

**Intuitively:**

![Debye screening](../figures/Debye-screening.jpg)



How to describe the density $\rho(x)$ of charges and the electric potential $V(x)$?

What's the shape of the charge distribution? 

- The Boltzmann distribution dictates the density given the electrostatic potential 

$$n_{ \pm}(r)=e^{-\frac{ q_{\pm} V(r)}{k T}} \cdot n_{\infty}$$ (elec-potential)

- But the electric potential $V(r)$ depends on the density via the Poisson equation (in 1D):

$$\quad \nabla^{2} V(r) =-\frac{\rho(r)+\rho_{ext}(r)}{\varepsilon_{0} D}=-\frac{n_{+}(r) z e-n_{-}(r) z e}{\varepsilon_{0} D}-\frac{\rho_{ext}(r)}{\varepsilon_{0} D}
$$ (poisson)

- where we introduced an externally fixed charge density $\rho_{ext}(r)$.

- {eq}`elec-potential` and {eq}`poisson` have to be solved self-consistently, which is hard in general.

But when $q V \ll K T$ (ie. assume $x \gg l_{\beta}$ ), we can expand: $n_{ \pm}=n_{\infty}\left(1 \mp \frac{z e V(r)}{k T}\right)$

$$
\nabla^{2} V=\frac{2(z e)^{2} c_{\infty} V(r)}{\varepsilon_{0} D k T} -\frac{\rho_{ext}(r)}{\varepsilon_{0} D}\equiv\kappa_D^2V(r) -\frac{\rho_{ext}(r)}{\varepsilon_{0} D}\;.
$$

In Fourier space, this equation reads

$$
(-q^2-\kappa_D^2)V(q)=-\frac{\rho_{ext}}{D\epsilon_0}
$$

$$
V(q)=\frac{\rho_{ext}}{D\epsilon_0} \frac{1}{q^2+\kappa_D^2}
$$


So, the electrical potential of a point charge $\rho_{ext}(q)=1$ decays exponentially,

$$
V_{\text{eff}}= \frac{1}{4 \pi r D \epsilon_0} e^{-\frac{x}{\lambda_{D}}}
$$ (Yukawa)

on a length scale called the Debye screening length,

$$
\lambda_{D}=\sqrt\frac{\epsilon_0 D k_BT}{2(ze)^2 c_\infty} \;.
$$

The potential in {eq}`Yukawa`is called "Yukawa potential".

```{note} Where did the above analysis make a mean field approximation?

We light-heartedly assumed that the probability of a charge distribution,

$$ 
p({\rho})\propto e^{-\beta U} \;,\propto e^{-\beta\langle V(\vec r) \rho(\vec r)}
$$

with the interaction energy $U$ given by {eq}`interaciton`, can be written as

$$
p({\rho})\propto e^{-\beta\int \langle V(\vec r) \rho(\vec r)}
$$

This ignores that terms of order $\int \delta V \delta \rho$, where $\delta V=V-\langle V\rangle$ and $\delta \rho=\rho-\langle \rho\rangle$
```


```{note} Significance of Debye screening for protein binding:

Inside biological cells, $\lambda_D\approx 0.8$ nm due to ion concentrations in the 100mM range. Since proteins have typical diameter of $4$ nm, electrostatic protein-protein interactions usually play out on their surfaces:

![](https://cdn.mathpix.com/cropped/2024_03_05_6d0b0833bad953ee6990g-4.jpg?height=369&width=750&top_left_y=746&top_left_x=733)

- Binding requires complementary surface shapes and charge distributions.
- Even if complimentary charges get close, interaction potentials barely exceeds $k_BT$ (technically, because thermal fluctuations let charges fluctuate on a scale comparable to $\lambda_D$) $\Rightarrow$ need several electrostatic bonds.
- together, this implies that binding is highly specific
- Bulk structure and bulk charge distribution are  less critical to binding.
- caveat: The last decade has revealed that weak binding due to unspecific binding between intrinsically disordered proteins can generate protein condensates that form membrane-less droplet-like organelles -> hot/hyped field.
```


rem: our assumption $q V \gg k_{B} T$ works well for proteins

![](https://cdn.mathpix.com/cropped/2024_03_05_6d0b0833bad953ee6990g-3.jpg?height=299&width=1270&top_left_y=1232&top_left_x=536)
