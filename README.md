# Module 20 Challenge
### Miguel Fidelino

## Overview of the Analysis
create a binary classifier that is capable of predicting whether applicants will be successful if funded by our company.


### Data Preprocessing
1. What variable(s) are considered the target(s) for your model?

    We use the IS_SUCCESSFUL variables as the target column. 

2. What variable(s) are considered to be the features for your model?

    The columns 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT', "STATUS","ASK_AMT", and "SPECIAL_CONSIDERATIONS" as our features.

3. What variable(s) are neither targets nor features, and should be removed from the input data?

    Columns 'EIN' and 'NAME' will be removed as they are neither.

### Compiling, Training, and Evaluating the Model
4. How many neurons, layers, and activation functions did you select for your neural network model, and why?

    I arbitrarily chose 10 neurons and slowly reduced it to resemble a funnel. I chose 3 layers deep due to 4 layers stagnating at 73.5%.

5. Were you able to achieve the target model performance?

    Unfortunately, we were not able to achieve 75%. My closest estimated was around 74% at one point.

6. What steps did you take to try and increase model performance?

    dropped 'STATUS' as the majority are "1"
    dropped 'ASK_AMT' as the majority are within 5000
    dropped 'SPECIAL_CONSIDERATIONS' as only 27 are 'yes' out of 342799 rows.

    I lowered the amount of layers and neurons to increase the speed of the load.


## Summary

I would not recommend my model as it does not achieve the required 75% rate. I would try to use unsupervised learning to drill down to what types of columns to keep or discard. This way, the neural network would run faster, and perhaps achieve a better accuracy score.
