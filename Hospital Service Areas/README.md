# Nighttime Population and Hospital Service Areas in Atlanta, GA

**Tools:** ArcGIS Pro | Spatial Join | Thiessen Polygons | Census Blocks | Population Summaries

## Project Overview

This project examines nighttime population and service areas for hospitals in Atlanta, Georgia. I used hospital locations and census blocks to estimate the population associated with each hospital service area and displayed the results in a map with charts.

## Methods

The steps I performed were:

1. Derived centroids for census blocks.
2. Created Thiessen polygons for hospital points.
3. Joined Thiessen polygons to centroids by spatial location.
4. Summarized population counts by hospital names.
5. Joined attributes from the summarized table to Thiessen polygons.

I used centroids located **inside** the census blocks. When *Inside* is not checked, the program calculates the center of the polygon by geometry, including any empty spaces or holes. If the center is within a hole, it can be placed outside the polygon, which would interfere with identifying locations within the census blocks.

## Final Map and Charts

![Nighttime Population and Service Areas for Hospitals in Atlanta, GA](images/hospital-service-map.png)

The map displays nighttime population and hospital service areas in Atlanta, with charts comparing population density, acreage coverage, and the hospitals with the largest percentages of population coverage.

## Interpretation and Limitations

A service area based on straight-line, or **Euclidean, distance** is different from one based on network distance. Euclidean distance is the shortest path between two points, a straight line, while network distance follows a network such as roads.

Nighttime population does not always represent the population present when a medical emergency occurs. People are often away from their homes during the day, so they may be in a different census block. The map therefore describes a geographic approximation, not actual hospital patient counts or road-travel service areas.

**Data/source noted in original map:** U.S. Census Bureau and Esri Maps and Data.

*Course project: GEOG 4370, Introduction to GIScience.*
