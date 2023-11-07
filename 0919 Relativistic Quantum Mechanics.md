# Schrödinger Equation
$$
H\psi = i\hbar \frac{\partial \psi}{\partial t}\quad \psi\text{ or }\ket{\psi} \text{ is the wave function/quantum state}
$$
For free particles, the Hamiltonian consists of only the kinetic energy part $$
H = \frac{|\vec{p}|^2}{2m}\Rightarrow \hat{H} = \frac{1}{2m}(-i\hbar\nabla)^2
$$
Incorporating the energy-momentum relation from special relativity:
$$
\begin{align}
&H = \sqrt{|\vec{p}|^2c^2 + m^2c^4}\Rightarrow \sqrt{-\hbar^2\nabla^2 + m^2c^4}\\
\Rightarrow &H^2 = \left(-i\hbar\frac{\partial \psi}{\partial t}\right)^2\\
\Rightarrow &(-\hbar^2c^2\nabla^2 + m^2c^4)\psi = -\hbar^2 \frac{\partial^2 \psi}{\partial t^2}
\end{align}
$$
Identify that the derivatives can be collected and be expressed using the four-divergence:
$$
\begin{gather}
\hbar({\partial_t}^2 - c^2\nabla^2)\psi + m^2c^4\psi = 0\\
\Rightarrow (\partial_\mu\partial^\mu + m^2)\psi = 0
\end{gather}
$$
This is the expression for the *Klein-Gordon* equation. A relativistic wave function for scalar particles (spin-0).
# Klein-Gordon Equation
$$
(\partial_\mu \partial^\mu + m)\psi = 0
$$
*  There exists a negative energy solution: 
  $$
  \begin{gather}
  \psi \sim \exp(-iEt + i \vec{p}\cdot\vec{x})\\
  E^2 = p^2 + m^2\rightarrow E = \pm \sqrt{p^2 + m^2}
  \end{gather}
  $$
  We identify the negative energy solution as anti-particles
  *  How do we deal with spin? Spin transforms non-trivially under Lorentz transformation. We also want something that is linear in $\partial_t$ for probability interpretation. $$
    {\partial \over \partial_t}(\psi^* \psi) + \nabla\cdot\mathbf{J} = 0 $$this necessitates the development of the **Dirac Equation** 
# Dirac Equation
Goal is to find an equation of motion that's linear in $\partial_t$ and is Lorentz-invariant
Guess work:$$
(i\gamma^\mu\partial_\mu -m)\psi = 0
$$
What is $\gamma^\mu$ ?
* $\gamma^\mu$ cannot be numbers, otherwise it specifies a special direction in spacetime
* We expect to recover the Klein-Gordon equation in 
  $$
  \begin{gather}
  (i\gamma^\nu\partial_\nu + m)(i\gamma^\mu\partial_\mu -m)\psi = 0\\
  [-\gamma^\nu\gamma^\mu\partial_\nu\partial_\mu + im(\partial_\nu - \partial_\mu ) -m^2]\psi = 0\\
  -(\gamma^\mu\gamma^\nu \partial_\mu \partial_\nu + m^2)\psi=0
  \end{gather}
  $$
* The structure above suggests symmetric and an anti-commutation relation of:$$
  \{\gamma^\mu,\gamma^\nu\} = 2\eta^{\mu\nu}
  $$$\gamma^0\gamma^0 = \mathrm{I}_{4\times4}$ and $\gamma^i\gamma^i = -\mathrm{I}_{4\times4}$ $\gamma^\mu$  $(i = 1,2,3)$
  $\gamma$ defined by four $4\times4$ matrices, one possible solution is :
  $$\gamma^0 = \begin{pmatrix}\mathrm{I}_{2\times2} & 0\\
  0 &-\mathrm{I}_{2\times2}\end{pmatrix}\quad
  \gamma^i = \begin{pmatrix} 0 & \sigma^i\\
  -\sigma^i & 0 \end{pmatrix}$$
  termed the *Dirac basis*, where $\sigma_i$ are Pauli matrices. The quantum state vector is now of dimension 4, however, we expect a spin-1/2 particle to have only 2 degrees of freedom. Additional constraints apply.
