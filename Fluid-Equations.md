A variety of fluid equations are available, capable of modeling different phenomena.  Common examples include the Euler equations, the Navier-Stokes equations, the viscid and inviscid Burgers's equations, etc.  This will not be an exhaustive discussion of all important fluid equations, but will discuss several important sets of equations.

# Kinetic Theory #

Many equations of fluid dynamics can be derived from kinetic theory.  In order to do so, we will begin with the Boltzmann equation, which is commonly used in transport applications.<a name="footmark1"></a>[<sup>\[1\]</sup>](#footnote1)  The Boltzmann equation describes the evolution of a distribution function \\\(f\\\), which specifies the number density of particles in a given segment of a six-dimensional space: three position dimensions (\\\(\vect{x}\\\), often referred to as coordinate or configuration space) and three motion dimensions (\\\(\vect{v}\\\) or \\\(\vect{p}\\\), often referred to as either velocity or momentum space, depending on the basis you choose).  Thus the units of \\\(f\\\) are m<sup>-6</sup> s<sup>3</sup>.  Integrating the distribution function over motion space yields the number density:
$$n = \iiint\ f \, \mathrm{d}^3v.$$$
The Boltmann equation is
$$\frac{\partial f}{\partial t} + \vect{\nabla}_x \\!\cdot\\! \left( \dot{\vect{x}} \\, f \right) + \vect{\nabla}_v \\!\cdot\\! \left( \dot{\vect{v}} \\, f \right) = \mathcal{C} \\! \left[ f \right].$$
The right-hand side \\\(\mathcal{C}\\!\left[f\right]\\\) is the collision operator.  Because \\\(\dot{\vect{x}} = \vect{v}\\\), which are independent variables, space and velocity operations are interchangeable.<a name="footmark2"></a>[<sup>\[2\]</sup>](#footnote2)  We additionally define the acceleration \\\(\vect{a} = \dot{\vect{v}}\\\) and assume that it has zero velocity-divergence.<a name="footmark3"></a>[<sup>\[3\]</sup>](#footnote3)<a name="footmark4"></a>[<sup>\[4\]</sup>](#footnote4)  In order to derive fluid equations from the Boltzmann equation, you take velocity moments.

## Zeroth Moment ##

The distribution function is normalized

# Footnotes #

<a name="footnote1"></a>[<sup>\[1\]</sup>](#footmark1) The Boltzmann equation itself can be derived from the Klimontovich or Liouville equations, making use of the BBGKY hierarchy, but we won't go that deep.  Those interested can find such discussions in various books on kinetic theory and plasma physics, such as _Introduction to Plasma Theory_ by Dwight R. Nicholson (John Wiley & Sons, 1983).

<a name="footnote2"></a>[<sup>\[2\]</sup>](#footmark2) If you choose the momentum basis instead of the velocity basis, the position and motion operators still interchange because \\\(\dot{\vect{x}} = \vect{v} / m\\\), where \\\(m\\\) is constant.  If you are in the relativistic limit, the relation between \\\(\dot{\vect{x}}\\\) and velocity, momentum, or celerity is more complex but the operators still interchange.

<a name="footnote3"></a>[<sup>\[3\]</sup>](#footmark3) If you choose the momentum basis, then use the force \\\(\vect{F}\\\) instead of the acceleration.

<a name="footnote4"></a>[<sup>\[4\]</sup>](#footmark4) It can be shown that the Lorentz electromagnetic force has zero velocity divergence, despite its dependence on velocity.