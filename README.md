# MB5370 Module 2: Data Science in R

This repository documents four computer workshops from the JCU MB5370 'Data Science in R' module. Building on the concepts introduced in [Module 1](https://github.com/katiedyck/MB5370_Module01), it covers more advanced data science approaches. I learned how to compile complex environmental monitoring pipelines, create journal-quality visualizations, manipulate spatial datasets, and generate automated, reproducible scientific reports.

| Workshop | Topic | Summary | 
| :---- | :---- | :---- |
| 1 | Foundations of Data Science — Wrangling and Plotting | Importing, cleaning/wrangling, and visualizing data in R, without using an AI extensions (e.g. [GitHub Copilot](https://docs.github.com/en/copilot/get-started/what-is-github-copilot), [`chattr`](https://mlverse.github.io/chattr/) to help generate code. |
| 2 | Advanced Data Wrangling: Extracting ecological signals from noisy systems | Pivoting data frames (`pivot_longer()`, `pivot_wider()`), splitting a data frame column into multiple columns, combining multiple data frame columns into one column, wrangling strings and dates using the `stringr` and `lubridate` packages, and how to handle missing values in data frames. This workshop also included an exercise where I cleaned and analysed 4 data files containing information on water quality and predatory fish species along the Ross River Estuary gradient in Queensland, Australia. | 
| 3 | Plot Deconstruction | An exercise where I found a published figure, extracted the data, and reconstructed the figure using the concepts covered in workshop 1 and 2. I extracted data that I used to map trends in global fisheries over time in terms of fish stock status (fully, partially, or under-exploited). | 
| 4 | Spatial Data in R | Visualizing spatial data (i.e. GPS coordinates) in R. I wrangled multiple datasets to map how copepod species richness in Australia changed through 2009 with variation in water temperature. A basic introduction to the packages [`sf`](https://r-spatial.github.io/sf/), [`terra`](https://rspatial.github.io/terra/), [`leaflet`](https://rstudio.github.io/leaflet/) and [`tmap`](https://r-tmap.github.io/tmap/), all of which have different capabilities for mapping spatial data in R. |
-----------

The [code](code) folder contains the R Quarto markdown files I created for these workshops; each workshop has its own file.

## Overview of data files
The [data](data) folder contains .csv, .txt, and .xlsx files that I uploaded to R to complete workshops 1 through 4.

### Workshop 1
- [`acoustic_telemetry_stream.txt`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop1/acoustic_telemetry_stream.txt) - Acoustic tracking data for 4 sea turtles, collected in May 2026 (specific location unknown).
- [`fish_catch_data.xlsx`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop1/fish_catch_data.xlsx)(_must be downloaded to view_) - Information on fish species caught on the Great Barrier Reef in March 2026, including name of vessels that caught the fish, target species scientific name, total weight of fish caught, total weight of bycatch species caught, and the zone where the fish were caught.
- [`mangrove_survey_raw.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop1/mangrove_survey_raw.csv) - Information about mangroves located on Hinchinbrook Island, Queensland, Australia. The first five rows of the file contain information pertaining to weather, equipment used, and notes concerning data collection that are relevant to data analysis.
- [`reef_cover_log.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop1/reef_cover_log.csv) - Data collected from underwater transects performed on in various locations on Magnetic Island, Queensland, Australia, in May 2026. Contains information on coral reefs in Nelly Bay, Geoffrey Bay, and Florence Bay, such as depth (in metres) and percentage cover of hard corals, macroalgae, and bare substrate.

### Workshop 2
- [`estuary_catch_log.xlsx`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop2/estuary_catch_log.xlsx)(_must be downloaded to view_) - Fish catch data from the Ross River in Queensland, Australia. Contains data on area where fish were caught, date of the catch (May 1 to 30 2026), common species name, and number of fish caught. *Note that this file contains 4 sheets of data: each one contains data on a separate area of the Ross River (lower, mid, river mouth, and upper)*.
- [`estuary_metadata.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop2/estuary_metadata.csv) - Latitude, longitude, and zone for each area of the Ross River. Corresponds with the data in 'estuary_catch_log.xlsx'.
- [`estuary_sonde_data.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop2/estuary_sonde_data.csv) - Temperature (°C), salinity (PSU), and turbidity (Nephelometric Turbidity Units, NTU) data for each area of the Ross River (lower, mid, river mouth, upper). Data for all 3 variables was collected from May 1 to 27 2026.
- [`species_dictionary.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop2/species_dictionary.csv) - Scientific and common species name of each fish species included in 'estuary_catch_log.xlsx' and 'estuary_metadata.csv'.

### Workshop 3
- [`global_fish_stocks.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop3/global_fish_stocks.csv) - Date/time and percentage of fish caught, based on the data shown in the first graph at [](https://reefresilience.org/coral-reef-fisheries-module/coral-reef-fisheries/overfishing/).

### Workshop 4
- [`Route-data.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop4/data-for-course/Route-data.csv) - Movement trajectories travelled by vessels towing Continuous Plankton Recording (CPR) devices throughout Australia. This file can be used to create maps of where plankton were caught in Australia in 2009.
- [`copepods_abundance.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop4/data-for-course/copepods_abundance.csv) - Copepod species counts throughout Australia, collected in 2009, counted using samples taken from a Continuous Plankton Recorder (CPR). "Silk" refers to silk bands continuously run through the CPR; they trap plankton as the vessel towing the CPR moves through the water. 
- [`copepods_raw.csv`](https://github.com/katiedyck/MB5370_Module02/blob/main/data/workshop4/data-for-course/copepods_raw.csv) - Raw copepod measurement data collected in 2009. 

In the `spatial-data` folder:
- Shapefile of Australia with state/territory boundary lines ([`Aussie`](https://github.com/katiedyck/MB5370_Module02/tree/main/data/workshop4/data-for-course/spatial-data/Aussie) folder)
- Shapefile of the Australian coastal shelf ([`aus_shelf`](https://github.com/katiedyck/MB5370_Module02/tree/main/data/workshop4/data-for-course/spatial-data/aus_shelf) folder)
