<h1 align='center'>Introduction to Machine Learning</h1>
<h2 align='center'>Exoplanet Classification</h2>

<img align='center' src='Images/exoplanets.jpg'>

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created multiple machine learning models capable of classifying candidate exoplanets from the raw dataset.

## Data

The full dataset can be found [here](https://www.kaggle.com/nasa/kepler-exoplanet-search-results) through Kaggle. The data can be difficult to understand so I'm including a reference to the columns, https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html. 

### PreProcessing Data

The most important part of machine learning is preparing the data before creating a model and training. If your data isn't in the correct format, the models won't work and if you have too much data, you run the risk of overtraining your model. Overtraining can lead to your model 'memorizing' the data as opposed to training to the level where your model will accurately predict data.

In order to clean up the data, I dropped features (columns) that correlate with other features. This is done to make sure overtraining doesn't occur. Rows with NA values were also dropped. 
