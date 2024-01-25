Principles of classical statistical mechanics Vardar Ch. 4

Note: We skipped
- Ch I an thermos: pare requisite - ch 3 on kin theory some of
this comes later

Today: - Max Ext principle in stat mech.
- thermal "equilibrium"

$\sigma \frac{1}{T} \equiv \frac{\partial S}{\partial E}$
- spotaneons reactions
- gen. coordinates and work

Classical Statistical Mechanics

equilibrium

- Basic principle: Jun an isolated system, all allowed (sec" érgaokicity hypothesis" "n Wiki"

microstates are equally likely.

$$
\leftrightarrow \text { Max EnTropy! }
$$

$\left(\vec{q}_{1}, \ldots \vec{a}_{N}\right)$

Let $\mu=\{q, p\}$ a point in $6 \mathrm{ND}$ dim. ph. space: $\left(\vec{p}_{1}, \ldots p_{N}\right)$

$$
P_{E}(\mu) d \mu \equiv \frac{1}{\Omega(E)} \delta(E-H(\mu)) d \mu
$$

micro-canouical ensemble

where $\Omega(E) \equiv \int d \mu \delta(E-H(\mu))$ is the density of microstates consistent with $H=E$
$\left(" D .0 . S^{\text {s }}\right.$ )

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-02.jpg?height=445&width=380&top_left_y=2264&top_left_x=312)

insulation

N.B.: - if states are discrete, esq. for Is ing spins $\sigma_{i}= \pm 1, \int d \mu \rightarrow \sum_{\mu}$

$$
\delta(E-H(u)) \rightarrow \delta_{E_{1} H}
$$

- Postulate implies

$$
\begin{aligned}
\langle f\rangle_{E} & =\lim _{T \rightarrow \infty} \frac{1}{T} \int_{0}^{T} f(\mu(t)) d t \\
& =\int d \mu P_{E}(\mu) f(\mu) .
\end{aligned}
$$

Longtime average $\rightarrow$ ensemble

The celebrated ergadicity theorem explains why ( $x$ ) is to be expected for Hamiltonian dynamics. (later)

But we can also argue for (*) to be the most un biased (Max End) dist. subject to $H=E=$ canst

Recall: entropy of a prob. dist: is $S=-\sum_{i} P_{i} \ln \left(P_{i}\right)$, which is maximized for $P_{i}=$ canst $=\frac{1}{\Omega(E)}$ In that case, $S=\ln (\Omega)$.

Historically, Boltzmann defined $S \equiv k_{B} \ln (2)$ with $\left[k_{B}\right]=J / k$ a historical con venation.

N.1.: - Do continuous state space$\Omega$ is dimension fol.

$$
[\Omega]=([p][q])^{3 N} \cdot[E]^{-1} .
$$
- to obtain a sensible difinition of $S$, we should define

$$
S=k_{B} \ln \left(\frac{\Omega}{[\Omega]}\right) .
$$

- However, only differences $S\left(E_{1}\right)-S\left(E_{2}\right)$ matter in classical stat mech $\rightarrow \Delta S=k_{B} \ln \left(\frac{\Omega_{1}}{\Omega_{2}}\right)$ is coll-defined.

- $Q M \Rightarrow$ units of $[p] \cdot[q]=h$. well-defined.

Thermal equilibrium

Consider is cleared system $\{\mu, E\}$ consisting of tiro subsystems

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-06.jpg?height=393&width=1192&top_left_y=744&top_left_x=396)

$$
\begin{aligned}
& \mu=\mu_{1} \otimes \mu_{2} . \\
& E=E_{1}+E_{2}+\text { surface confillo. }
\end{aligned}
$$

NB.:
- $E_{1}, E_{2}$ cere extensive $(\alpha, N, V)$

- surface contrib_ does nat grow awl system size if inter actions are local $\rightarrow$ negligible as $N / t \rightarrow \infty$

$$
\begin{aligned}
\Rightarrow & P_{E}(\mu)=\frac{1}{\Omega(E)} \delta(E-H(\mu)) \\
& H(\mu)=H_{1}\left(\mu_{1}\right)+H_{2}\left(\mu_{2}\right)+\text { h. at. }
\end{aligned}
$$

$$
\begin{aligned}
\Omega(E) & =\int d \mu_{1} d \mu_{2} \delta(E-H(\mu)) \\
& =\int d E_{1} \Omega_{1}\left(E_{1}\right) \Omega_{2}\left(E-E_{1}\right) \\
e^{S(E) / k_{B}} & =\int d E_{1} e^{\left[S_{1}\left(E_{1}\right)+S\left(E-E_{1}\right)\right] / k_{B}}
\end{aligned}
$$

$S_{1}, S_{2}$ extensive:

$$
S(E)=N s_{1}\left(\frac{E_{1}}{N}\right)+N s_{2}\left(\frac{E-E_{1}}{N}\right)
$$

$\Rightarrow$ as $N \rightarrow \infty$
$\Delta$ deminated boy.meximum of inbeprond, i.e.

$$
S(E) \approx S_{1}\left(E_{1}^{*}\right)+S_{2}\left(E_{2}^{*}=E-E_{1}\right)
$$

where

$$
\begin{aligned}
0 & \left.\left.=\frac{d}{d E_{1}} \right\rvert\, \int_{E_{1}^{x}} S_{1}\left(E_{1}\right)+S_{2}\left(E-E_{1}\right)\right]= \\
& =\left.\frac{d S_{1}}{d E_{E_{1}}}\right|_{E_{1}^{x}}-\left.\frac{d S_{2}}{d E_{2}}\right|_{E_{2}^{x}=E-E_{1}}
\end{aligned}
$$

Defining $\frac{1}{T}=\frac{d S}{d E}, E^{*}$ is set by

$$
\frac{1}{T_{1}}=\frac{1}{T_{2}}
$$
$\Rightarrow$ we identify $T=\frac{d E}{d S}$ as the teu perature

Noto: $t$ adjucts itself so as to maximize $S$.

If we prepare initial cond. where $E_{i} \neq E_{1}^{N}$, by ergedicity $E_{i} \rightarrow E_{i}^{*}$ at long fime banse $E_{i}^{*}$ is mula more likely.

$$
\Delta S=S_{1}^{\prime}\left(E_{1}^{*}\right)+S_{2}\left(E_{2}^{*}\right)-S\left(E_{1}\right)-S\left(E_{2}\right) \geq 0
$$

To first arder in $E_{1}^{*}-E_{1}=\delta E_{1}$

$$
\left(\frac{1}{T_{1}}-\frac{1}{T_{2}}\right) \delta E_{1} \geqslant 0
$$

