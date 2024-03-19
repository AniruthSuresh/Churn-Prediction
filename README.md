# Churn-Prediction
Predicting the Churning of customers using ANN

We use the kaggle dataset to predict the churning of customers using ANN .

We start by cleaning the dataset : 
1) The monthly charges column was in type "object" and also had lot of NaN values , we drop such columns (since their number was much less than the total number of columns)
2) We one hot encode all the column so that no columns are of type "object" and everything is numerical values

Modelling the ANN :
 we have 3 hidden layer of units 40 , 40 , 20 each with reLu activation
 and the output layer has 1 unit and of sigmoid activation since it's a bianry classification porblem 


 We obtained an accuracy: 81.68 - loss: 0.3932 - val_accuracy: 80.98 - val_loss: 0.4289 on training and validation set 

 Evaluating on the test data :
 Accuracy is 79.24662232398987
 Loss is 0.44684383273124695

