# README

## Overview

💡 This GitHub repository contains a Python script aimed at analyzing inland water bodies using a GeoJSON file and a specified time range. It generates a time series representing the surface water extent for the selected water body during the provided period. The script uses Google Earth Engine Python API to access the images that correspond to the polygon geometries(lake boundaries) on the GeoJSON file.

## GeoJSON Information

💡 The historic lakes data is sourced as shapefile from Natural Earth Data (1:10m Physical Vectors) for the United States region. You can access the dataset [here](https://www.naturalearthdata.com/downloads/10m-physical-vectors/). It encompasses polygon geometry for four significant lakes within the region. The original shapefile has been converted to GeoJSON format using the GeoCloud converter, accessible [here](https://mygeodata.cloud/converter/shp-to-geojson). The chosen time range for analysis spans from 2016 to 2023. 

## JRC Global Surface Water Dataset

- **Description:** Surface water extent dataset from Google Earth Engine.
- **Source:** Retrieved using the Earth Engine API (JRC/GSW1_2/MonthlyHistory).
- **Filtering Criteria:** Filtered based on specified time range and water body bounds.

## How to Run the Analysis

💡 To conduct the analysis:
- Start by loading the provided GeoJSON file from the data directory as 'geojson_path'.
- Execute all cells within the 'script.ipynb' notebook.
- The GeoJSON file contains data for four distinct polygons, each representing a different lake. To focus on a specific lake, adjust the line "water_body_geom = gdf.geometry.iloc[3]" by substituting the index number (3) with the corresponding index for the desired lake's polygon. Use 0 for the first lake, 1 for the second, 2 for the third, and so forth.
- The resulting time series plot will be rendered in your integrated development environment (IDE) and saved to the 'results' directory.
