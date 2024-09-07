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

The data is downloaded from [ Crime Survey for England and Wales, 2013-2014](https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=8011#!/access-data)

NumPy is the numerical library in Python. Used Google Colab to work on this activity.

1. Loading Data: We loaded the SPSS file csew1314teachingopen.sav into a pandas DataFrame.
2. Filtering Data: We filtered the dataset to include only individuals aged 75+ who were victims of crime in the last 12 months.
3. Saving Data: We saved the filtered data as a new SPSS file named [crime_75victim.sav](https://github.com/m-kanuri/m-kanuri.github.io/blob/ad43e2af50b0b4df599c14244b12c7c4291f81fa/crime_75victim.sav)

Screenshot from Google Colab

![Screenshot 2024-08-24 at 03 12 13](https://github.com/user-attachments/assets/699bbcd2-004a-46c3-98cc-fbc6886f1cbe)

  


