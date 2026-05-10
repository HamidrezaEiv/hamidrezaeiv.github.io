---
layout: post
title: Successful PhD Defence with Summa Cum Laude Distinction
date: 2025-08-27 12:00:00-0000
inline: false
related_posts: false
_styles: |
  .phd-defense-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
    gap: 0.75rem;
    max-width: 680px;
    margin: 1rem 0 1.5rem;
  }

  .phd-defense-gallery figure {
    margin: 0;
  }

  .phd-defense-gallery img {
    height: 130px;
    object-fit: cover;
  }
---

I successfully defended my PhD thesis at Technische Universität Clausthal on August 27, 2025, and received the grade **summa cum laude**.

**Thesis title:** Physics-Informed Machine Learning for Multiscale Simulations

<div class="phd-defense-gallery">
  {% include figure.liquid path="/assets/img/phd_defense/defense_1.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="PhD defense photo with coworkers and supervisors" %}
  {% include figure.liquid path="/assets/img/phd_defense/defense_2.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="PhD defense photo with coworkers and supervisors" %}
  {% include figure.liquid path="/assets/img/phd_defense/defense_3.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="PhD defense photo with coworkers and supervisors" %}
  {% include figure.liquid path="/assets/img/phd_defense/defense_4.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="PhD defense photo with coworkers and supervisors" %}
</div>

**Abstract**

Multiscale problems are ubiquitous in physics. Numerical simulations of such problems by solving partial differential equations (PDEs) at high resolution using numerical schemes, e.g. the finite element method (FEM), are computationally too expensive for many-query scenarios, such as uncertainty quantification and topology optimization. This limitation has motivated the application of data-driven surrogate models, where the microscale computations are performed with a surrogate.

This thesis explores the algorithmic structure of multiscale simulations and the integration of deep-learning approaches. The discussion includes a suitable training strategy that incorporates specific knowledge of the material behavior to reduce the amount of required training data. An analysis is conducted on the dataset size necessary for reliable hybrid multiscale simulations, with particular emphasis on errors compared to conventional multiscale simulations. Moreover, implementation strategies are addressed to achieve significant speedup. This approach results in a so-called substitutive surrogate model, where microscale numerical computations are replaced by a data-driven surrogate, typically acting as a black box mapping between macroscale quantities. Our results show that substitutive surrogate models can achieve speedup by several orders of magnitude, however, they often have high data demands. Furthermore, since the microscale is entirely replaced, these models generally face challenges in incorporating microscale physical constraints, such as the balance of linear momentum and constitutive material laws. To address these limitations, this research introduces the first operator-learning-based surrogate model that provides microscale solutions for heterogeneous microstructures. Unlike most studies that focus on macroscale mappings, this model integrates known microscale physical relationships, such as the kinematic and constitutive relations. Furthermore, the trained operator network is incorporated into a multiscale solver, where global macroscale mechanics are simulated using FEM, and the microscale quantities are evaluated by the operator network. The results highlight the method's ability to produce accurate solutions.

Additionally, this work introduces the Equilibrium Neural Operator (EquiNO) as a complementary physics-informed PDE surrogate model for predicting microscale physics and evaluates its performance against variational physics-informed neural networks and operator networks. These physics-informed operator networks are trained in an unsupervised manner using physical principles, removing the necessity for large datasets. EquiNO approximates microscale solutions by projecting the governing equations onto a set of divergence-free basis functions, which are obtained by applying proper orthogonal decomposition (POD) to a small dataset. This forms an efficient reduced-order model for rapid inference while inherently preserving equilibrium. The periodic boundary conditions are also enforced as hard constraints.

The proposed framework, applicable to multiscale FE² computations, introduces the Finite Element-Operator Learning (FE-OL) method. Results demonstrate that FE-OL provides accurate solutions for quasi-static solid mechanics problems, even with limited training data. Moreover, EquiNO achieves speedup factors exceeding 8000-fold compared to traditional methods and offers an optimal balance between data-driven and physics-based strategies. EquiNO enables real-time simulations in additive manufacturing and topology optimization and makes high-fidelity modeling feasible for industrial use.
