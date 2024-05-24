# README

<aside>
💡 This GitHub repository consists of a Python script that takes a GeoJSON file representing an inland water body and a time range as input and returns the surface water extent time series for the specified water body and period.
</aside>

<aside>
  
  💡 The shapefile is downloaded from Natural Earth Data (**1:10m Physical Vectors**) for the historic lakes from the United States region, [https://www.naturalearthdata.com/downloads/10m-physical-vectors/](https://www.naturalearthdata.com/downloads/10m-physical-vectors/).

- It comprises polygon geometry for 4 large lakes in the region.
- The period chosen for the time series is from 2016 to 2023.
- This shapefile has been converted to a GeoJSON using GeoCloud converter [https://mygeodata.cloud/converter/shp-to-geojson](https://mygeodata.cloud/converter/shp-to-geojson)
</aside>

<aside>
💡 To run the analysis,

- load the provided GeoJSON file from the data directory as geojsonpath
- Run all the cells in script.ipynb
- The GeoJSON file contains information for four distinct polygons, each representing a different lake. To analyze a specific lake, adjust the line "water_body_geom = gdf.geometry.iloc[3]" by replacing the index number (3) with the corresponding index of the desired lake's polygon: 0 for the first lake, 1 for the second lake, 2 for the third lake, and so on
- The timeseries plot gets rendered in IDE and saved to the results directory.
</aside>
