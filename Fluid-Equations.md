A variety of fluid equations are available, capable of modeling different phenomena.  Common examples include the Euler equations, the Navier-Stokes equations, the viscid and inviscid Burgers's equations, etc.  This will not be an exhaustive discussion of all important fluid equations, but will discuss several important sets of equations.

# Kinetic Theory #

Many equations of fluid dynamics can be derived from kinetic theory.  In order to do so, we will begin with the Boltzmann equation, which is commonly used in transport applications.<a name="footmark1"></a>[<sup>\[1\]</sup>](#footnote1)  The Boltzmann equation describes the evolution of a distribution function \\\(f\\\), which specifies the number density of particles in a given segment of a six-dimensional space: three position dimensions (\\\(\vect{x}\\\), often referred to as coordinate or configuration space) and three motion dimensions (\\\(\vect{v}\\\) or \\\(\vect{p}\\\), often referred to as either velocity or momentum space, depending on the basis you choose).  Thus the units of \\\(f\\\) are m<sup>-6</sup> s<sup>3</sup>.  Integrating the distribution function over motion space yields the number density:
$$n = \iiint f \, \mathrm{d}^3v.$$
The Boltmann equation is
$$\pder{f}{t} + \vect{\nabla}_x \dotprod \left( \dot{\vect{x}} \\, f \right) + \vect{\nabla}_v \dotprod \left( \dot{\vect{v}} \\, f \right) = \mathcal{C} \\! \left[ f \right].$$
The right-hand side \\\(\mathcal{C}\\!\left[f\right]\\\) is the collision operator.  Because \\\(\dot{\vect{x}} = \vect{v}\\\), which are independent variables, space and velocity operations are interchangeable.<a name="footmark2"></a>[<sup>\[2\]</sup>](#footnote2)  We additionally define the acceleration \\\(\vect{a} = \dot{\vect{v}}\\\) and assume that it has zero velocity-divergence.<a name="footmark3"></a>[<sup>\[3\]</sup>](#footnote3)<a name="footmark4"></a>[<sup>\[4\]</sup>](#footnote4)  In order to derive fluid equations from the Boltzmann equation, you take velocity moments.

## Important Quantities for Velocity Moments ##

We have already shown that the number density is the integral of the distribution function over velocity space.  We will use this to define average quantities:
$$\left< q \right> = \frac{1}{n} \iiint q \, f \, \mathrm{d}^3 v.$$
Some authors will define a normalized distribution function \\\(P = f / n\\\) in order to simplify this notation.

The velocity will be split into its average value and its deviations from the average:
$$\vect{v} = \left<\vect{v}\right> + \left(\vect{v} - \left<\vect{v}\right>\right) = \vect{u} + \vect{w}.$$

Additional quantities that will come up include the mass density
$$ \rho = m n,$$
with \\\(m\\\) the rest mass of a single particle, the pressure
$$ P = \frac{\rho}{3} \mbox{Tr}\left( \left< \vect{w} \vect{w} \right> \right) = \frac{\rho}{3} \left< \left| \vect{w} \right|^2 \right>,$$
the viscous stress tensor
$$\tens{\tau} = - \left( \rho \left< \vect{w} \vect{w} \right> - P \tens{I} \right),$$
the specific internal energy
$$\eint = \half \left< \left| \vect{w} \right|^2 \right>,$$
the specific total energy
$$ e = \eint + \half \vect{u} \dotprod \vect{u}$$
and the conductive heat flux
$$\vect{q} = \half \rho \left< \vect{w} \left| \vect{w} \right|^2 \right>.$$
In place of the conductive heat flux, some authors prefer to formulate the equations using the rate of viscous dissipation:
$$ \Psi = \tens{\tau} : \left( \del_x \vect{u} \right).$$
Note that these equations imply a particular relationship between the internal energy and the pressure; this will be discussed later.

## Zeroth Moment ##

Let us multiply the Boltzmann equation by the per-particle rest mass and then take the zeroth velocity moment:
$$ \iiint m \pder{f}{t} + \del_x \dotprod \left( \vect{v} \, m\, f \right) + \del_v \dotprod \left( \vect{a} \, m \, f \right) \, \mathrm{d}^3 v = \iiint m \, \mathcal{C}\\!\left[f\right] \, \mathrm{d}^3 v.$$

Let us begin with the first term:
$$ \iiint m \pder{f}{t} \, \mathrm{d}^3 v
    = \pder{}{t} \left[ m \iiint f \, \mathrm{d}^3 v \right]
    = \pder{}{t} \left[ m \, n \right]
    = \pder{\rho}{t}. $$
We are able to move the time derivative outside of the integral because we are integrating over all velocity space, so the control volume is time-independent.

The second term makes use of the independence of position and motion:
$$ \iiint \del_x \dotprod \left( \vect{v} \, m \, f \right) \, \mathrm{d}^3 v
    = \del_x \dotprod \left[ m \iiint \vect{v} \, f \, \mathrm{d}^3 v \right]
    = \del_x \dotprod \left[ m \, n \left< \vect{v} \right> \right]
    = \del_x \dotprod \left( \rho \, \vect{u} \right).$$

For the third term:
$$ \iiint \del_v \dotprod \left( \vect{a} \, m \, f \right) \, \mathrm{d}^3 v
    = \oiint m \, f \, \vect{a} \dotprod \unitv{n} \, \mathrm{d}^2 v
    = m \vect{a} \dotprod \oiint f \, \unitv{n} \, \mathrm{d}^2 v
    = 0.$$
We have used the divergence theorem to change the volume integral of a divergence into a surface integral.  Do not confuse the unit vector normal to the surface of integration (\\\(\unitv{n}\\\)) with the number density (\\\(n\\\)).  This integral goes to zero because the surface surrounding an infinite space is out at \\\(\left|\vect{v}\right| \to \infty\\\), and the distribution function goes to zero in this limit (there are no particles moving with infinite velocity; even if we were using momentum or celerity, which are not bound by the speed-of-light limit, there would still be no particles with infinite kinetic energy).

# Footnotes #

<a name="footnote1"></a>[<sup>\[1\]</sup>](#footmark1) The Boltzmann equation itself can be derived from the Klimontovich or Liouville equations, making use of the BBGKY hierarchy, but we won't go that deep.  Those interested can find such discussions in various books on kinetic theory and plasma physics, such as _Introduction to Plasma Theory_ by Dwight R. Nicholson (John Wiley & Sons, 1983).

<a name="footnote2"></a>[<sup>\[2\]</sup>](#footmark2) If you choose the momentum basis instead of the velocity basis, the position and motion operators still interchange because \\\(\dot{\vect{x}} = \vect{v} / m\\\), where \\\(m\\\) is constant.  If you are in the relativistic limit, the relation between \\\(\dot{\vect{x}}\\\) and velocity, momentum, or celerity is more complex but the operators still interchange.

<a name="footnote3"></a>[<sup>\[3\]</sup>](#footmark3) If you choose the momentum basis, then use the force \\\(\vect{F}\\\) instead of the acceleration.

<a name="footnote4"></a>[<sup>\[4\]</sup>](#footmark4) It can be shown that the Lorentz electromagnetic force has zero velocity divergence, despite its dependence on velocity.