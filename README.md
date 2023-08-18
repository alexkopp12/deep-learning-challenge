#Report
#Overview of the analysis: 
For the Alphabet Soup Charity analysis we are using a neural network to create a model that accurately selects Charity ventures that will be successful. Using this model we could support a team in allocating capital to investments in which there is a higher chance of success thus returning more for the team's investment. We used a 5 layer karas neural network with a combination of Relu and Elu activation funtions and over 14,000 parameters in our model to look at roughly 50 features from the dataset.


#Results: 

#Data Preprocessing

What variable(s) are the target(s) for your model? 
'IS_SUCCESSFUL' was our target

What variable(s) are the features for your model? 
'INCOME_AMT', 'CLASSIFICATION', 'APPLICATION_TYPE',  'ORGANIZATION', 'AFFILIATION', "USE_CASE", 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT' were our features. Note that 'INCOME_AMT', 'CLASSIFICATION', 'APPLICATION_TYPE',  'ORGANIZATION', 'AFFILIATION', "USE_CASE", 'SPECIAL_CONSIDERATIONS' are all collumns that represent a subset of bins of features we looked at.

What variable(s) should be removed from the input data because they are neither targets nor features?
'EIN', 'NAME' were columns that were removed from the dataset because they were neither targets nor features.

#How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the optimized model I included 5 layers with 14,220 parameters, 237 neurons in my model.
I included 5 layers because I wanted to increase the number of neurons to increase performance.
I utilized a Sigmoid activation function to predict an outcome between 0 and 1, and Relu/Elu activation functions in the final model because I wanted to see how a mixed function model would handle the data..
I included 237 neurons because that allowed me to accurately process the data through the first four layers and come to a single outcome at the end.

Were you able to achieve the target model performance?
I was not.

What steps did you take in your attempts to increase model performance?
I tried removing features such as SPECIAL_CONSIDERATIONS and AFFILIATION because I did not think they would have as much impact on the final outcome. I tried increasing the number of nuerons to enhancce the models ability to interpret the data. I used multiple activation functions to see how they would interact with the data. I adjusted the bins on APPLICATION_TYPE and CLASSIFICATION to increase the number of features included in the data set.

Summary: My final optimized model had the below performance:
268/268 - 1s - loss: 0.5591 - accuracy: 0.7304 - 509ms/epoch - 2ms/step
Loss: 0.5591038465499878, Accuracy: 0.7303789854049683

Based on my research the model created in this activity is a standard for Binary Classification Objective models so I likely would not make major adjustments to the model used. I would likely just expand the dataset to include more data points and would maybe change the parameters to ones the had more direct weight on success criteria such as valuation, Total Addressable Market, etc. 