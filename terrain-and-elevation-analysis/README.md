# Terrain and Elevation Analysis in ArcGIS Pro

## Project Overview

This project examines elevation, slope, aspect, shaded relief, and 3D terrain representations using ArcGIS Pro. I produced maps of Clarke County and the Lake Lanier area and compared how different terrain-processing settings change the appearance and detail of the results.

## Tools and Techniques

- ArcGIS Pro
- Elevation and terrain visualization
- Slope and aspect analysis
- Hillshade with changing illumination parameters
- TIN simplification and Z-tolerance comparison
- 3D land-cover and shaded-relief visualization

## Slope and Aspect — Clarke County

### Elevation slope

![Clarke County elevation slope map](terrain-and-elevation-analysis/Clarke-County-Maps/SlopeLayout.jpg)

The slope chosen at a given cell is the **maximum rate of elevation change**, or the steepest slope. Percent rise represents the vertical elevation change divided by the horizontal distance, multiplied by 100.

### Aspect

![Clarke County aspect map](terrain-and-elevation-analysis/Clarke-County-Maps/aspectlayout.jpg)

Aspect is the cardinal or intercardinal direction that the slope faces. It is measured in degrees, with 0 and 360 degrees representing north, using the direction of the steepest downhill slope.

## Shaded Relief — Lake Lanier

![Lake Lanier shaded relief](terrain-and-elevation-analysis/Lake-Lanier-Maps/relieflayout.jpg)

Different versions of shaded relief look different because changing the illumination parameters changes which portions of the surface are brighter or darker. **Azimuth** controls the direction of the illumination, while **altitude** affects the intensity of the shadows. With lower illumination altitude, shadows appear to extend farther.

### Elevation and shaded relief

![Lake Lanier elevation and shaded relief](terrain-and-elevation-analysis/Lake-Lanier-Maps/elevationandshadedrelieflayout.jpg)

## 3D Terrain and Land Cover

### 3D land cover

![Lake Lanier 3D land cover](terrain-and-elevation-analysis/Lake-Lanier-Maps/lakelanierlandcover.jpg)

### 3D shaded relief

![Lake Lanier 3D shaded relief](terrain-and-elevation-analysis/Lake-Lanier-Maps/3drelief.jpg)

## TIN Simplification and Z-Tolerance

![TIN comparison screenshot](terrain-and-elevation-analysis/z-tolerance-comparison/tin-z-tolerance.jpg)

In the lab, I compared terrain surfaces with different Z-tolerance values. A higher Z-tolerance produced shapes that appeared sharper and less smooth, with less detail. I also compared their file sizes:

| Z-tolerance | Output file size |
|---|---:|
| 0 | 1.50 MB |
| 20 | 79.3 KB |
| 40 | 31.1 KB |

The Z-tolerance of 0 took up the most space, while a Z-tolerance of 40 took up the least. Increasing Z-tolerance reduced file size, but the loss of detail was more noticeable at higher values.

## Key Takeaways

This lab gave me experience comparing terrain representations, interpreting slope and aspect, producing shaded-relief maps, and visualizing geographic data in 3D. It also demonstrated how terrain-processing choices affect both visual detail and output file size.

## Project Notes

This project was completed as part of GIS coursework. The figures are drawn from my submitted Lab 11 report. The maps use the course-provided geographic datasets; this repository contains presentation images and explanation rather than a fully reproducible dataset and analysis pipeline.
