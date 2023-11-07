# Recurrent neural network
* Used in DL1R
* MLP input
* DeepSets
	* Pooling
	* Permutation invariant
	* No interaction between input objects
# Transformers
* Used in SPANet
* 2039.01886
* Attention
# Normalizing flows for neutrino reconstruction
## A review on Neutrino Weighting
### References
*  [PRL 80 1998 pp. 2063-2068](https://arxiv.org/pdf/hep-ex/9706014.pdf)
  Top quark mass measurement in dilepton events (Original NW paper)
* [arXiv:1903.07570](https://arxiv.org/pdf/1903.07570.pdf)  
  Top quark pair spin correlation   
* [arXiv:2307.13783](https://arxiv.org/pdf/2307.13783.pdf)  
  Bell inequality tests in H-> WW semi-leptonic channel
### Method
* Known:
	* Jet four-momentum (from hadronic decaying W)
	* Lepton four-momentum (from leptonic decaying W)
	* MET
* Unknown:
	* Leptonic decaying W boson four-momentum
	* Neutrino four-momentum (from leptonic decaying W)
	* 
* Assumptions:
	* Higgs boson is 125 GeV (constraint)
	* Hadronically decaying W boson is on-shell (constraint)
	* Leptonically decaying W boson mass (test parameter)
	* Neutrino pseudorapidity (test parameter)
In the assumed $\eta_\nu$ and $M(W_\text{lep})$ phase space, reconstruct the neutrino momentum $p_x$ and $p_y$ components, assign weight using following formula:
$$
\exp \left[-{(\hat{p}_x - p_x^\text{miss})^2 \over \sigma_{p_x}}\right]
\exp \left[-{(\hat{p}_y - p_y^\text{miss})^2 \over \sigma_{p_y}}\right]
$$
$$
\begin{align*}
&p(W_H): (E^j,p^j_x,p^j_y,p^j_z)\\
&p(W_L): (E^\nu+E^\ell, p^\nu_x + p^\ell_x,p^\nu_y + p^\ell_y,p^\nu_z + p^\ell_z  )\\
&(E^j + E^\nu + E^\ell)^2 - |\vec{p}^j + \vec{p}^\nu + \vec{p}^\ell|^2 = 125\\
&p(\nu):(E^\nu,\hat\eta )
\end{align*}
$$

## $\nu$ - Flows [arXiv:2207.00664](https://arxiv.org/abs/2207.00664)
## Case study: Semi-leptonic ttbar decay

## $\nu^2$ - Flows [arXiv:2307.02405](https://arxiv.org/abs/2307.02405) 
