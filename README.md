# Alphabet Soup Funding Predictor

## Overview

In this challenge, you worked as a risk management associate at Alphabet Soup. Your task was to create a binary classification model using a deep neural network to predict whether applicants would become successful if funded by Alphabet Soup. You were provided with a CSV file containing funding data for over 34,000 organizations that had previously received funding from Alphabet Soup.

## Dataset Preprocessing

- Read the applicants_data.csv file into a Pandas DataFrame. Review the DataFrame to identify categorical variables that need to be encoded and potential features and target variables.

- Drop the "EIN" and "NAME" columns from the DataFrame since they are not relevant to the binary classification model.

- Encode the categorical variables using the OneHotEncoder and create a new DataFrame containing the encoded variables.

- Add the original DataFrame's numerical variables to the DataFrame containing the encoded variables using the Pandas concat() function.

- Create the features (X) and target (y) datasets. The target dataset should be defined by the preprocessed DataFrame column "IS_SUCCESSFUL", while the remaining columns define the features dataset.

- Split the features and target sets into training and testing datasets.

- Scale the features data using scikit-learn's StandardScaler to ensure all variables have a similar scale.

## Compile and Evaluate Binary Classification Model

- Design the deep neural network model using the number of input features, the number of layers, and the number of neurons on each layer. 

- Compile the model using the binary_crossentropy loss function, the adam optimizer, and the accuracy evaluation metric.

- Fit the model to the training data.

- Evaluate the model using the test data to calculate the model's loss and accuracy.

- Save and export your model to an HDF5 file.

## Conclusion

- Original Model Results:
    - Loss: 0.5604
    - Accuracy: 0.7298
***
- Alternative Model 1 Results:
    - Loss: 0.7140
    - Accuracy: 0.7265
***
- Alternative Model 2 Results:
    - Loss: 0.5510
    - Accuracy: 0.7308 

Comparing the results, we can see that both alternative models have slightly higher loss values and accuracy scores compared to the original model. However, the differences in loss and accuracy between the models are relatively small.

Based on these results, it appears that the alternative models did not significantly improve the model's performance compared to the original model. The changes made in the alternative models, such as adjusting te number of neurons, hidden layers, epochs, or using different activation functions, did not lead to substantial improvements in accuracy.

While the alternative models did not achieve a significantly higher accuracy, it is important to note that model optimization is an iterative process. The results obtained here can serve as a starting point for further exploration and experimentation to continue improving the model's performance.

In conclusion, while the alternative models did not yield a substantial improvement in accuracy compared to the original model, they demonstrate the iterative nature of model optimization. Further experimentation and fine-tuning may be necessary to achieve better results.

## Technologies Used

- tensorflow
- pandas
- sklearn
- pathlib