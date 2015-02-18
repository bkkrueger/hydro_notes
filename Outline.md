# The Fluid Equations #

This page will introduce the main fluid equations.

First, we will begin from kinetic theory.  A vague, hand-wavy explanation of the Liouville and Klimontovich equations and the BBGKY hierarchy will be given (ideally with reference to better discussions), so that we can begin with the Boltzmann equation (including accelerations).  Then a discussion of the moment process.  Then we will develop the 0th, 1st, and 2nd moments.

We will introduce the "Euler" approximation (thermal velocity distribution, and how that sets the dissipative effects to zero).

This will give us the "Euler" moments, which we will identify as linear advection, isothermal/adiabatic Euler, full Euler.

We will also introduce nonlinear advection, aka inviscid Burgers's, and viscid Burgers's (which do not follow from the moment process, but are interesting equations nevertheless).

# Solving the Fluid Equations #

This section will begin with the simplest fluid equation: linear advection.  The analytic solution (translation of the initial profile at a constant velocity) will be demonstrated.  Then we will discuss the conservative and non-conservative forms of the linear advection equation.  Then I will show the general form of a conservation law.  This will lead into a basic discussion of finite volume and finite difference methods (for this, Wikipedia's "difference quotient" article should be useful).  I will also discuss Fourier transforms and spectral methods.  Finally I will discuss the strange hybrids that are finite element methods.  Each will be given a cursory discussion, with pointers to the appropriate pages to develop the ideas more thoroughly.