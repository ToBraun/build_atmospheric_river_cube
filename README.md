# The PIKART atmospheric river datacube
An open accessible datacube for global analyses of atmospheric rivers and extreme precipitation, based on the [PIKART catalog](https://github.com/PIKART-Catalog/Vallejo-Bernal_Braun_etal_2025): a global, 0.5°, 6-hourly catalog of atmospheric rivers (PIKART v1.1) with co-located ERA5 precipitation variables, spanning 1940–2023. Extensive documentation is provided on the [PIKART website](https://ar.pik-potsdam.de).

**References:**
- Vallejo-Bernal, S. M. & Braun, T., Marwan, N., & Kurths, J. (2025). *PIKART: A comprehensive global catalog of atmospheric rivers.* JGR Atmospheres, 130, e2024JD041869. https://doi.org/10.1029/2024JD041869
- Vallejo-Bernal, S., Braun, T., Marwan, N., & Kurths, J. (2026). *PIKART Version 1.1: Release Notes.* https://doi.org/10.31223/X5PB5Z

## Working with the datacube 
We provide a basic tutorial Jupyter notebook for a quick-start.

## Building the datacube 
We provide a Jupyter notebook that reproduces the build of `atmospheric_river_cube.zarr` as published on
the ESA EarthCODE Open Science Catalog. The build can take a while depending on the network. The notebook is interruption-safe:
re-running picks up from the cube's last successful timestamp.

## Requirements for building
- DeepESDL JupyterLab with the `deepesdl-xcube-1.11.x` kernel (or equivalent
  conda env with xcube, xarray, zarr, s3fs, xrlint, cartopy)
- Access to the PIK THREDDS server (`ar.pik-potsdam.de`)
- A writable S3 bucket; credentials in env vars `S3_USER_STORAGE_*`

## Contributors
Tobias Braun
Sara M. Vallejo-Bernal
Norbert Marwan
Juergen Kurths

## Acknowledgements
The cube was built by **Tobias Braun** within the ARNETLAB project (ESA Living Planet Fellowship 2024-2026, grant no. 4000144018/24/I-DT-lr, access to DeepESDL through NoR) with the kind assisstance of **Tejas Morbagal Harish** (Brockmann Consult GmbH) and **Anca Anghelea** (European Space Agency).

## Contact
Feel free to raise an issue or [contact us](https://ar.pik-potsdam.de/?a=contact).

