# APCD — Time Series and Spatial Data Analysis

Python and Jupyter notebook solutions for five APCD exercises at the Technical University of Košice (TUKE). The notebooks include calculations, visualizations, explanations, and bonus assignments.

| Exercise | Topics |
| --- | --- |
| [01 — Time series fundamentals](01_exercises/01_exercises.ipynb) | Aggregation, seasonal decomposition, differencing, stationarity tests, autocorrelation, STL, and Box–Cox transformations. |
| [02 — Time series forecasting](02_exercises/02_exercises.ipynb) | ARIMA model selection, residual diagnostics, rolling forecasts, exponential smoothing, and SARIMA/SARIMAX electricity forecasts. |
| [03 — Multivariate and state space models](03_exercises/03_exercises.ipynb) | Cross-correlation, cointegration, VAR/VECM forecasts, impulse responses, and hidden-state simulations. |
| [04 — Kalman filtering and spatial statistics](04_exercises/04_exercises.ipynb) | Kalman filtering, coordinate transformations, spatial joins, Moran's I, spatial validation, and OLS/SAR predictions. |
| [05 — Semivariograms and kriging](05_exercises/05_exercises.ipynb) | Variogram fitting, directional dependence, model validation, and Ordinary Kriging maps of heavy metal concentrations and uncertainty. |

## Running the notebooks

Open a notebook in Jupyter or VS Code, select a Python environment with its dependencies installed, and run the cells from top to bottom. Exercises 03–05 provide their own `requirements.txt` files; use a separate environment for each dependency specification.

Datasets, source information, and exported results are stored alongside the relevant notebooks. Exercise 05 also includes a [detailed setup and output guide](05_exercises/README.md).