$\Rightarrow$ Everyy flews form hat $\rightarrow$ cald.

Stability: Since the point $\left(E_{1}^{*} E_{2}^{*}\right)$ is a maximum of $S\left(E_{1}^{*}\right)+S_{2}\left(E-E_{1}^{*}\right)$ we must have

$$
\left.\frac{\partial^{2} S_{1}}{\partial E^{2}}\right|_{x_{1}}+\left.\frac{\partial^{2} S_{2}}{\partial E_{2}^{2}}\right|_{x_{2}} \leq 0
$$

Suppose both systems are identical, $S_{1}=S_{2}$

$$
\left.\Rightarrow \partial_{t}^{2} S\right|_{x} \leq 0 \Rightarrow \text { S is concave }
$$

Also, since $\left.\partial_{E} S\right|_{x}=T^{-1}$, we have $\left.\frac{\partial E}{\partial T}\right|_{x} \geq 0$.

specific heat $C_{x} \geqslant 0$

Manipulating therma dyn. coordinets e.y.

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-12.jpg?height=507&width=608&top_left_y=346&top_left_x=473)

$$
: \underline{x} \rightarrow \underline{x}+\underline{\delta x}
$$

$$
\text { reversibly }
$$

change in $E: E \rightarrow E+f \cdot \partial \underline{x}$

$$
\begin{aligned}
\delta S= & S\left(E+f \cdot \frac{d x}{x}, \underline{x}+\underline{\partial x}\right)- \\
& -S(E, \underline{x})= \\
= & \left.\frac{\partial S}{\partial t}\right|_{x}\left(\underline{f}(\underline{d x})+\left.\frac{\partial S}{\partial x}\right|_{E} \delta x \geq 0\right.
\end{aligned}
$$

$$
\text { én inilitar }
$$

revesilde $\rightarrow "=0$.

$$
\left.\Rightarrow \frac{\partial S}{\partial x_{1}}\right|_{E_{1} x_{j+i}}=-\frac{J_{i}}{T}
$$

$$
\begin{gathered}
\Rightarrow d S(E, x)=\frac{d E}{T}-\frac{F \frac{d x}{T}}{T} \\
\Rightarrow \underbrace{T d S}_{d Q}+J d x
\end{gathered}
$$

Hent.

Glass of water, Biological cells, e tc. are open systems

$\Rightarrow$ trade E,V,N with environment

(aka reservoir)

- Energy exchange: system $(S)+$ reservoir $(R)=$ composite

system has fixed $E \rightarrow$ is isolated

bath $\Rightarrow$ all states $w / E_{S}+E_{B}=E$ are equally likely.

What's probability $P\left(\mu_{s}\right)$ of System to be in state $r_{S}$, irrespective of lath's state?

$$
\begin{aligned}
P\left(\mu_{S}\right) & =\sum_{\mu_{S}} P\left(\mu_{S}, \mu_{R}\right)=\frac{\Omega_{R}\left(E-E_{S}\right)}{\Omega(E)} \\
& E_{R}=E-E_{S}\left[\Omega\left(E_{1}, N\right)\right]^{-1} \\
& \Rightarrow\left(P\left(\mu_{S}\right) \propto \Omega_{R}\left(E-E_{S}\right)\right.
\end{aligned}
$$

Or, using $S_{b} \equiv k_{B} \ln \Omega_{R}$,

$$
P\left(v_{S}\right) \propto e^{\hat{k}{ }^{-1} S_{R}\left(E-E_{S}\right)}
$$

Bath is big $\rightarrow$ Taylor expand:

$$
S_{R}\left(E-E_{S}\right)=S_{R}(E)+\left(\frac{\partial S_{R}}{\partial E}\right)_{K N}\left(-E_{S}\right)+\text { het. }
$$

lusert in (1):

$$
P\left(\mu_{S}\right) \propto \exp \left(\text { const. }-k_{B}^{-1}\left(\frac{\partial S_{R}}{\partial E_{1}}\right)_{\mathbb{N}_{S}} E_{S}\right) \propto e^{-b E_{S}}
$$

This is the Boltrmann factor $e^{-\beta E_{S}}$ if we identify $b$ and $\beta_{R} \equiv \frac{1}{k_{B} T_{b}}$.

$$
\begin{aligned}
& \Rightarrow \beta_{R} \equiv\left(\frac{\partial \ln l_{R}}{\partial E}\right)_{V, N}=\frac{1}{k_{B}}\left(\frac{\partial S_{R}}{\partial E}\right)_{V, N} \\
& \text { or } T_{R}^{-1}=\left(\frac{\partial S_{R}}{\partial E}\right)_{V, N} \quad \begin{array}{l}
\text { Thermady } \\
\text { def. Aftemperature } \\
\text { of the reservere }
\end{array}
\end{aligned}
$$

$\Rightarrow$ - Likelitioal natio of two microrerts

$$
\frac{P\left(\gamma_{s}^{(1)}\right)}{P\left(v_{s}^{(2)}\right)}=e^{-\frac{E_{s}^{(2)}-E_{s}^{(1)}}{k_{B} T}}=e^{-\frac{\Delta E}{k_{B} T}}
$$

fully coutrolled by multiplicity of
- $\beta_{R}=\frac{1}{k_{B}{ }^{T}}$ : How willing reservoive gives eneryy; elepends on hew rapiellyp state space shrinks.

$$
\cdot k_{B} T_{\text {Rooln }} \approx 4 k_{B 3} T_{\text {mm }} \approx 0,25 \mathrm{meV}
$$

Excrise: compare kBT w. $\Delta E$
- Gramity : $\Delta E=m g h$

$$
\frac{p(h)}{p(0)}=e^{-\frac{h}{\lambda}}, \lambda=\frac{k_{B} T}{m y} \approx 8 k m
$$
- Bending of biopolymer tending

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-16.jpg?height=497&width=1635&top_left_y=1481&top_left_x=303)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-16.jpg?height=310&width=1068&top_left_y=1869&top_left_x=1056)
- Electrostatic altraction

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-16.jpg?height=423&width=1750&top_left_y=2220&top_left_x=368)

we will see hav this cantrols pratein-pontein interations.

What is the probability that System has energy $E_{s}$ ?

$=$ Probe that system is in one of states with energy Es

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-18.jpg?height=372&width=970&top_left_y=0&top_left_x=515)

Lecture 4

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-19.jpg?height=663&width=530&top_left_y=504&top_left_x=69)

Intro to Silt. Mech. of

the Cell.

