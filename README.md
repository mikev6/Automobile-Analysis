# Automobile-Analysis

## Overview (10-15)

I'm analyzing a set of data from 1985 that includes City-mpg for various cars. I'm building a multiple linear regression model on this data.
I'm doing this in part because I found a good data set, and I'm also interested in cars. I'm interested in what the strongest influences are  


## Goals
The goal of this is to estimate a car's city miles per gallon based on other data that it's the data set. There's all kinds of interesting data, such as the cars' dimensions, fuel type, fuel deliverry system, engine size and number of cylinders. This could be useful for estimating a car's city miles per gallon if it hasn't been measured, or validating a quoted city mpg balue

## Motivation & Background
I find data like this interesting, as there are countless factors that car manufacturer's weigh when designing a car, many of which affect the fuel efficiency. Fuel efficiency isn't the only outcome they're optimizing for, but quantifying how some of the design decisions affect the fuel economy are helpful in understanding tradeoffs and other optimization features
I used a few sites as a guide, including:
  https://www.kaggle.com/spscientist/students-performance-in-exams
  https://www.kaggle.com/ashydv/sales-prediction-simple-linear-regression

I got the data from here:
https://archive.ics.uci.edu/ml/datasets/Automobile

## Data
There are 26 attributes and 206 entries. There are some missing values, but they few and far between. In one case, (bore and stroke), I removed the features, as engine size (displacement) was also given, so it was somewhat duplicative. In another, I removed a row as it had a missing piece of data that was interfering with the modeling tools.

The data was orignially put together for insurance purposes, and it also quoted the price of the cars. I removed insurance-related data  (symboling, normalized-losses, price), as it was not relevant to the analysis, and this data would likely not be known at the juncture in which this model was used (pre-production, for example)

I downloaded this data from the website listed above and imported the csv with a Jupyer notebook.
## Table of Content (5--)
The code can be found here:
https://github.com/mikev6/mv6-Automobile-Analysis/tree/main/code
The technical report is in the same Jupyter notebook, usin markdown.

A copy of the input data is saved off here:
https://github.com/mikev6/mv6-Automobile-Analysis/tree/main/data

## Software Requirements - Packages used (5--)
The software packages used are:
  pandas
  numpy
  from sklearn.model_selection:
    train_test_split
    StandardScaler
    LinearRegression
  from sklearn.metrics
    mean_squared_error
    r2_score
  statsmodels.api
