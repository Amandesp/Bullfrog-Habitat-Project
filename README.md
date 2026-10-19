# Potential Bullfrog Habitat in Concrete, Washington

## Project Overview

This project uses Geographic Information Systems (GIS) and QGIS to identify areas in Concrete, Washington, that may provide suitable habitat for American bullfrogs, an invasive species in Washington State.

The goal was to identify areas that meet environmental conditions associated with bullfrog habitat, including proximity to freshwater, slow-moving streams, and vacant or undeveloped land.

By combining multiple geographic datasets and applying spatial analysis techniques, I created a map highlighting potential bullfrog habitat zones.

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

The final map highlights areas around Concrete, Washington, that meet the project's habitat suitability criteria.

This project demonstrates how GIS can combine geographic and environmental datasets to identify locations for further ecological investigation. It also demonstrates the use of spatial buffers, terrain analysis, attribute filtering, and overlay operations to investigate an environmental question.

## Limitations

- The mapped areas represent **potential habitat**, not confirmed bullfrog populations or verified observations.
- Stream speed was approximated using terrain slope rather than direct measurements of water velocity.
- Results depend on the quality, resolution, coverage, and currency of the input datasets.
- Field observations and additional ecological data would be needed to validate the predicted habitat areas.
- The original datasets are not included in this repository. Reproducing the analysis may require downloading the data and relinking the layers in QGIS.