* $\psi$ is now a four component column vector (spinors), and transforms either as left- or right-handed particles under Lorentz transform

In the rest frame of a spin-1/2 particle of mass m:$$
\psi(x) = \int \frac{\mathrm{d}^4 p }{(2\pi)^4}\exp(-ip\cdot x)\psi(p)
$$
In momentum-space:
$$
\begin{gather}
(\partial^\mu p_\mu - m)\psi(p) = 0 \rightarrow (\gamma^0 - \mathrm{I})\psi = 0 \\
\begin{pmatrix}0&0\\0&\mathrm{I}_{2\times2}\end{pmatrix}\psi = 0
\end{gather}
$$
and as expected, we only require 2 degrees of freedom for a spin-1/2 particle.
### Weyl basis
$$
\gamma^0 = \begin{pmatrix}0&\mathrm{I}\\\mathrm{I}&0\end{pmatrix}\quad
\gamma^i = \begin{pmatrix}0&\sigma_i\\\sigma_i&0\end{pmatrix}\quad
\gamma^5 = \begin{pmatrix}-\mathrm{I}&0\\0&\mathrm{I}\end{pmatrix}
$$ Otherwise known as the *chiral basis*. This formulation has the advantage that it's chiral projection takes the simple form of:$$
\psi_L = \frac{1}{2}(1-\gamma^5)\psi = \begin{pmatrix}\mathrm{I}&0\\0&0\end{pmatrix}\psi
$$
The construction of a spinor: $\psi = (\psi_L \: \psi_R)^T$
### Dirac basis
# Path integrals
The action $S$ associated with a particular path: $$
S = \int^{t_2}_{t_1} \mathrm{d}t \mathcal{L}(q,\dot{q},t)
$$
Classical path extremizes (minimizes) action $\delta S = 0$ , the resulting equation of motion is the **Euler Lagrange Equation** $$
{\partial\mathcal{L}\over \partial q} - {\mathrm{d}\over \mathrm{d}t}{\partial\mathcal{L}\over \partial \dot{q}} = 0
$$
In quantum mechanics, we take into account all possible paths:$$
\bra{q_f}\exp[-i H(t_2 - t_1)]\ket{q_I} = \int[Dq(t)]\exp\left[i\int_{t_1}^{t_2}\mathcal{L}\mathrm{d}t\right]
$$
Dividing the space into segments, and take the continuum limit gives the integral in the exponent. 
For the following, we will call the "Lagrangian density" as Lagrangian 
Euler Lagrange equation (equation of motion):$$
\partial_\mu {\partial \mathcal{L}\over \partial(\partial_\mu \phi)} - {\partial\mathcal{L}\over\partial\phi}
$$ By generalized momenta in the classical Lagrangian constructed with four-momentum, the function resembles that of a field equation.
To quantize the theory, define the canonical momentum:$$
\Pi_a \equiv {\partial \mathcal{L}\over\partial\dot{\phi}_a}
$$
Hamiltonian density:$$

\mathcal{H} = \sum_a \dot{\phi}_a \Pi_a - \mathcal{L}
$$
Impose the canonical quantization condition:$$
[\phi_a(\vec{x},t),\Pi_b(\vec{y},t)] = i\delta^a_b\delta^3(\vec{x}-\vec{y})\quad[\phi_a,\phi_b] = 0\quad [\Pi_a,\Pi_b] = 0
$$
The field $\phi$ is constructed by a *linear combination* of annihilation and creation operators of the particle $\phi$, e.g. electromagnetic field and photons $$
\phi \leftrightarrow\sum\hat{a}\hat{a}^\dagger
$$
## A scalar particle toy model
* $\phi = \phi^*$
* Lorentz invariant
* Quadratic
$$ \mathcal{L} = -\frac{1}{2}a\:\partial_\mu\phi\:\partial^\mu \phi+ \frac{b}{2}\phi^2 $$
a and b are real factors, for simplicity, we can set absorb the factors into the field. 
$$ \mathcal{L} = \pm\frac{1}{2}(\partial_\mu\phi\:\partial^\mu \phi+ b\phi^2 )$$

