# Churn-Prediction
Predicting the Churning of customers using ANN

We use the kaggle dataset to predict the churning of customers using ANN .


We start by cleaning the dataset : 
1) The monthly charges column was in type "object" and also had lot of NaN values , we drop such columns (since their number was much less than the total number of columns)
2) We one hot encode all the column so that no columns are of type "object" and everything is numerical values

We visualise the data as follows :

![churn vs tenure](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/08856bd9-284a-4b68-9bde-0f29d2e6c5fe)

![cust vs churn](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/fefab892-55fb-437b-b9bd-31fc499e16d6)



Modelling the ANN :
 we have 3 hidden layer of units 40 , 40 , 20 each with reLu activation
 and the output layer has 1 unit and of sigmoid activation since it's a bianry classification porblem 


 We obtained an accuracy: 81.68 - loss: 0.3932 - val_accuracy: 80.98 - val_loss: 0.4289 on training and validation set 

 Evaluating on the test data :
 Accuracy is 79.24662232398987
 Loss is 0.44684383273124695

Now , we make a classification report whcih is as follows 

![classification_report](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/89dbf241-5fe7-4c54-a0c6-196a41424f6d)

![confusion_matrix](https://github.com/AniruthSuresh/Churn-Prediction/assets/137063103/6ca5d873-e809-494a-9e4b-b0e7c4f4bc52)
