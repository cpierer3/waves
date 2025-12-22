# Implementation of Time Domain Perfectly Matched Layers in Generalized Star-Shaped Coordinates

This Jupyter Book contains the computational implementations from the Bachelor Thesis **"Time Domain Perfectly Matched Layers in Generalized Star-Shaped Coordinates for Scalar Problems."**.

📄 **[Access the complete Bachelor Thesis PDF here](./thesis.html)**

## Abstract

The technique of *complex scaling* is a popular choice when treating such problems. First, the Fourier transformation is applied, which transforms the system from the time domain into the frequency domain. This allows to introduce a complex coordinate transformation outside of a chosen domain of interest, which is done to ensure artificial damping of the wave without spurious reflections. When using so called *Perfectly Matched Layers*, the exterior domain (i.e, the subdomain where the complex scaling is introduced) is truncated and discretized with finite element methods. Then again, applying the inverse Fourier transformation yields the corresponding system in the time domain. Common choices for these scalings are the so called *cartesian scaling* and *radial scaling*. Depending on the application, especially the geometry at hand, one approach may be more suitable than the other. In this work, we introduce a generalization of these methods, amenable to applications on star-shaped domains. Based on findings of [[Wess20](https://doi.org/10.34726/hss.2020.78903)], we introduce specific complex transformations and develop the corresponding formulation in the time domain to solve source problems. Concerning the discretization of the problem, we follow the approach of decomposing a wave into an oscillating transversal and a propagating radial part. This decomposition allows a quick adaptation of our method to specific geometries at hand. Moreover, this particular approach avoids the need of explicit meshing of the exterior domain, and can therefore be easily implemented into regular finite element software (e.g. netgen/ngsolve).

## Book Contents

This book provides practical implementations and numerical experiments that complement the theoretical framework in the thesis:

1. **📄 Bachelor Thesis PDF** - Complete theoretical foundation and mathematical derivations
2. **Frequency Domain PMLs** - Basic Cartesian PML implementation in NGSolve
3. **Star-Shaped PML Methods** - Core methodology with frequency-dependent scaling
4. **Time-Domain Scattering** - Solving source problems in the Time Domain
5. **Eigenvalue Analysis** - Spectral validation and robustness testing

## Dependencies

To run the notebooks, you need the supporting Python files:
- `fem1d.py` - 1D finite element utilities
- `nonlin_arnoldis.py` - Eigenvalue solver routines

```{note}
The notebooks are configured for display only. To execute them, you need NGSolve installed and the supporting `.py` files in your path.
```

```{tableofcontents}
```
