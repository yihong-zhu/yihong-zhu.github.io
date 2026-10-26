---
title: "CS229 Class - Nonlinear Manifold Approximation for Constraint Modes in Substructuring"
excerpt: "Learning nonlinear corrections to substructuring constraint modes with quadratic operator inference and neural networks <br/> (Stanford CS229 Machine Learning, Spring 2026)"
collection: portfolio
share: false
comments: false
---

For my Stanford CS229: Machine Learning final project (Spring 2026), I studied how to extend the constraint modes used in substructuring to nonlinear problems.

In substructuring, the constraint mode $$C$$ couples neighboring substructures and also serves as a set of shape functions for each substructure's interior. It is derived for linear problems, so for nonlinear ones it can still enforce continuity at the interfaces but no longer represents the interior solution well. I augment it with a correction learned from data, either a quadratic term from operator inference or a neural network:

$$u \approx Cq + \mathcal{H}\,(q \otimes q) \qquad \text{or} \qquad u \approx Cq + \mathcal{N}(q)$$

As a test problem, I used the nonlinear heat equation $$\nabla \cdot \left(\kappa(T;\alpha)\nabla T\right) = 0$$ with diffusivity $$\kappa(T;\alpha) = T^\alpha$$, which shares its elliptic structure with structural mechanics. Across a sweep of the nonlinearity strength $$\alpha \in [0, 2]$$, both corrections beat the linear constraint mode, and the neural network was the most accurate.

[Poster (PDF)](/files/CS229_Poster.pdf)

[![CS229 poster: Nonlinear Manifold Approximation for Constraint Modes in Substructuring](/images/portfolio/cs229/poster.png)](/files/CS229_Poster.pdf)
