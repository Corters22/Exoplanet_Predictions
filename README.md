<h1 align='center'>Introduction to Machine Learning</h1>
<h2 align='center'>Exoplanet Classification</h2>

<img align='center' src='Images/exoplanets.jpg'>

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created multiple machine learning models capable of classifying candidate exoplanets from the raw dataset.

## Data

The full dataset can be found [here](https://www.kaggle.com/nasa/kepler-exoplanet-search-results) through Kaggle. The data can be difficult to understand so I'm including a reference to the columns, https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html. 

### Pre-Processing Data

The most important part of machine learning is preparing the data before creating a model and training. If your data isn't in the correct format, the models won't work and if you have too much data, you run the risk of overtraining your model. Overtraining can lead to your model 'memorizing' the data as opposed to training to the level where your model will accurately predict data.

In order to clean up the data, I dropped features (columns) that correlate with other features. This is done to make sure overtraining doesn't occur. Rows with NA values were also dropped. The features are then scaled and encoded.

## Models

1. Linear Regression - [model_1_LR.ipynb](model_1_LR.ipynb)
      - using sklearn linear model
          R2 score = 0.6393
      - using grid search to hyper tune the model
          best score = 0.8276
          elapsed time to run parameters = 3.1 minutes
      - Conclusions: Using simple linear regression does not have a very good R2 score until we add in the grid search to test a lot of different parameters. The time to run the grid search model was extensive. If the data was any larger, it would have taken too much time to run. Predicted test data correctly.
2. Random Forest - [model_2_RF.ipynb](model_2_RF.ipynb)
      - using sklearn random forest classifier
          R2 score = 1.000
      - Conclusions: This model has a very good R2 score and ran very quickly. It also predicted the test data correctly.
3. Neural Network - [model_3_NN.ipynb](model_3_NN.ipynb)
      - using tensor flow and keras sequential and dense to build model layers
          model accuracy = 0.8473
      - Conclusions: This model also predicted correct classifications and ran very quickly. I also ran a deep network, but didn't get a better accuracy school and it took much longer.

## Final Conclusions

