---
layout: page
title: Research
permalink: /research
sidebar_link: true
sidebar_sort_order: 2
---

### Entropy Stable Discontinuous Galerkin-Fourier methods

We developed a novel discontinuous Galerkin-Fourier method for systems of nonlinear conservation laws. It is suitable
for simulating flows with spanwise homogeneous geometries. The computational domain is discretized into wedges, and the
approximation space is the tensor product of polynomial basis and nodal Fourier basis. The construction
of such methods depends on the summation-by-parts (SBP) operators. In particular, we used the **hybridized SBP
operator**
introduced by Chan and the **spectral differentiation matrix**. The resulting formulation satisfies a discrete entropy
inequality. We accelerate the implementation using GPU, and we divide the computation into two passes, one through
triangles,
another through Fourier slices, to utilize the data locality.

***Figure***  Sparsity plot of the hybridized SBP operators and the spectral differentiation matrices. Highlighted nodes
correspond to flux evaluations in the physical space.  

<img src="image/ESDG-Fourier_plot.png" width="500" style="display: block; margin: 0 auto;">
