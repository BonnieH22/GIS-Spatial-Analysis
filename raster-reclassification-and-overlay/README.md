# Raster Data Analysis: Reclassification, Overlay, and Map Algebra

**Tools:** ArcGIS Pro | Raster Reclassify | Raster Overlay | Raster Calculator | Map Algebra

## Project Overview

This project uses raster data for the Maple Mountain area in the Temagami district of Ontario. I worked with recreation, roads, and watershed layers to practice raster reclassification, overlay operations, and map algebra.

The dataset contained **205 columns and 80 rows** with a cell size of **350 meters**. The supplied raster data had an unknown coordinate system.

## Methods

### 1. Recreation Classes

I reclassified the recreation class raster to select **Class 2** recreation areas, then used an overlay with the recreation subclass raster to determine the recreation types in those areas. The resulting categories were **Lodging** and **Beach**.

![Recreation Types Within Class 2](images/recreation-class-2.png)

### 2. Roads Over Recreation

I combined the roads and recreation raster datasets so road cells were assigned the roads value, while other cells kept their recreation class values.

![Roads Over Recreation](images/roads-over-recreation.png)

### 3. Weighted Overlay

I used Raster Calculator to create a weighted sum of multiple layers:

```text
recclass * 0.3 + roads * 0.4 + watershed * 0.3
```

![Weighted Overlay of Recreation, Watersheds, and Roads](images/weighted-overlay.png)

## Interpretation and Limitations

Raster data represents geographic features using grid cells. A river, for example, is represented by several cells, so its shape or position may not be as precise as a vector line.

This lab demonstrates the **process of weighted raster overlay**, but the weights were provided as part of the lab exercise. The resulting weighted values should not be presented as a validated suitability or risk score without additional interpretation and a justified weighting method.

**Data:** MAPLE / Canada Land Inventory course dataset.

*Course project: GEOG 4370, Introduction to GIScience.*
