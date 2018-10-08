### 2.4.3: The Energy of a Continuous Charge Distribution

For a volume charge density \( \rho \), \( \eqref{2.42} \) becomes
$$
W = \frac{1}{2} \int \rho V \dd{\tau} \label{2.43}
$$
There is a lovely way to write this result, in which \( \rho \)  and \( V \) are eliminated in favor of \( \vec{E} \). First, use Gauss's law to express \( \rho \) in terms of \( \vec{E} \) 
$$
\rho = \epsilon_0 \div{\vec{E}} \qquad \text{so,} \qquad W = \frac{\epsilon_0}{2} \int (\div{\vec{E}}) V \dd{\tau}
$$
Now, use integration by parts to transfer the derivative from \( \vec{E} \) to \( V \):
$$
W = \frac{\epsilon_0}{2} \left[ - \int \vec{E} \cdot (\grad{V}) \dd{\tau} + \oint V \vec{E} \cdot \dd{\vec{a}} \right]
$$
But \( \grad{V} = - \vec{E} \), so
$$
 W = \frac{\epsilon_0}{2} \left( \int_{\mathscr{V}} E^2 \dd{\tau} + \oint V \vec{E} \cdot \dd{\vec{a}} \right) \label{2.44}
 $$ 

But what volume is this we're integrating over? Let's go back to the formula we started with, \( \eqref{2.43} \). From its derivation, it is clear that we should integrate over the region where the charge is located. But actually, any larger volume would do just as well: The "extra" territory we throw in will contribute nothing to the integral, since \( \rho = 0 \) out there. With this in mind, we return to \( \eqref{2.44} \). What happens here, as we enlarge the volume beyond the minimum necessary to trap all the charge? Well, the integral of \( E^2 \) can only increase (the integrand being positive); evidently the surface integral must decrease accordingly to leave the sum intact. (In fact, at large distances from the charge, \( E \) goes like \( 1 / r^2 \) and \( V \) like \( 1/r \), while the surface area grows like \( r^2 \); roughly speaking, then, the surface integral goes down like \( 1/r \). Please understand: \( \eqref{2.44} \) gives you the correct energy W, whatever volume you use (as long as it encloses all the charge), but the contribution of the volume integral goes up, and that of the surface integral goes down, as you take larger and larger volumes. In particular, why not integrate over _all_ space? Then the surface integral goes to zero, and we are left with
$$
W = \frac{\epsilon_0}{2} \int E^2 \dd{\tau} \quad \text{(all space)} \label{2.45}
$$

