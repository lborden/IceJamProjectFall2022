# IceJamProjectFall2022

This repository contains information regarding the Mohawk River Ice Jam Project for CEE/EAR600M002: Environmental Data Science.

# Introduction
Upstate New York is known for its fierce winters, leading to large build ups of snow and ice deposits, especially in rivers. The Mohawk River is a 149-mile-long water way acting as the largest tributary of the Hudson River. There has been a history of ice jam formation on the Mohawk, so stream gauges and arial radar data is used to analyze the likelihood of future ice jams occurring. 

# Research Question
Can Sentinel-1 Interferometric Spectral Aperture Radar (InSAR) data be used to accurately detect conditions of ice jam formation in frozen channels (i.e., emergent slopes) in the Mohawk River system? 

This study will focus specifically on the years 2015-2020 to evaluate whether InSAR data can be used to detect the occurrences of historic ice jam formation on the Mohawk River. The level of accuracy (i.e., the correlation of fit between emergent slope prediction and ice jam formation) will additionally be assessed throughout this period.

# Data and Methods
Data Source Description

Our first dataset will be collected via the USGS Mohawk River Ice Jam Monitoring interactive data portal (https://ny.water.usgs.gov/maps/mohawk-icejam/). The measurements within this portal contain those recorded by stream gauges placed at five locations (Lock 8, Lock 9, Freeman’s Bridge, Rexford, and Vischer Ferry Dam). Concerning the period in question, gauge height (in ft) will be obtained during the year range of 2015-2020. 

This study will also utilize Interferometric Spectral Aperture Radar (InSAR) data collected by the Sentinel-1 satellite. The data will be acquired using the Copernicus Open Access Hub (Copernicus Sentinel data, 2010) and the Alaska Satellite Facility (ASF, https://storymaps.arcgis.com/stories/68a8a3253900411185ae9eb6bb5283d3), which allows for fast, cloud-based processing of InSAR products from Sentinel-1.  Sentinel-1 collects C-band radiation, which is useful for this study in that it is not limited by cloud cover and can detect the presence of wet snow. Sentinel-1 data from the winters of 2015-2020 in the vicinity of the Mohawk River will be analyzed in October and November of 2022. 

Additionally, records concerning time points of historic ice jams in the years 2015-2020 will be collected from the Cold Regions Research Engineering Laboratory (CRREL)’s Ice Jam Database (https://icejam.sec.usace.army.mil/).

Data Processing Description

	Records containing time-points and geographic coordinates will first be gathered from the US Army Corps of Engineer’s database for reference of historic ice jams in the Mohawk River. These records will provide reference for selective periods to analyze within the InSAR and in situ stream gauge measurements. Following, the in-situ stream gauge data will be collected for the range of time those records suggest for analysis (i.e., 2015-2020). For each of the five sites that are monitored yearly, the geographic location of monitoring will be obtained. Using the geographic locations, corresponding InSAR images of vertical displacement and coherence will be obtained from the Sentinel-1 satellite. Vertical displacement will be masked by corresponding coherence values of greater than 0.8, ensuring data integrity. Vertical displacement calculated within the InSAR images will be compared to in-situ measurements of stream flow from the USGS gauges via regression and correlation analyses. A table containing summary statistics will be provided for dataset representations. Pre-processing above will be calculated using the Python library Pandas.
	Visualization of the relative time-periods will be produced for the InSAR and stream gauge measurements. Time-series plots across the range of 5 years will be produced using the Python libraries Seaborn and Lux. This will show the “normal” activity within the time span as well as the increases in vertical displacement caused by the formation of ice jams. Assessment of variability in InSAR data over time relative to stream gauge data will be conducted through visual analysis. Commonalities in variability spanning the various sites measured by InSAR will be assessed for the potential of climatological influence on measurements. Differences in variability will also be assessed for the potential of evidence concerning uncertainty within InSAR measurements, or variability caused by ice cover (ice surface roughness, ice depth, chemical composition, etc.).

Model Description

	Linear regression models will be developed using Python’s library SciPy. Using InSAR as the dependent variable and stream gauge data as the independent variable, correlation, model strength, and statistical significance of the relationship will be assessed. We will perform these tasks through the assessment of Pearson’s r and Spearman’s r, R2, and p-value produced in the modeling process. Evidence from this assessment will be used for the determination of the feasibility of InSAR data in the future development of a predictive model for ice jam formation. Three models will be developed, the first including only data measured during periods of historic ice jams and rapid increase of vertical displacement. Second, a model will be developed that includes only data from periods of vertical stability of the Mohawk River. Our final model will include all data from the periods with potential for ice jam formation. These models will show the accuracy, precision, and uncertainty associated with InSAR measurements during the varying periods. All developed models will be visualized using the Python libraries Matplotlib, Seaborn and Lux.

# Results

# Discussion

# Conclusion
#put file structure here
