---
title: "Rocket Propulsion Lab at UCSD"
excerpt: "A MATLAB project I built to teach new members of my propulsion team the basics of supersonic nozzle flow."
collection: portfolio
share: false
comments: false
---

At UC San Diego's Rocket Propulsion Laboratory (RPL), I built this MATLAB project to onboard new members of our propulsion team. Starting from the 2D nozzle geometry, the chamber stagnation temperature $$T_0$$ and pressure $$P_0$$, and an operating altitude, it walks through a quasi-1D isentropic analysis of the nozzle flow.

The Equations
======

The Mach number at each station follows from the area–Mach relation, taking the subsonic root upstream of the throat and the supersonic root downstream:

$$\frac{A}{A^*} = \frac{1}{M}\left[\frac{2}{\gamma+1}\left(1+\frac{\gamma-1}{2}M^2\right)\right]^{\frac{\gamma+1}{2(\gamma-1)}}$$

Pressure and temperature then follow from the isentropic relations:

$$\frac{P}{P_0} = \left(1+\frac{\gamma-1}{2}M^2\right)^{-\frac{\gamma}{\gamma-1}}, \qquad \frac{T}{T_0} = \left(1+\frac{\gamma-1}{2}M^2\right)^{-1}$$

With the throat choked, the mass flow rate and the thrust are

$$\dot{m} = \rho_0 a_0 A^* \left(\frac{\gamma+1}{2}\right)^{-\frac{\gamma+1}{2(\gamma-1)}}, \qquad F = \dot{m}\, u_e + \left(P_e - P_a\right) A_e$$

where the ambient pressure $$P_a$$ comes from the standard atmosphere at the operating altitude. Finally, the combustion chamber is sized from its characteristic length $$L^* = V_c / A^*$$.

Results
======

Temperature, pressure, and Mach number through the combustion chamber ($$x < 0$$) and the nozzle ($$x > 0$$), normalized by the stagnation values:

![Temperature, pressure, and Mach number contours through the combustion chamber and nozzle](/images/portfolio/rpl/nozzle-contours.jpg)

The same quantities along the nozzle. The dashed line marks the throat, where $$M = 1$$; the flow leaves the nozzle at about $$M_e \approx 3.2$$.

![Pressure, temperature, and Mach number distributions along the nozzle](/images/portfolio/rpl/nozzle-profiles.png)
