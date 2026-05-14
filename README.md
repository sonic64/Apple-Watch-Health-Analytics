# Apple Watch Health Analytics

### *Analyzing health and activity trends from a simulated Apple Watch study.*

![Banner.png](./Images/Banner.png)

### Introduction

The purpose of this study is to use the following two datasets to generate insights on a simulated experimental study. Participants were asked to wear an Apple Watch and record several aspects of their activity and health at three different timepoints. Some aspects of the participants changed over the course of the trial, e.g. smoking status. These aspects were recorded in the first dataset, [**health_irreg_rhythm**](Data/health_irreg_rhythm.xlsx).

Participants were also organized into cohorts: groups of individuals to help facilitate the study. Each cohort’s average temperature was aggregated for each month of the study and is stored in a second dataset, [**health_cohort_monthly**](Data/health_cohort_monthly.xlsx).

The detailed schemas of the two tables are as follows:

**health_irreg_rhythm**
- `id`: A unique identifier for the participant
- `date`: Date participant recorded their data
- `smoker`: "yes" if the person smokes, "no" if they don't
- `rings_closed`: Median number of rings closed per day
- `watch_type`: The material type for the Apple Watch
- `diff_exer_types`: Median of different types of exercise types per week
- `max_hr`: Maximum heart rate recorded during the week
- `irreg_rhythm`: "1" if the person exhibited irregular heart rhythm; "0" if they did not.
- `cohort`: The group of the participant in the study

**health_cohort_monthly**
- `cohort`: The group of the participant in the study
- `month`: Month of the study
- `mean_temp`: The average temperature of the cohort during the specified month

The interactive Tableau dashboard shown below provides a comprehensive look at health analytics for this simulated experimental study over a three-month trial period from January to March 2022. While specific cohort treatments and detailed demographic information are not available, the dashboard visualizes key longitudinal trends and correlations across multiple metrics.

[![Tableau Dashboard](./Images/Dashboard.png)](https://public.tableau.com/views/Apple-Watch-Health-Analytics/Dashboard2?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

Key features of the analysis include:

- **Weekly Cohort Trends**: The main line chart tracks the percent difference in average health metrics, such as "ring closure," across five different cohorts over the course of the trial.

- **Smoking Status Dynamics**: A dedicated bar chart reveals participant behavior changes, showing that while 59% of participants maintained their smoking status, 26% quit and 15% started smoking during the study.

- **Body Temperature Analysis**: The heatmap investigates potential relationships between average body temperature (ranging from 98.00°F to 103.00°F), smoking status changes, and Apple Watch hardware types, such as Aluminum, Ceramic, Steel, and Titanium.

- **Interactive Exploration**: Users can filter the data by cohort number and toggle between different health metrics to perform their own self-guided exploration of the dataset.