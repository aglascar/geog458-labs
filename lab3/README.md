# Western Washington Summer Temperature Map

## Overview
This interactive web map displays spatial variations in daily maximum temperatures across Western Washington, focusing on the Puget Sound lowlands and Cascade foothills. The visualization combines an interpolated continuous temperature surface with discrete NOAA weather station monitoring points.

## Target Audience & Purpose
* **Audience:** Urban heat researchers, local public health officials, and regional residents.
* **Purpose:** Helps users understand how summer temperatures fluctuate across marine microclimates (near Puget Sound), urban heat corridors along Interstate 5, and higher-elevation foothills. It identifies areas of potential heat vulnerability compared to cooler coastal zones.

## Data Sources
1. **Thematic Surface & Stations:**
   * **Source:** NOAA Climate Data Online (CDO) — Daily Summaries (GHCN-Daily).
   * **Variables:** Daily Maximum Temperature (`TMAX`), Station Name, and Geographic Coordinates.
   * **Date:** [July 22, 2026].
   * **Units:** Degrees Fahrenheit (°F).
2. **Basemap:**
   * Custom raster tile style designed and exported via Mapbox Studio and OpenStreetMap contributors.

## Methodology & Relationship Between Layers
* **Thematic Raster Surface:** An Inverse Distance Weighted (IDW) interpolation was computed in QGIS using the NOAA weather station points across the bounding extent `[-123.30, 46.90]` to `[-121.10, 48.50]`. This estimates continuous temperature gradients across areas without direct monitoring stations.
* **Vector Layer:** The underlying NOAA weather station locations are displayed as an overlay. Clicking an individual station opens a popup displaying its exact measured temperature, station name, and ID.
* **Coherence:** Both layers represent the exact same phenomenon (temperature) for the identical geographic extent and date, allowing users to cross-reference raw observational ground truth with modeled regional trends.

