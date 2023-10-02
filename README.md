# Quantum spectral methods for differential equations

Original authors of research paper: A. M. Childs, J.-P. Liu (2021)

Link to paper: https://link.springer.com/article/10.1007/s00220-020-03699-z

Author of this repo: Óscar Amaro (2023)

Abstract: _Recently developed quantum algorithms address computational challenges in numerical analysis by performing linear algebra in Hilbert space. Such algorithms can produce a quantum state proportional to the solution of a d-dimensional system of linear equations or linear differential equations with complexity poly(log𝑑). While several of these algorithms approximate the solution to within 𝜖 with complexity poly(log(1/𝜖)), no such algorithm was previously known for differential equations with time-dependent coefficients. Here we develop a quantum algorithm for linear ordinary differential equations based on so-called spectral methods, an alternative to finite difference methods that approximates the solution globally. Using this approach, we give a quantum algorithm for time-dependent initial and boundary value problems with complexity poly(log𝑑,log(1/𝜖))._

```FAQ (suggestion):```

- **what is actually being solved?** the linear system $L |X> = |B>$ eq 3.12
- **what is the trick?** using Chebyshev coefficients
- **what are $h, m$?** $h$ is the index running through the different $m$ chunk
- **what is $\gamma$?** initial condition of $x(t=t_0)$
- **what is $\tau_h$?** see before eq 3.3
- **what is $A_h(t)$?** see eq 3.3
- **what are the $P_n$ operators?** see eq 3.20 discrete cosine transform matrix (see [SciPy](https://docs.scipy.org/doc/scipy/reference/generated/scipy.fft.dct.html)/[stackoverflow](https://stackoverflow.com/questions/53875821/scipy-generate-nxn-discrete-cosine-matrix) or [MATLAB page]( https://www.mathworks.com/help/images/discrete-cosine-transform.html) )

```How to read the paper (suggestion):```

- **read** ```§1```: skip theorems
- **read** ```§3```: only beginning, understand mapping eq 3.2, $\tau_h$, $A_h(t)$
- **read** ```§7```: state preparation
- **implement the approach of appendix ```B```** (like in this repo)
- **further reading:** appendix A for eq A.18, A.19 which is the main trick in this approach, ```§8``` main result, ```§9``` application to BVP
- **research questions:** ```§10```
- if you're interested in the **detailed proofs:** ```§4``` for bounds on solution error, ```§5``` on allowed condition number, ```§6``` on success probability
