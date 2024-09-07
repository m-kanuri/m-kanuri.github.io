---
layout: post
title: Numerical Analysis - Data Activity 4
subtitle: Unit 5 - Data Activity 4
categories: Rstudio
tags: [Data Activity 4]
---
# Data Activity 4

Using the Crime Survey for England and Wales, 2013-2014: Unrestricted Access Teaching Dataset (see Unit 1), perform the following activities:

Create a boxplot for the variable 'antisocx'

Follow the instructions below to create a boxplot for assessing levels of anti-social behaviour that the survey respondents experience in their neighbourhood (use the variable: antisocx).

If you’re using ‘graphics’: Add “Levels of anti-social behaviour in neighbourhood ‘antisocx’” as a title and colour the plot in purple and colour the outliers in blue.

If you’re using ‘ggplot2’: Add “Levels of anti-social behaviour in neighbourhood ‘antisocx’ as a title, colour the plot in yellow and colour the outliers in red.

Create a bar plot using either the barplot() function or the ggplot() function to assess whether or not the survey respondents experienced crime in the 12 months prior to the survey (use the variable 'bcsvictim'). Give the graph a suitable title and choose a colour for the bars (e.g., orange).

Solution

The data is downloaded from [ Crime Survey for England and Wales, 2013-2014](https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=8011#!/access-data)

Loaded the data to R Studio 
<img width="807" alt="Screenshot 2024-09-07 at 05 51 44" src="https://github.com/user-attachments/assets/36976f91-afe1-4740-971b-a41282a2d80d">

Using the ggplot and the following script was used in R Studio

# Create the boxplot using ggplot2

<img width="813" alt="Screenshot 2024-09-07 at 06 02 14" src="https://github.com/user-attachments/assets/ff0bc862-99e5-417e-aa1d-c3c2a50c08c5">

  ![Rplot](https://github.com/user-attachments/assets/52a1b634-0d8b-4ac7-8896-e52919680f92)

# Create a bar plot using ggplot2

<img width="801" alt="Screenshot 2024-09-07 at 06 02 48" src="https://github.com/user-attachments/assets/90ba307f-a216-4d20-ba46-aa177dc1186c">

  ![Rplot01](https://github.com/user-attachments/assets/6ecbdf2e-66aa-4d37-bac9-9788c9894f26)



