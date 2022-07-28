Seoul Rental Bike prediction Part III
Executive Summary
• Converted the data set to 2 classes based on Rented Bike Count median value, if <= Median it is treated as class 0, otherwise class 1.
• After Experimenting with Neural Network MLP classifier below are the best tuned hyper parameters :- Nr of hidden layers =2, Nr of nodes =10 per each layer, activation function = ‘relu’ has best performance, solver = ‘sgd’ has best performance, learning rate = 0.001 has best convergence and tol has no much significance .
• Model accuracies have been 93.3 and 93.4 for train and test accuracies respectively with 0.93 as AUC and having 98 Type 1 and 75 Type II Errors .
• Model performed better during cross validation and achieved 91~93 score , and baselined cv = 10 .
• When KPI/Statistics compared with assignment II and assignment III Neural network model performed better w.r.t Accuracies, Type 1, Type II Errors, Cross validation, AUC , but only limitation is very hard to interpret and uses machine capabilities for performance .

Introduction
In this project, the objective is to use the dataset that is converted during assignment II and implement neural networks package for classifying either class 0(less than median value) or class 1(more than median value) and perform different experimentation w.r.t nr of hidden layers, nr of nodes, different activation functions, different values of learning_rate_init, different values of threshold where model is converging etc., and identify the best tuned hyper parameter for the model and evaluate the model using confusion matrix, AUC and compare the performance w.r.t models implemented as part of assignment II .

About the Data
The dataset consists of 14 features and 8760 records. T
information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation,
he dataset contains weather
Snowfall, Rainfall),
the number of bikes rented per hour and date information. In order to
remove the serial correlation with time, hours variable is hot encoded and converted to
dummies and ran the model .