$\Omega_{S / b}\left(E_{S / b}\right):$ Nr of micrestates $v_{S / B}$ of system/bath.

$$
P\left(E_{s}\right) \propto \Omega_{s}\left(E_{s}\right) e^{-\beta E_{s}}
$$

has a sharp peak at $E_{s}=\left\langle E_{s}\right\rangle=U$ (called "internal energy"j

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-19.jpg?height=182&width=1824&top_left_y=1766&top_left_x=277)

$$
\left(\frac{\partial S_{b}}{\partial t}\right)^{-1}=\left(k_{B} \frac{d l_{u} \Omega_{b}}{d E^{2}}\right)^{-1}=T_{b}=T_{S}=\left(k_{B} \frac{d l_{u} \Omega_{S}}{d E_{\delta}}\right)^{-1}=\left(\frac{\partial S_{S}}{\partial E_{S}}\right)^{-1}
$$

Equilibrium

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-19.jpg?height=288&width=1914&top_left_y=2486&top_left_x=162)
Puling on molecular motor. $\quad \approx(0 \pm+3) k_{B} T$

Normalization:

Partition $Z \equiv \int d E_{S} \Omega_{s}\left(E_{s}\right) e^{-\beta E_{s}} \Rightarrow P\left(E_{s}\right)=\frac{\Omega_{s}\left(E_{S}\right) e^{-\beta E_{s}}}{Z}$

Jularge systems, $z \approx \Omega_{S}\left(\omega e^{-\beta u)}\right.$ (Saddle paint approx) Free Energy $A=-k_{B} T \ln Z \stackrel{!}{=}-k_{B} T \ln \Omega_{S}(U)+U=\underline{U-T S_{S}}$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-20.jpg?height=232&width=2068&top_left_y=1006&top_left_x=20)

Spoutaneans Reactions (Change in macro state of the system):

$\Delta S_{\text {tot }} \geq 0 \quad$ (Second law)

heat added to system

$$
\Delta S_{S}+\Delta S_{b}=\Delta S_{S}-\frac{Q^{\Delta^{2}}}{T_{b}} \geqslant 0
$$

$\left(Q \equiv-\Delta E_{b}\right)$

$\Rightarrow \Delta S_{S} \geqslant \frac{Q}{T_{b}}$ Clausius inequality "il leif process is

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-20.jpg?height=246&width=1818&top_left_y=2093&top_left_x=270)

added to
system $\Delta E_{S}$ work dene by the system

$$
W=0 \stackrel{C J}{=} \quad \Delta A=U-T \Delta S_{S} \leq 0
$$
$=0$ - Spontaneous reactions reduce free energy A
- Equilibrimen $\cong$ na spant.reach. $\Rightarrow A$ is minimal.

$$
\begin{aligned}
& \text { If } Q=u+W_{\text {useful }} \\
& \text { Eyeful work done by system. } \\
& =0 \quad v_{\text {useful }} \leqslant-\Delta A
\end{aligned}
$$

Example:

Mast cellular processes are powered by

$$
A T P \rightarrow A D P+P_{i}
$$

Well later show that $\triangle A_{A T P} \approx 2 O k T$ in the all

(depends on ion court)

$\Delta A_{A T P}$ is used to do useful work in the cell.

egg vesicle transport

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-21.jpg?height=547&width=813&top_left_y=1775&top_left_x=925)

$$
\begin{gathered}
\text { Wars }=F \cdot \Delta r \leq \Delta A \\
\Delta r(\text { Kinesin }) \approx 8 \mathrm{~nm} \Rightarrow \begin{aligned}
F & \leq \frac{20 \mathrm{kT}}{8 \mathrm{~nm}}=\frac{20 \cdot 4 \mathrm{pN} \mathrm{nm}}{8} \\
& \approx 10 \mathrm{p} \mathrm{N} .
\end{aligned}
\end{gathered}
$$

Measurement shows $F_{\text {stall }}=5-7$ pH (Visscher, Schnitzer, Block Nature 'Mg) deparalin on AP care. Suppl. Reading

Summary.Addendum:

Work done bysystem:

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-22.jpg?height=344&width=334&top_left_y=0&top_left_x=1223)

2nd law: $\langle\delta W \leq-\Delta A \quad$ (sige
More generally: $\left\langle e^{+\beta \delta W}\right\rangle=e^{-\beta \Delta A}$

(*) can be used to extract free energy differences from nonequilibrinm pocesses (iae. Collins, kiboted.al. Nature 'es)

A end of lecture 4

Leckere 5:- Morie a bant Kinesin walking a leng a microtubule MTs provido tracks along which vesicles, and ather carga, travel accross thecell.

Each step is powered bogit ATP $\longrightarrow A D P+P_{i}$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-23.jpg?height=330&width=990&top_left_y=843&top_left_x=142)

=Ultimate link behoem mascle contracion,

food and useful wooki; elechochem - radiaters accross mentanues
- Brief summary of Block paper

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-23.jpg?height=495&width=1000&top_left_y=1491&top_left_x=137)

orthophosphate

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-23.jpg?height=199&width=314&top_left_y=963&top_left_x=1518)

$$
\begin{aligned}
\Delta A(60 l) & \approx 20 \mathrm{kT} \\
C(A T P) & =1-10 \mathrm{mM} \\
& \Rightarrow \pm 3 k_{B} T .
\end{aligned}
$$

We estimated.

$V=0$ for $F \leq 10 p \mathrm{~N}$

$\forall$ dynamics
- $\forall$ concentration alependence: bolloy

Teday: Statistical Mechanics Review II

Read Primer an bconrses!

and Chap. 6

Joleal Gas low
- particle ur. exchange between B and S
- Chamicalpstential and its equilibration
- dependence en particle factions
- asuatic fressure
- chemical reactions (next tive)

$\left(d S_{b}\right)$

Ist faw: $d U=\underbrace{T d S}_{\delta Q_{\text {rev }}}-\delta V I t$ Tor acell, this is the thest commer torm

$$
\delta W=+p d V=\sum_{i} p_{i} d N_{i}
$$

Today: Thenical pockutiol offeciesi ; $U(S, V, W)$

$$
\begin{aligned}
& d A=d(U-T S)=-S d T-p d V+\sum_{i} \mu_{i} d N_{i} ; A(T, V, N) \\
& \left.d G=d(U-T S+p V)=-S d T+V d p+\sum_{i} \mu_{1} d N_{i} ; G(T, p, N)\right)
\end{aligned}
$$

What happens where particle uris change? exchange!

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-25.jpg?height=570&width=737&top_left_y=354&top_left_x=133)

