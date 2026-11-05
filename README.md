# ROAGI_V1 — Rownok Ocean–Atmosphere Genesis Index, Version 1

Code and outputs for the manuscript *"A Region-Specific Ocean–Atmosphere Coupled Genesis Index for Tropical Cyclones: Development and Validation in the Bay of Bengal"* (submitted to the Journal of Earth and Ocean Science).

ROAGI_V1 is a surface-based diagnostic of genesis-favourable conditions in the Bay of Bengal (5–25°N, 78–100°E). It combines daily ERA5 10-m relative vorticity, convergence and precipitation with GLORYS12V1 SST and its gradient, multiplied by a coastal-distance factor. It is evaluated against IBTrACS genesis events for 2015–2024.

## Contents
| File / folder | Description |
|---|---|
| `ROAGI_01_diagnostics.ipynb` | Audit of the original implementation |
| `ROAGI_02_revision_analysis.ipynb` | Full corrected pipeline: index, statistics, ablation, time-matched evaluation, sensitivity analyses |
| `ROAGI_make_figures.py` | Publication figures (1000 dpi) |
| `tables/` | All output tables (CSV), including the complete sensitivity results |

## Input data (not included; freely available)
- ERA5 hourly single levels: u10, v10, total precipitation, land–sea mask — https://doi.org/10.24381/cds.adbb2d47
- CMEMS GLORYS12V1 (GLOBAL_MULTIYEAR_PHY_001_030), monthly thetao, top level — https://doi.org/10.48670/moi-00021
- IBTrACS v04r01, North Indian Ocean — https://doi.org/10.25921/82ty-9e16
- Natural Earth 1:10m coastline — https://www.naturalearthdata.com

## How to run
1. Open the notebooks in Google Colab (or Jupyter with Python 3).
2. Put the input files in one folder and set `BASE` in section 0 of the notebook to that folder.
3. Run all cells in order. Tables are written to `tables/` and figures to `figures_publication/`.

Requirements: numpy, scipy, pandas, xarray, netCDF4, geopandas, matplotlib, cartopy.

## Citation
If you use this code, please cite the paper (details will be added after publication) and this archive (DOI to be added).

## License
Code: MIT License. Tables: CC BY 4.0.

