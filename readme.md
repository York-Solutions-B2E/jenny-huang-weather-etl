### DETAILS ABOUT TEMP STATS
* Temperature mean and median were calculated from the TEMP column
* TEMP_min is the monthly average of the MIN column, and TEMP_max is the monthly average of the MAX column
* All stats were calculated with missing values ( = 999.9 or 99.99 depending on var) removed

### ASSIGNMENT INSTRUCTIONS!

Dear Data Science Team,

* We are seeking your expertise to develop an ETL (Extract, Transform, Load) pipeline that will enable us to analyze historical weather data. Our focus is on understanding the changes in temperature and precipitation across the 48 contiguous United States between the years 1950 and 2000.

* Your primary data source will be the NOAA GSOD dataset, accessed here: https://www.ncei.noaa.gov/access/metadata/landing-page/bin/iso?id=gov.noaa.ncdc:C00516

* We need detailed statistical data on temperature and precipitation, aggregated monthly. This data should include metrics such as mean, median, variance, minimum, and maximum values.

### Technical Requirements:
* All scripts and data processing must be conducted in Jupyter Notebook. 
* Please set up a dedicated project folder and Git repository for this assignment, using the naming convention <firstname>-<lastname>-weather-etl.  For example, Tom Cruise would name his repository -tom-cruise-weather-etl. All code should be done in a jupyter notebook
* Global Surface Summary of the Day - GSOD
### Goals:
* Programatically (in python) download the appropriate gzip data from the link above one at a time.
* Unzip the data, and then delete the gzip file.
* Go through each csv and filter / clean out the appropriate data into a dataframe. This may require other libraries, such as reverse_geocoder.
* Delete the csvs when you are finished with them.
* Repeat steps 3-4 until you have a months worth of data, then transform that data to get the requested information above.
* Repeat steps 1-5 for each month and then for year between 1950 and 2000.
* At this point you should have a fully transformed dataset with yearly statistical data between 1950 and 2000.
* Export that data into a postgres database using sql alchemy.
* NOTE:  You will want to stop your existing container from running, then start a fresh database by making a new docker-compose file.  Ensure you have a .gitignore file so that the data on this postgres database isn't stored in git.

### Final Execution:
* Upon completion of the above steps, the following actions should replicate the database successfully:
* Run docker-compose up
* Run the jupyter notebook.

### End-State:
* The project should be finalized with a clean workspace, meaning no unnecessary files remain in the project directory, and a fully operational database reflecting the processed data.

### Project Maintenance (KEEP THESE IN MIND):
* Efficient Development: Be mindful of the time taken to download files. Develop strategies to test your program without needing to download all 50 years of data simultaneously.
* File and Memory Management: Ensure the deletion of files post-processing and avoid retaining unnecessary data in memory. This approach is crucial to prevent system overload or program crashes due to excessive memory usage or storage constraints.
* Many of these steps may require you to do additional research to complete.  Ensure you have understanding of the code in your project, even if its code copied from online.
