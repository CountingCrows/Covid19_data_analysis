![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/4f7f62a4-ddff-431a-b286-1e93ed1bc425)# Covid19_data_analysis

In this portfolio, we'll delve into the nuances of data preparation and analysis. Starting with the preprocessing and merging of key datasets, we'll focus on fine-tuning the COVID19 dataset by eliminating specific columns and consolidating rows. Our exploration involves identifying meaningful metrics, merging datasets to discover underlying correlations, and ultimately visualizing our findings using the powerful Seaborn tool. This process aims to provide a clear understanding of our objectives, datasets, and the pertinent questions our analysis addresses.

## Dataset
We'll explore the COVID19 dataset from John Hopkins University, detailing daily confirmed cases by country. We'll also examine a global dataset on life factors rated by residents of each nation. Our goal is to merge these datasets and investigate any potential links between the virus's spread and the happiness of a country's inhabitants.

## Tasks
- Deleting useless columns from our dataset
- Aggregating the rows by the country
- Visualizing data related to a country for example China
- Calculating a good measure
- Calculating the first derivative of the curve
- Find maxmimum infection rate for China, Italy, and Spain
- Find maximum infection rate for all of the countries.
- Merging two datasets
- Finding and visualizing correlations between the maximum infection rate and other variables

## Data Cleaning
We delete the Columns 'Lat' for Latitude and 'Long' for Longitude. We aggregate the data because in each row of our dataframe we had data related to each province in each country, but for our analysis we needed number of confirmed cases related to each country.

## Analysis
First, we try to visualize the cummulative confirmed cases in China, Italy and Spain to understand the data. 
![Screenshot 2023-09-02 161925](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/578239a9-1858-4d3a-bf07-595ba15bc25b)

As we can see, COVID19 cases for the first three months of 2022 were rocketly rising in China. So we need to find a good measure reperestend as a number, describing the spread of the virus in a country.
![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/1a7031a0-f7ae-42ff-a9c7-6a4aa154d3f7)
The timeline of this plot is from January the 1st to end of April, but we can see in January there's a peak rise of cases in the first month. So we want to make another plot where the timeline is the first 3 days of Covid 19 in China.
![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/4909d083-19e3-4e9b-9df9-59cffb530420)
We can notice that in the first 24 hours, infected cases rise slightly for 100 new cases. In the next day, the growth of new infected cases increased again for 250 new cases.




## Conclusion
We can conclude based on the correlation between GDP per capita and maximum infection rates, that developed countries are more prone to getting the infection. We can also notice that the other variables such as Social support, Healthy life expectancy, Freedom to make life choices also have a postivie linear relationship with the maximum infection rates
