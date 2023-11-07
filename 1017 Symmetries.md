# Noether's Theorem
> If there exists a continuous, global symmetry, then there is a corresponding conserved *charge* (some quantity). 

Consider a Lagrangian $\mathcal{L}(\phi,\partial_\mu\phi)$ 
If there is a continuous symmetry $\phi\to\phi+\alpha\delta\phi$  ($\alpha$ is some parameter) that leaves $\delta\mathcal{L}=0$
$$
\delta\mathcal{L} = \frac{\partial\mathcal{L}}{\partial\phi}\alpha\delta\phi + \frac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\delta(\alpha\partial_\mu\phi)
$$
Using the Euler-Lagrange equation
$$
\delta\mathcal{L}=0= \partial_\mu \underbrace{\left[ {\partial\mathcal{L}\over\partial(\partial_\mu\phi)}\delta\phi\right]}_{J^\mu}
$$
More generally, to leave the physics unchanged, one only needs to require 
$$
\Delta S = \Delta \int \mathrm{d}^4x\mathcal{L} = 0
$$
$\to \Delta \mathcal{L} = 0$ To an overall surface term.
$J^\mu$ is termed the Noether Current
$$
\partial_\mu J^\mu = 0 \quad\text{if}\quad\phi\to\phi+\alpha\delta\phi\quad\text{ is a symmetry }
$$
This is essentially the *continuity equation*, for example, in electrodynamics:
$$
\partial_\mu J^\mu = \frac{\partial\rho}{\partial t}+\nabla\cdot\vec{J}
$$
The *charge* is conserved 
$$
Q \equiv \int \mathrm{d}^3 \vec{x} J^0
$$
## (Free) Complex scalar field
$$
\mathcal{L} = (\partial_\mu\phi^*)(\partial^\mu\phi)-m^2\phi^*\phi
$$
Changing $\phi$ to an overall phase $\phi \to \exp(-i\alpha)\phi\quad(\alpha \in \mathbb{R})$ 
The conjugate field $\phi*\to\exp(i\alpha)\phi^*$  The parameter $\alpha$ is not dependent on space or time, and we may call this demonstration the global $U(1)$ symmetry.
$$
\begin{gather}
\phi = \int [\mathrm{d}k][\hat{a}(k)\exp(-ikx) + \hat{b}^\dagger \exp(ikx)]\\
Q = \int \mathrm{d}^3\vec{x} J^0(x=0,t=0)=\int \mathrm{d}^3\vec{k}[\hat{a}^\dagger(k)\hat{a} - \hat{b}^\dagger(k)\hat{b}(k)] = N_a - N_b
\end{gather}
$$
We can think of $a$ as a *particle* with charge $Q=1$ and $b$ as an *anti-particle* with charge $Q=-1$
# Dirac equation and Noether's Theorem
$$
\mathcal{L} = \bar\psi(i\gamma^\mu\partial_\mu - m)\psi \quad (\bar\psi = \psi^\dagger \gamma^0) 
$$
Here the field $\psi$ as four components, we can express it as a  *2-component spinors*
$$
\psi = \begin{pmatrix}\phi \\ \chi \end{pmatrix}
$$
## Lorentz transformation of spin-1/2 fields
$$
\psi \to \exp(-i\vec{\theta}\vec{J}-i\vec{\phi}\vec{K})\psi
$$
The Lorentz transformation is a rotation and translation (boost) operation
$\vec{\phi}$ is the direction of the boost $|\vec{\phi}|$ is called the *Rapidity*
$\vec{J}$ and $\vec{K}$ are the generators of the Lorentz Group
They satisfy the commutation relation
$$
\begin{align}
[J^i,J^j] &= i\epsilon_{ijk}J^k \\
[K^i,K^j] &= -i\epsilon_{ijk}J^k \\
[K^i,J^j] &= i\epsilon_{ijk}J^k
\end{align}
$$
Define $\vec{J}^\pm\equiv \frac12 (\vec{J}+\vec{K})$ 
$$
\begin{gather}
[J^{\pm,i},J^{\pm,j}] = i\epsilon_{ijk}J^{\pm,k}\\
[]
\end{gather}
$$
The behavior of a field $\psi$ under Lorentz transformation is decomposed into $(j_+,j_-)$ 
There are then two kinds of spin-1/2 fields (spinors): $(\frac12,0)$ and $(0,\frac12)$ 
$$
D_{L/R} = \exp(-\frac i2\vec\theta\cdot\vec\sigma \pm \frac12\vec\phi\vec\sigma)
$$
Where $\vec{\sigma}$ denotes the Pauli matrices. $L/R$ represents the *chirality* , and corresponds to the behavior of a particle that spins clock/counter-clock wise around the direction of motion.

