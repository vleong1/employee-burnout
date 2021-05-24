# Modeling Employee Burnout

### OVERVIEW

### Table of Contents:
- Executive Summary
- Problem Statement
- Data Sources
- Data Dictionary
- Conclusion

### Executive Summary
Employee burnout rate can affect the productivity of an organization. Ever since the COVID-19 pandemic, employees were forced the work from home, which may often benefit or curtain employee productivity.


### Problem Statement

Using supervised learning and regression analysis, can we predict employee burnout rate? What features are most important when predicting the burnout rate?

### Data Sources
- [Employee Burnout - Kaggle Dataset](https://www.kaggle.com/blurredmachine/are-your-employees-burning-out?select=train.csv)

### Data Dictionary
|Feature|Data Type|Description|
|---|---|---|
|**Employee ID**|*object*|The unique ID allocated for each employee (example: fffe390032003000)| 
|**Date of Joining**|*object*|The date-time when the employee has joined the organization (example: 2008-12-30)|
|**Gender**|*object*|The gender of the employee (Male/Female)|
|**Company Type**|*object*|The type of company where the employee is working (Service/Product)|
|**WFH Setup Available**|*object*|Is the work from home facility available for the employee (Yes/No)|
|**Designation**|*float*|The designation of the employee of work in the organization. (In the range of [0.0, 5.0] bigger is higher designation.)|
|**Resource Allocation**|*float*|The amount of resource allocated to the employee to work, ie. number of working hours. (In the range of [1.0, 10.0] (higher means more resource))|
|**Mental Fatigue Score**|*float*|The level of fatigue mentally the employee is facing. (In the range of [0.0, 10.0] where 0.0 means no fatigue and 10.0 means completely fatigue)|
|**Burn Rate**|*float*|The value we need to predict for each employee telling the rate of Bur out while working. (In the range of [0.0, 1.0] where the higher the value is more is the burn out)|

### Conclusion
When looking at several data visualizations, Males have a higher average burnout rate than Females. This may be due to Males holding a higher average Designation than Females, thus having greater responsibility and stress in a work place. Additionally, 'Resource Allocation' and 'Designation' were positively correlated with burnout rate. 

The best performing model was **Hist Gradient Booster**. This model model was able to explain 93.05% of the variation in the data, based on the features in the dataset. When comparing against the **null baseline RMSE**, on average, the model was 0.053 units away from the actual Burn Rate. Compared to the Baseline model (0.198), the Hist Gradient Booster model performed significantly better (0.053). Based on permutation feature importance, 'Mental Fatigue Score' was the most important feature of predicting employee burnout rate compared to the other features. This makes sense, as mental health often relates to behavior and everyday performance.