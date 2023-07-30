# Source Code

The original source code is located here: AlphabetSoupCharity_Base.ipynb. It was created using Colab.

The source code for the optimizations are located here: AlphabetSoupCharity_Optimization_X.ipynb. They were all created using Colab.


# HDF5 Files

HDF5 files that resulted from the base model and the various optimization efforts reside here: "\HDF5 Files"


# Purpose of Analysis

The purpose of this analysis is to help the organization Alphabet Soup to predict the likelyhood of a funding venture to be successful or not. 

They provided a database of over 34,000 records with 12 variables/fields. Two of the fields, EIN and NAME, were not relevant to the predictions and were thus removed. This left 9 variables to be used as features in the model and one variable to be used as the target.

The variables used as features were: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMOUNT.

The variable used as a target was IS_SUCCESSFUL


# Initial Base Model

For the base model, I went with three layers. The first layer consisted of 80 units, relu activation, and 36 input units. The second layer consisted of 30 units with relu activation. The third (output) layer consisted of 1 unit with a sigmoid activation because it was a simple binary classification result.


# Attempts to Increase Model Performance

For my first optimization, I adjusted the units from 80 to 100 on the first layer and from 30 to 70 on the second layer. It resulted in an accuracy of 0.7268.

For my second optimization, I kept the units from the first optimization and added a new third layer with 15 units and relu activation. It resulted in an accuracy of 0.7281.

For my third optimization, I increased the units for the first three layers to 120, 70, and 30. It resulted in an accuracy of 0.7411.

For my fourth optimization I used tanh for the first three layers instead of relu. It resulted in an accuracy of 0.7256.


# Summary

While my optimization efforts resulted in a 74% accuracy, I believe there are still opportunities to further enhance the model's performance. Exploring different activation functions could lead to improved accuracy in predicting funding outcomes.


# Resources

I obtained the code to export the HDF5 file to Google Drive from a classmate.