---
layout: post
title: EquiNO is now available in Journal of Computational Physics
date: 2026-02-05 12:00:00-0000
inline: false
related_posts: false
---

Our paper, [EquiNO: A physics-informed neural operator for multiscale simulations](https://www.sciencedirect.com/science/article/pii/S0021999126000951), is now available in *Journal of Computational Physics*. The source code, datasets, trained models, and supplementary materials are available in the [GitHub repository](https://github.com/HamidrezaEiv/EquiNO).

{% include figure.liquid path="/assets/img/publication_preview/equino.png" class="img-fluid rounded z-depth-1" zoomable=true alt="Graphical abstract for the EquiNO paper" %}

**Highlights**

- Introduces EquiNO, a physics-informed neural operator for multiscale simulations.
- Presents FE-OL, a framework that integrates the finite element method with operator learning.
- Enforces equilibrium and periodic boundary conditions by construction.
- Provides an efficient reduced-order model for rapid inference.
- Achieves a speedup of more than three orders of magnitude over FE2 methods.

**Abstract**

Multiscale problems are ubiquitous in physics. Numerical simulations of such problems by solving partial differential equations at high resolution are computationally too expensive for many-query scenarios, such as uncertainty quantification, remeshing applications, and topology optimization. This limitation has motivated data-driven surrogate models that replace microscale computations with black-box mappings between macroscale quantities. Although these approaches can provide substantial speedups, they often struggle to incorporate microscale physical constraints such as the balance of linear momentum.

In this work, we propose the Equilibrium Neural Operator (EquiNO), a physics-informed PDE surrogate in which equilibrium is enforced by construction. EquiNO projects the solution onto divergence-free basis functions obtained through proper orthogonal decomposition, satisfying equilibrium without penalty terms or multi-objective loss functions. We compare EquiNO with variational physics-informed neural and operator networks, as well as purely data-driven operator-learning baselines. The proposed finite element-operator learning framework is applied to quasi-static solid-mechanics problems and yields accurate solutions even with restricted training datasets. EquiNO achieves speedup factors exceeding 8000-fold compared with traditional FE2 simulations while providing a robust and physically consistent surrogate model.
