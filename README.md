# Potential Bullfrog Habitat in Concrete, Washington

## Project Overview

This project was completed as part of a GIS and Mapping course to analyze potential habitat for American bullfrogs, an invasive species in Washington State.

Bullfrogs are amphibians that require freshwater and tend to prefer still or slow-moving water, particularly in areas surrounded by undeveloped land. The goal of this project was to use GIS tools and spatial analysis to identify areas that may provide suitable bullfrog habitat in Concrete, Washington.

Using data on waterbodies, streams, elevation, and land use, I developed and ran a conceptual spatial model in QGIS. The analysis involved creating buffers, analyzing and reclassifying slope, selecting suitable land-use areas, and combining spatial datasets using union and intersection operations. The project also involved creating maps to communicate the spatial analysis results.

## Final Map

<img width="861" height="606" alt="Project Map" src="https://github.com/user-attachments/assets/bf37ef3a-9985-4c9e-b365-964edd358448" />


*Green areas represent locations identified by the analysis as potential bullfrog habitat.*

## Tools and Technologies

- **QGIS** — Geographic information system software used for mapping and spatial analysis
- **Spatial Analysis** — Buffering, slope analysis, reclassification, union, and intersection
- **Geographic Data Processing** — Combining waterbody, stream, elevation, and land use datasets
- **Cartographic Design** — Creating a map with a title, legend, scale bar, and north arrow

## Data Sources

The analysis used four main types of geographic data: waterbodies, streams, elevation, and land use.

The original datasets are not included in this repository because of file-size limitations. The links below provide access to the corresponding data resources.

- **Waterbodies:** [Washington State Department of Ecology — Major Waterbodies](https://fortress.wa.gov/ecy/gispublic/DataDownload/ECY_WAT_NHDWAMajorWaterbodies.htm)
- **Streams:** [Washington State Department of Ecology — Major Streams](https://fortress.wa.gov/ecy/gispublic/DataDownload/ECY_WAT_NHDWAMajorStreams.htm)
- **Elevation:** [University of Washington — Washington State Digital Elevation Models](http://gis.ess.washington.edu/data/raster/tenmeter/byquad/index.html)
- **Land Use:** [Washington State Department of Ecology — Land Use 2010](https://fortress.wa.gov/ecy/gispublic/DataDownload/ECY_CAD_Landuse2010.htm)

These datasets were used to evaluate waterbody proximity, terrain slope, stream locations, and vacant land as part of the habitat suitability analysis.

## Methodology

The analysis was performed in QGIS using a series of spatial processing steps.

1. **Waterbody Buffering:** Created one-mile buffers around lakes and other still bodies of water to identify nearby areas.
2. **Slope Analysis:** Used elevation data to calculate terrain slope and estimate areas where streams may have slower-moving water.
3. **Slope Reclassification:** Classified areas with slopes below the assignment's 0.19 threshold as potential slow-moving water areas.
4. **Stream Analysis:** Identified stream segments intersecting low-slope areas, buffered the streams, and created one-mile buffers around the resulting areas.
5. **Land Use Filtering:** Selected vacant land categories using land use codes 90–99.
6. **Spatial Overlay:** Combined waterbody and slow-moving stream buffer areas using a union, then intersected the result with selected vacant land.
7. **Map Creation:** Visualized the resulting potential habitat zones on a final map of Concrete, Washington.

## Findings

The map identifies areas around Concrete, Washington, that may provide suitable habitat for invasive bullfrogs. Bullfrogs require freshwater environments and tend to prefer lakes, ponds, and slow-moving streams, particularly in areas surrounded by undeveloped or open land.

Using elevation, land-use, and waterbody data, the QGIS spatial analysis model identifies locations that meet the project's habitat suitability criteria. The green shaded areas represent potential bullfrog habitat based on these conditions.

These results indicate areas that may be suitable for bullfrogs, not confirmed populations. Field surveys would be needed to verify whether bullfrogs are present in the identified locations.

## Limitations

- The mapped areas represent **potential habitat**, not confirmed bullfrog populations or verified observations.
- Stream speed was approximated using terrain slope rather than direct measurements of water velocity.
- Results depend on the quality, resolution, coverage, and currency of the input datasets.
- Field observations and additional ecological data would be needed to validate the predicted habitat areas.
- The original datasets are not included in this repository. Reproducing the analysis may require downloading the data and relinking the layers in QGIS.
