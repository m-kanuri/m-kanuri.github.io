---
layout: post
title: Numerical Analysis
subtitle: Unit 2 - Data Activity 2
categories: Python
tags: [Data Activity 2]
---

The data is downloaded from https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=8011#!/access-data

1) Explore whether survey respondents experienced any crime in the 12 months prior to the survey using the variable bcsvictim.

  The bcsvictim variable should indicate whether a respondent experienced crime in the 12 months before the survey.

  Using the command > unique(data$bcsvictim)

  <img width="1096" alt="Screenshot 2024-08-18 at 12 53 42" src="https://github.com/user-attachments/assets/6e819c7e-9eee-4ea3-ba7d-a085222866ec">

2) Create a frequency table to count if the survey respondents experienced any crime in the previous 12 months. Use the table() command.

  Using the commend > table(data$bcsvictim) 

  This will display the count of respondents based on their responses regarding whether they experienced any crime.

  <img width="1097" alt="Screenshot 2024-08-18 at 12 57 42" src="https://github.com/user-attachments/assets/9ac51f10-406a-4695-88e0-446d3936a9c2">

3) Assess the results and decide if you need to convert this variable into a factor variable. Use as_factor.

   The bcsvictim variable might need to be converted into a factor if it is not already. This is especially useful if the variable represents categorical data (e.g., "Yes", "No").

   If the variable is not already a factor, you can convert it using as_factor() from the haven package (or as.factor() from base R).

   After converting bcsvictim to a factor, recreate the frequency table to ensure the values are correctly labeled.

   <img width="1369" alt="Screenshot 2024-08-18 at 13 04 53" src="https://github.com/user-attachments/assets/ef29cac8-31be-416d-8da6-2b4093ea7b49">


  
