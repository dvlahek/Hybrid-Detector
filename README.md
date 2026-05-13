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

## Live demo on GitHub Pages

This repository is ready for GitHub Pages. After pushing it to GitHub:

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **GitHub Actions** as the source.
4. Push to the `main` branch.
5. The workflow in `.github/workflows/pages.yml` will publish the static site.

The site will be available at:

```text
https://<your-github-username>.github.io/<repository-name>/
```

GitHub Pages supports publishing static files from a branch or by using a GitHub Actions workflow. The entry file for a Pages site should be named `index.html`, `index.md`, or `README.md` at the top level of the published artifact.

## Local use

Open `index.html` directly in a browser.

The demo uses Plotly from a CDN:

```html
https://cdn.plot.ly/plotly-2.35.2.min.js
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

## Repository structure

```text
hybrid-detector-lab-v1/
├── index.html
├── README.md
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
├── VERSION
├── .gitignore
├── .github/
│   └── workflows/
│       └── pages.yml
└── docs/
    ├── USER_GUIDE.md
    └── PAPER_ALIGNMENT.md
```


## Citation

If you use this demo in teaching, presentation, or research discussion, please cite the accompanying paper and/or this repository. Paper is currently in review.
