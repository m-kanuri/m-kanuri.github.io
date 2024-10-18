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

> # Load required packages
install.packages("haven")
library(haven)

> # Load the dataset into R
health_data <- read_sav("/Users/murthykanuri/Downloads/Health_Data.sav")

> # Calculate mean and median of 'age' variable
mean_age <- mean(health_data$age, na.rm = TRUE)
median_age <- median(health_data$age, na.rm = TRUE)

> # Function to calculate mode
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

# median diastolic blood pressure is same among diabetic and non-diabetic participants.

> # Group by occupation and calculate summary statistics
summary_systolic_bp <- health_data %>%
  group_by(occupation) %>%
  summarise(mean_bp = mean(sbp, na.rm = TRUE), 
            median_bp = median(sbp, na.rm = TRUE))

> # Print results
summary_systolic_bp

> summary_systolic_bp
# A tibble: 4 × 3
  occupation      mean_bp median_bp
  <dbl+lbl>         <dbl>     <dbl>
1 1 [GOVT JOB]       129.      126.
2 2 [PRIVATE JOB]    126.      120 
3 3 [BUSINESS]       128.      122 
4 4 [OTHERS]         127.      123 

# Suitable hypothesis test to see if there is any association between systolic blood pressure and presence and absence of peptic ulcer.**

# Perform ANOVA test to check for differences in systolic blood pressure across occupation groups
anova_result <- aov(sbp~ occupation, data = health_data)
summary(anova_result)
> anova_result <- aov(sbp~ occupation, data = health_data)
> summary(anova_result)
             Df Sum Sq Mean Sq F value Pr(>F)
occupation    1    101   101.4   0.251  0.617
Residuals   208  83984   403.8     

