# 🌿 Internship Project

## 📄 Summary

**Author:** Hudson Passos  
**Institution:** Wageningen University & Research (WUR)  
**Internship Host:** Netherlands Institute of Ecology (NIOO-KNAW)  
**Duration:** April 2, 2025 – August 4, 2025  
**Project Title:** *Simplified Access to Veluwe Ecological Data Through Open Geospatial APIs*  
**Host Supervisor:** Stefan Vriend (NIOO-KNAW)  
**WUR Supervisor:** Liesbeth Bakker (WUR, NIOO-KNAW)  
**Repository Name:** `research-project-internship-nioo`

---

## 🧭 Project Overview

In recent decades, the volume of ecological data available at national and international levels has expanded significantly, with many open-access datasets now offered through online platforms (Güntsch et al., 2025). Despite this progress, much legacy data remains fragmented — spread across various small-scale studies — making it time-consuming and difficult to identify relevant datasets for a specific region (Reyserhove et al., 2020).

Ecologists, especially those working on data-intensive tasks such as modelling, frequently face challenges in efficiently locating and manually downloading data. Moreover, repetitive preprocessing steps — like spatial clipping or reprojection — are often necessary before datasets can be used for analysis.

This project addresses these limitations by leveraging standardized Open Geospatial Consortium (OGC) web services and APIs (OGC, 2016) to automate the discovery and processing of ecological data. The solution aims to simplify access to distributed geospatial datasets, particularly for the Veluwe region in the Netherlands.

---

## 🔧 Methodology

The developed pipeline enables:

- **Automated discovery** of datasets from:
  - NGR (Dutch National Georegister)  
  - PDOK (Publieke Dienstverlening Op de Kaart)  
  - AgroDataCube  

- **Spatial filtering** to identify datasets intersecting the Veluwe region

- **Metadata filtering**, using:
  - A curated list of ecological keywords provided by NIOO experts  
  - Optionally, a large language model (LLM) to interpret metadata descriptions and improve relevance

- **Preprocessing** of raster data, including:
  - Reprojection  
  - Resampling  
  - Clipping to study area

This approach significantly reduces manual effort and increases reproducibility in ecological research workflows (Brousil et al., 2023). It also supports the broader objectives of the **LTER-LIFE initiative**, coordinated by NIOO-KNAW, by promoting the reuse and integration of ecological datasets.

---

## 📚 References

- Brousil, M., Filazzola, A., Meyer, M., Sharma, S., & Hampton, S. (2023). Improving ecological data science with workflow management software. *Methods in Ecology and Evolution*, 14, 1381–1388. https://doi.org/10.1111/2041-210X.14113  
- Güntsch, A., Overmann, J., Ebert, B., Bonn, A., Bras, Y., Engel, T., ... & Luther, K. (2025). National biodiversity data infrastructures: ten essential functions for science, policy, and practice. *BioScience*, 75, 139–151. https://doi.org/10.1093/biosci/biae109  
- OGC. (2016). *OGC® Catalogue Services 3.0 – General Model* (Version 3.0, OGC 12-168r6). http://docs.opengeospatial.org/is/12-168r6/12-168r6.html  
- Reyserhove, L., Desmet, P., Oldoni, D., Adriaens, T., Strubbe, D., ... & Groom, Q. (2020). A checklist recipe: making species data open. *Database*, baaa084. https://doi.org/10.1093/database/baaa084  

---

