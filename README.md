# MechaCar_Statistical_Analysis
## Overview
The purpose of this project is to understand the statistics and hypothesis testing to analyze a series of datasets from the automotive industry.The analysis includes visualizations, statistical tests, and interpretation of the results. All statistical analysis and visualizations were written in the R programming language. The main objectives of this project is to
* Load, clean up, and reshape datasets using tidyverse in R.
* Visualize datasets with basic plots such as line, bar, and scatter plots using ggplot2.
* Generate and interpret more complex plots such as boxplots and heatmaps using ggplot2.
* Plot and identify distribution characteristics of a given dataset.
* Formulate null and alternative hypothesis tests for a given data problem.
* Implement and evaluate simple linear regression and multiple linear regression models for a given dataset.
* Implement and evaluate the one-sample t-Tests, two-sample t-Tests, and analysis of variance (ANOVA) models for a given dataset.
* Implement and evaluate a chi-squared test for a given dataset.
* Identify key characteristics of A/B and A/A testing.
* Determine the most appropriate statistical test for a given hypothesis and dataset.

## Results
### Linear Regression to Predict MPG
Mechacar dataset has been used to calculate the linear regression using R in R studio, 
![Linear_regression](https://user-images.githubusercontent.com/108298416/195654424-a02e18e6-8891-49bd-8dd8-161b7f400949.PNG)

![summary_linear_regression](https://user-images.githubusercontent.com/108298416/195654486-8c1e16a5-ca77-4369-8388-df6b375eb22b.PNG)

1. The variables/coefficients which provided a non-random amount of variance to the mpg values in the dataset are Vehicle Length and 
Ground clearance with a p-value of 2.60e-12 and 5.21e-08 respectively.
2. The slope of the linear model cannot be considered to be zero, as the p-value is 5.35e-11, which is way lower than the significance level of p-value = 0.05 and the slope coefficients of vehicle_length,ground_clearance and AWD are having non-zero values. Hence, we can reject the null hypothesis.
3. For the data what we have, the R-squared value is 0.7149, which shows the linear model does predict the mpg of MechaCar prototypes relatively effective. However, there are so many factors needs to be considered.

### Summary Statistics on Suspension Coils

![total_summary](https://user-images.githubusercontent.com/108298416/195660559-74f6134e-eb44-4c23-a25e-88ff189471aa.PNG)

![lot_summary](https://user-images.githubusercontent.com/108298416/195660677-e7449ef6-9abe-4bde-a5ba-5e013086143a.PNG)

The overall variance shown in the total summary is 62.29356 which is lesser than 100 psi and meets the design specifications for the MechaCar suspension coils, whereas, the variance for lot 3 is significantly higher, 170.286 psi and does not meet the design specifications

### T-Tests on Suspension Coils

![T_test_all_lots](https://user-images.githubusercontent.com/108298416/195662109-45f65ae1-8cc2-42cc-ae6e-8567f205f34d.PNG)

![T_test_lot1](https://user-images.githubusercontent.com/108298416/195662433-b3568747-bd51-4b7d-ae94-29e9e93f4d28.PNG)

![T_test_lot2](https://user-images.githubusercontent.com/108298416/195662461-0823b027-144e-4f97-8a6c-60aeb4aea1cf.PNG)

![T_test_lot3](https://user-images.githubusercontent.com/108298416/195662482-947c3d4e-9a31-43a7-88a4-3d3e91603a9b.PNG)

T-Test results for all lots shows that the sample mean is not statistically different from the population mean of 1500 PSI and the p-value is 1. The T-test for lot 1 and lot 2 are not statistically different from the population mean of 1500 PSI with the p-values of 1.568e-11 and  0.0005911 respectively. The results for the lot 3 is slightly statistically different from the population mean of 1500 PSI with the p-value of 0.1589

### Study Design: MechaCar vs Competition
Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?
What statistical test would you use to test the hypothesis? And why?
What data is needed to run the statistical test?

MechaCar performance against the competitiors can be analysed based on some metrics that would be of interest to a consumer for example, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
1. The metric which should be tested is horsepower, safety rating and highway fuel efficiency which would help customers in decision making.
2. The metric which is being tested in MechaCar should have statistically significant differences when compared to competitor's models. The null hypothesis would  be the metrics don't vary significantly from the competitor's metrics and the alternative hypothesis would be the metrics vary significantly when compared to the competitor's metrics. For example, if the metric highway fuel efficiency is tested, if the p-value is above the assumed significance level, we would state that there is not enough evidence to reject the null hypothesis. In null hypothesis the mean is equal to zero and in alternate hypothesis the mean is not zero.
3. The statistical test for testing highway fuel efficiency would be two sample T-tests.
4. In order to run the statistical tests for the metrics, we would need, fuel efficiency and horsepower from Mechcar and competitors.




