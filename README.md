# Wildfire Impact Assessment on Climate, Air Quality, and Human Health

## Overview
Processed data for assessing the 2013 wildfires in Canada, on climate, air quality, and human health over the period 2013–2020.

## Repository Structure

```
wildfire-impact-assessment/
├── README.md
├── shapefile/                    # Fire zone shapefile (2013 wildfires)
├── impact_rasters/               # Grayscale impact index rasters (2013-2020)
├── images colored maps/          # Colored classified maps with legend
└── colored maps/                 # Additional colored map outputs
```

## Data Description

### shapefile/
- `feux_contours_2013.shp` - Fire perimeters of the 2013 wildfires in Quebec, Canada
- **Source**: Canadian National Fire Database

### impact_rasters/
- Grayscale impact index rasters (0-1 scale, higher = greater impact)
- Files: `impact_2013.tif` to `impact_2020.tif`, `final_impact.tif`
- Resolution: 1 km
- Projection: WGS 84 / UTM zone 19N (EPSG:32619)

### images colored maps/
- Colored classified maps with 5 severity levels
- GeoTIFF files are georeferenced
- PNG files include legend

### colored maps/
- Additional colored map outputs
- Georeferenced TIFF and PNG formats

## Color Legend

| Color | Severity | Impact Range |
|-------|----------|--------------|
| Light Green | Very Low | 0.00 – 0.20 |
| Light Yellow | Low | 0.20 – 0.40 |
| Light Orange | Moderate | 0.40 – 0.60 |
| Red-Orange | High | 0.60 – 0.80 |
| Dark Red | Severe | 0.80 – 1.00 |
| White | Outside Fire Zone | - |

## Usage

### Open in QGIS
1. Add raster layer: `Layer > Add Layer > Add Raster Layer`
2. Select any `.tif` file
3. Add shapefile: `Layer > Add Layer > Add Vector Layer` → select `shapefile/feux_contours_2013.shp`

### Load in Python
```python
import rasterio
import geopandas as gpd

# Load impact raster
with rasterio.open('impact_rasters/impact_2020.tif') as src:
    data = src.read(1)

# Load shapefile
gdf = gpd.read_file('shapefile/feux_contours_2013.shp')
```

## Contact

For questions: y.ouladsayad@uiz.ac.ma
```

