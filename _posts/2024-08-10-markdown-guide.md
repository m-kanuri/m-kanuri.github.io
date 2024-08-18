---
layout: post
title: Numerical Analysis Data Activity 1.2
subtitle: Data Activity 1.2
categories: markdown
tags: [Data Activity 1.2]
---

Using the Crime Survey for England and Wales, 2013-2014: Unrestricted Access Teaching Dataset, assess the level of anti-social behaviour that the survey respondents experience in their neighbourhood by creating a summary statistic, using the ‘antisocx’ variable.

The ‘antisocx’ variable captures the level of anti-social behavior experienced by respondents.

Check the unique values and a summary of the antisocx variable

summary(data$antisocx)

unique(data$antisocx)

<img width="611" alt="Screenshot 2024-08-18 at 14 37 18" src="https://github.com/user-attachments/assets/f67f0408-4a1d-4479-bab3-fc3385352c30">


<img width="1512" alt="Screenshot 2024-08-18 at 14 42 18" src="https://github.com/user-attachments/assets/0a534864-63ed-42cf-833f-4870164f77d4">

The antisocx variable is likely numeric or ordinal (e.g., ratings from 1-5 or similar). You can create summary statistics using functions like mean(), median(), sd(), and summary()

<img width="1257" alt="Screenshot 2024-08-18 at 14 47 36" src="https://github.com/user-attachments/assets/a2ce2caf-ab0e-47b5-aba4-ef3c8ef31485">


