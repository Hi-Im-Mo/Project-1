# US RSV Trend Analysis
This project seeks to analyze regional and demographic trends using the data provided from the [CDC's RSV-NET](https://cdc.gov/rsv/research/rsv-net/dashboard.html). The code is authored entirely by the contributers to this repo and this README template is from the Data Science Working Group.

#### -- Project Status: [Completed]

## Project Intro/Objective
The purpose of this project is to reveal regional hotpots in the United States with the highest proportion of RSV hospitalizations as well as any groups of people (sex, race, age) that are particularly at risk for positive Respiratory Syncytial Virus testing or hospitilization due to the virus. 

### Methods Used
* Data Cleaning 
* API Requests
* Data Visualization

### Technologies
* Python
* Pandas, jupyter
* Matplotlib
* [Weekly Lab-Confirmed Hospitalizations from RSV API](https://data.cdc.gov/Public-Health-Surveillance/Weekly-Rates-of-Laboratory-Confirmed-RSV-Hospitali/29hc-w46k)

## Project Description
The data source for this project comes from the Centers for Disease Control and Prevention's RSV-NET which is a part of the grander RESP-NET encompassing the Influenza, COVID-19 and RSV surveillance networks. Our team pulled a dataset from National Respiratory and Enteric Virus Surveillance System (NREVSS) on [lab testing data for RSV](https://healthdata.gov/dataset/Respiratory-Syncytial-Virus-Laboratory-Data-NREVSS/7zgq-bp9w/data) and made requests to an API created by the CDC's data team on [weekly hospitalization rates](https://data.cdc.gov/Public-Health-Surveillance/Weekly-Rates-of-Laboratory-Confirmed-RSV-Hospitali/29hc-w46k) throughout the US. We were able to work with these datasets in parallel by matching the MMWR week data provided from the API to the weekly records on the NREVSS datset. We also cleaned up the data from our API to be in HHS regions rather than separated by state. This allowed us to visualize the trends by age group, race, sex and region over time and overall. 

## Getting Started

1. Clone this repo (for help see this [tutorial](https://help.github.com/articles/cloning-a-repository/)).
2. Jupyter Notebook scripts for data cleaning are available in the front of the repo in "api_cdc_data" and "CSV cleanup".
3. Our visualizations and output are being kept [here](output_data) within this repo.
4. Cleaned datasets are available [here](Resources).
5. Visualization scripts are in the front of the repo saved under "kiara_s" and "vis_code".
6. The PDF copy of our presentation slides is named RSV Data Analytics in the front of the repo. 
   
## Project Analysis
Overall, we can conclude from these data that RSV spikes greatest during the fall and winter months when viral illness tends to thrive, as evidenced by the line charts across all years in our data (October, November, December, January, and February). The south-central area of the United States (Arkansas, Louisiana, New Mexico, Oklahoma, and Texas) sees more hospitalizations related to RSV. In particular, there are more hospitalized male infants possibly due to males having a smaller diameter airway than females. We noticed a slight decrease in positive tests in 2020 which could be related to the increased global focus on the COVID-19 epidemic. Additionally, the available data for 2020 stops after 6 months, which is a sizable limiting factor and could be responsible for the decreased positive tests. Like we concluded earlier, RSV surges in the winter months, and while our dataset has pertinent data for January and February, the data for the colder months at the end of 2020 are absent. Given the trend of the overall positive cases in previous years, we can safely predict that if the 2020 data were fully available, positive tests would surge at the end of the year and balance out around an average of 7.5% percent positive cases for the year. Thus, this also represents a potential future direction for the dataset. Another interesting analysis that could be conducted in the future would be the correlation between positive RSV tests and hospitalization for a given region. We explored whether there were just regional trends for positive testing or regional trends in hospitilzation rates; however, it is worth exploring if the amount of postive tests in a region can predict hospitalizations for RSV. Our data would support a strong positive correlation, but without a correlational analysis, we can not confirm there is any relationship. 
