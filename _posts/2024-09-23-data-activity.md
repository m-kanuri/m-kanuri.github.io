---
layout: post
title: Numerical Analysis - Data Activity 6
subtitle: Unit 8 - Data Activity 6
categories: Rstudio
tags: [Data Activity 6]
---
# Data Activity 6

Using the Health_Data, please perform the following functions in R:

Find out the mean, median and mode of ‘age’ variable.

Find out whether median diastolic blood pressure is same among diabetic and non-diabetic participants.

Find out whether systolic BP is different across occupational group.

Solution

The data is downloaded from https://www.my-course.co.uk/pluginfile.php/1201624/mod_page/content/5/Health%20Data.sav

# mean, median and mode of 'age' variable

# Load required packages
install.packages("haven")
library(haven)

# Load the dataset into R
health_data <- read_sav("/Users/murthykanuri/Downloads/Health_Data.sav")

# Calculate mean and median of 'age' variable
mean_age <- mean(health_data$age, na.rm = TRUE)
median_age <- median(health_data$age, na.rm = TRUE)

# Function to calculate mode
get_mode <- function(v) {
  uniq_v <- unique(v)
  uniq_v[which.max(tabulate(match(v, uniq_v)))]
}

mode_age <- get_mode(health_data$age)

# Print results
mean_age
median_age
mode_age

> # Print results
> mean_age
[1] 26.51429
> median_age
[1] 27
> mode_age
[1] 26

# Five-figure summary of income variable and present it using a Boxplot.

summary(Health_Data$income)
---Console displays---
> summary(Health_Data$income)
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
  52933   68636   86560   85194   99696  117210

![Rplot07](https://github.com/user-attachments/assets/e1c997d1-1b69-4c1e-97e0-08906f7e7ff4)


# Suitable hypothesis test to see if there is any association between systolic blood pressure and presence and absence of peptic ulcer.



