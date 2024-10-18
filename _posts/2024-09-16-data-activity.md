---
layout: post
title: Numerical Analysis - Data Activity 5
subtitle: Unit 7 - Data Activity 5
categories: Rstudio
tags: [Data Activity 5]
---
# Data Activity 5

Using the Health_Data, please perform the following functions in R:

Find out mean, median and mode of variables sbp, dbp and income.

Find out the five-figure summary of income variable and present it using a Boxplot.

Run a suitable hypothesis test to see if there is any association between systolic blood pressure and the presence and absence of peptic ulcer.

Solution

The data is downloaded from https://www.my-course.co.uk/pluginfile.php/1201624/mod_page/content/5/Health%20Data.sav

Loaded the data to R Studio and check the head and tail data

<img width="734" alt="Screenshot 2024-10-04 at 12 20 53" src="https://github.com/user-attachments/assets/08c63d33-7820-49cd-96b5-32e321c747f5">

# mean, median and mode of variables sbp, dbp and income.

<img width="737" alt="Screenshot 2024-10-04 at 13 26 22" src="https://github.com/user-attachments/assets/6feb1d1c-3ab8-4a66-8730-fa26dc911490">


# Five-figure summary of income variable and present it using a Boxplot.

summary(Health_Data$income)
---Console displays---
> summary(Health_Data$income)
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  52933   68636   86560   85194   99696  117210

![Rplot07](https://github.com/user-attachments/assets/e1c997d1-1b69-4c1e-97e0-08906f7e7ff4)


# Suitable hypothesis test to see if there is any association between systolic blood pressure and presence and absence of peptic ulcer.

<img width="656" alt="Screenshot 2024-10-18 at 21 58 45" src="https://github.com/user-attachments/assets/214d4b62-d15b-46c7-b8e6-12c8a98d4d58">

Summary
- t-value: 1.2142
- Degrees of freedom (df): 57.562
- p-value: 0.2296 > 0.05 there is no statistically significant difference between the systolic blood pressure means of those with and without peptic ulcers
- 95% Confidence Interval: (-2.8894, 11.7957) suggests that the true difference in means lies somewhere within this range
- Mean of group 1 (with peptic ulcer): 131.3171
- Mean of group 2 (without peptic ulcer): 126.8639
  
In conclusion, based on this analysis, there is no sufficient evidence to reject the null hypothesis that the systolic blood pressure means of individuals with and without peptic ulcers are equal. Therefore, we conclude that there is no significant association between systolic blood pressure and the presence or absence of peptic ulcers.
