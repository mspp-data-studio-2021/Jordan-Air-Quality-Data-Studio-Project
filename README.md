# Air Quality during the COVID-19 Pandemic 
This project explores Air Quality Index (AQI) levels for Ozone and PM2.5 pollutants across counties in New York State (NYS) over the course of the COVID-19 pandemic (from March 2020 to March 2021). 
*This project is my final assignment for my M.S. in Public Policy degree from NYU Wagner as part of the NYU Wagner MSPP 2021 cohort.* 
## Getting Started
This project uses [R](https://cran.rstudio.com/) and [RStudio](https://www.rstudio.com/products/rstudio/download/). 
* First, you will need to download and install R and RStudio
* Second, you will need to clone this repository and open the file ```Jordan-Air-Quality-Data-Studio-Project.Rproj``` to launch the project in RStudio. 
* My project uses ```renv``` to handle dependency managemnt. When you launch the project in RStudio, this package will automatically be installed. Or you can do so manually using ```install.packages("renv"))```. Then to install all the required packages, run the following on the R console in RStudio, and when prompted, select the option ```Restore the project from the lockfile```:
  * ```renv::init()```
## Data Sources Used
This project uses three datasets from two different sources. 
* [Environmental Protection Agency (EPA) data](https://aqs.epa.gov/aqsweb/airdata/download_files.html#AQI): 
  * Both the 2020 and 2021 dataset can be found at this link. You will need to download "daily_aqi_by_county_2020.zip" and "daily_aqi_by_county_2021.zip"
  * The EPA tracks AQI levels for 5 recognized pollutants by county each day across the country. The 2020 dataset are these measurements for the entire year of 2020. The 2021 dataset includes measurements up to and including March 2021.  
* [NYS Department of Health](https://health.data.ny.gov/Health/New-York-State-Statewide-COVID-19-Fatalities-by-Co/xymy-pny5) 
  * This dataset reports COVID-19 fatalities each day for each county in NYS from March 2020 to June 2021 as recorded by the NYS Department of Health. 
* All three raw datasets can be found in the folder titled [raw data](https://github.com/mspp-data-studio-2021/Jordan-Air-Quality-Data-Studio-Project/tree/main/raw%20data) 
* All three cleaned datasets can be found in the folder titled [clean data](https://github.com/mspp-data-studio-2021/Jordan-Air-Quality-Data-Studio-Project/tree/main/clean%20data) 
## Replicating the Analysis
* All necessary code is located in the folder titled [code](https://github.com/mspp-data-studio-2021/Jordan-Air-Quality-Data-Studio-Project/tree/main/code) 
* All notebooks are numbered in the order they need to be run in: 
  * [01_Clean data.Rmd](https://github.com/mspp-data-studio-2021/Jordan-Air-Quality-Data-Studio-Project/blob/main/code/01_Clean%20data.Rmd) 
    * This notebook loads in the three needed datasets and cleans them to prepare them for the analysis. 
  * [02_Merge Data.Rmd](https://github.com/mspp-data-studio-2021/Jordan-Air-Quality-Data-Studio-Project/blob/main/code/02_Merge%20Data.Rmd) 
    * This notebook merges the now clean datasets into one merged dataset to be used in the analysis. 
  * [03_Regression Analysis and Visualization.Rmd](https://github.com/mspp-data-studio-2021/Jordan-Air-Quality-Data-Studio-Project/blob/main/code/03_Regression%20Analysis%20and%20Visualization.Rmd) 
    * This notebook runs regressions to explore the relationship between 1. AQI levels for Ozone and PM2.5 pollutants and 2. NYS COVID-19 fatalities. The regression results are then visualized in multiple tables and graphs. 
  * [04_Visualizations.Rmd](https://github.com/mspp-data-studio-2021/Jordan-Air-Quality-Data-Studio-Project/blob/main/code/04_Visualizations.Rmd) 
    * This final notebook creates other visualizations of the data, including graphs that track AQI levels for Ozone and PM2.5 pollutants by county from March 2020 to March 2021 and graphs that track COVID-19 fatalities by county over the same time period. Both static and interactive graphs are included in this notebook. Finally, this notebook includes code to find basic information about the data, including the average AQI by county for each pollutant and the average COVID-19 fatalities for each county. 
## Methods Used 
This project uses a regression analysis to explore the relationship between 1. AQI levels for Ozone and PM2.5 pollutants and 2. NYS COVID-19 fatalities using data from March 2020 to March 2021, which was downloaded from the EPA and the NYS Department of Health websites. Visualizations are also created to track AQI levels and COVID-19 fatalities over the course of this time period, and to visualize the regression results. 
## Acknowledgments 
* Thank you to Professor Maxwell Austensen and the other members of the NYU Wagner MSPP 2021 cohort for their guidance and support throughout this project. 
