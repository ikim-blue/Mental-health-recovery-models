# Predicting Mental Health Recovery: A Mixed-Effects Modeling Approach

**[Read the full published analysis on Medium](https://ucladatares.medium.com/what-predicts-bouncing-back-from-mental-health-struggles-775586d166af)**

## Summary
This repository contains the code and methodology for analyzing longitudinal mental health recovery outcomes. Using data from the UK Household Longitudinal Study (UKHLS) spanning 2010 to 2024 (n > 13,000), this project utilizes mixed-effects modeling to account for hierarchical variance across time and demographic cohorts. The analysis identifies the primary physical and social factors that predict sustained mental health recovery (defined as a drop of at least 4 points on the GHQ-12 index). The findings from this analysis were published as a featured article on Medium by UCLA DataRes. 

## Methodology
Standard associational models fail to capture the inherent within-subject correlation present in longitudinal health surveys. To rigorously map this data-generating process across two-year intervals, this project implemented **Mixed-Effects Models** (Hierarchical Linear Modeling). 

* **Fixed Effects:** Sleep duration, physical activity intensity (walking vs. moderate/vigorous), dietary habits (fruit and vegetable intake), and social relationship metrics (support vs. strain from friends, family, and romantic partners).
* **Random Effects:** Random intercepts for individual subjects to account for baseline psychological variance and inherent demographic baseline differences (age, sex, education, and financial strain).

## Repository Structure
*(Note: Raw survey data from UKHLS is excluded to protect subject anonymity and comply with UK Data Service terms of use).*
* `MH_data_pipeline.ipynb` : Python notebook that standardizes inputs, handles missingness, and formats the longitudinal data into a tidy format.
* `MH_mixed_effects_modeling.Rmd` : R Markdown file containing the core model architecture (fitting the mixed-effects equations) and generating the model-related data visualizations used in the Medium publication.

## Coding Information
* **Languages:** Python, R
* **Key Libraries:** pandas, lme4, ggplot2
