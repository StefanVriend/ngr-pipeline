# Internship project - description
## Repository: research-project-internship-nioo
Author: Hudson Passos

This is a research report prepared to accomplish my internship at Netherlands Institute of Ecology (NIOO-KNAW).
Duration: 4 months (2 April 2025 - 4 August 2025)

Project name: Simplified Access to Veluwe Ecological Data Through Open Geospatial APIs
Host Supervisor: Stefan Vriend | NIOO-KNAW 
WUR Supervisor: Liesbeth Bakker | Wageningen U&R, NIOO-KNAW 

Summary:

In recent decades, the volume of ecological data available at the national and international level has grown significantly, with many open-access datasets now accessible through various online platforms (Güntsch et al., 2025). However, much of this legacy data remains fragmented, dispersed across numerous small-scale studies, making it difficult and time-consuming to identify relevant datasets for a specific region (Reyserhove et al., 2020). Ecologists — particularly those involved in data-intensive tasks such as modelling — often face challenges in efficiently locating and manually downloading the data needed to support their research and conduct repeatedly the same preprocessing tasks to adjust the data to their study area.  
An effective approach to overcome this challenge is by using APIs and standardized Open Geospatial Consortium (OGC) web services (OGC, 2016), which allow for more efficient discovery, filtering, and retrieval of geospatial data directly from online sources. These technologies offer powerful tools for automating data access, but they remain unfamiliar to many ecologists and can be difficult to use without technical expertise. This project addresses that gap by developing an automated pipeline for the discovery and processing of ecological datasets from multiple sources, with a focus on the Veluwe region in the Netherlands.
The pipeline leverages standardized OGC geospatial APIs to automate dataset selection from three major open data sources: NGR (Dutch National Georegister), PDOK (Publieke Dienstverlening Op de Kaart), and AgroDataCube. First, it applies spatial filtering to select datasets that intersect the Veluwe region. Next, it filters the resulting metadata based on a set of keywords (or “wish list”) relevant to ecological studies, provided by experts at NIOO-KNAW. Alternatively, a pre-trained large language model (LLM) may be used to interpret metadata and identify datasets aligned with ecological research, enhancing the relevance of the selection. Finally, a preprocessing step (e.g., reprojection, resampling, clipping) ensures that selected raster datasets are harmonized and ready for analysis.
The resulting workflow streamlines the process of accessing, selecting, and preparing ecological data from diverse sources, reducing manual effort and increasing reproducibility (Brousil et al., 2023). Ultimately, this project aims to support the broader goals of the LTER-LIFE initiative, coordinated by NIOO-KNAW, by enabling more efficient and integrated reuse of ecological data for long-term research and monitoring. 