$$
P\left(r_{s}\right) \propto e
$$

$$
k^{-1} S_{s}\left(E-E_{s,} N-N_{s}\right)
$$

Ty for: $S_{b}=$ cont. $-\frac{1}{T_{b}}\left[E_{S}-\mu_{b} N_{S}\right]$ with each particle

equilibrium: Maximize $Z=\Omega_{S}\left(E_{s}, N_{s}\right) \cdot P\left(v_{s}\right)$

$$
\begin{aligned}
& \text { brine : Maximize } Z=\Omega_{S}\left(E_{S}, N_{S}\right) \cdot P\left(v_{S}\right) \text { Grad potential minimal } \\
& \Rightarrow \quad T_{b}=T_{S} ; \mu_{b}=\mu_{S} ;\left(\sum=-k_{B} T \ln Z=U-T S-\mu N\right)
\end{aligned}
$$

$$
-d S_{S} \stackrel{\text { equilibrium }}{=} d S_{b} \stackrel{\oplus}{=}-\frac{d E_{s}}{T}+\frac{\mu}{T} d N_{S} \Rightarrow d U_{s}=\mu d N_{s}+T d S_{s}-p d V
$$

$$
\Rightarrow \mu d N_{S} \stackrel{(\Delta)}{=} d E_{S}-T d S_{S} \quad \begin{array}{ll}
d A & =d(U-T S)=-S d T+\mu d N-p d V \\
& d \Sigma=-S d T-N d \mu
\end{array}
$$

$d \Sigma=-\int d T-N d \mu$

Several molecular species: $\mu N \rightarrow \Sigma_{i} \mu_{i} N_{i}$.

Volume exchange : Similes story

$$
P\left(r_{s}\right) \propto e^{-\beta_{s}\left[E_{s}-\mu_{b} W_{s}+p_{B} d V\right]} \cdots=p_{b}=p_{s}=\left(\frac{\partial S}{\partial V}\right)_{E_{1} N}
$$

minimize
$\left.G=U-T S+P V=\Sigma_{i} \mu_{i} N_{i}\right)$ Gibbs pee energy.

The chemical potential of a molecule elements on its concentration

$$
\left.\mu_{i}=\mu_{i}^{0}+k_{B} T \ln \left(\frac{x_{i}}{x_{i}}\right)\right)_{\text {mol, species } i}^{x_{i}: \text { number }}
$$

reference chemical Derivation: See primer.
potential

Basic idea:

Suppose Niches in volume V. Then add ane more, $N \rightarrow N+1$

How many extra confine?

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-26.jpg?height=640&width=1202&top_left_y=1365&top_left_x=303)

\# ways to arrange $\overbrace{}^{N_{S}+N+1 \text { items }}$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-26.jpg?height=507&width=1971&top_left_y=2105&top_left_x=0)

identical particles
or $\frac{\Omega_{N+1}}{\Omega_{N}}=x^{-1}$ where

$X \equiv \frac{N}{N+N_{S}}$ is the number faction of solutes.

$$
\begin{array}{r}
\Delta S=k_{B}\left(\ln \Omega_{N+1}-\ln \Omega_{N}\right)=k_{B} \ln \frac{\Omega_{N+1}}{\Omega_{N}}=-k_{B} \ln (x) \\
=\text { extra entropy } \\
\text { per added solute particle. }
\end{array}
$$

Suppose we know reprence clam port $\mu_{0}\left(x_{0}\right)$ at $x=x_{0}$. From ( $\Delta$ ), we know: $\mu \stackrel{(\Delta)}{=} \Delta u-T \Delta s$.

$$
\Rightarrow \mu-\mu=T\left(\Delta S_{0}-\Delta S\right)=\operatorname{kB} T \ln \left(\frac{x}{x_{\theta}}\right)
$$

Works for any $0<x<1$.

- Recap Chemical Potential

$\frac{\text { number fraction: }}{d} X_{i}=\frac{u_{i}}{N_{\text {rot }}}$

$$
\begin{aligned}
& \mu_{i}=\mu_{i 0}+k T \ln \left(\frac{x_{i}}{x_{i 0}}\right) \text { (SEEPRIMER) } \\
& \approx \mu_{i 0}+k T \ln \left(\frac{C_{i}}{C_{i 0}}\right) \begin{array}{l}
\text { (assuming dilute solutions) } \\
\text { because then } \frac{x_{i}}{x_{i 0}} \approx \frac{n_{i}}{u_{i 0}}=\frac{C_{i}}{C_{i 0}}
\end{array}
\end{aligned}
$$

requires non-interacting components sided solutes Or interaction energy between like particles $z$ regular $=-11$ between unlike particles solutions

Osmotic pressure inside bacteria s

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-29.jpg?height=432&width=818&top_left_y=187&top_left_x=308)

shes in, but allows far exchange of हैO

$\mu_{\mu_{2} a}^{\text {in }}$ deaneries with $c_{s c l}$ (Ming eaters ) increases with pin (Energy)

$\mu_{H_{2} \mathrm{O}}^{\text {out }}$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-29.jpg?height=187&width=712&top_left_y=624&top_left_x=388)

$$
\begin{aligned}
& \text { Molfractin of water }=1-X_{\text {sol }} \quad \frac{\text { mel lar friction }}{N \approx \frac{\Delta C}{N}} \\
& \left(\begin{array}{c}
\mu \\
X_{\mathrm{H}_{2} \mathrm{O}}
\end{array}\right) \approx \mu-k T X_{\text {SOl }}^{c_{\mathrm{H}_{2} \mathrm{O}}}
\end{aligned}
$$

Qequilb.:

