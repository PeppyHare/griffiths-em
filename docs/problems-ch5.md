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
    <p align="center"> <img alt="Figure 5.25" src="../img/5.25.png" /> </p>
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

#### Problem 5.23

!!! question "Find the magnetic vector potential of a finite segment of straight wire carrying a current I. [Put the wire on the z axis, from \( z_1 \) to \( z_2 \), and use Eq. 5.66.] Check that your answer is consistent with Eq. 5.37."

    <p align="center"> <img alt="Figure 5.e.23" src="../img/5.e.23.png" /> </p>
    We will get our vector potential using Eq 5.66, as suggested
    $$
    \begin{align*}
    \vec{A} & = \frac{\mu_0 }{4 \pi} \int \frac{I \vu{z}}{\gr} \\
    & = \frac{\mu_0 I}{4 \pi} \vu{z} \int _{z_1} ^{z_2} \frac{dz}{\sqrt{z^2 + s^2}} \\
    & = \left. \frac{\mu_0 I}{4 \pi} \vu{z} \left[ \ln \left( z + \sqrt{z^2 + s^2}  \right) \right] \right|_{z_1} ^{z_2} \\
    & = \frac{\mu_0 I}{4 \pi} \ln \left( \frac{z_2 + \sqrt{(z_2)^2 + s^2}}{z_1 + \sqrt{(z_1)^2 + s^2}}  \right) \vu{z}
    \end{align*}
    $$

    To get the magnetic field, we need to take the curl of __A__. We can easily tell from the symmetry of the problem that the field will be "circumferential" (in the \( \vu{\phi} \) direction):

    $$
    \begin{align*}
    \vec{B} & = \curl \vec{A} = - \pdv{A}{s} \vu{\phi} \\
    & = - \frac{\mu_0 I}{4 \pi} \left( \frac{1}{z_2 + \sqrt{(z_2)^2 + s^2}} \frac{s}{\sqrt{(z_2)^2 + s^2}} - \frac{1}{z_1 + \sqrt{(z_1)^2 + s^2}} \frac{s}{\sqrt{(z_1)^2 + s^2}} \right) \vu{\phi} \\
    & = - \frac{\mu_0 I s}{4 \pi} \left( \frac{z_2 - \sqrt{z_2 ^2 + s^2}}{z_2 ^2 - (z_2 ^2 + s^2)} \frac{1}{\sqrt{z_2 ^2 + s^2}} - \frac{z_1 - \sqrt{z_1 ^2 + s^2}}{z_1 ^2 - (z_1 ^2 + s^2)} \frac{1}{\sqrt{z_1 ^2 + s^2}} \right) \vu{\phi} \\
    & = - \frac{\mu_0 I s}{4 \pi} \left( - \frac{1}{s^2} \right) \left( \frac{z_2}{\sqrt{z_2 ^2 + s^2}} - 1 - \frac{z_1}{\sqrt{z_1 ^2 + s^2}} + 1  \right) \vu{\phi} \\
    & = \frac{\mu_0 I}{4 \pi s} \left( \frac{z_2}{\sqrt{(z_2) ^2 + s^2}} - \frac{z_1}{\sqrt{z_1 ^2 + s^2}} \right) \vu{\phi}
    \end{align*}
    $$

    or, in terms of the angles made between __r__ and the axis of the wire,

    $$
    \sin \theta_1 = \frac{z_1}{\sqrt{z_1 ^2 + s^2}} \quad \text{ and } \quad \sin \theta_2 = \frac{z_2}{\sqrt{z_2 ^2 + s^2}} 
    $$

    $$
    \vec{B} = \frac{\mu_0 I}{4 \pi s} (\sin \theta_2 - \sin \theta_1) \vu{\phi} 
    $$
    which is just what we got back in Eq. 5.37.