Projection operators
$$
\psi_L = \frac{1-\gamma^5}{2}\psi\quad\psi_R = \frac{1+\gamma^5}{2}\psi
$$
We may write the Dirac equation in terms of  chiral fields $\psi_{L/R}$ in the Weyl basis
$$
\begin{pmatrix}
\psi_L\\ \psi_R
\end{pmatrix}
\quad \gamma^\mu = \begin{pmatrix}
0 &\sigma^\mu\\\bar\sigma & 0
\end{pmatrix}\quad
\gamma^5 = \begin{pmatrix}
-\mathrm{I} & 0 \\ 0 &\mathrm{I} 
\end{pmatrix}
$$
$$
(i\gamma^\mu\partial_\mu-m)\psi = \begin{pmatrix}
-m & i(\partial_0 + \vec\sigma\cdot\nabla)\\
i(\partial_0 - \vec\sigma\cdot\nabla) & -m
\end{pmatrix}
\begin{pmatrix}
\psi_L\\ \psi_R
\end{pmatrix} = 0
$$
$i(\partial_0 + \vec\sigma\cdot\nabla)\psi_L$ 
$i(\partial_0 - \vec\sigma\cdot\nabla)\psi_R$ 
## Dirac Fermions
$$
\psi = 
\begin{pmatrix}
\psi_L\\ \psi_R
\end{pmatrix} \quad or \quad 
\psi = \underbrace{{1 - \gamma^5\over2}\psi}_{\psi_L} + \underbrace{{1 + \gamma^5\over2}\psi }_{\psi_R}
$$
* Chirality of spinors (L/R)
$$
\psi_{L/R}\to \exp[-i\vec\theta\cdot{\vec\sigma\over2} - i\vec \phi \vec K]\psi_{R/L}
$$
* Eigenvalues  

* Mass mixes up $\psi_{L/R}$ 
  $$
\mathcal{L} = \bar\psi(i\not\partial - m)\psi = \bar\psi_Li\not\partial\psi_L
+ \bar\psi_Ri\not\partial\psi_R - m(\bar\psi_L\psi_R + \bar\psi_R\psi_L)
$$Chiral symmetry is an exact symmetry for massless fermions
  

* Helicity: the projection of spin vector to momentum
  $$
 \sim \vec{J}\cdot\vec{p} 
 $$
 For massless particles, helicity is conserved (Lorentz invariant)
Chiral symmetry/helicity is useful in the ultra-relativistic limit and for massless particles.
## Chiral Theory
$$
n\to p\:e^-\:\bar\nu
$$
The interaction lagrangian
$$
\mathcal{L}_\text{int} = G\bar\psi_{1,L}\gamma^\mu\psi_{2,L}\bar\psi_{3,L}\gamma_\mu\psi_{4,L}
$$
# Discrete Symmetries
## Parity

## Charge Conjugation
*Charge* appears in the presence of electromagnetic field $A_\mu$ 
$$
[i\gamma^\mu(\partial_\mu - ieA_\mu) -m]\psi = 0
$$
Charge conjugation can be achieved by taking the complex conjugate of the field equation.
