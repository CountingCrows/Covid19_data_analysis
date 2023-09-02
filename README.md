# Covid19_data_analysis

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

![Screenshot 2023-09-02 161925](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/578239a9-1858-4d3a-bf07-595ba15bc25b)"

As we can see, COVID19 cases for the first three months of 2022 were rocketly rising in China. So we need to find a good measure reperestend as a number, describing the spread of the virus in a country.

![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/1a7031a0-f7ae-42ff-a9c7-6a4aa154d3f7)

The timeline of this plot is from January the 1st to end of April, but we can see in January there's a peak rise of cases in the first month. So we want to make another plot where the timeline is the first 3 days of Covid 19 in China.

![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/4909d083-19e3-4e9b-9df9-59cffb530420)

We can notice that in the first 24 hours, infected cases rise slightly for 100 new cases. In the next day, the growth of new infected cases increased again for 250 new cases.
We want to find a measure for the spread of the virus in this period. We can say the spread of the virus is the average number of new confirmed cases or the maximum number of new cases. Maximum number of new infected cases in every 24 ours, over our time period

![Screenshot 2023-09-02 163422](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/f646c8fc-be89-4636-a6de-65b75c5be34e)

This plot shows us the number of infection rates day by day in our period. Now we want to know the exact amoun of the maximum number in the plot in China and for other cou ntries.
From this point, we will find the maximum infection rates for all countries and adding it to our dataset.

We then make a new dataset to be merged with the WorldHappinessReport.csv dataset. Data cleaning is also used for this dataset where we drop the useless columns for analysis such as 'Overall Rank', 'Score', 'Generosity', and 'Perceptions of corruption'. After we change the indexes of the WorldHapinessReport.csv with the country names, we can merge both datasets by 'Country or region'.

![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/ed79a944-75fe-4d6e-aed3-5ce13c744706)

We want to analyse the correlation between max_infection_rates with the other 4 variables.

![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/51b1a4b5-7c0a-4dcd-94ae-be02ba8165c9)

In this slope, you can see there is an increase. There is a positive correlation between maximum infection rates and GDP per capita. 

![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/0faff248-a815-48dc-b5dd-7899d0c1bcee)

In this slope, you can see there is also an increase. There is a positive correlation between maximum infection rates and Social Support.

![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/03faad06-2458-4478-853f-74b68e461fd7)

In this slope, you can see there is also an increase. There is a positive correlation between maximum infection rates and Healthy Life Expectancy.

![image](https://github.com/CountingCrows/Covid19_data_analysis/assets/85608120/4ba6cfd7-6657-4e84-b8fd-7bd87bd32946)

In this slope, you can see there is also an increase. There is a weak positive correlation between maximum infection rates and Freedom to make life choices.


## Conclusion
We can conclude based on the correlation between GDP per capita and maximum infection rates, that developed countries are more prone to getting the infection. We can also notice that the other variables such as Social support, Healthy life expectancy, Freedom to make life choices also have a postivie linear relationship with the maximum infection rates
