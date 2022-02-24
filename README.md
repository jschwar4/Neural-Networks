# Neural-Networks
Overview of the analysis: Explain the purpose of this analysis.

* This analysis is meant to predict the success of organizations funded by Alphabet Soup based on a variety of metrics like application type, income, organization type, etc.

Results: Using bulleted lists and images to support your answers, address the following questions.

Data Preprocessing
What variable(s) are considered the target(s) for your model?
* The "IS_SUCCESSFUL" variable is considered the target for this model. This is a binary varibale, necessitating a logistic output ("sigmoid").
What variable(s) are considered to be the features for your model?
* The features included in this model are: "APPLICATION_TYPE," "AFFILIATION," "CLASSIFICATION," "USE_CASE," "ORGANIZATION," "STATUS," "INCOME_AMT," "SPECIAL_CONSIDERATIONS," "ASK_AMT."
What variable(s) are neither targets nor features, and should be removed from the input data?
* "EIN" and "NAME" should both be removed from the input data.
Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
* Neurons for the input layer were in each case equal to the number of input features. I tried with two and three hidden layers and a widely variable number of neurons in order to try to find a general zone of optimal performance. It appears that two hidden layers, with about 15-20 neurons in the first hidden layer and 5-10 neurons in the second layer are optimal.
Were you able to achieve the target model performance?
* I was unable to reach 75%, with the highest model topping out at about 70%.
What steps did you take to try and increase model performance?
* I dropped the classification variable, raised the threshhold for each of the categorical variable buckets, and trained a wide range of models with different neuron structures and layers.
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation
* This model was able to correctly classify whether an applicant would be successful about 70% of the time. Unfortunately, the opaque nature of this type of model gives us little indication as to exactly how this classification is occuring. I would recommend attempting a random forest model with an ensamble of weak learners, which would allow for some more transparency in the model with respect to feature impact. The binary nature of the random forest model would also be much more suited to the high number of one-hot encoded variables present in this dataset.
