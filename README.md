# Neural_Network_Charity_Analysis

## Overview of the challenge

A way to invest is to identify potential risk factors and minimize the risk for optimal gain. In
other to predict any future events associated with financial loss, we have to study the future
events given historical precedents. Deep learning algorithms are tools that can help us
understand these future events with some level of certainty.

The purpose of this analysis is to help Beks design a Neural Network model capable of
predicting whether applicants will be successful if funded by Alphabet Soup. A tabular metadata
of over 34,000 organizations that have received funding from Alphabet Soup over the years
with 12 raw features was used for the analysis.

## Results

### Data Preprocessing

- The variable IS_SUCCESSFUL was considered the target. It was a binary variable.

-  Nine (9) variables were used as raw features for the model design and preprocessed to obtain
about 43 features. They are: APPLICATION TYPE, CLASSIFICATION,USE CASE, ORGANIZATION,
INOCME AMOUNT, STATUS, SPECIAL CONSIDERATIONS and ASK AMOUNT.

- Two of the raw variables were dropped from the dataset namely EIN and NAME.

### Compiling, Training and Evaluating
The initial Neural Network model was designed with 43 features as input layers, 80 neurons
for the first hidden layer, and 30 neurons for the second hidden layer acting as inputs for
the output layer. The Rectified Linear Unit (relu) activation function was used for both
hidden layers with the sigmoid activation function applied to the output layer.

The initial model designed was able to predict the test data 69.6% of the time with a
training accuracy of about 53.2% and associated loss of 0.6912. Such an accuracy score is
not enough to predict the outcome of successful application.

A modified strategy was adopted to improve the performance of the initial model. Several
activities were taken:

## Activity one
I fine-tuned the model (hyperparameters) by setting up different activation functions,
varying number of hidden layers, number of neurons to optimize the model. In doing so,
STATUS variable was dropped since less than 1% of the organizations were not active at the
time of data collection. An accuracy score of 72.9% was obtained for this modification.


## Activity two

The CLASSIFICATION and APPLICATION TYPE were binned further to reduce the noise and
non-linearity in the input layer. Considering a threshold for both variables, and STATUS
removed from the data an accuracy score of 72.3% was obtained.

The target performance of 75% and above was not achieved even though some measures
were taken into consideration.
In summary, even though the modified deep learning model was able to reasonably predict
successful applicants funded by Alphabet Soup, it couldn’t meet the targeted performance
of about 75% or more.

I would recommend a robust ensemble algorithm in particular a Random forest that uses
less resources to achieve same of better performance than the deep learner especially
when the features are small and all data preprocessing have been done.