$$
\begin{aligned}
& \mu_{H_{2} O}^{i n}=\mu_{H_{2} \omega}^{\text {out }} \\
& D)-k T x_{s c l}=\mu^{0}(T \\
& \frac{\partial \mu^{0}}{\partial P} \cdot \Delta P=k T x_{s o l}
\end{aligned}
$$

$$
\mu_{k_{2} a}^{O}(T ; P+\Delta P)-k T x_{s c l}=\mu^{a}(T ; P)
$$

$$
G=N_{H_{2} O^{2}} \mu_{H_{1}^{0}}^{0}=D \quad \frac{\partial \mu^{0}}{\partial P}=\frac{1}{N_{H_{2} O}} \frac{\partial G}{\partial P}=\frac{V}{N_{H_{2}} O}
$$

So, $\Delta P=R T \frac{x_{s 1} N_{\mathrm{H}_{2} \mathrm{O}}}{V}=R T c_{\text {sol }}$

$$
\Delta P(O, M) \approx 1 \text { atm }=10^{5} P_{q}=\text { con tire presser } x 1 / 2
$$

1 Fore of $\approx 10^{5} \mathrm{p} \mathrm{N}$ a all wall.

Ex.: Estimate the turgor pressure inside the all

Typical solute concentration $\approx 91 M-1 M$

$$
=10^{8} n M-10^{9} M M
$$

use $\ln M \triangleq 0,6$ mol. $/ \mathrm{fl}=0,6 /\left[2 \mu \mathrm{m} \cdot\left(l_{\mathrm{mm}}\right)^{2}\right]$

$$
\begin{aligned}
& \approx 0,3 \cdot 10^{-9} \mathrm{um}^{-3} \\
P_{\text {loom }} & =\frac{N_{\text {om m }}}{V} \cdot k_{B} T=10^{8} \cdot 0,3 \cdot 10^{-9} \mathrm{~mm}^{-3} \cdot 4 \mathrm{pN} \cdot \mathrm{nm}=10^{8} \cdot 1,2 \cdot 10^{-9} \mathrm{pNmm} \mathrm{mm}^{-2} \\
& =1,2 \cdot 10^{5} \mathrm{pN} \mathrm{mm}^{-2} \\
& =1,2 \cdot 10^{5} \cdot 10^{-12} \mathrm{~N} \cdot 10^{12} \mathrm{~m}^{-2}=1,2 \cdot 10^{5} \mathrm{P}_{a}=0,1 \mathrm{MPa} .
\end{aligned}
$$

Conditions for chemical equilibrucm

e.g. $\quad L+k \underset{ }{\rightleftarrows} L k$

Stoichometric $-1-1+1$ coefficients

$$
v_{1}=-1, v_{2}=-1 ; v_{3}=+1
$$

Equilibrium:

$$
\begin{aligned}
& O=\Delta G=\sum_{i} \mu_{i} d N_{i}=\lambda_{D} \bar{\Sigma}_{i} \mu_{i} v_{i} \\
& =0 \quad D=\sum_{i} \mu_{i} r_{i}(*)
\end{aligned}
$$

$$
\mu_{i}=\mu_{i}^{0}+k T \ln \left(\frac{c_{i}}{c_{i}}\right)-1 \mu
$$

$\nu(t): \Delta G^{0} \equiv \sum_{i} \mu_{i}^{e} \nu_{i}=-k T \sum_{i} v_{i} \ln \left(\frac{c_{i}}{c_{i 0}}\right)=-k T \ln \left(k_{\text {eq }}\right)$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-31.jpg?height=286&width=1240&top_left_y=1468&top_left_x=628)
measures/finty,

$$
K_{e q}=\frac{[L R]}{[L] \cdot[R]}=\frac{1}{K_{d}}
$$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-31.jpg?height=559&width=1671&top_left_y=2231&top_left_x=108)

So

Ex: ATP undrolysis notate equilibrium

$$
\begin{aligned}
& A T P+H_{2} \mathrm{O} \rightleftarrows A D P+P_{i} \\
& \left.\Delta G=\Delta G_{0}+k T \ln \frac{[A D P][P]}{[A T P]\left[H_{2} Q\right.}\right]
\end{aligned}
$$

concentrations very but topically values are

$$
\left.\begin{array}{l}
\text { ions very but typically values are } \\
[A T P] \sim[A D P] \sim 8 \mu M\} \Delta G=-20 k T \\
{[P] \sim 0,4 \mu M}
\end{array}\right\}
$$

Appendix: $\Delta G^{0}$ is same limos given in units of $\frac{k J}{H_{0} l}$

This is the $\Delta G^{0}$ for 1 Mol of product.@standad condificus.

or $\Delta G^{O}=R T \ln \left(K_{e q}\right)=\Delta H_{f}^{c^{2}}-T \Delta s^{0}$
$\frac{\text { Transcription: A crucial element of gene expression }}{\text { Promoter }}\left(C_{1} .6\right)$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-33.jpg?height=728&width=1788&top_left_y=119&top_left_x=324)

Expression of a gene requires 1 ant of $P$ RNA polymerase to bind specifically to the promoter sequence of the gene: Energy lest $\Sigma_{s p}$ However, RNAP may also bind unspecifically to N $(\rightarrow P)$ other pasts of the chromosome: Eurerg level $\approx \varepsilon_{n s}\left(>\varepsilon_{p p}\right)$ What's the proa (RNAP bend to prom. )? (\#truacriphtsec a Prompt)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-33.jpg?height=656&width=1839&top_left_y=1448&top_left_x=257)

$$
p_{\text {pound }}=\frac{\Omega_{s p} e^{-\beta \varepsilon_{s p}}}{\Omega_{s p} e^{-\beta \varepsilon_{s p}}+\Omega_{n s} e^{-\beta \varepsilon_{n s}}}=\frac{1}{1+\frac{\Omega_{n s}}{\Omega_{s p}} e^{-\beta\left(\varepsilon_{n s}-\varepsilon_{s p}\right)}}
$$

Ratio of $\nexists^{-1}$ differences multiplicities,

1 differences in entreaties

$$
\begin{aligned}
& \frac{\Omega_{u s}}{\Omega_{s p}}=\frac{(P-D) !(N-P+1) !}{P !(N-P) !}=\frac{N-P+1}{P} \approx \frac{N}{P}\left(\begin{array}{l}
\text { Dilute } \\
\text { Limit }
\end{array}\right)
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-34.jpg?height=493&width=1949&top_left_y=284&top_left_x=175)

Real life numbers? Promoter: $\underset{-35=10}{\sim 10^{2}}$

in $\varepsilon$.coli.

Genome $\approx 10^{6-7 b p}$. (E.coli)

\# KNAP $\approx \cdot 10^{3} \cdot\left(\sigma^{70} R N A P\right)$

So $\frac{N}{P} \approx 10^{3-4}$

$p_{\text {bond }} \approx \frac{1}{2} \rightarrow \beta \Delta \varepsilon \approx \ln \left(\frac{\mu}{\theta}\right)=\frac{\ln (\theta) \cdot\{3.4\} \approx 7 \ldots 9}{2,3} \approx$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-34.jpg?height=231&width=1243&top_left_y=1533&top_left_x=811)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-34.jpg?height=262&width=1594&top_left_y=1721&top_left_x=343)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-34.jpg?height=319&width=1110&top_left_y=1953&top_left_x=585)

$S_{0}, \Delta \varepsilon \mid \approx k T \ln \left(10^{2} \ldots 10^{3}\right) \approx 5 \ldots 7 k_{B} T$

