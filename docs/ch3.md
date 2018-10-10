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

Still, even _this_ integral is often too tough to handle analytically. Moreover, in problems involving conductors \( \rho \) itself may not be known in advance; since charge is free to move around, the only thing we control directly is the total charge (or perhaps the potential) of each conductor.

In such cases, it is fruitful to recast the problem in differential form, using Poisson's equation
$$
\laplacian{V} = - \frac{1}{\epsilon_0} \rho \label{3.3}
$$
which, together with appropriate boundary conditions, is equivalent to \( \eqref{3.2} \). Very often, in fact, we are interested in finding the potential in a region where \( \rho = 0 \). (If \( \rho = 0 \) everywhere, of course, then \( V = 0  \), and there is nothing further to say - that's not what I mean. There may be plenty of charge elsewhere, but we're confining our attention to places where there is no charge.) In this case, Poisson's equation reduces to Laplace's equation
$$
\laplacian{V} = 0 \label{3.4}
$$
or, written out in Cartesian coordinates,
$$
\frac{\partial^2{V}}{\partial{x^2}} + \frac{\partial^2 V}{\partial{y^2}} + \frac{\partial^2{V}}{\partial{z^2}}  = 0 \label{3.5}
$$

This formula is so fundamental to the subject that one might almost say electrostatics is the study of Laplace's equation. At the same time, it is a ubiquitous equation, appearing in such diverse branches of physics as gravitation and magnetism, the theory of heat, and the study of soap bubbles. In mathematics, it plays a major role in analytic function theory. To get a feel for Laplace's equation and its solutions (which are called __harmonic functions__), we shall begin with the one- and two-dimensional versions, which are easier to picture, and illustrate all the essential properties of the three-dimensional case.