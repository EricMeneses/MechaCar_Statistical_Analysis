# MechaCar_Statistical_Analysis

## Project Overview
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.


## Linear Regression to Predict MPG

![](Resources/Photos/Deliverable1.png)

In the Above output, we are able to tell that:
- Vehicle length and vehicle ground clearance provide non-random amounts of variance to the model statistically. Both have an impact on miles per gallon (mpg) for the MachaCar prototype. Alternatively, the other three (vehicle weight, spoiler angle, and AWD-All Wheel Drive) have p-values that distribute a random amount of vairance within the dataset.
- The p-value we are working with is smaller than the assumed significance level of 0.05%. What this tells us is that we can reject the null hypothesis because we have enough evidence to do so, confirming that the slope is not zero.
- Looking at the r-squared value of this linear model, we can determine that 0.7149 (approximately 72%) of the mpg predictions will be determined by this model. Based on this, we can confirm that this model does predict mpg of MechaCar pprototypes effectively.

## Summary Statistics on Suspension Coils

![](Resources/Photos/Deliverable2_total_summary.png)
![](Resources/Photos/Deliverable2_lot_summary.png)

When we look at all of the manufacturing lots and whetherthe design fits the specifications for MechaCar suspension coils, we notice that the variance of the coils is approximately 62.3 PSI, which it well within the 100 PSI variance requirement. Because of this, the current manufacturing data does meet the design specification of 100 pounds per square inch for all manufacturing lots in total.

When we break the lots down to their prospective lots (1, 2 & 3) we notice that lot 1 (0.98 variance) and lot 2 (7.47 variance) are most certainly within the 100 PSI vairance requirement. Lot 3, however, has a much higher variance (170.29 variance). With this variance so high, it is causing a disproportionate variance at the full lot reading. In other words, this means that the current manufacturing data does not meet the design specification of 100 pounds per square inch for each lot individually.

## T-Tests on Suspension Coils
The next step in our process is to administer a t-test based on the suspension coil data so that we can determine if there is a statistical difference between the mean of our dataset and a potential population dataset. The population mean of 1500 is what we used in the following analysis:

### Sample t-test
![](Resources/Photos/Deliverable3_sampletest.png)
- Above is the summary of the t-test results from all manufacturing lots.

In the above sample test, we find that the true mean of the sample is actually 1498.78. We cannot reject the null hypothesis because there is not enough evidence to support the decision to do so. Combined, all three manufacturing lots are statistically comparable to the presumed population mean of 1500.

### 1. Sample t-test: lot1
![](Resources/Photos/Deliverable3_sampletest_Lot1.png)

1. Lot 1 has an actual sample mean of 1500, which is spot on with the average of the 3 lots. Because lot 1 has a p-value of 1, we do not want to reject the null hypothesis because there would be no statistical difference between the sample and population mean.

### 2. Sample t-test: lot2
![](Resources/Photos/Deliverable3_sampletest_Lot2.png)

2. Similar to lot 1, lot 2 had a sample mean of 1500.02. It's p-value was 0.61. Because of these details, the null hypothesis shouuld not be rejected.

### 3. Sample t-test: lot3
![](Resources/Photos/Deliverable3_sampletest_Lot3.png)

3. Lot 3, is a bit different compared to its counter lots. The sample mean here is 1496.14 but the p-value is at a 0.04, which is below the common significance level (0.05). Because of this, we need to reject the null hypothesis because the sample mean and the presumed population mean are not statistically different.

## Study Design: MechaCar vs Competition

### Metrics to Test

Collect data over time of similar models from competitive manufacturers to receive the following metrics:
1. Cost - Dependent Variable
2. Horse Power - Independent Variable
3. Maintenance - Independent Variable
4. Safety Rating - Independent Variable

### Null or Alternative Hypothesis
- Null Hypothesis: MechaCar accurately priced according to the performance of key factors for the competitive market
- Alternative Hypothesis: MechaCar inaccurately priced according to the performance of key factors for the competitive market

### What Statistical Test to use to Test the Hypothesis
By using a multiple linear regression, we can determine the factors that have the more favorable correlation and/or predictability with the listed selling price to see which combination of features hold the greatest impact.

