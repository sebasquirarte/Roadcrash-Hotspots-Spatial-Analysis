# Mapping Road Crash Hotspots

### A Comparative Spatial Data Mining Study

![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)
![GitHub last commit](https://img.shields.io/github/last-commit/sebasquirarte/mapping-road-crash-hotspots)

## Project Description

Road traffic crashes are an important urban safety issue. Understanding
where they occur and which characteristics are associated with more
severe outcomes can help identify patterns that may otherwise be
difficult to observe.

This project analyzes open data on road crashes in Guadalajara, Jalisco,
Mexico, using spatial data mining methods and logistic regression. The
main goal is to compare different spatial analysis approaches for
identifying crash hotspots and examine which recorded characteristics
are associated with fatal outcomes.

The primary analysis uses road traffic crash data from 2015 to 2025
published by the Jalisco Institute of Statistical and Geographical
Information (IIEG). If time and data compatibility allow, the analysis
will also be replicated using data from Mexico City and Monterrey.

## Research Questions and Methods

The study addresses three main research questions:

1.  **Where are road crash hotspots located, and how do the results
    differ across methods?**

    Three spatial approaches will be used:

    -   **Kernel Density Estimation (KDE)** to visualize crash
        concentrations.
    -   **Getis--Ord Gi\*** to identify statistically significant
        clusters of high crash counts.
    -   **DBSCAN** to identify clusters based on spatial density.

    The results will be compared using spatial overlap, the proportion
    of recorded crashes captured by identified hotspots, and sensitivity
    to parameter choices.

2.  **Which recorded characteristics are associated with fatal crash
    outcomes?**

    Logistic regression will be used to examine associations between
    fatal outcomes and recorded characteristics such as crash type, time
    of day, day of week, and municipality. The response variable will
    indicate whether a crash involved at least one recorded fatality.
    Results will be interpreted as associations rather than causal
    effects.

3.  **Can the spatial analysis be replicated in other cities?**

    If time and data compatibility allow, the spatial methods will be
    applied to data from Mexico City and Monterrey. Comparisons will
    account for differences in geographic coverage, time periods, and
    reporting practices.

## Data Sources

The primary dataset is **Siniestralimap 2015-2025**, published by the
[Jalisco Institute of Statistical and Geographical Information
(IIEG)](https://iieg.jalisco.gob.mx/datos-abiertos/es/dataset/sinestralimap-2015-2025).
It contains records of people involved in road crashes, with temporal,
geographic, and crash-related variables.

Additional sources for a possible comparison across cities are:

- [Mexico City: Road Traffic Incidents (SSC)](https://www.datos.cdmx.gob.mx/es_AR/dataset/hechos-de-transito-reportados-por-ssc-base-comparativa)
- [Monterrey: Road Traffic Crash Records](https://mide.monterrey.gob.mx/datasets/god_datosmty_data:geonode:incidentes_viales/metadata_detail)

Differences in data collection, geographic coverage, and variable
definitions will be considered before comparing results across cities.

## Geographic Scope

The main analysis focuses on six municipalities in the Guadalajara
Metropolitan Area:

-   Guadalajara
-   Zapopan
-   San Pedro Tlaquepaque
-   Tonalá
-   El Salto
-   Tlajomulco de Zúñiga

## Tools and Visualization

All data processing, statistical modeling, and visualization will be
conducted in R. The analysis will use established packages for spatial
analysis, data wrangling, visualization, and statistical modeling.

Planned outputs include comparative hotspot maps and plots summarizing
spatial agreement and parameter sensitivity. If time permits, an
interactive dashboard will be developed using R Shiny or D3.js.

## Limitations

The data is recorded at the person level, so observations will be
examined carefully to avoid counting the same crash multiple times in
the spatial analysis. Missing coordinates and changes in data collection
will also be considered during data preparation.

Since the datasets do not necessarily include traffic exposure measures,
the analysis will focus on recorded crash patterns and associations
rather than causal effects or crash risk per trip.

## Project Status

In development.
