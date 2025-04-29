# Internship project - description
## Repository: research-project-internship-nioo
Author: Hudson Passos

This research report was prepared to fulfill the requirements of my internship at the Netherlands Institute of Ecology (NIOO-KNAW), conducted over a four-month period from April 2, 2025, to August 4, 2025.

Project name: Simplified Access to Veluwe Ecological Data Through Open Geospatial APIs  
Host Supervisor: Stefan Vriend | NIOO-KNAW  
WUR Supervisor: Liesbeth Bakker | Wageningen U&R, NIOO-KNAW  
  
Summary:  
  
In recent decades, the volume of ecological data available at the national and international level has grown significantly, with many open-access datasets now accessible through various online platforms (Güntsch et al., 2025). However, much of this legacy data remains fragmented, dispersed across numerous small-scale studies, making it difficult and time-consuming to identify relevant datasets for a specific region (Reyserhove et al., 2020). Ecologists — particularly those involved in data-intensive tasks such as modelling — often face challenges in efficiently locating and manually downloading the data needed to support their research and conduct repeatedly the same preprocessing tasks to adjust the data to their study area.  
  
An effective approach to overcome this challenge is by using APIs and standardized Open Geospatial Consortium (OGC) web services (OGC, 2016), which allow for more efficient discovery, filtering, and retrieval of geospatial data directly from online sources. These technologies offer powerful tools for automating data access, but they remain unfamiliar to many ecologists and can be difficult to use without technical expertise. This project addresses that gap by developing an automated pipeline for the discovery and processing of ecological datasets from multiple sources, with a focus on the Veluwe region in the Netherlands.  
  
The pipeline leverages standardized OGC geospatial APIs to automate dataset selection from three major open data sources: NGR (Dutch National Georegister), PDOK (Publieke Dienstverlening Op de Kaart), and AgroDataCube. First, it applies spatial filtering to select datasets that intersect the Veluwe region. Next, it filters the resulting metadata based on a set of keywords (or “wish list”) relevant to ecological studies, provided by experts at NIOO-KNAW. Alternatively, a pre-trained large language model (LLM) may be used to interpret metadata and identify datasets aligned with ecological research, enhancing the relevance of the selection. Finally, a preprocessing step (e.g., reprojection, resampling, clipping) ensures that selected raster datasets are harmonized and ready for analysis.  
  
The resulting workflow streamlines the process of accessing, selecting, and preparing ecological data from diverse sources, reducing manual effort and increasing reproducibility (Brousil et al., 2023). Ultimately, this project aims to support the broader goals of the LTER-LIFE initiative, coordinated by NIOO-KNAW, by enabling more efficient and integrated reuse of ecological data for long-term research and monitoring.  

## References:  
* Brousil, M., Filazzola, A., Meyer, M., Sharma, S., & Hampton, S. (2023). Improving ecological data science with workflow management software. Methods in Ecology and Evolution, 14, 1381-1388. https://doi.org/10.1111/2041-210X.14113.  
* Güntsch, A., Overmann, J., Ebert, B., Bonn, A., Bras, Y., Engel, T., Hovstad, K., Canhos, D., Newman, P., Kloeke, E., Ratcliffe, S., le Roux, M., Smith, V., Triebel, D., Fichtmueller, D., & Luther, K. (2025). National biodiversity data infrastructures: ten essential functions for science, policy, and practice. BioScience, 75, 139-151. https://doi.org/https://doi.org/10.1093/biosci/biae109.  
* OGC. (2016). OGC® Catalogue Services 3.0 - General Model (Version 3.0, OGC 12-168r6). https://doi.org/http://docs.opengeospatial.org/is/12-168r6/12-168r6.html.  
* Reyserhove, L., Desmet, P., Oldoni, D., Adriaens, T., Strubbe, D., Davis, A., Vanderhoeven, S., Verloove, F., & Groom, Q. (2020). A checklist recipe: making species data open. Database, XXXX, 1-12. https://doi.org/10.1093/database/baaa084.  

