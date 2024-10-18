---
layout: post
title: Numerical Analysis - Data Activity 9
subtitle: Unit 11 - Data Activity 9
categories: Rstudio
tags: [Data Activity 9]
---
# Data Activity 9

Using the Health_Data, please perform the following functions in R:

Perform simple linear regression analysis to find the population regression equation to predict the diastolic BP by systolic BP.
Interpret the findings of regression analysis at 5% level of significance.

Solution

The data is downloaded from https://www.my-course.co.uk/pluginfile.php/1201624/mod_page/content/5/Health%20Data.sav

# mean, median and mode of 'age' variable

> # Load required packages
install.packages("haven")
library(haven)

> # Load the dataset into R
health_data <- read_sav("/Users/murthykanuri/Downloads/Health_Data.sav")
> # Check the variable names
names(health_data)

> # Perform linear regression
model <- lm(dbp ~ sbp, data = health_data)
<img width="653" alt="Screenshot 2024-10-18 at 21 34 29" src="https://github.com/user-attachments/assets/2e7f04be-c4a1-4158-bff8-7f186662ca98">


> # # Scatter plot with regression line
ggplot(health_data, aes(x = sbp, y = dbp)) +
  geom_point() +
  geom_smooth(method = "lm", col = "red") +
  labs(title = "Regression of Diastolic BP on Systolic BP",
       x = "Systolic Blood Pressure",
       y = "Diastolic Blood Pressure") +
  theme_minimal()

![Rplot29](https://github.com/user-attachments/assets/394ec69f-7e39-4c41-9b81-a249b75ef5f4)




