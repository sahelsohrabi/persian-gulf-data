# Persian Gulf Data

## Dataset Overview
This repository contains data of the Persian Gulf, obtained from the **Copernicus Marine Service**, for **26 August 2025**. 
The dataset includes the following variables:

- **thetao**: Potential temperature (°C)  
- **so**: Salinity (PSU)  
- **uo, vo**: Surface current components (m/s)  
- **zos**: Sea surface height (m)  
- **siconc, sithick, usi, vsi**: Sea ice concentration, thickness, and ice currents  
- **bottomT, mlotst**: Bottom temperature and mixed layer thickness  

Dimensions: `time:1, latitude:73, longitude:144, depth:1`  

---

## Analyses and Plots

| Analysis | Short Description | Description |
|----------|-----------------|------------|
| Sea Surface Temperature | SST - Persian Gulf | Map of surface temperature |
| Sea Surface Salinity | SSS - Persian Gulf | Map of surface salinity |
| Surface Currents | Surface Currents Plot | Vector plot of surface currents |
| Surface Currents + Kinetic Energy | Surface Currents with KE | Vector plot with kinetic energy overlay |
| Sea Surface Height | Sea Surface Height - Persian Gulf | Map of sea surface height |
| Approximate Surface Water Density | Approx. Surface Water Density | Density calculated from temperature and salinity |
| Temperature Spatial Gradient | SST Spatial Gradient | Map of spatial temperature gradient |
| Salinity Spatial Gradient | SSS Spatial Gradient | Map of spatial salinity gradient |
| Temperature vs Salinity | Temp vs Salinity Correlation | Scatter plot and correlation coefficient |
| Temperature Distribution | Temperature Distribution | Histogram of surface temperature |
| Salinity Distribution | Salinity Distribution | Histogram of surface salinity |

---

## Quick Start

To quickly load and explore the dataset:

```python
import xarray as xr

# Load the dataset
persiangulf = xr.open_dataset("data/raw/persian_gulf_2025-08-26.nc")

# Check variables and dimensions
print(persiangulf)
