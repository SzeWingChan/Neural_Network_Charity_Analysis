# Neural_Network_Charity_Analysis

## Overview of the analysis
The goal is to use the dataset provided and apply a neural network model to predict whether applicants will be successful if funded by Alphabet Soup.

## Results
- Data Preprocessing
    - What variable(s) are considered the target(s) for your model?
      The “IS_SUCCESSFUL” variable is considered as the target of the model.

    - What variable(s) are considered to be the features for your model?
      All variables except for “STATUS”, “EIN” and “NAME” are considered features for the model.

    - What variable(s) are neither targets nor features, and should be removed from the input data?
      “STATUS”, “EIN” and “NAME” are neither targets nor features and have been removed from the input data.

- Compiling, Training, and Evaluating the Model
    - How many neurons, layers, and activation functions did you select for your neural network model, and why?
      - There were 80 neurons in the first layer, 40 neurons in the second layer and 10 neurons in the third layer.  It is the industry norm to set the number of neurons in the first layer as double to triple of the number of input features (40 in this case). 
      - The activation function of the first layer is ReLU, the second layer is sigmoid, the third layer is ReLU and the output layer is sigmoid.  Since we are predicting if the application will be successful, the sigmoid activation function will produce a probability output and the ReLu action function will enable nonlinear relationships.  Different activation functions are tested and this combination gives the best results.  

    - Were you able to achieve the target model performance?
      - Unfortunately, the model accuracy is 72.7% and therefore, does not meet the targe model performance of 75.0%.

    - What steps did you take to try and increase model performance?
      - The below steps have been taken to increase the model performance.
        - The “Status” column is being dropped to reduce the noisiness of the dataset.
        - The “INCOME_AMT” columns is being bucketed to reduce the number of variables.
        - Neurons are to the second hidden layer to increase the accuracy.
        - The activation function of the first hidden layer was changed to Tanh to see if that will make a difference.
        - A third hidden layer is added.
        - The model’s weight is saved for every 5 epochs.
        
## Summary
- The accuracy of the model has changed with different setups of the neural network model. 
    - Model 1
      ![Model1](https://github.com/SzeWingChan/Neural_Network_Charity_Analysis/blob/main/Resources/NNW1.png)
    - Model 2
      ![Model2](https://github.com/SzeWingChan/Neural_Network_Charity_Analysis/blob/main/Resources/NNW2.png)  
    - Model 3
      ![Model3](https://github.com/SzeWingChan/Neural_Network_Charity_Analysis/blob/main/Resources/NNW3.png)  
    - Model 4
      ![Model4](https://github.com/SzeWingChan/Neural_Network_Charity_Analysis/blob/main/Resources/NNW4.png)
- Since the original dataset does not contain a lot of features, a logistic regression model could have been utilized to predict whether applicants will be successful if funded by Alphabet Soup. A logistic regression model can analyze both continuous and categorical variables and therefore, is suitable for this dataset.  The setup is also less complicated than a neural network model.
