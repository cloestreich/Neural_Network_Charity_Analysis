# Neural_Network_Charity_Analysis

## Purpose and Overview of Analysis

To continue our exploration into Machine Learning we take a deep dive into Neural Nets, and the TensorFlow module. For this analysis we aim to create a Binary Classifier Neural Net that would be capable of predicting whether applicants will be successful.

We read in a dataset containing details about every organization to receive funding and whether the money was used successfully. We use this to train a model and have that model predict the whether a company will be successful. We split the data into training and testing and validate the performance of the model based on how correct the test predictions are.

## Results

## Data Processing

1. What variable(s) are considered the target(s) for your model?
Checking to see if the target is marked as successful in the DataFrame, indicating that it has been successfully funded.

2. What variable(s) are considered to be the features for your model?
The IS_SUCCESSFUL column is the feature chosen for this dataset.

3. What variable(s) are neither targets nor features, and should be removed from the input data?
The EIN and NAME columns will not increase the accuracy of the model and can be removed to improve code efficiency.

## Compiling, Training, and Evaluating the Model

4. How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the optimized model, layer 1 started with 80 neurons with a relu activation. For layer 2, it dropped to 60 neurons and continued with the relu activation. From there, the sigmoid activation seemed to be the better fit for layers 3 (30 neurons) and layer 4 (15 neurons).

5. Were you able to achieve the target model performance?
The target for the model was 75%, but the best model I could get it to produce was 72.5%.

6. What steps did you take to try and increase model performance?
Columns were reviewed and the STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the number of neurons and layers. Other activations were tried such as tanh, but the range that model produced went from 40% to 68% accuracy. The linear activation produced the worst accuracy, around 28%. The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.

## Summary

The relu and sigmoid activations yielded a 72.5% accuracy, which is the best the model could produce using various number of neurons and layers. The next step should be to try the random forest classifier as it is less influenced by outliers.
