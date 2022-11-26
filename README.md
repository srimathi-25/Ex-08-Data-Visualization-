# Ex-07-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE

import pandas as pd

import seaborn as sns

df=pd.read_csv("/content/SuperStore (1).csv")

df.info()

df.isnull().sum()

![ds 1](https://user-images.githubusercontent.com/114581999/204091750-8d2dec9b-cc98-4fe2-a1e3-330559bd50fc.jpeg)

![ds 2](https://user-images.githubusercontent.com/114581999/204091772-b7450b5f-cbbc-472d-bf60-8e1217cd6258.png)

import matplotlib.pyplot as plt

import numpy as np

sns.distplot(df['Sales'])

plt.axvline(x=np.mean(df['Sales']), c='red', ls='--', label='mean')

plt.axvline(x=np.percentile(df['Sales'],25),c='green', ls='--', label = '25th percentile:Q1')

plt.axvline(x=np.percentile(df['Sales'],75),c='orange', ls='--',label = '75th percentile:Q3' )

plt.legend()

![ds 3](https://user-images.githubusercontent.com/114581999/204091927-8450f7bc-eb40-4e05-96fd-0ba8b41c17e6.png)



sns.boxplot(x=df['Segment'], y=df['Sales'])

![ds 4](https://user-images.githubusercontent.com/114581999/204091895-30cdd957-9b99-494f-ae21-b048a558d4d4.png)

sns.scatterplot(x=df['City'], y=df['Sales'])

![image](https://user-images.githubusercontent.com/114581999/204091971-63154ccf-de44-49d0-b64f-76fd09f3b476.png)

sns.boxplot(df['Region'], df['Sales'])

![image](https://user-images.githubusercontent.com/114581999/204092036-a7906fe3-cd5e-44f9-98ed-a5163078ff6a.png)







