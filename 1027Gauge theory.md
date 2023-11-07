# Rotational Group
Orthogonal group $O(N)$ 
$\vec{V} = (V_1, V_2, \dots, V_N)^T\quad V_i \in \mathbb{R}$ 
$\vec{V}^\prime = R\vec{V}$
$\vec{W}^\prime = R\vec{W}$ 
# Gauge group in the Standard Model
$$
G = SU_c(3)\otimes SU_L(2)\otimes U_Y(1)
$$
* $SU_c(3)$ c for color (QCD/Strong)
* $SU_L(2)$ Left chiral (weak interaction)
* $U_Y(1)$ Y: Hypercharge
## Special Unitary Group (SU)
$N\times N$ unitary matrices
A complex vector $\vec{V} = (V_1\dots V_N)^T$
$$
SU(N) = \{U_{N\times N} | U^\dagger U = \mathrm{I}, \det[U] = 1\}
$$
$V\to UV$ and $W \to UW$ leaves $V^\dagger U$ invariant since $U^\dagger U = \mathrm{I}$ 
We may express $U$ as $U = \exp(iT_{N\times N})$ where  $T^\dagger = T$ is Hermitian
$\mathrm{tr}[T] = 0$ therefore $T_{N\times N}$ has $N^2 - 1$ degrees of freedom
Recall that the Lagrangian takes the general form of
$$
\mathcal{L}(\Phi,\partial_\mu \Phi) 
$$
Is a function of fields and derivative of fields. The Lagrangian is invariant under some continuous symmetry group $G$ 
$$
G : \Phi\to D(g)\Phi \quad g\in G
$$
$D(g)$ is a representation of $g\in G$ 
# Lie Group
$g(\alpha_1,\alpha_2,\dots,\alpha_N)$ where $\alpha_i$ are continuous parameters, group $G$ is of dimension $N$ 
$g\to D(g)$ a finite dimension ($M$) representation of G acting on a $M$ dimension vector space.
Unitary $D^\dagger(g) = D^{-1}(g) = D(g^{-1})$   is termed a *compact lie group* 
$D[g(\alpha_a)] = \exp(i\alpha_aT^a),\: \alpha = 1,2,\dots,N$  
$T_a$ are generators ($M\times M$ matrix)
Commutation relations: $[T^a,T^b] = if^{abc}T^c$ 
* $f^{abc}$ is the structure constant
* We call the set of $M\times M$ representation of $a(G)$: $\{T^a\}$ the *Lie algebra*
* $\Phi(x)\to D[g(\alpha)]\Phi \approx(1 + i\alpha_aT^a)\Phi + \mathcal{O}(\alpha^2)$      $g(x)\Phi(x)$ has local symmetry
Gauge transformation
$$
D_\mu \Phi = \partial_\mu \Phi - iA_\mu \Phi
$$
$\mathcal{L}[\Phi, D_\mu\phi]\to \mathcal{L}[\Phi,gD_\mu \Phi]$
Gauge Fields:
* In $U_Y(1)$: Photons $A^\mu$
* In $SU_L(2)$ : W bosons in the standard model
* In $SU_c(3)$: 8 gluons 
