# **SQLAlchemy Challenge**

## Background 
In this assignment, a basic climate analysis was preformed to understand the area of Honolulu, Hawaii in order to plan a vacation. Analysis was preformed using SQLAlchemy ORM, Python, Pandas, Matplotlib, and Flask to further explore climate data. 

## Challenge

### Part 1: Analyze and Explore the Climate Data
#### Create Database 
A Jupyter database was created using a starter code provided to complete climate analysis and data exploration. Using SQLAlchemy the create_engine() function was used to connect to the SQLite database. Using the automap_base() function, I was able to refect the tables into classes. A Python database was linked by creating an SQLAlchemy session. 

#### Precipitation Analysis 
Several steps were taken in this analysis to find various datapoints. Firstly, the most recent date in the dataset was found, then using that date, the previous 12 months of precipitation data was found by querying the data to find only the "date" and "prcp" values. This query was loaded into a Pandas DataFrame and sorted by "date". After, the results were plotted using plt.plot method. Using Pandas, a summary statistics for the precipitation data was printed. 

#### Station Analysis 
Next, a query was designed to calculate the total number of stations in the dataset. This was done to fine the most-active stations (i.e. the stations that have the most rows). A query was designed to calculate the lowest, highest, and average temperatures of that station once discovered. Lastly, a query was designed to get the previous 12 months of temperature observation (TOBS) data. This was then plotted as a histogram. 


### Part 2: Climate Application 

In this secion, a Flask API was created based on the queries devloped in Part 1. Flask was used to create six routes and each root was queried and returned using JSON representaiton of the dictonary. 

## Results: 
### Analyze and Explore the Climate Data 
Based on the data found when performing an exploratory precipitation analysis, the most recent date within the dataset is August 23, 2017. From here, a query was designed to retrieve the last 12 months of precipitation data and plot it on a graph. 

 ![alt text](https://github.com/maddieemihle/sqlalchemy-challenge/blob/main/Images/precipitation.png)

This allowed for the visualization and analysis of precipitation levels for the last twelve months in Hawaii. The results showed that the months with the most percipitation were around July-August.

Based on the data found in the Exploratory Station Analysis, I was able to determine which station had the greatest number of observations. Currently, station USC00519281 was the station with the greatest number of observations. This was found by designing a query to find the most active stations and list in descending order. I calculated the lowest, highest, and average temperatures from there. Based on the results, the data told me that: 
* The lowest temperature recorded at station USC00519281 is 54.0 degrees Fahrenheit.
* The highest temperature recorded at station USC00519281 is 85.0 degrees Fahrenheit.
* The average temperature recorded at station USC00519281 is 71.66 degrees Fahrenheit.

Afterwards, I plotted using a histogram to show the temperature frequency for station USC00519281.

 ![alt text](https://github.com/maddieemihle/sqlalchemy-challenge/blob/main/Images/most_act_temperature_frequency.png)

## Methods Used
* Python 
* SQLAlchemy ORM 
* Pandas
* Matplotlib 
* JSON 
* Flask API 
* API SQLite Connection & Landing page
* API Static Routes

## Software Used 
Coding was preformed via VSCode using Jupyter notebooks and app.py. 

## References
Data for this dataset was given by _edX Boot Camp LLC (2025), and is intended for educational purposes only. Menne, M.J., I. Durre, R.S. Vose, B.E. Gleason, and T.G. Houston, 2012: An overview of the Global Historical Climatology Network-Daily Database. Journal of Atmospheric and Oceanic Technology, 29, 897-910, https://journals.ametsoc.org/view/journals/atot/29/7/jtech-d-11-00103_1.xml.
