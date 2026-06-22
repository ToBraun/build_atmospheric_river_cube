# Build the PIKART atmospheric river datacube

Notebook reproducing the build of `atmospheric_river_cube.zarr` as published on
the ESA EarthCODE Open Science Catalog: a global, 0.5°, 6-hourly Eulerian
catalog of atmospheric rivers (PIKART v1.1) with co-located ERA5 precipitation
diagnostics, spanning 1940–2023.

**Reference:** Vallejo-Bernal et al. (2025), JGR Atmospheres,
https://doi.org/10.1029/2024JD041869

## Requirements
- DeepESDL JupyterLab with the `deepesdl-xcube-1.11.x` kernel (or equivalent
  conda env with xcube, xarray, zarr, s3fs, xrlint, cartopy)
- Access to the PIK THREDDS server (`ar.pik-potsdam.de`)
- A writable S3 bucket; credentials in env vars `S3_USER_STORAGE_*`

## Usage
Open `Build_atmospheric_river_cube.ipynb` and run cells top to bottom.
Two placeholders need editing before running:
- Cell 4: `THREDDS_AR_ROOT` — verify the PIK THREDDS subpath
- Cell 18: `gcmd_keyword_url` entries — paste real GCMD Keyword Viewer URLs

The build takes 1–3 days from THREDDS. The notebook is interruption-safe:
re-running picks up from the cube's last successful timestamp.
