# Internship Project

## Summary

**Author:** Hudson Passos  
**Institution:** Wageningen University & Research (WUR)  
**Internship Host:** Netherlands Institute of Ecology (NIOO-KNAW)  
**Duration:** April 2, 2025 – August 12, 2025  
**Project Title:** *Simplified Access to Veluwe Ecological Data Through OGC Web Services*  
**Host Supervisor:** Stefan Vriend (NIOO-KNAW)  
**WUR Supervisor:** Liesbeth Bakker (WUR, NIOO-KNAW)  
**Repository Name:** `research-project-internship-nioo`

---

This repository contains a reproducible pipeline for discovering, filtering, and downloading ecological geospatial datasets for the Veluwe region (Netherlands). It uses standardized OGC (Open Geospatial Consortium) web services to automate access to open geodata from the [Nationaal Georegister (NGR)](https://www.nationaalgeoregister.nl/).

---

## Context

Although ecological data availability has grown significantly, researchers still face major challenges accessing relevant datasets—particularly legacy datasets scattered across studies or national databases requiring regional filtering.

This project addresses those challenges by building an automated Python pipeline that streamlines the discovery, filtering, and retrieval of geospatial data. It is fully aligned with the [FAIR data principles](https://www.go-fair.org/fair-principles/) — **Findable, Accessible, Interoperable, and Reusable** — and evaluates the compatibility between NGR metadata and the [LTER-LIFE](https://lter-nl.nl/en) metadata structure.

---

## Pipeline Overview

The pipeline consists of four main components. Each is implemented in a separate Jupyter Notebook and can be run independently or sequentially.

![Data Pipeline](https://github.com/hudson-passos/research-project-internship-nioo/blob/main/figures/DataPipeline.png?raw=true)

### Part 1: Harvesting Metadata from NGR

📄 **File:** `01_ngr_metadata_extractor.ipynb`

- Retrieves metadata records from the NGR catalog using CSW (Catalogue Service for the Web)
- Parses XML responses to extract metadata fields such as:
  - Title
  - Abstract
  - Bounding box
  - Service URLs
  - Keywords

---

### Part 2: Extracting OGC Service Metadata

📄 **File:** `02_get_coverage_and_feature_names.ipynb`

- Uses OGC operations:
  - `GetCapabilities`
  - `DescribeCoverage` (for rasters)
  - `DescribeFeatureType` (for vectors)
- Retrieves:
  - Spatial resolution
  - CRS
  - Coverage names / feature type names
  - Geometry types

---

### Part 3: Spatial and Content-Based Filtering

📄 **File:** `03_filters_spatial_semantic.ipynb`

- **Spatial filter:** selects datasets intersecting the Veluwe region (EPSG:28992), including a second-pass check to verify data presence
- **Content filter:** applies fuzzy string matching (`fuzzywuzzy`) to metadata keywords and abstracts using a predefined ecological keyword list

---

### Part 4: Data Download via WCS and WFS

📄 **File:** `04_download_wcs_and_wfs.ipynb`

- Downloads **raster data** via WCS and **vector data** via WFS
- Features:
  - Tiling support for large rasters (with merging)
  - Pagination for WFS downloads
  - Fallbacks for version and axis label inconsistencies
- Controlled via two editable CSVs (`wcs_table.csv`, `wfs_table.csv`) to manually select layers for download

---

### Additional Jupyter notebooks

📄 **File:** `00_install_packages.ipynb`

This notebook ensures that all necessary Python packages are installed on the user’s machine before running the project. It serves as a setup step to prepare the working environment.

📄 **File:** `05_data_analysis.ipynb`

This notebook contains exploratory and analytical scripts used to create visualizations and calculate summary statistics for the internship report. It supports the internship report but is not an essential part of the data pipeline.

---

## Output

- Metadata tables (`.csv`)
- Raster files (`.tif`)
- Vector files (`.geojson`)
- Download logs and statistics

---

## Requirements

- Python 3.11+
- Jupyter Notebook
- Dependencies:

