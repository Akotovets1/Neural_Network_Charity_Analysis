# Neural_Network_Charity_Analysis

Neural Networks and Deep Learning Models


## Overview

The Company Alphabet Soup requested a binary classifier that is capable of predicting whether organizations will be successful if Alphabet Soup provides them funding. Alphabet Soup provided a dataset that contained more than 34,000 organizations that received funding from them as well as metadata about each organization from past successful fundings. Alphabet Soup required that the model's target predictive accuracy should be 75%.


## Results

### Data Preprocessing


#### What variable(s) are considered the target(s) for your model?
Target variable: IS_SUCCESSFUL


#### What variable(s) are considered to be the features for your model?
The following variables should be considered as features: APPLICATION_TYPE, 'AFFILIATION, 'CLASSIFICATION', USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS


#### What variable(s) are neither targets nor features, and should be removed from the input data?
The following variable(s) should be removed from input and data: EIN and NAME columns.
They did not increase the accuracy and did not add value to the model.


### Compiling, Training, and Evaluating the Model


#### How many neurons, layers, and activation functions did you select for your neural network model, and why?

For layer 1 we started with 120 neurons with a relu activation. 
For layer 2, we applied the same relu activation, but reduced to 80 neurons. 
For layer 3 with 40 neurons and layer 4 with 20 neurons we applied the the sigmoid activation and it showed the best result.

#### Were you able to achieve the target model performance?

The target for the model was 75%, but the best the model could produce was 72.7%.


#### What steps did you take to try and increase model performance?

- Columns STATUS and SPECIAL_CONSIDERATIONS were dropped
- The number of neurons and layers were increased
- The linear activation produced the worst accuracy, 28%. 
- Other activations were tried such as tanh, but the range that model produced went from 40% to 68% accuracy 
- The relu activation at the early layers and sigmoid activation at the latter layers give the best results.

## Summary:

The relu and sigmoid activations produced a 72.7% accuracy. So, this is the best model we used. 
The next step could be trying a random forest classifier because this model is less influenced by outliers.

