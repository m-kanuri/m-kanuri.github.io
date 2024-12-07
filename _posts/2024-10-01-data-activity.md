---
layout: post
title: Numerical Analysis - Data Activity 8
subtitle: Unit 10 - Data Activity 8
categories: Module2
tags: [Data Activity 8]
---
# Data Activity 8

Using the Health_Data, please perform the following functions in R:

Find out correlation between systolic and diastolic BP.
Produce a scatter plot between systolic and diastolic BP.

Solution

The data is downloaded from https://www.my-course.co.uk/pluginfile.php/1201624/mod_page/content/5/Health%20Data.sav

# mean, median and mode of 'age' variable

> # Load required packages
install.packages("haven")
library(haven)
install.packages("ggplot2")
library(ggplot2)

> # Load the dataset into R
health_data <- read_sav("/Users/murthykanuri/Downloads/Health_Data.sav")
> # Check the variable names
names(health_data)


> # Calculate correlation
correlation <- cor(health_data$sbp, health_data$dbp, use = "complete.obs")
print(correlation)
[1] 0.846808

> # Create a scatter plot

![Rplot28](https://github.com/user-attachments/assets/8f21674c-9209-440e-837e-1739ab457288)


