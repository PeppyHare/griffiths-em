#### Problem 7.7

!!! question "A metal bar of mass _m_ slides frictionlessly on two parallel conducting rails a distance _l_ apart. A resistor R is connected across the rails, and a uniform magnetic field __B__ pointing into the page fills the region. (a) If the bar moves to the right at speed _v_, what is the current in the resistor? (b) What is the magnetic force on the bar? In what direction? (c) If the bar starts out with speed \( v_0 \) at time \( t = 0 \), and is left to slide, what is its speed at a later time t? (d) The initial kinetic energy of the bar was, of course, \( 1/2 m v_0 ^2 \). Check that the energy delivered to the resistor is exactly \( 1/2 m v_0 ^2 \)"
    
    (a) To get the current through the resistor, calculate the flux through the loop:
    $$
    \Phi_B = B l x \\
    emf = - \pdv{\Phi}{t} = - Blv
    $$
    We can always use good old Ohm's law
    $$
    I = V / R = -Blv / R
    $$
    The induced magnetic flux opposes the change in flux, so the current flows down through the resistor.

    (b) Force on the bar? Just use Lorentz force law
    $$
    F = I \int \dd \vec{l} \cross \vec{B} = - \frac{B^2 l^2 v}{R}
    $$
    The direction opposes _x_ (force is to the left).

    (c)
    $$
    v(t = 0) = v_0 \\
    F = m \dv{v}{t} = - \frac{B^2 l^2}{R} v \\
    \frac{\dd v}{v} = - \frac{B^2 l^2 }{m R } \dd t \\
    \int_{v_0} ^v  \frac{\dd v}{v} = - \frac{B^2 l^2 }{m R } \int_0 ^t  \dd t \\
    \ln \frac{v}{v_0} = - \frac{B^2 l^2 }{m R } t \\
    v = v_0 e^{-\frac{B^2 l^2 }{m R } t}
    $$

    (d) Power dissipated in a resistor is
    $$
    P = I^2 R 
    $$
    So energy delivered is
    $$
    \int_0 ^\infty I^2 R \dd t = \frac{B^2 l^2 v^2}{R^2} R \dd t \\
     = \int_0 ^\infty \frac{B^2 l^2}{R} v_0 ^2 e^{-2\frac{B^2 l^2 }{m R } t} \dd t \\
     = - \frac{B^2 l^2}{R} v_0 ^2 \frac{m R}{2 B^2 l^2} [ 0 - 1 ] \\
     = \frac{1}{2} m v_0 ^2
    $$
    Hooray!

#### Problem 7.34

!!! question "A fat wire, radius _a_, carries constant current _I_, uniformly distributed over its cross section. A narrow gap in the wire of width \( w << a \) forms a parallel-plate capacitor, as shown. Find the magnetic field in the gap, at a distance \( s < a \) from the axis."
    
    Within the wire, you can draw an Amperian loop to find B within the wire with 
    $$
    \int B \cdot \dd l = \mu_0 I_{enc}
    $$
    Within the gap, we need the Ampere's correction term
    $$
    \curl \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \pdv{\vec{E}}{t} \\
    \oint B \cdot \dd l = \mu_0 \epsilon_0 \int \pdv{\vec{E}}{t} \cdot \dd l
    $$
    Current is flowing to the end of the wire with nowhere to go, so it must build up there. We've got a parallel plate capacitor within the gap
    $$
    B(s) \cdot 2 \pi s = \mu_0 \epsilon_0 \dv{}{t} \int \frac{\sigma (t) }{\epsilon_0} \dd a
    $$
    $$
    B(s) = \frac{\mu_0}{2} s \pdv{\sigma}{t} = \frac{\mu_0 s}{2} \frac{I}{\pi a^2}
    $$
    where \( \pdv{\sigma}{t} = \dv{A}{t} \frac{1}{\pi a^2} \) 
    $$
    B(s) = \frac{\mu_0 I}{2 \pi a^2} s \hat{\phi}
    $$
