# Wildfire Impact Assessment on Climate, Air Quality, and Human Health

## Overview
This repository contains satellite data, shapefile, and processed impact rasters used to assess the impacts of the 2013 wildfires in Quebec, Canada, on climate, air quality, and human health over the period 2013–2020.

## Data Description

### Shapefile
- `feux_contours_2013.shp` - Fire perimeters of the 2013 wildfires in Quebec, Canada
- **Source**: Canadian National Fire Database

### Satellite Data

| Folder | Sensor | Variable | Period | Resolution |
|--------|--------|----------|--------|------------|
| NDVI | MODIS MOD13Q1 | Vegetation Index | 2013-2020 | 250 m |
| MODIS_LST | MODIS MOD11A1 | Land Surface Temperature | 2013-2020 | 1 km |
| MODIS_FireMask | MODIS MOD14A1 | Fire Detection (0-5) | 2013-2020 | 1 km |
| ERA5_Climate | ERA5 | Temperature, Wind, Radiation | 2013-2020 | 0.25° |
| S5P_CO | Sentinel-5P | Carbon Monoxide | 2018-2020 | 7 km |

### Impact Rasters
- `impact_YYYY.tif` - Annual impact index for each year (2013-2020)
- `final_impact.tif` - Average impact for 2019-2020
- **Resolution**: 1 km (aligned to MODIS LST grid)
- **Projection**: WGS 84 / UTM zone 19N (EPSG:32619)

## Contact

For questions about this dataset, please contact: y.ouladsayad@uiz.ac.ma
```