stop here

Alternative appraach using the concest of chemical potatid

$$
\text { System }=\text { Pramcter }
$$

Bath = Rest of the Chromoseme $\} \begin{aligned} & \text { can exchange } \\ & \text { RNAPs! }\end{aligned}$

RNAP

RNAP

in butes

in syetem

$\Rightarrow$ De obtain a simple 2-ctate system:

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-35.jpg?height=349&width=1577&top_left_y=1270&top_left_x=469)

$$
\begin{aligned}
& \text { unbound } 1 \\
& \Rightarrow p_{\text {bound }}=\frac{1}{1+e^{-\beta\left(\varepsilon_{\text {gp }}-\mu\right)}} \\
& \mu=\mu_{0}+k T \ln \left(\frac{N}{P}\right) \\
& =\frac{1}{1+\frac{N}{p} e^{-\beta \Delta \varepsilon}} ; \Delta \varepsilon=\varepsilon_{b}-\mu^{0}
\end{aligned}
$$

N.B.: System=Small; $T_{S,}$, pe not aldined. But hethis big.

Above approach has explanation' portholes.- in particles:

$\frac{N}{P}$ is the inverse RNAP concentration.

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-36.jpg?height=624&width=766&top_left_y=543&top_left_x=197)

Cequilib $\mu_{s}=\mu_{6}$

$$
\mu_{s}^{0}+k T \ln \left(\frac{\left(P_{s}\right\rangle|| N_{s p}^{\prime}}{\left\langle P_{s}^{0}\right\rangle \mid N_{s_{p}}}\right)=\mu_{b}^{0}+k T \ln \left(\frac{\left\langle P_{b}\right\rangle}{\left\langle s_{p}^{0}\right\rangle}\right)
$$

We know that $\Omega_{S}^{0}=1$ if $P_{S}^{0}=N_{S P}$ and hence $N_{s p} \cdot \varepsilon_{s p}=G=N_{s p} / s_{s}^{0} \rightarrow \mu_{s}^{0}=\varepsilon_{s p}$

Similarly $P_{b}^{0}=\omega_{b} \Rightarrow \mu_{b}^{0}=\varepsilon_{\text {usp. }}$.

$$
\begin{aligned}
& \Rightarrow \quad \varepsilon_{s p}+k T \ln (\underbrace{\frac{\left\langle P_{s p}\right\rangle}{N_{s p}}})=\varepsilon_{h+p}+k T \ln (\underbrace{\frac{\left\langle P_{b}\right\rangle}{N_{b}}}_{\langle p 1}) \\
& P_{\text {bound }} \\
& \frac{P-\left\langle P_{s}\right\rangle}{N_{\text {usp }}}=\frac{P}{N_{\text {upi }}}-P_{\text {b }}: \frac{N_{\text {sp }}}{N_{\text {ump }}} \\
& \frac{P_{b}}{\frac{P}{N_{\text {up }}}-P_{b} \frac{N_{\text {sp }}}{N_{\text {up. }}}}=e^{-\beta\left(\frac{\left.\varepsilon_{s p}-\varepsilon_{\text {nip }}\right)}{\Delta \varepsilon}\right.} ; \Delta \varepsilon<0 \\
& R=\frac{\frac{P}{N_{\text {usp }}} e^{-\beta \Delta \varepsilon}}{1+\frac{N_{\text {sp }}}{N_{\text {spp }}} e^{-\beta \Delta \varepsilon}}
\end{aligned}
$$

$$
\varphi_{b}=\frac{1}{\frac{N_{s p}}{P}+\frac{N_{\text {sp }}}{P} e^{+\beta \Delta \varepsilon}}
$$

Does this make sense?

$$
\begin{aligned}
& \text { bes this make sense: } \\
& \Delta \varepsilon \rightarrow-\infty=0 p_{b} \rightarrow \frac{P}{N_{s p}} \int\left(\begin{array}{c}
\text { in diddle } \\
\text { limit }
\end{array}\right) \\
& \Delta \varepsilon \rightarrow+\infty=0 p_{b} \rightarrow 0 \\
& \Delta \varepsilon \rightarrow 0=0 \quad p_{b}=\frac{P}{N_{s p}+N_{s s p} .}
\end{aligned}
$$

But hew to queralize this to the non dilute case?

Third approach using concept of chemical equitibrium

$$
\begin{aligned}
& \bigcap_{\substack{x \\
\text { manng }}} \mid \operatorname{RNAP} P_{\text {unsp }}+P_{\text {romoter }}^{\text {undend }} \longrightarrow \text { RNAP-P } \\
& L+R \rightarrow L R \\
& P_{\text {bound }}=\frac{[L R]}{[R]+[L R]}=\frac{1}{1+K_{e q} \cdot \frac{c_{o}}{[L]}}
\end{aligned}
$$

$$
\text { So if we choose } c_{0}=N=0 L=P, K_{e q}=e^{-\beta \Delta E} \text {. }
$$

Ex: Ligand-Receptor binding:

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-39.jpg?height=487&width=1386&top_left_y=262&top_left_x=510)

System = Receptor $=$ A simple 2-ctate system:

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-39.jpg?height=446&width=1252&top_left_y=916&top_left_x=828)
the entropic piece

$$
\begin{aligned}
& \Rightarrow \quad p_{\text {bound }}=\frac{1}{1+e^{-\beta\left(\varepsilon_{\text {sp }}-\mu\right)}} \\
& \frac{h}{h_{0}}=1-\frac{\Delta n_{H_{0} O}}{n_{0}}
\end{aligned}
$$

$$
\begin{aligned}
& =\frac{1}{1+e^{-\beta\left(\varepsilon_{s p}-\mu\right)}} \\
& =\frac{1}{1+\frac{c}{c} e^{-\beta \Delta \varepsilon}} ; \Delta \varepsilon=\varepsilon_{b}-\mu^{0} \ln \left(\frac{c}{c_{0}}\right) . \\
& \longrightarrow \text { compare. RNAP problem. }
\end{aligned}
$$

Attenative Bottimann derivations: - Jentical particles poobben

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-40.jpg?height=683&width=943&top_left_y=243&top_left_x=187)
- Why Garin caid that

Defailed babance = Maxk $E_{\text {k }}$.

S'Asey GBatumann $\&$
- $\Delta G$ business case for ATP.

$$
\begin{aligned}
& P_{s}(n) \propto \Omega_{B}^{(k)}(N-n)=k^{N-n} \propto e^{-\ln (k) \cdot n} \\
& \times \frac{1}{(N-n) !} \rightarrow e^{-(N-n) \ln (N-n)-1]} \\
& \propto e^{[\ln N-\ln k] \cdot n}
\end{aligned}
$$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-40.jpg?height=309&width=241&top_left_y=1408&top_left_x=1167)

