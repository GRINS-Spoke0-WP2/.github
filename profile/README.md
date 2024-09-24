# Organisation of Work Package 2 - Spoke 0 - GRINS (Growing Resiliant, INclusive and Sustainable)

This organization on GitHub stems from the need to collect in one place the code produced by the Bergamo team related to downloading and handling environmental data: climate, air quality and emissions. More specifically, this reproducible code will enter the AMELIA platform for the automatisation of the download process, to make the AMELIA platform updatable every release of dataasets.

Several repositories can be found within the organization, each of them almost independent. After downloading the data and preparing them for use, there is a repository that refers to the statistical model used for the techniques of data fusion, change of spatial and temporal support, and uncertainty quantification.

## What is GRINS?

GRINS ([link](https://www.grins.it)) produces frontier research in the economic-political-social science and data science spectrum to provide scientific evidence to guide public policy as well as the choices of citizens and companies in complex decision-making contexts. Grins' mission translates into the realisation of an open data platform designed to support the decision-making processes of all actors, from citizens to administrators, through the production of high quality statistical information and analysis, in compliance with strict professional ethical principles and the most advanced scientific standards. 

### The Spoke 0

Spoke 0, or the Hub, is entirely dedicated to the construction, development and maintenance of the AMELIA (dAta platforM for the transfEr of knowLedge and statistIcal Analysis) data platform. The other eight thematic Spokes will provide Spoke 0 with primary sources, intermediate data, statistical analyses, software codes and final deliverables, which will be processed and harmonised through the platform.

The goal of the AMELIA platform is to help the Italian community to grow efficiently as well as resilient, inclusive and sustainable. This important and challenging platform will be used toward a deeper comprehension of the reality. Data are the mirror of reality, however they must be collected, validated, re-organised, harmonised, analysed, visualised and finally interpreted. Statistical tools are the only instruments capable of performing these operations on the data, so they are indispensable for achieving the goals of the AMELIA platform, and therefore of the GRINS project.

#### The Work Package 2

Work Package 0.2 focuses on ensuring the quality of the indicators available on the platform referring to the economic actors and territories examined, spatially and temporally determined, obtained by means of classical statistical models and machine learning techniques. These indicators will be based on harmonised datasets obtained from the integration of heterogeneous and georeferenced data sources. Frontier research in statistical science and machine learning will be used to build pilot statistical models for record linkage and statistical matching of survey data, spatio-temporal fusion of data, e.g. from Copernicus sources, and small area estimation. The quality of the developed indicators will be evaluated in accordance with the FAIR, SAFE and open data principles.

The team of the University of Bergamo (UNIBG) involved in the spoke 0, more specifically in the Work Package 0.2 (WP0.2), leaded by Prof. Alessandro Fassò, is proposing to use a geostatistical approach to harmonise spatio-temporal data. Indeed, UNIBG team work mainly with environmental data: weather, air quality and emissions. Harmonised data, i.e. with the same spatial and temporal resolution (e.g. municipality and daily), will be part of the AMELIA platform. More specifically, this dataset will represent the deliverable D.0.2.1

# Repositories

This organisation has been created within the GRINS project to take trace of the scripts used for generating intermediate and final outputs of the projects. Several repositories are available and extensive descriptions are contained within each of them. Within the same repository, there are several versions of code (*v.0.0.1* or *v.1.0.0* etc.) that generate respective versions of datasets.

## Data 

Environmental data include different dimensions represented here by different acronyms: **AQ** for Air Quality, **WE** for Weather, **EM** for Emissions. Within the same dimension, data can be substantially different: observed by land monitoring stations, measured by satellites, produced by mathematical models, and others. Several different organisations managing the release of these data, use different procedures. For this reason, the pair dimension-source is used to identify a dataset. Each dataset has his own repository. For example, the air quality data (AQ) downloaded from the European Environmental Agency (EEA) is a repository called **AQ-EEA**. Each repository containes the code used from the download to the final dataset. Common tasks operated with R routines within these repositories are: automatic download, converting format (e.g. from csv or netcdf to Rdata), changing temporal resolution (e.g. from hourly to daily), solving critical situations about the quality of raw data (e.g. errors in the raw data), quality check (e.g. removing anomalies in the data). The spatial resolution is not changed. For data, the following repositories are available:

1. **AQ-EEA** contains the data flow for air quality measurements obtained by the European Environmental Agency.
2. **AQ-CAMS** contains the data flow for air quality numerical models output obtained by the Copernicus Atmosphere Monitoring Service (CAMS).
3. **WE-C3S** contains the data flow for weather data obtained by the Climate Change Service (C3S).
4. **EM-CAMS** contains the data flow for emission data obtained by the Copernicus Atmosphere Monitoring Service (CAMS).

### Available input data (updated 24-09-2024)

| Repo    | Description                  | Period    |
|---------|------------------------------|-----------|
| AQ-EEA  | Air quality station measures | 2013-2023 |
| AQ-CAMS | Air quality numerical output | 2013-2023 |
| WE-C3S  | Weather variables            | 2013-2023 |
| EM-CAMS | Emissions variables          | 2013-2023 |

## Modelling

To reach the ultimate goal of the GRINS project, we need an harmonised dataset at municipal level, daily, containing all the variables considered. However, while administrative data come naturally at municipal level, environmental data can have different resolutions, as points-referenced or grids, but almost never at municipal level. For the change of the spatial resolution we use a statistical modelling approach. The repositories linked to these operations are under the dimension **FRK** (Fixed Rank Kriging) that is the acronym of the model used to tackle the problems of change of support and up/down-scaling faced during the change of spatial resolution. 


