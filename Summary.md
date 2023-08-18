## Overview: 
This analysis will go over the successes and failures in tackling the challenges of this week's assignment.

## Data Preprocessing
* What variable(s) are the target(s) for your model?
    - The IS_SUCCESSFUL column acts as a target for the NN model.  
* What variable(s) are the features for your model?
    - Every variable that has an effect on target column; their idnividual weights would take more time to determine.
* What variable(s) should be removed from the input data because they are neither targets nor features
    - Identification columns (such as names), these variables have no effect on target and should be cleaned.

## Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - My final model had an input layer where unit = input_dim, a single hidden layer where unit = mean of input and output.
    - The input and hidden layer used ReLU, and the output used Sigmoid.
    - From what I understood the numberof neurons followed general rules, it also had marginally better accuracy score than my other models. As for activation functions, I understood that ReLU offered good general performance and Sigmoid was suited for binary outcome (IS_SUCCESSFUL = 0 or 1)
* Were you able to achieve the target model performance?
    - No. I think given more time I can achieve better accuracy. At the moment I think the key for higher accuracy would primarily lie in better pre-processing of the data. 
* What steps did you take in your attempts to increase model performance? 
    - Further reduced categorical values to > 7
    - Used OneHotEncoder instead of pd.get_dummies
    - Variations of neurons and hidden layers, plus activation functions

## Summary: 
Unfortunately the final model fell short of the target. As stated above I believe the model parameters are a step in the right direction and further pre-processing is required to optimize model accuracy. The exercise could also be tackled by using a logistical regression model from scikit-learn, which would take much less time to optimize inbetween iterations compared to a deep learning model. 