# Hybrid Gaussian–Wavelet Detector Lab

**Version:** 1.0.0  
**Author:** Dino Vlahek

Interactive browser-based demo for visualizing a hybrid Gaussian–wavelet multiscale detector landscape for zero localization in oscillatory functions.

The demo illustrates the detector framework from the accompanying paper. The default detector corresponds to:

\[
\alpha = 1, \qquad \beta = 1, \qquad \gamma = 0.5.
\]

Other values of \(\alpha\), \(\beta\), and \(\gamma\) are provided only for exploratory visualization.

> Important: the **Synthetic zeta-zero test function** is a controlled toy example with zeta-zero ordinates built in as exact zeros. It is **not** the true Riemann \(\Xi\) function or a high-precision Hardy \(Z\) implementation.


The site is available at:

```text
https://dvlahek.github.io/Hybrid-Detector/
```

Therefore, an internet connection is required unless you replace the CDN script with a local Plotly bundle.

## Features in version 1.0.0

- Interactive detector landscape: 2D heatmap and 3D surface.
- Function view showing \(f(b)\), zero line, reference zeros, and detector estimates.
- 1D detector slice at selected scale.
- Multiple built-in test functions.
- Custom function input.
- Optional manual reference zeros for custom functions.
- Detector parameters: alpha, beta, gamma, epsilon.
- Scale parameters: `a_min`, `a_max`, number of scales, grid points.
- Detection parameters: minima quantile, merge tolerance, match tolerance, max estimated zeros.
- Persistence diagnostics: cluster support and persistence score.
- Optional sign-change diagnostic near detector candidates.
- Parameter warnings.
- Auto-tune balanced mode.
- Auto-tune dense-zero mode.
- CSV export of detection results.
- Built-in tutorial explaining the visualization and parameters.

## Scientific scope

This is an educational and exploratory visualization tool. It is intended to illustrate the detector framework, not to replace the numerical experiments from the paper.

The demo stays close to the paper’s framework:

- Gaussian amplitude probe \(P(a,b)\),
- wavelet-like variation response \(W(a,b)\),
- scale-normalized detector \(D(a,b)\),
- local minima as candidate zero locations,
- merging candidates across scales,
- optional interpretation of stable candidates as persistent multiscale valleys.

The sign-change check is an auxiliary diagnostic only. It is not the main detector.


## Citation

If you use this demo in teaching, presentation, or research discussion, please cite the accompanying paper and/or this repository. Paper is currently in review.
