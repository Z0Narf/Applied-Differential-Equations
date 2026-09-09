# Applied Differential Equations

This is a collection of analytical and numerical solutions to ordinary and partial differential equations, developed in Python as part of the ODE and PDE courses at the Institute of Science Tokyo.

## Overview

This repository contains Jupyter notebooks originally developed for coursework and later revised for public sharing. The original assignment instructions have been rewritten, and each notebook includes the governing equation, mathematical approach or discretization, Python implementation, and an explanation of the results.

The ODE notebooks cover analytical solutions, numerical methods, and nonlinear systems, including chaotic behavior. The PDE notebooks cover different types of equations, progressing from parabolic and nonlinear equations to hyperbolic and elliptic equations. Each problem is solved using an appropriate finite-difference or numerical method.

## Repository structure

```
Applied-Differential-Equations/
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
├── ode/
│   ├── 01_logistic_growth.ipynb
│   ├── 02_second_order_linear_homogeneous.ipynb
│   ├── 03_second_order_nonhomogeneous.ipynb
│   ├── 04_runge_kutta_methods.ipynb
│   └── 05_lorenz_system.ipynb
└── pde/
    ├── 01_diffusion_2d.ipynb
    ├── 02_burgers_equation_2d.ipynb
    ├── 03_advection_1d.ipynb
    ├── 04_poisson_sor.ipynb
    └── other output gifs
```

## Contents

### Ordinary Differential Equations (`/ode`)

| # | Notebook | Topic | Methods |
|---|----------|-------|---------|
| 01 | [Logistic Growth Model](ode/01_logistic_growth.ipynb) | Population growth with a carrying capacity | Separation of variables, partial fraction decomposition |
| 02 | [Second-Order Linear Homogeneous ODEs](ode/02_second_order_linear_homogeneous.ipynb) | Damped mass–spring motion across four regimes | Characteristic equation, case classification |
| 03 | [Second-Order Nonhomogeneous ODEs](ode/03_second_order_nonhomogeneous.ipynb) | Driven oscillator, resonant vs non-resonant | Analytical particular + homogeneous solution |
| 04 | [Runge–Kutta Methods](ode/04_runge_kutta_methods.ipynb) | Numerical integration accuracy vs step size | Euler, Heun (RK2), RK4; error comparison |
| 05 | [The Lorenz System](ode/05_lorenz_system.ipynb) | Chaotic dynamics, sensitivity to initial conditions | RK4, 3D phase-space visualization |

### Partial Differential Equations (`/pde`)

| # | Notebook | Type | Equation & Methods |
|---|----------|------|--------------------|
| 01 | [2-D Diffusion Equation](pde/01_diffusion_2d.ipynb) | Parabolic | Heat equation via FTCS explicit scheme; periodic, Dirichlet, and Neumann (no-flux) boundary conditions |
| 02 | [2-D Burgers' Equation](pde/02_burgers_equation_2d.ipynb) | Nonlinear | Forward-time/backward-space advection with centered diffusion; includes the temperature-dependent (nonlinear) case |
| 03 | [1-D Advection Equation](pde/03_advection_1d.ipynb) | Hyperbolic | Upwind, Leith (Lax–Wendroff), and CIP schemes compared across Courant numbers |
| 04 | [2-D Poisson Equation](pde/04_poisson_sor.ipynb) | Elliptic | Successive Over-Relaxation (SOR) iterative solver; effect of source strength and relaxation factor |

Some PDE notebooks also include `.gif` animations to show how the field changes over time. These animations are displayed directly in the notebook and can be viewed on GitHub without running the code.

## Concepts & tools demonstrated

- **Analytical methods:** separation of variables, partial fractions, characteristic equations, and undetermined coefficients
- **Numerical methods:** finite difference methods (explicit FTCS, upwind, Lax–Wendroff, and CIP), Runge–Kutta integration, SOR, and stability and error analysis
- **Qualitative analysis:** phase portraits, boundary-condition behavior, numerical diffusion/dispersion, chaotic sensitivity
- **Python:** NumPy, SciPy, Matplotlib, Pillow, Jupyter

## Running locally

```bash
git clone https://github.com/Z0Narf/Applied-Differential-Equations.git
cd Applied-Differential-Equations
pip install -r requirements.txt
jupyter notebook
```

The plots and animations are already included in the notebooks, so the results can be viewed directly on GitHub without running the code. To regenerate them, run the notebook from top to bottom (Run All). The animation cells will create new `.gif` files from the computed frames.

## License

Code and write-ups in this repository are shared under the MIT License (see [LICENSE](LICENSE)). Problem statements are paraphrased from course material and belong to the original instructors.
