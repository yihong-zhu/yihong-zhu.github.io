---
title: "AA214 Class - 2D Compressible Euler with Finite Volume Method"
excerpt: "A 2D vertex-based finite volume solver for the compressible Euler equations <br/> (Stanford AA214 Numerical Methods for Compressible Flows, Winter 2026)"
collection: portfolio
share: false
comments: false
---

For Stanford's AA214: Numerical Methods for Compressible Flows (Winter 2026), I wrote a 2D vertex-based finite volume solver for the compressible Euler equations and applied it to two problems: an unsteady shock tube and steady supersonic flow over a ramp.

Shock Tube
======

The tube starts with two fluid states separated at $$x = 0$$:

| | Pressure $$p$$ $$(\mathrm{N/m^2})$$ | Density $$\rho$$ $$(\mathrm{kg/m^3})$$ | $$u$$ $$(\mathrm{m/s})$$ | $$v$$ $$(\mathrm{m/s})$$ |
|---|---|---|---|---|
| Left ($$L$$) | $$10^5$$ | $$1$$ | $$100$$ | $$0$$ |
| Right ($$R$$) | $$10^4$$ | $$0.125$$ | $$50$$ | $$0$$ |

![Shock tube: evolution of pressure, density, and u and v velocity](/images/portfolio/aa214/shock-tube.gif)

Supersonic Ramp
======

Free-stream Mach number $$M_\infty = 2$$ over an $$8^\circ$$ ramp, marched to steady state with local time stepping. 
<!-- I compared two $$60 \times 20$$ grids: a uniform one ($$r = 1$$) and one stretched toward the outlet ($$r = 0.1$$). -->

<!-- ![Computational grids for r = 1 and r = 0.1](/images/portfolio/aa214/ramp-grids.png) -->

<!-- **Uniform grid ($$r = 1$$):** converged to a residual tolerance of $$\varepsilon = 2 \cdot 10^{-5}$$ in 21,962 iterations (259.1 s wall-clock time).

![Density, pressure, Mach number, and convergence history on the r = 1 grid](/images/portfolio/aa214/ramp-solution-r1.png) -->

<!-- **Stretched grid ($$r = 0.1$$):** converged to the same tolerance in 20,652 iterations (231.4 s wall-clock time).

![Density, pressure, Mach number, and convergence history on the r = 0.1 grid](/images/portfolio/aa214/ramp-solution-r01.png) -->

![Density, pressure, Mach number, and convergence history](/images/portfolio/aa214/ramp-solution-r01.png)
