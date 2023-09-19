# Klein-Gordon Equation
$$
(\partial_\mu \partial^\mu + m)\psi = 0
$$
*  There exists a negative energy solution: $$\begin{gather*}
  \psi \sim \exp(-iEt + i \vec{p}\cdot\vec{x})\\
  E^2 = p^2 + m^2\rightarrow E = \pm \sqrt{p^2 + m^2}
  \end{gather*}
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
* We expect to recover the Klein-Gordon equation in $$\begin{gather*}(i\gamma^\nu\partial_\nu + m)(i\gamma^\mu\partial_\mu -m)\psi = 0\\
  -(\gamma^\mu\gamma^\nu \partial_\mu \partial_\nu + m^2)\psi=0
  \end{gather*}$$
* The structure above suggests symmetric and an anti-commutation relation of:$$
  \{\gamma^\mu,\gamma^\nu\} = 2\eta^{\mu\nu}
  $$$\gamma^0\gamma^0 = \mathrm{I}_{4\times4}$ and $\gamma^i\gamma^i = -\mathrm{I}_{4\times4}$ $\gamma^\mu$  $(i = 1,2,3)$
  $\gamma$ defined by four $4\times4$ matrices:
  $$\gamma^0 = \begin{pmatrix}\mathrm{I}_{2\times2} & 0\\
  0 &-\mathrm{I}_{2\times2}\end{pmatrix}\quad
  \gamma^i = \begin{pmatrix} 0 & \sigma^i\\
  -\sigma^i & 0 \end{pmatrix}$$
* $\psi$ is now a four component column vector (spinors), and transforms either as left- or right-handed particles under Lorentz transform

In the rest frame of a spin-1/2 particle of mass m:$$
\psi(x) = \int \frac{\mathrm{d}^4 p }{(2\pi)^4}\exp(-ip\cdot x)\psi(p)
$$
In momentum-space:$$\begin{gather*}
(\partial^\mu p_\mu - m)\psi(p) = 0 \rightarrow (\gamma^0 - \mathrm{I})\psi = 0 \\
\begin{pmatrix}0&0\\0&\mathrm{I}_{2\times2}\end{pmatrix}\psi = 0\end{gather*}
$$
and as expected, we only require 2 degrees of freedom for a spin-1/2 particle. 
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
$$
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
a and b are real factors, we can set absorb the factors into the field for simplicity
$$ \mathcal{L} = \pm\frac{1}{2}(\partial_\mu\phi\:\partial^\mu \phi+ b\phi^2 )$$

$$\begin{gather*}\Pi = {\partial\mathcal{L}\over\partial\dot{\phi}} = \pm \dot{\phi}\quad \\
\mathcal{H} = \dot{\phi}\Pi - \mathcal{L} = \pm\Pi^2 \mp \frac{1}{2}(\Pi^2)
\end{gather*}$$
Considering the positive energy solution, we require $\mathcal{H}$ to be bounded from below. Demand $b < 0$ and we can see that $b = -m^2\:(m>0)$ is the mass term
$$
\mathcal{L} = \frac{1}{2}(\partial_\mu\phi\:\partial^\mu\phi) - \frac{1}{2}m^2\phi^2
$$ We can verify that:$$
\partial_\mu {\partial\mathcal{L}\over\partial(\partial_\mu\phi)}-{\partial{L}\over\partial\phi}
$$
# The Dirac Lagrangian

$$$\mathcal{L} = \bar{\psi}i(\gamma^\mu\partial_\mu - m)\psi$$