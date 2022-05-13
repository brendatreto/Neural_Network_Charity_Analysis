# Neural Network Charity Analysis

## Overview of the Analyis
The purpose of this project was to design a machine learning model to create a binary classifier that can accurately predict whether aplicants will be successful if funded.

We followed these steps to achieve (at least) a 75% accuracy in our model:
1. Preprocess the data
2. Compile, train and evluate the deep neural net
3. Optimize the model

### Resources
- Data: charity_data.csv
- Software:
-   Python 3.7
-   Anconda Navigator
-   Jupyter Notebook

## Results
### Data Preprocessing
*What variable(s) are considered the target(s) for your model?*

Since we are trying to evaluate the success of funds used the column **IS_SUCCESSFUL** is our target

*What variable(s) are considered to be the features for your model?*

Features are all the other columns that provide information that influences the outcome

*What variable(s) are neither targets nor features, and should be removed from the input data?*

The identification columns **EIN** and **NAME** can be removed since they don't provide useful information to determine the result. For the optimization process, we would recommend processing separately the **ASK_AMT** (Funding amount requsted) since it can be noisy and negatively impact the results. It might also be convenient to remove the **SPECIAL_CONSIDERATIONS** columns becuase in its shape it mught not provide important insight.

### Compiling, Training, and Evaluating the Model
*How many neurons, layers, and activation functions did your select for your neural network model, and why?*

We began the model with two hidden layers -80 and 30 neurons respectively- and using relu activation for input layers and sigmoid  activation for the output layer.
*Were you able to achieve the target model performance?*

This structure was only capable of achieven a 72.75% accuracy

*What steps did you take to try and increase model performance?*

- The first step was to work separately with th ASK_AMT feature, that alone increased the accuracy to 73.00%
- We later added a third layer with 10 neurons but the accuracy stayed at 73.00%
- The third attempt was to change the number of neurons per layer (80, 40, 20) with a minimum impact in accuracy 73.06%
- Our last attempt was to change the activation function to tahn in the output layer but it had the opposite of the expected effect in the accuracy, decreasing to 72.75%

## Summary
This deep learning neural network model did not reach the target of 75%. We could improve the accuracy by cleansing the dataset, but in order to do this, we would need to work together with the organization to better understand the data. 
Although the accuracy is not subpar we could have gotten useful results using a Random Forest classifier because of the robustness of the model.