$$
\begin{align}
\Pi =& {\partial\mathcal{L}\over\partial\dot{\phi}} = \pm \dot{\phi}\quad \\
\mathcal{H} = \dot{\phi}\Pi - \mathcal{L} = &\pm\Pi^2 \mp \frac{1}{2}[\Pi^2 - (\nabla\phi)^2 + b\phi^2)]\\
=&\pm\frac{1}{2}[\Pi^2 - (\nabla\phi)^2 + b\phi^2)]\\
\end{align}
$$
Considering the positive energy solution, we require $\mathcal{H}$ to be bounded from below. Demand $b < 0$ and we can see that $b = -m^2\:(m>0)$ resembles the mass term
$$
\mathcal{L} = \frac{1}{2}(\partial_\mu\phi\:\partial^\mu\phi) - \frac{1}{2}m^2\phi^2 = 0
$$ We can verify that:$$
\partial_\mu {\partial\mathcal{L}\over\partial(\partial_\mu\phi)}-{\partial{L}\over\partial\phi}=0
$$
# The Dirac Lagrangian

$$\mathcal{L} = \bar{\psi}i(\gamma^\mu\partial_\mu - m)\psi$$

# Scalar field (Path integral formulation)
Disturb the vacuum by adding a potential term $J(x)$
$$
\mathcal{L} = \frac{1}{2}[(\partial \phi)^2 - m^2\phi^2] + J\phi
$$
The transition amplitude of a vacuum state:
$$
\begin{gather}
\bra{0} \exp(-i\hat{\mathcal{H}}t)\ket{0}\Rightarrow\text{Path integral}\\
Z = \int D\phi \exp\left\{i\int\mathrm{d}^4x \frac{1}{2}[(\partial \phi)^2 - m^2\phi^2] + J\phi\right\}
\end{gather}
$$
We can assume the boundary terms vanishes. Rearranging the integral in the exponent: 
$$
\begin{gather}
(\partial \phi)= \partial(\phi\partial\phi) - \phi \partial^2\phi\rightarrow \int \mathrm{d}^4 x\frac12 [\phi(\partial^2 + m^2)\phi + J\phi]\\
\text{"Gaussian Integral" }A\equiv (\partial^2 + m^2)\\ 
(\text{constant})\exp(-\frac i2 JA^{-1}J)
\end{gather}
$$
[Ref: Gaussian integrals in higher dimensions](https://en.wikipedia.org/wiki/Common_integrals_in_quantum_field_theory#Gaussian_integrals_in_higher_dimensions)
Integrate over discretized spacetime in continuous limit
$J^{-1}J\to J_x A_{xy}^{-1}J_y$ Dependent on initial and final state
$A^{-1}\equiv D(x-y)\quad AA^{-1} = \mathrm{I} \to -(\partial^2 + m^2)D(x-y) = \delta^4(x-y)$ "Propagator"
[Ref: Green's Function](https://en.wikipedia.org/wiki/Green%27s_function_(many-body_theory))
[Ref: Correlators](https://en.wikipedia.org/wiki/Correlation_function_(quantum_field_theory))
In the momentum space:
$$
\begin{gather}
\delta^4(x-y) = \int {\mathrm{d}^4 k \over (2\pi)^2} \exp[ik(x-y)] \Rightarrow (-p^2 + m^2)D_p = 1\\
D(x-y) = \int {\mathrm{d}^4 k \over (2\pi)^4}{\exp[ik(x-y)]\over k^2 - m^2 + i\epsilon}
\end{gather}
$$
The $i\epsilon$ is placed to help the integral converge.
$$
\begin{gather}
Z(J) = Z(0)\exp[iW(J)]\quad\text{"Partition function"}\\
W(J) = -\frac12\int{\mathrm{d}^4k\over(2\pi)^4}J^*(k){1\over k^2-m^2+i\varepsilon}J(k)\\
J(k) = \int\mathrm{d}^4x \exp(-ikx)j(x)
\end{gather}
$$
## Summary of the scalar field toy model
Path integral: $\int D\phi \exp(iS) = \int D \phi \exp[i\int \mathrm{d}^4 \mathcal{L}(\phi,\dot{\phi})]$
The Lagrangian: $\mathcal{L} = \underbrace{\frac12 (\partial_\mu)^2 - \frac12 m^2 \phi^2}_\text{free field} + \underbrace{J\phi}_\text{"potential"}$  
$$
\begin{align}
Z &= \bra{0}\exp(-i\hat{H}t)\ket{0}\quad \text{"Partition" (Generating) function}\\
&= \int D\phi \exp\left\{i\int \mathrm{d}^4 x \frac12 \phi [-(\partial^2 + m^2)]\phi + J\phi\right\} \\
&= \text{(const.)}\exp(-\frac12 JA^{-1}J) \\
A^{-1} &= D(x-y) = \int {\mathrm{d}^4k\over(2\pi)^4}{\exp[ik(x-y)]\over k^2 - m^2 + i\epsilon}\quad\text{"Propagator"}\\
Z &= \text{(const.)}\exp\left[-\frac i2 \mathrm{d}^4 x\int \mathrm{d}^4 y J(x) D(x-y) J(y) \right] \equiv \text{(const.)}\exp[iW(J)]\\
J(k)&\equiv \int \mathrm{d}^4 x \exp(-ikx) J(x)\\
W(J)&=-\frac12 \int {\mathrm{d}^4k\over (2\pi)^4} J^*(k){1\over k^2 - m^2 + i\epsilon}J(k)
\end{align}
$$
Interpretation of: $J(x)= J_1(x) + J_2(x)\sim C_1 \delta^3(\vec{x} - \vec{x}_1) + C_2 \delta^3(\vec{x} - \vec{x}_2)$ 
*  $W(J)$ is large if 
	1. $J_{1,2}(k)$ overlaps significantly
	2. $k^2 \to m^2$ gives the main contribution. This disturbance propagates like a particle of mass $m$, the case $k^2=m^2$ is termed the *on-shell* condition. $k^2 \neq m^2$ contributions are included from $\mathrm{d}^4k$ integral ("off-shell (virtual) particles")
$W(J)$ Includes terms like: $J_1^*J_1, J_2^*J_2, J_1^*J_2, J_2^*J_1\Rightarrow$
$$
\begin{align}
W(J) \sim -\frac12 \int \mathrm{d}x^0 \int \mathrm{d}y^0 \int {\mathrm{d}k^0\over (2\pi)}\exp[ik^0(x^0-y^0)]\int {\mathrm{d}^3\vec{k} \over (2\pi)^3}{\exp[i\vec{k}\cdot(\vec{x}_1 - \vec{x}_2)]\over k^2 - m^2 + i\epsilon} \times 2
\end{align}
$$
Using the identity: $$
\delta(x-y) = \int {\mathrm{d}^N\over (2\pi)^N}\exp[ik(x-y)]
$$
We can assert that $k^0 = x^0 - y^0$ , subsequently, by integrating over $x_0$ or $y_0$ , it must be true that $x^0 = y^0$ , and equivalently $k^0 = 0$ . From this, we find that $k^2 = 0 - |\vec{k}|^2$ 
$$
W(J)\sim -\int{\mathrm{d}^3\vec{k} \over (2\pi)^3}{\exp[i\vec{k}\cdot(\vec{x}_1 - \vec{x}_2)]\over -|\vec{k}|^2 - m^2 + i\epsilon} \to \int{\mathrm{d}^3\vec{k} \over (2\pi)^3}{\exp[i\vec{k}\cdot(\vec{x}_1 - \vec{x}_2)]\over |\vec{k}|^2 + m^2}
$$
Returning to the generating function:
$$
Z = \bra{0}\exp(-i\hat{H}t)\ket{0}\to \text{(const.)}\exp[iW(J)]
$$
Comparing the expression $Z \sim \exp(-iEt) \Rightarrow E \sim -W(J$) 
From this toy model, we find the *interaction* between $J_1$ and $J_2$ is *attractive*. Recall that the path(/time)-ordered integral $D\phi$ , we can interpret the path-integral as a description of the exchange (couplings) to $\phi$ "particles" between $J_1$ and $J_2$.
In the $W(J)$ integral, we should be able to derive $E$  as:
$$
E = \frac{1}{4\pi r}e^{-mr}\quad r = |x_1 - x_2|
$$
Which resembles the form of the "Yukawa Potential", which appears in the nucleon binding. The protons and neutrons are bound together by the exchange of pions ($\pi^0$)
## Vector fields
### Fermions (spin-1/2)
* The Dirac Lagrangian:
  $$
 \mathcal{L} = \bar{\psi}(i\not\partial - m \psi)
 $$
 Here we introduce the shorthand "slash notation" : $\not k = \gamma^\mu k_\mu$    where $k^\mu$ is some four-vector. The adjoint spinor $\bar{\psi} = \psi^\dagger \gamma^0$ 
 * The Fermion propagator:
   $$
   D_F(x-y) = \int {\mathrm{d}^4p \over (2\pi)^4}{i(\not p + m)\over p^2 - m^2 + i\epsilon} \exp[-ip\cdot(x-y)]
 $$ 

### Photons (spin-1)
* The electromagnetic Lagrangian:
$$
\mathcal{L}_\text{EM} = -\frac14 F_{\mu\nu}F^{\mu\nu}
$$
* The photon "field": $A_\mu = (\phi,\vec{A})$ where $\phi$ is the electric potential and $\vec{A}$ is the vector potential.
* The photon propagator: 
  $$ -i \frac{g_{\mu\nu}}{k^2+i\epsilon}$$
* The QED Lagrangian:
  $$
 \mathcal{L}_\text{QED} = \underbrace{\bar{\psi}(i\not\partial - m)\psi}_\text{free Fermion} + \underbrace{\left(-\frac14 F_{\mu\nu}F^{\mu\nu}\right)}_\text{free photon} + \underbrace{eA_\mu\bar\psi\gamma^\mu\psi}_\text{EM coupling}
 $$
### Gauge transformation
* $A_\mu$ transform under local gauge as $A_\mu\to A_\mu + \partial_\mu \lambda(x)$ 
* The spinors also undergoes a unitary transformation  : $\psi \to \exp[ie\lambda(x)]\psi$ 
* The derivative of the transformed spinor creates a new term: $[ie\partial_\mu \lambda(x)]\bar{\psi}\gamma^\mu\psi$ 
	* For other terms, the transform meets its conjugate, leaving those terms gauge invariant
* The local gauge transformed Lagrangian reads:$$
  \mathcal{L}\to \mathcal{L} + [ie\partial_\mu \lambda(x)]\bar{\psi}\gamma^\mu\psi + e[\partial_\mu\lambda(x)]\bar{\psi}\gamma^\mu\psi
  $$ Here, we define the covariant derivative $D_\mu$: $$
 \partial_\mu \to D_\mu =  \partial_\mu + ieA^\mu 
 $$ If we promote the four-gradient into the covariant derivative, we will obtain a Lagrangian that is invariant under the $U(1)$ local gauge transformation.
 
 