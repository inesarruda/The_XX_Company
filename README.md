## **The XX Company**
By: Maria Inês Arruda Gonçalves

In order to preserve the reak company name, we'll call it: The XX Company

This notebook is a part of the technical test for the Junior Data Analyst Role.

The aim of this notebook is to make an Exploratory Data Analysis (EDA) of the metrics provided by The XX Company. Here I have to analyze the data available and write my insights about the behavior of:
- Volume (impressions, clicks, overall website traffic…)
- CPC: Cost per click
- Total number of conversions
- XX’s share of the website
- Overall traffic of the advertiser

## There are also some questions that need to be answered:

1) Is it possible to see any kind of seasonality? Did the values increase or decrease? By how much?

2) Are XX’s results and delivery stable?

## The original data came with missing values of:

- CTR: click-through rate
- CPC: cost per click
- CR: conversion rate
- ROAS: return on advertising spend
- Share: percentage of how many conversions are from XX

## To fill out these columns I had to perform some calculations on the excel file:

- CTR: click-through rate: Is the proportion of people who clicked by the people that saw a propaganda.

CTR = $\frac{\text{Clicks}}{\text{Imps}}$

- CPC: cost per click: Is the cost of each click\

CPC = $\frac{\text{Cost (BRL)}}{\text{Clicks}}$

- CR: conversion rate: Is the proportion of conversions from XX by the amount of Clicks

CR = $\frac{\text{XX}{\space}{\space} \text{Conversions}}{\text{Clicks}}$

- ROAS: Return on the amount spent on advertising

ROAS = $\frac{\text{XX}{\space}{\space} \text{Conversions}{\space}{\space} \text{value (BRL)}}{\text{Cost (BRL)}}$

- Share: percentage of how many conversions are from XX

Share = $\frac{\text{XX Conversions}}{\text{Total number of conversions}}$

## It's always important to verify the type of the columns to see if they are in the proper format

<img width="300" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/ee88b140-0b05-49f7-8c2c-1df1c013e3ab">


We can see date is not in the appropriate format and needs to be transformed.


## Exploratory Data Analysis (EDA)

### One of the best ways to analyze the correlations between features is through a correlation heatmap:
<img width="650" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/dcbd393f-fb0c-4f04-815a-2b539c7c04eb">

### One of the first analyses we can do is identify the behavior of the metrics depending on the day of the week

### To do this, we can create a new column on the dataframe called 'Day of the Week'

### To identify the day of the week through the date, we can use the command 'dt.dayofweek'. Then, we can make a dictionary to write the day of the week on the column:

<img width="400" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/40fbb275-0541-4568-be71-a8fe26793e5d">

Then we can transform some analysis into a barplot 

<img width="500" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/0cace443-9201-4f09-9556-aa84d705d303">

## On the heatmap we saw a very strong correlation between Impressions and Clicks. We can also plot them through the whole period, to see how they look. In other words, the impressions and clicks throughout the days of November.

<img width="500" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/3c318e19-00b2-40d0-9112-716ebadd16ce">

## We can also see a very interesting pattern by the end of november. Let's analyze this carefully!

### From November 22nd to November 29th, we have a great peak!
<img width="500" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/b7682bed-5dee-4dfc-8ae3-4b19b750f78b">

### This most likely happened because of ***BLACK FRIDAY***, on November 23rd, 2018.

### The Monday after Black Friday, we also have Cyber Monday.

### Let's remake this same plot, but adding a vertical line to **'Black Friday'** and **'Cyber Monday'**.

<img width="500" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/36b189fb-671d-4389-bead-a55efcec8ab1">

### We can notice that Black Friday had a great impact!

## Another great metric is to analyze the importance of hiring the The XX Company.

### One way to see this is to analyze the XX Conversions value compared to the costs. Let's do it!

<img width="700" alt="image" src="https://github.com/inesarruda/The_XX_Company/assets/112672449/26f9d6c7-e9d3-41fd-a7e0-ecafcda51c29">

### We can see that Monday and Sunday are the days where we have a greater dispersion, and they’re also the worst days when it comes to clicks and impressions.

### An interesting point is that the outlier on the ROAS doesn't happened on the Black Friday, it happened on November 30th.

### Looking into the data, this might have happened because on Black Friday it's when we spend the most with advertisements. Even though we had a great earning, the biggest ROAS actually happened on November 30th. That was the day where we got the higher return compared to the amount spent.


## Conclusions

### After the analysis above we're now ready to answer the questions:

**1) Is it possible to see any kind of seasonality? Did the values increase or decrease? By how much?**

**2)Are XX’s results and delivery stable?**

## Answers:

### **1)** We can notice some kind of seasonality when it comes  to impressions and clicks. Through the plots above we can identify that Friday, Saturday and Thursday are the days when there are most impressions and clicks. This may be due to getting closer to the weekend and also because we had a Black Friday event this month.

### **2)** When it comes to the results and delivery of XX we can see very clearly through the last graph that the gains promoted due to XX far exceed the costs of propaganda and thus generate 

##
The full analyses can be seen in the jupyter notebook in this repository: XXCompany_Technical_Test.ipynb











