This organisation has been created within the GRINS project to take trace of the scripts used for generating intermediate and final outputs of the projects. Several repositories are available and extensive descriptions are contained within each of them. Within the same repository, there are several versions of scripts (*v.0.0.1* or *v.1.0.0* etc.) that generate respective versions of dataset.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

# GRINS Goal

The goal of the GRINS (Growing Resiliant INclusive and Sustainable) project is to help the Italian community to grow efficiently as well as resilient, inclusive and sustainable. This important and challenging goal will be reached thank to the deeper comprehension of the reality. Data are the mirror of reality, but they must be collected, validated, re-organised, harmonised, analysed, visualised and finally interpreted. Statistical tools are the only instruments capable of performing these operations on the data, so they are indispensable for achieving the goals of the GRINS project.

The team of the University of Bergamo (UNIBG) involved in the spoke 0, more specifically in the Work Package 0.2 (WP0.2), leaded by Prof. Alessandro Fassò, is proposing to use a common methodology for data harmonisation among the groups of the project. In particular, these methods are suitable for spatial and temporal data. UNIBG works mainly with environmental data: weather, air quality and emissions. Harmonised data, with the same spatial and temporal resolution (i.e. municipality and daily), will compose the dataset used by the AMELIA platform. More specifically, this dataset will represent the deliverable D.0.2.1 of the GRINS project.

# Repositories

Environmental data include different dimensions represented here by different acronyms: **AQ** for Air Quality, **WE** for Weather, **EM** for Emissions. Within the same dimension, data can be substantially different: observed by land monitoring stations, measured by satellites, produced by mathematical models, and others. Several different organisations managing the release of these data, use different procedures. For this reason, the pair dimension-source is used identifto identify a dataset. Each dataset has his own repository. For example, the air quality data (AQ) downloaded from the European Environmental Agency (EEA) is a repository called **AQ-EEA**. Each repository containes the code used from the download to the final dataset. Common tasks operated with R routines within these repositories are: automatic download, converting format (e.g. from csv or netcdf to Rdata), changing temporal resolution (e.g. from hourly to daily), solving critical situations about the quality of raw data (e.g. errors in the raw data), quality check (e.g. removing anomalies in the data). The spatial resolution is not changed. For the change of the spatial resolution we use a statistical modelling approach. The repositories linked to these operations are under the dimension **FRK** (Fixed Rank Kriging) that is the acronym of the model used to tackle the problems of change of support and up/down-scaling faced during the change of spatial resolution. 

## Repositories
1. **AQ-EEA** contains the data flow for air quality measurements obtained by the European Environmental Agency.
2. **AQ-CAMS** contains the data flow for air quality numerical models output obtained by the Copernicus Atmosphere Monitoring Service (CAMS).
3. **WE-C3S** contains the data flow for weather data obtained by the Climate Change Service (C3S).
4. **EM-CAMS** contains the data flow for emission data obtained by the Copernicus Atmosphere Monitoring Service (CAMS).

# Modelling

To reach the ultimate goal of the GRINS project, we need an harmonised dataset at municipal level, daily, containing all the variables considered. However, while administrative data come naturally at municipal level, environmental data can have different resolutions, as points-referenced or grids, but almost never at municipal level. We decided to tackle this problem using a statistical approach. Different models are considered: Hidden Dynamic Geostatistical Model (HDGM), Fixed Rank Kriging (FRK), and other models are under investigation.



