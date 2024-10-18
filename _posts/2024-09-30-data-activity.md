---
layout: post
title: Numerical Analysis - Data Activity 7
subtitle: Unit 9 - Data Activity 7
categories: Rstudio
tags: [Data Activity 7]
---
# Data Activity7

Using the Crime Survey for England and Wales, 2013-2014: Unrestricted Access Teaching Dataset, perform the following activities:

Create a crosstab to assess how individuals’ experience of any crime in the previous 12 months bcsvictim vary by age group agegrp7. Create the crosstab with bcsvictim in the rows and agegrp7 in the columns, and produce row percentages, rounded to 2 decimal places.

Looking at the crosstab you have produced, which age groups were the most likely, and least likely, to be victims of crime?

Solution

The data is downloaded from [https://www.my-course.co.uk/pluginfile.php/1201624/mod_page/content/5/Health%20Data.sav](https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=8011#!/access-data)

# Install and load the necessary packages
install.packages("haven")
library(haven)

install.packages("gmodels")
library(gmodels)

# Load your SPSS file
health_data <- read_sav("/Users/murthykanuri/Downloads/csew1314teachingopen.sav")

# Create the crosstab with row percentages

<img width="908" alt="Screenshot 2024-10-18 at 21 13 59" src="https://github.com/user-attachments/assets/734ca695-1d85-4079-beb2-3e8724ae92b1">