$\Omega_{B}^{(k)}(M)=$ \# ways bo distribute 11 mits of energy ancug $k$ bins

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-40.jpg?height=216&width=133&top_left_y=924&top_left_x=1692)

$$
=\frac{(M+k) !}{M ! k !}
$$

if we assume eversy units are indistinguishable

$$
\text { Co } P_{S}(n) \propto \Omega_{B}^{(k)}(N-n)=\frac{(N-n+k) !}{(N-n) ! k !} \propto \frac{(N-n+k) !}{(N-n) !}
$$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-41.jpg?height=809&width=1776&top_left_y=0&top_left_x=139)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-41.jpg?height=281&width=1791&top_left_y=999&top_left_x=45)

use $l_{n} M \cong 0,6 \mathrm{mal} / \mathrm{fl}=0,6 /\left[2 \mu \mathrm{m} \cdot\left(l_{\mathrm{m}}\right)^{2}\right]$

$$
\begin{aligned}
& \approx 0,3 \cdot 10^{-9} \mathrm{um}^{-3} \\
P_{\text {om }} & =\frac{N_{\text {om m }}}{V} \cdot k_{B} T=10^{8} \cdot 0,3 \cdot 10^{-9} \mathrm{~mm}^{-3} \cdot 4 \mathrm{pN} \cdot \mathrm{nm}=10^{8} \cdot 1,2 \cdot 10^{-9} \mathrm{pNmm}^{-2} \\
& =1,2 \cdot 10^{5} \mathrm{pN} \mathrm{mm}^{-2} \\
& =1,2 \cdot 10^{5} \cdot 10^{-12} \mathrm{~N} \cdot 10^{12} \mathrm{~m}^{-2}=1,2 \cdot 10^{5} \mathrm{~Pa}=0,1 \mathrm{MPa} .
\end{aligned}
$$

Ex.: $\quad 3 \xi \xi_{\text {Q Polgeth. }}$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-41.jpg?height=239&width=1090&top_left_y=2140&top_left_x=287)

Ex: ATPlydrolysis. Explain well: $\Delta G=k T \ln \left(\frac{\prod_{i} c_{i}^{v_{i}}}{k_{q}}\right)=\Delta G_{g}+k T \ln \left(\prod_{i}\left(c_{i}\left(\frac{c_{i}}{i r}\right)^{v_{i}}\right)\right.$

$$
\begin{aligned}
& \stackrel{A T P}{\longrightarrow} \rightarrow A D P+P_{i} \\
& \Delta G=\Delta G_{i}+k \ln \frac{[A D P][P]}{[A T P]}=-20 \mathrm{kT} \\
&-12 k T
\end{aligned}
$$

\section*{Entropy rules!!}

If accessible states of a system have different associated energies, the probabilities of these states depend on their energies.

Assume that the system $A$ is in contact with a much larger system $A^{\prime} . \quad A \ll A^{\prime}$

$$
E+E^{\prime}=E_{0} \text { and } E \ll E_{0}
$$

What is the probability $P_{r}$ of finding the system $A$ in one particular microstate $r$ of energy $E_{r}$. There may be multiple accessible states at energy $E_{r}$.

Since $A$ is in one microstate $(\Omega=1), P_{r}$ is proportional to the number of accessible states available to the $A^{\prime}$.

$$
\begin{gathered}
P_{r}=C^{\prime} . \Omega^{\prime}\left(E_{0}-E_{r}\right) \\
\ln \Omega^{\prime}\left(E_{0}-E_{r}\right)=\ln \Omega^{\prime}\left(E_{0}\right)-\frac{d \ln \Omega^{\prime}\left(E_{0}\right)}{d E^{\prime}} E_{r}=\ln \Omega^{\prime}\left(E_{0}\right)-\beta E_{r} \\
\Omega^{\prime}\left(E_{0}-E_{r}\right)=\Omega^{\prime}\left(E_{0}\right) e^{-\beta E_{r}} \\
P_{r}=\frac{e^{-\beta E_{r}}}{Z}, \text { where } Z \text { is constant } \\
Z=\sum_{r} e^{-\beta E_{r}}=\sum_{E_{r}} \Omega\left(E_{r}\right) e^{-\beta E_{r}} \quad \text { sum of all states (also called the partition function) } \\
P(E)=\frac{\Omega(E) e^{-\beta E}}{Z} \quad \text { (See Appendix } \mathbf{2} \text { and 3) }
\end{gathered}
$$

\section*{Example: Basic Control of Gene Expression}
![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-44.jpg?height=1038&width=898&top_left_y=249&top_left_x=51)
- RNA polymerase (RNAP) recognizes a promoter sequence preceding the gene of interest.
- Consider there are $\mathrm{N}$ nonspecific binding site and 1 specific binding site on a DNA for P RNAP molecules (N>>P).
- Energy for specific binding is $\varepsilon_{\mathrm{s}}$ and for nonspecific binding is $\varepsilon_{\mathrm{n}}$. Find the probability of the specific site to be occupied.
- All RNAPs are bound to DNA.

Case 1. unoccupied. $\mathrm{E}=\mathrm{P} \varepsilon_{\mathrm{n}}$

$$
\Omega(N, P)=\frac{N !}{P !(N-P) !}=\left(\begin{array}{l}
N \\
\text { to DNA. }
\end{array}\right.
$$

Case 2: Occupied $\mathrm{E}=\varepsilon_{\mathrm{s}}+(\mathrm{P}-1) \varepsilon_{\mathrm{n}}$

$$
\Omega(N, P-1)=\frac{N !}{(P-1) !(N-P+1) !}
$$

Statistical weight of each state is the multiplication of $\Omega$ by the Boltzmann factor.

Probability is the ratio of statistical weight divided by total partition function.

$\Omega(N, D)$

$p_{\text {bound }}=\frac{\frac{N !}{(P-1) !(N-P+1) !} e^{-\beta\left(\varepsilon_{s}+(P-1) \varepsilon_{n}\right)}}{\frac{N !}{(P-1) !(N-P+1) !} e^{\left.-\beta\left(\varepsilon_{s}+(P-1) \varepsilon_{n}\right)+\frac{N !}{P !(N)} e^{-\beta P}\right)}} \quad \Delta \varepsilon=\varepsilon_{s}-\varepsilon_{n}$

$p_{\text {bound }}=\frac{\frac{P}{N} e^{-\beta \Delta \varepsilon}}{1+\frac{P}{N} e^{-\beta \Delta \varepsilon}}=\frac{1}{1+\frac{N}{P} e^{\beta \Delta \varepsilon}}$

\section*{Example: Ligand-Receptor Binding}
![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-45.jpg?height=672&width=2538&top_left_y=194&top_left_x=77)

In the presence of $C$ crowding agents, the volume in which ligand molecules can distribute themselves reduce.

Entropic cost of stealing one ligand from solution decreases.

Therefore, crowding molecules favor binding of ligand to receptor.

$Z(L, C)=\frac{\Omega !}{\mathrm{L} ! \mathrm{C} !(\Omega-\mathrm{L}-\mathrm{C}) !} e^{-\beta\left[L \varepsilon_{L}^{\text {sol }}+C \varepsilon_{C}^{\text {sol }}\right]}+\frac{\Omega !}{(\mathrm{L}-1) ! \mathrm{C} !(\Omega-\mathrm{L}-\mathrm{C}+1) !} e^{-\beta\left[(L-1) \varepsilon_{L}^{\text {sol }}+C \varepsilon_{C}^{\text {sol }}+\varepsilon_{b}\right]}$

$p_{\text {bound }}=\frac{\frac{\Omega !}{(\mathrm{L}-1) ! \mathrm{C} !(\Omega-\mathrm{L}-\mathrm{C}+1) !} e^{-\beta\left[(L-1) \varepsilon_{L}^{\text {sol }}+C \varepsilon_{C}^{\text {sol }}+\varepsilon_{b}\right]}}{Z}=\frac{1}{1+\left(\frac{\Omega-\mathrm{L}-\mathrm{C}}{\mathrm{L}}\right) e^{\beta \Delta \varepsilon_{L}}}$

Assuming that $L \ll \Omega$,

crowding will be significant when $C$ is comparable to $\Omega$

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-45.jpg?height=628&width=954&top_left_y=1426&top_left_x=1740)

