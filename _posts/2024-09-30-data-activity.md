
---
layout: post
title: Numerical Analysis - Data Activity 7
subtitle: Unit 9 - Data Activity 7
categories: Rstudio
tags: [Data Activity 7]
---
# Data Activity 

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
CrossTable(health_data$bcsvictim, health_data$agegrp7, prop.r = TRUE, digits = 2, format = "SPSS")
> CrossTable(health_data$bcsvictim, health_data$agegrp7, prop.r = TRUE, digits = 2, format = "SPSS")

   Cell Contents
|-------------------------|
|                   Count |
| Chi-square contribution |
|             Row Percent |
|          Column Percent |
|           Total Percent |
|-------------------------|

Total Observations in Table:  8843 

                      | health_data$agegrp7 
health_data$bcsvictim |        1  |        2  |        3  |        4  |        5  |        6  |        7  | Row Total | 
----------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
                    0 |      523  |     1049  |     1194  |     1242  |     1226  |     1194  |     1032  |     7460  | 
                      |     5.21  |     8.28  |     0.42  |     1.02  |     0.38  |     6.46  |    11.86  |           | 
                      |     7.01% |    14.06% |    16.01% |    16.65% |    16.43% |    16.01% |    13.83% |    84.36% | 
                      |    76.35% |    77.19% |    82.80% |    81.98% |    85.85% |    90.80% |    93.90% |           | 
                      |     5.91% |    11.86% |    13.50% |    14.05% |    13.86% |    13.50% |    11.67% |           | 
----------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
                    1 |      162  |      310  |      248  |      273  |      202  |      121  |       67  |     1383  | 
                      |    28.10  |    44.69  |     2.24  |     5.49  |     2.04  |    34.85  |    64.00  |           | 
                      |    11.71% |    22.42% |    17.93% |    19.74% |    14.61% |     8.75% |     4.84% |    15.64% | 
                      |    23.65% |    22.81% |    17.20% |    18.02% |    14.15% |     9.20% |     6.10% |           | 
                      |     1.83% |     3.51% |     2.80% |     3.09% |     2.28% |     1.37% |     0.76% |           | 
----------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
         Column Total |      685  |     1359  |     1442  |     1515  |     1428  |     1315  |     1099  |     8843  | 
                      |     7.75% |    15.37% |    16.31% |    17.13% |    16.15% |    14.87% |    12.43% |           | 
----------------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
