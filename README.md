# PwC--Retention-Analysis using powerBI and Python
## Introduction
In this analysis, I worked with a telecom dataset aimed at predicting customer churn. The objective was to clean the data, remove irrelevant or redundant columns, handle missing values, and determine the correlation between various service-related variables and customer churn. This process involved several key steps, from uploading the data to conducting a correlation analysis, which I'll outline below.
## Step 1: Uploading the Dataset
First, I uploaded the dataset into the Python environment using the Pandas library. Pandas is a powerful tool for data manipulation and analysis.

import pandas as pd
import numpy as np
df =pd.read_excel(r"C:\Users\USER\Desktop\yemmite\PwC Internship\PhoneNow.xlsx")
df.head() --> to show the first 5 rows of my dataset

## Step 2: Handling Missing Values
Handling missing values is crucial for ensuring the accuracy of our analysis. I began by checking for any null values in the dataset.

df.info() ---> To show information of my data if it has null values or not
df.dropna() ---? to drop null values in my data 

I found that some columns are not beeded for the analysis . These were handled as follows:

Dropping Columns: I dropped columns that are  irrelevant to the analysis to prevent redundancy
df.drop(['column_1', 'column_2', ....], axis=1, inplace=True)