\section*{Clausius Inequality}

Heat Reservoir: Imagine a small system $A$ is submerged in a large system $\mathrm{A}^{\prime}$, whose temperature remains unchanged of any amount of $\mathrm{Q}$ absorbed $\left(\mathrm{Q}^{\prime}=-\mathrm{Q}\right)$. A and $\mathrm{A}^{\prime}$ are thermally interacting with each other and have the same final temperature. $Q^{\prime}$ is small relative to $E^{\prime}$.

$$
\begin{gathered}
\frac{\Delta S^{\prime}}{k}=\ln \Omega^{\prime}\left(E^{\prime}+Q^{\prime}\right)-\ln \Omega^{\prime}\left(E^{\prime}\right)=\frac{\delta \ln \Omega^{\prime}\left(E^{\prime}\right)}{\delta E^{\prime}} Q^{\prime}=\beta^{\prime} Q^{\prime} \\
\Delta S^{\prime}=\frac{Q^{\prime}}{T^{\prime}} \\
\Delta S_{\text {total }}=\Delta S+\Delta S^{\prime} \geq 0 \\
\Delta S^{\prime}=-\frac{Q}{T^{\prime}} \quad \text { and } \Delta S-\frac{Q}{T^{\prime}} \geq 0 \\
Q=\Delta E+W
\end{gathered}
$$

the work done by the system is $P^{\prime} \Delta V$.

$$
\begin{gathered}
Q=\Delta E+P^{\prime} \Delta V \quad \text { so } \quad \Delta S-\frac{\Delta E+P^{\prime} \Delta V}{T^{\prime}} \geq 0 \\
\text { therefore } A \equiv \Delta E+P^{\prime} \Delta V-T^{\prime} \Delta S \leq 0 \quad \text { free energy }
\end{gathered}
$$

Helmholtz Free Energy: System interacts thermally with a heat bath.

$$
F=E-T S
$$

Enthalpy: System interacts mechanically with a heat bath.

$$
\mathrm{H}=E+P V
$$

Gibbs Free Energy: System interacts both thermally and mechanically.

$$
G=E+P V-T S
$$

In water, we do not make a distinction between $\mathrm{F}$ and $\mathrm{G}$, because $\Delta \mathrm{V}$ is small.

$$
\Delta S_{\text {total }}=\frac{T^{\prime} \Delta S-\Delta E-P^{\prime} \Delta V}{T^{\prime}}=\frac{-\Delta G}{T^{\prime}} \geq 0
$$

$\Delta G \leq 0 \quad$ free energy tends to decrease towards equilibrium

$$
\text { probability } \propto \Omega=\mathrm{e}^{S / k}=\mathrm{e}^{-\frac{\Delta G}{k T^{\prime}}}
$$

Probability is maximum when $\Delta G$ is minimum. Maximizing total $S$ of a system (i.e. a molecule) and the surrounding (i.e. cell) is equivalent to the $\Delta G$ minimization of the system. The beauty of this principle is that we do not have to worry about the complexities of the surrounding.

If the system also does useful work, $\quad W=P^{\prime} \Delta V+W_{\text {useful }}$

$$
\begin{gathered}
\Delta S_{\text {total }}=\frac{T^{\prime} \Delta S-\Delta E-P^{\prime} \Delta V-W_{\text {useful }}}{T^{\prime}}=\frac{-\Delta G-W_{\text {useful }}}{T^{\prime}} \geq 0 \\
-W_{\text {useful }} \leq \Delta G
\end{gathered}
$$

Maximum useful work that can be done by the system is equal to its free energy, which is less than its total energy.

(A)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-48.jpg?height=831&width=344&top_left_y=202&top_left_x=168)

ATP

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-48.jpg?height=246&width=596&top_left_y=789&top_left_x=502)

ADP
![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-48.jpg?height=400&width=678&top_left_y=1168&top_left_x=130)

(B)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-48.jpg?height=358&width=1108&top_left_y=1599&top_left_x=137)

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-48.jpg?height=336&width=410&top_left_y=1228&top_left_x=833)

-(Left) An example of mechanical work performed by the kinesin motor carrying a large vesicle against hydrodynamic drag.
- (Bottom) An example of chemical work by maltose transporter that concentrates nutrient (maltose) inside the cell.
- Both processes are driven by ATP hydrolysis.
- $\Delta \mathrm{G}_{\text {ATP }}$ limits the extent to which maximum work can be done to drive these unfavorable processes.

![](https://cdn.mathpix.com/cropped/2024_01_25_6d1709e92b553fd7440eg-48.jpg?height=926&width=1287&top_left_y=1119&top_left_x=1345)