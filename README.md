## Overview of Neural_Network_Charity_Analysis:

From Alphabet Soup’s business team, we received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

With the knowledge of machine learning and neural networks, we’ll use the features in the provided dataset to help us create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.


## Results: 

### Data Preprocessing

* Variable that was considered as the target for the model: IS_SUCCESSFUL Column
* Variables that were considered features for the model: Every Column except for IS_SUCCESSFUL which is our target and the ones we will drop
* Variable that were neither targets or features for the dataset: Columns that we dropeed are EIN, NAME, and (later SPECIAL_CONSIDERATIONS) because they will have little to no impact om our outcome

![Screen Shot 2022-06-22 at 2 24 45 PM](https://user-images.githubusercontent.com/98566486/175109587-1903a34f-d38a-4701-941d-2476b0c21538.png)

![Screen Shot 2022-06-22 at 2 25 36 PM](https://user-images.githubusercontent.com/98566486/175109705-fb7d164b-b69f-4728-9e6a-ecd02475c6b5.png)


### Compiling, Training, and Evaluating the Model

We selected the following number of neurons, layers, and activation functions for the neural network model:

*  2 hidden layers - first layer had 25 neurons, the second had 20 neurons. Both hidden layers had "relu" as the activation function.
*  There is also an output layer. The activation function for the output layer is "sigmoid."

![Screen Shot 2022-06-22 at 2 31 08 PM](https://user-images.githubusercontent.com/98566486/175110638-b7bffb59-2979-4fdc-91a3-8228162e8697.png)

The model was not able to reach the target 75%. The accuracy for our model was 72.5% with a Loss of 0.55.

### Steps taken to try and increase model performance

* Attempt 1: Removed additional feature, that is the 'SPECIAL_CONSIDERATIONS' column. Rest of the model components stayed the same, however model accuracy went down to 72.3%.

![Screen Shot 2022-06-22 at 2 36 48 PM](https://user-images.githubusercontent.com/98566486/175111631-349089d2-e565-4dc8-81c5-97b3dccab13c.png)

* Attempt 2: Adding Additional neurons to hidden layers and additional hidden layers are added. The accuracy went down again, this time it was 53%.

![Screen Shot 2022-06-22 at 2 38 51 PM](https://user-images.githubusercontent.com/98566486/175111992-7b324a6d-46bc-4803-912e-e04ade67be9d.png)

* Attempt 3: Changing activation function of input layers from "relu" to "tanh." The accuracy of the model came back to 72.3%, however despite trying different attempts we were unable to reach the 75%  accuracy target.  

 ![Screen Shot 2022-06-22 at 2 49 41 PM](https://user-images.githubusercontent.com/98566486/175113994-0c5ce2f1-4304-4bf3-b3a2-2a5243416082.png)


## Summary
Our analysis shows that the deep neural network machine learning model produced a moderately useful binary classifier in predicting whether loans should be given to certain applicants/organizations that will produce successful outcomes. However, the predictive capability never reached above 75% accuracy, even after additional optimization tests. It may be worthwhile to either attempt additional optimization techniques for this model (removing more input variables) or to try a new supervised learning classification model altogether for AlphabetSoup's needs. For example, an ensemble-based random forest classifier may be a feasible option as a structurally similar comparison to a neural network.
