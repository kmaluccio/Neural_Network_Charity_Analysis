# Neural_Network_Charity_Analysis
With knowledge of machine learning and neural networks, we use the features provided in the dataset to help create a binary classifier that is capable of predicting whether or not applicants will be successful if funded by Alphabet Soup.

## Overview of the analysis

From Alphabet Soup's business team, we are using a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. We take a look at all of the columns and the metadata for each organization to help us determine what can be used in our model. First, we preprocess the data for a neural network model. Then, we compile, train and evaluate the model. Finally, we optimize the model and make updates to try getting an accuracy of 75% or higher.

## Results

Data Preprocessing:
- For our model, we used the target variable as the column that said whether or not the application was successful or not (returning 1 for success and 0 for not a success)
- For our model, the feature variables are the application type affiliation, classification, organization, status,  income amount and special considerations columns 
- The variables that we removed from the data are: EIN (ID column) and names

Compiling, Training, Evaluating the Model:

- Summary of our neural network

![structure summary](https://github.com/kmaluccio/Neural_Network_Charity_Analysis/blob/main/images/structure_summary.png)

- We used a total of 419 parameters for our training model
- We trained the model with both two hidden layers and three hidden layers
- We used two different activation functions: RELU for our hidden layers and sigmoid for our output layer since these are the most common for data that is nonlinear
- These were chosen based on the data we have and it made sense to start with two hidden layers, but then for better accuracy we added a hidden layer since this can sometimes help the model have higher accuracy and lower loss

![scaled data](https://github.com/kmaluccio/Neural_Network_Charity_Analysis/blob/main/images/scaled_data.png)

- Below are the density plots we used to create a cutoff point to bin the categorical variables of application type and classification

![app density](https://github.com/kmaluccio/Neural_Network_Charity_Analysis/blob/main/images/application_density_plot.png)


![class density](https://github.com/kmaluccio/Neural_Network_Charity_Analysis/blob/main/images/class_density_plot.png)

- We were not able to achieve the target model performance of 75% or higher, although we were able to get close to this number and we improved the accuracy by almost 20 percent
- The steps taken to increase the model's performance include adding neurons to the hidden layers, adding a hidden layer, changing the activation function of the hidden layers and output layer

## Summary

We ran the model multiple times to get at least 75% accuracy, but were only able to get as high as 72% or 73% even after making adjustments to optimize the data. Perhaps if more noise was removed from the features or a different number of columns were dropped from the original data set, then we would have gotten a higher accuracy. It seems as though the RELU and sigmoid activations gave us similar results.

![test data](https://github.com/kmaluccio/Neural_Network_Charity_Analysis/blob/main/images/test_data.png)

The first time we tested our model we got about 55% (pictured above), but once some adjustments were made by adding a hidden layer and updating the activation, we were able to get almost 75%. The images captured below are the best results that we were able to get with our model.

![accuracy and loss](https://github.com/kmaluccio/Neural_Network_Charity_Analysis/blob/main/images/loss_accuracy2.png)


![final accuracy and loss](https://github.com/kmaluccio/Neural_Network_Charity_Analysis/blob/main/images/final_accuracy_loss.png)

My recommendation would be to sort through the data more carefully and drop columns with major outliers that might affect the accuracy of the model. By simply adjusting the hidden layers and activation, we were able to increase the accuracy from about 55% to 73% so one more small adjustment in the data should bring this accuracy to the desired percentage above 75.
