#### Problem 3.24

!!! question ""

    __Solution__
    Since we are in cylindrical coordinates, we will write Laplace's equation in cylindrical coordinates \( (s, \phi, z) \):
    $$
    \laplacian V = \frac{1}{s} \pdv{}{s} \left( s \pdv{V}{s}  \right) + \frac{1}{s^2} \frac{\partial ^2 V}{\partial \phi ^2} = 0 
    $$
    We'll try the method of separation of variables on s and \( \phi \) by searching for solutions which are products of the form
    $$
    V(s, \phi) = S(s) + \Phi(\phi)
    $$
    $$
    \frac{1}{s} \Phi \dv{}{s} \left( s \dv{S}{s} \right) + \frac{1}{s^2} S \frac{d^2 \Phi}{d\phi ^2} = 0 
    $$
    to separate the variables, we need to divide by V and multiply by \( s^2 \) 
    $$
    \frac{s}{S} \dv{}{s} \left( s \dv{S}{s} \right) + \frac{1}{\Phi} \frac{d^2 \Phi}{d \phi ^2}  = 0
    $$
    We define 
    $$
    f(s) = \frac{s}{S} \dv{}{s} \left( s \dv{S}{s} \right) 
    $$
    and
    $$
    g(\phi) = \frac{1}{\Phi} \frac{d^2 \Phi}{d \phi ^2} 
    $$
    Since we have separated our independent variables and the sum is equal to zero, they must both be constant
    $$
    f(s) = C_1 \qquad g(\phi) = C_2 \qquad C_1 + C_2 = 0
    $$
    Cylindrical symmetry implies that
    $$
    \text{ when } \phi \rightarrow \phi + 2 \pi : \qquad \Phi(\phi + 2 \pi) = \Phi(\phi)
    $$
    So \( C_2 \) must be the positive one, since we know that will give us the periodic solutions to Laplace's equation. We write our constant as \( k^2 \) so
    $$
    \frac{d^2 \Phi}{d \phi ^2} = - k^2 \Phi \\
     \rightarrow \Phi(\phi) = A \cos (k \phi) + B \sin (k \phi), \quad k = 0, 1, 2, 3, \ldots
    $$
    Back to the S part, we need a solution to 
    $$
    s \dv{}{s} \left( s \dv{S}{s} \right) = k^2 S
    $$
    A convenient solution would be a power function, \( S(s) = s^n \) if we choose the power _n_ appropriately
    $$
    \begin{align*}
    s \dv{}{s} \left( s \dv{s^n}{s} \right) & = s \dv{}{s} \left( s n s^{n-1} \right) \\
     & = s \dv{}{s} (n s^n) \\
     & = s n^2 s^{n-1} \\
     & = n^2 s^n \\
     & = k^2 S = k^2 s^n \\
     & \rightarrow n = \pm k
    \end{align*}
    $$
    So, our general solution for S is
    $$
    S(s) = C s^k + D s^{-k}
    $$
    And our general solution will be an infinite series over _k_. But we have to now be careful, because previously we've expressed our general solution in terms of strictly non-zero _k_, but here we have \( k = 0 \), which gives us a constant solution
    $$
    k = 0: \qquad S(s) = C s^0 + D s^0 = \text{const.}
    $$
    But we should get _two_ solutions for a second-order ordinary differential equation. If we go back to the differential equation for S,
    $$
    s \dv{}{s} \left( s \dv{S}{s} \right) = k^2 S \\
    \rightarrow s \dv{S}{s} = \text{ const. } = C \\
    \rightarrow \dv{S}{s} = \frac{c}{s} \\
    \rightarrow \dd S = C \frac{ds}{s} \\
    S(s) = C \ln s + D 
    $$
    This gives us our second solution for S for \( k = 0 \).

    Now what about for \( \Phi \)? Looking at the k = 0 case for the \( \Phi \) ODE,
    $$
    \frac{d^2 \Phi}{d \phi ^2} = - k^2 \Phi = 0 \quad \text{ for } k = 0 \\
    \frac{d \Phi}{d \phi} = \text{ const. } = B \\
    \rightarrow \Phi(\phi) = B \phi + A
    $$
    But this doesn't meet our periodicity requirement! This isn't a physically acceptable solution. For k = 0, \( \Phi = B \) is the only 'physically acceptable' solution (we discard \( B \phi + A \) out of hand.)

    Finally, our general solution looks like
    $$
    V(s, \phi) = a_0 + b_0 \ln s + \sum_{k=1} ^\infty \left[ s^k (a_k \cos k \phi + b_k \sin k \phi) + s^{-k} (a_k \cos k \phi + b_k \sin k \phi) \right]
    $$
    We've only been asked for the general solution in cylindrical coordinates (from which we can tell that our solution is independent of _a_), and we must be given boundary conditions in order to solve for the constants \( a_k, b_k \).
