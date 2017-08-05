# gmbtools
A set of utilities for DEM processing/analysis, calculating geodetic mass balance, and plotting

## Generic tools (some still have hardcoded paths):
- `make_mos.sh` - create 2, 8 and 32-m tiled mosaics, count maps, indices, etc. from a set of input DEMs
- `dem_mosaic_validtiles.py` - wrapper around ASP dem_mosaic utility to write valid mosaic tiles in parallel
- `mb_parallel.py` - parallel computation of geodetic mass balance for a set of input glacier polygons and DEM sources
- `mb_plot.py` - create regional mass balance plots for output from mb_parallel
- `dem_gallery.py` - create gallery plot for many input DEMs
- `dem_anomaly.py` - create anomaly maps and animations
- `lag_dz.py` - create Lagrangian Dh/Dt products (adapted from old script, needs refactoring), requires pixel disparity maps created using https://github.com/dshean/vmap

## Continental US (CONUS) tools:
- `prism.py` - create seasonal PRISM temp and precip products
- `mb_bar_plot.py` - create seasonal/annual mass balance bar plot (currently SCG, should add cumulative panel)
- `conus_site_poly.py` - filter available DEMS for sites of interest and generate time series stack products

## Data download and wrangling:
- `get_srtm_tilelist.py` and `get_srtm_tiles.sh` - Identify, download, process and mosaic SRTM tiles
- `get_ned_tiles.sh` - Identify, download, process and mosaic NED tiles
- `lidar_proc.sh` - clean up WA/OR LiDAR data
- `process_usgs_dem.py` - clean up USGS DEMs generated by M. Fahey from NTM and DG imagery using ERDAS Imagine+LPS

## Snow tools (moved to https://github.com/dshean/Stereo2SWE)
- `get_snotel.py` and `swe.py` - query and extract SNOTEL records, use to create SWE maps from DEM dh/dt
