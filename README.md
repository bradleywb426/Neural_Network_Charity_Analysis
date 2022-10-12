# Neural Network Charity Analysis

## Overview

Using our developed skills in neural networks and machine learning, we are predicting where Alphabet Soup should make investments. The goal is to create a binary classifier that can successfully predict how successful the investments will be.

## Results

### Data Preprocessing

- What variable(s) are considered the target(s) for your model?

  - Our target variable was the "IS_SUCCESSFUL" column.

- What variable(s) are considered to be the features for your model?

  - Our feature variables were "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION",  "SPECIAL_CONSIDERATIONS", "INCOME_AMT", and "ASK_AMT" columns.

- What variable(s) are neither targets nor features, and should be removed from the input data?

  - The "EIN" and "NAME" columns were considered neither a target nor a feature, and were subsequently removed.

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

  - The first neural network used two hidden layers and an output layer. The first hidden layer had 80 neurons and the second had 30 neurons. The hidden layers used the "relu" activation function, and the output layer had the "sigmoid" activation function. These were chosen based on both specifications from the challenge as well as familiarity of these decisions based on the module that I learned Neural Networks from.

- Were you able to achieve the target model performance?

- Desired target performance was 75% accuracy or higher, and the original model performed at 72.97% accuracy while an optimized model acheived 73.14% accuracy.

- What steps did you take to try and increase model performance?

  - In an attempt to increase model performance, the first set of changes were binning the ASK_AMT column using the INCOME_AMT column as a reference to reduce noise, and changing the second activation function to "sigmoid".

  - The second set of changes was changing the number of neurons to the hidden layers, making the totals 100 neurons in the first layer and 40 in the second layer.
  
  - The third set of changes was adding a third hidden layer that used the "sigmoid" function and had 15 neurons. It also changed the first activation function from "relu" to "tanh"

## Summary

Overall, the current model is able to classify/predict each point around 73% of the time. The model gained accuracy with hidden layers and neurons, and could further gain accuracy through more specific adaptations of the model. Another route to optimize the predictions/classifications is to pursue different models to see where they fail and succeed. A Random Forest model could be particularly helpful to look intoas they are good for classification problems.
