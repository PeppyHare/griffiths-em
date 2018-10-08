# Chapter 3: Potentials

## 3.1: Laplace's Equation

### 3.1.1: Introduction

The primary task of electrostatics is to find the electric field of a given stationary charge distribution. In principle, this purpose is accomplished by Coulomb's law, in the form of
$$
\vec{E}(\vec{r}) = \frac{1}{4 \pi \epsilon_0} \int \frac{\rho(\vec{r'})}{\gr ^2} \hat{\gr} \dd{\tau'} \label{3.1}
$$

Unfortunately, integrals of this type can be difficult to calculate for any but the simplest charge configurations. Occasionally we can get around this by exploiting symmetry and using Gauss's law, but ordinarily the best strategy is first to calculate the _potential_, V, which is given by the somewhat more tractable
$$
V(r) = \frac{1}{4 \pi \epsilon_0} \int \frac{\rho(\vec{r}')}{\gr} \dd{\tau'} \label{3.2}
$$