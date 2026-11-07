# Exercise V — semivariograms and kriging

Open `05_exercises.ipynb` and run its cells from top to bottom. The notebook includes all original tasks, their TODO comments, the cadmium bonus, saved tables, figures, and explanations.

In PowerShell, from the APCD workspace, install dependencies into the Python selected as the notebook kernel:

```powershell
& "$env:LOCALAPPDATA\Python\pythoncore-3.14-64\python.exe" -m pip install -r ".\05_exercises\requirements.txt"
```

Then restart that kernel in VS Code and select **Run All**. The tested Python version is 3.14.8. The SciKit-GStat requirement uses SciPy 1.16.3; it differs from the SciPy version pinned for earlier exercises.

The Meuse observations and requested Esri topographic raster are already cached in `data/`. A normal rerun needs no network connection. Source URLs, attribution, and SHA-256 checksums are in `data/sources.json`.

Results are in `results/`:

- `cadmium_six_variograms.png` and `cadmium_six_variograms.csv`: all six bonus fits and sill diagnostics.
- `cadmium_model_selection.csv`: fit parameters and five-fold predictive scores.
- `cadmium_cv_predictions.csv` and `cadmium_cv_fit_audit.csv`: held-out predictions and training-only fit settings.
- `lead_kriging_maps.png` and `cadmium_kriging_maps.png`: prediction in ppm and uncertainty maps.
- `*_kriging_grid.csv`: cell coordinates, hull mask, log predictions, log variance/SD, back-transformed medians, and labeled lognormal approximations.
- `*_kriging.tif`: EPSG:28992 raster bands for median ppm, log-scale standard deviation, and log-scale variance.

The cadmium model is selected by the declared log-scale held-out-point RMSE criterion. The uncertainty maps display standard deviation, obtained as the square root of SciKit-GStat's variance-valued `sigma` attribute. Back-transformed `exp(mu)` predictions are labeled as medians rather than arithmetic means.
