# MB5370 Module 2: Data Science in R

This repository contains code and data, and other supplementary files from Module 2 workshops.
- <ins>**Workshop 1**</ins> is a basic introduction to importing, cleaning/wrangling, and visualising data in R.
- <ins>**Workshop 2**</ins> covers R coding concepts such as pivoting data frames to make them longer or wider, separating data frame columns into multiple columns, combining multiple data frame columns into one column, wrangling strings and dates using the `stringr` and `lubridate` libraries, and how to handle missing values in data frames.
- <ins>**Workshop 3**</ins> is an exercise where I found a figure from a scientific paper, extracted the data, and reconstructed the figure using concepts covered in workshop 1 and 2. I extracted data that I used to map trends in global fisheries over time in terms of fish stock status (fully, partially, or under exploited).
- <ins>**Workshop 4**</ins> covered an introduction to visualizing spatial data (i.e. GPS coordinates) in R. I wrangled multiple datasets to map how copepod species richness in Australia has changed with variation in water temperature.

The [code](code) folder contains the R Quarto markdown files I created for these workshops; each workshop has its own file.

## Overview of data files
The [data](data) folder contains .csv, .txt, and .xlsx files that I uploaded to R to complete workshops 1 through 4.

### Workshop 1
- `acoustic_telemetry_stream.txt` - Acoustic tracking data for 4 sea turtles, collected in May 2026 (specific location unknown).
- `fish_catch_data.xlsx` - Information on fish species caught on the Great Barrier Reef in March 2026, including name of vessels that caught the fish, target species scientific name, total weight of fish caught, total weight of bycatch species caught, and the zone where the fish were caught.
- `mangrove_survey_raw.csv` - Information about mangroves located on Hinchinbrook Island, Queensland, Australia. The first five rows of the file contain information pertaining to weather, equipment used, and notes concerning data collection that are relevant to data analysis.
- `reef_cover_log.csv` - Data collected from underwater transects performed on in various locations on Magnetic Island, Queensland, Australia, in May 2026. Contains information on coral reefs in Nelly Bay, Geoffrey Bay, and Florence Bay, such as depth (in metres) and percentage cover of hard corals, macroalgae, and bare substrate.

### Workshop 2
- `estuary_catch_log.xlsx` - Fish catch data from the Ross River in Queensland, Australia. Contains data on area where fish were caught, date of the catch (May 1 to 30 2026), common species name, and number of fish caught. *Note that this file contains 4 sheets of data: each one contains data on a separate area of the Ross River (lower, mid, river mouth, and upper)*.
- `estuary_metadata.csv` - Latitude, longitude, and zone for each area of the Ross River. Corresponds with the data in 'estuary_catch_log.xlsx'.
- `estuary_sonde_data.csv` - Temperature (°C), salinity (PSU), and turbidity (Nephelometric Turbidity Units, NTU) data for each area of the Ross River (lower, mid, river mouth, upper). Data for all 3 variables was collected from May 1 to 27 2026.
- `species_dictionary.csv` - Scientific and common species name of each fish species included in 'estuary_catch_log.xlsx' and 'estuary_metadata.csv'.
