# Wave Propagation with PML Methods

This repository contains the numerical implementations and code examples for the methods presented in the accompanying bachelor thesis PDF document. The notebooks provide practical demonstrations of the theoretical concepts developed in the thesis, offering hands-on examples of Perfectly Matched Layer (PML) techniques for wave scattering problems.

## Abstract

The technique of *complex scaling* is a popular choice when treating such problems. First, the Fourier transformation is applied, which transforms the system from the time domain into the frequency domain. This allows to introduce a complex coordinate transformation outside of a chosen domain of interest, which is done to ensure artificial damping of the wave without spurious reflections. When using so called *Perfectly Matched Layers*, the exterior domain (i.e, the subdomain where the complex scaling is introduced) is truncated and discretized with finite element methods. Then again, applying the inverse Fourier transformation yields the corresponding system in the time domain. Common choices for these complex scalings are the so called *cartesian scaling* and *radial scaling*. Depending on the application, especially the geometry at hand, one approach may be more suitable than the other. In this work, we introduce a generalization of these methods, amenable to applications on star-shaped domains. Based on findings of [Wess dissertation], we introduce specific complex transformations and develop the corresponding formulation in the time domain to solve source problems. Concerning the discretization of the problem, we follow the approach of decomposing a wave into an oscillating transversal and a propagating radial part. This decomposition allows a quick adaptation of our method to specific geometries at hand. Moreover, this particular approach avoids the need of explicit meshing of the exterior domain, and can therefore be easily implemented into regular finite element software (e.g. netgen/ngsolve).

## Notebooks

**standard_pml.ipynb** - Demonstrates NGSolve's built-in Cartesian PML functionality for rectangular domains

**star-shaped.ipynb** - Implements star-shaped PML using frequency-dependent complex scaling for non-convex geometries

...