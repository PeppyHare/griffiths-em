#### Problem 5.5

!!! question "A current I flows down a wire of radius a. (a) If it is uniformly distributed over the surface, what is the surface current density K? (b) If it is distributed in such a way that the volume current density is inversely proportional to the distance from the axis, what is J(s)?"
    
    K is the current per unit width \( \perp \) to the direction of the flow.
    $$
    K = \frac{I}{2 \pi a} 
    $$
    Suppose instead the current is distributed somehow throughout the volume of the wire such that the current density is inversely proportional to the distance from the axis. Then
    $$
    j = \frac{\text{current}}{\text{unit area } \perp \text{ flow}} = \frac{d I}{da_{\perp}} 
    $$
    We suppose that _j_ has the form
    $$
    j = \frac{\text{const.}}{s} = \frac{c}{s} 
    $$
    $$
    \begin{align*}
    I & = \int j \dd a_{\perp} \\
    & = \int_{0} ^a \int_{0} ^{2 \pi} \frac{c}{s} s \dd s \dd \phi \\
    & = 2 \pi c a
    \end{align*}
    $$
    so
    $$
    c = \frac{I}{2 \pi a} 
    $$
    and
    $$
    j = \frac{I}{2 \pi a s} 
    $$

#### Problem 5.11

!!! question "Find the magnetic field at point P on the axis of a tightly wound solenoid (helical coil) consisting of _n_ turns per unit length wrapped around a cylindrical tube of radius _a_ and carrying current _I_ (Fig 5.25). Express your answer in terms of \( \theta_0 \) and \( \theta_2 \) (it's easiest that way). Consider the turns to be essentially circular and use the result of Ex 5.6. What is the field on the axis of an infinite solenoid (infinite in both directions)?"
    
    ![Figure 5.25](img/5.25.png)
    If I have _n_ turns per unit length, then I have \( n \dd z \) turns along a length \( \dd z \) (using the natural cylindrical coordinates of the problem). The total current of the resulting loop is \( I n \dd z \). From Ex 5.6, we know the magnetic field due to a circular loop is
    $$
    \dd \vec{B}(z) = \frac{ \mu_0 n I \dd z}{2} \frac{a^2}{(a^2 + z^2 )^{3/2}} \vu{\phi} 
    $$
    From the geometry of Fig 5.25,
    $$
    \tan \theta = \frac{a}{z} \quad \rightarrow \quad z = \frac{a}{\tan \theta} 
    $$
    $$
    \dd z = - \frac{a}{\sin ^2 \theta} \dd \theta
    $$
    $$
    (a^2 + z^2)^{3/2} = \left( a^2 + \frac{a^2}{\tan ^2 \theta} \right)^{3/2} = \left( \frac{a}{\sin \theta}  \right)^3
    $$
    $$
    \begin{align*}
    B(z) & = \frac{\mu_0 n I}{2} \left( - \frac{a}{\sin ^2 \theta} \dd \theta \right)\frac{a^2}{(a^3 / \sin ^3 \theta)} \\
    & = - \frac{\mu_0 n I}{2} \sin \theta \dd \theta
    \end{align*}
    $$
    $$
    \begin{align*}
    B(z) & = - \frac{\mu_0 n I}{2} \int _{\theta_1} ^{\theta_2} \sin \theta \dd \theta \\
    & = \frac{\mu_0 n I}{2} (\cos \theta_2 - \cos \theta_1)
    \end{align*}
    $$
    For an infinite solenoid, we get
    $$
    B(z) = \frac{\mu_0 n I}{2} (\cos(0) - \cos \theta_1)
    $$