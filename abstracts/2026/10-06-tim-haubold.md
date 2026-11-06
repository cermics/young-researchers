---
layout: page
abstract_page: true
title: "Unfitted Discontinuous Galerkin Methods for the First Order Linear Wave Equations"
permalink: /abstracts/2026/10-06-tim-haubold/
---

**Speaker:** Tim Haubold  
**Date:** Tuesday 6 October 2026

## Abstract

Simulating wave propagation on complex or moving geometries usually requires a mesh that conforms to the domain boundary, which is costly to generate and maintain. Unfitted (CutFEM) methods avoid this by embedding the domain in a fixed background mesh. The price is that arbitrarily cut elements make the discrete system ill-conditioned and can restrict the stable time step.

This talk presents an unfitted discontinuous Galerkin discretization for the first order linear wave equation. Boundary or interface conditions are imposed weakly with Nitsche's method, and a ghost penalty stabilizes the cut elements. We discuss how the stabilization gives conditioning and CFL bounds that do not depend on how the boundary cuts the mesh. Moreover, we will discuss the stability of an explicit third order Runge-Kutta scheme, where the mass matrix is perturbed by a ghost penalty.

Joint work with Alexandre Ern.
