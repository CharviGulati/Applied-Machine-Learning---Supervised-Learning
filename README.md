# Applied-Machine-Learning
## Applying supervised machine learning methods

The purpose of this assignment was to apply knowledge of supervised machine learning to toy datasets. 

The purpose of the assignment was to look at the Credit Card Clients Dataset  to determine whether or not a credit card client will default on their payments. Initially, just by observing the dataset we noticed that there were no missing values as well as enough data for a good 80-20 split. To explain what an 80-20 split means we must first understand how supervised learning is carried out. In supervised machine learning we are given some data and a question; for example, given this dataset of different flower and the associated number of petals per flower form previous years, predict the number of petals for the new flowers that will bloom this season (this will be our target data). So using the dataset from previous years we can develop an intelligent model that can accurately predict our target data. Therefore, we split our data into two sets; one to learn and develop the model from, the other to test the model on so that we can have some certainty and assurance that our model will work for real life data. 

So the 80-20 split means that one set contained 80% of the original dataset, the other 20%. The 80% set was used to train the machine learning models and the 20% set was used to test the model. The original dataset contained various pieces of information such as sex, education, marriage, various bill amounts, various pay amounts and more. A reference picture has been provided below. 

<img width="468" alt="image" src="https://user-images.githubusercontent.com/73089638/162645647-81cc62a7-3acc-4f9c-aab5-3682b245d7da.png">

We performed some initial exploratory data analysis to observe that credit card default rates were highest in university graduates. ![image](https://user-images.githubusercontent.com/73089638/162645656-0d1eb011-89b9-47e8-bfb3-d8e93c80d24e.png)


Afterwards, we proceeded to clean up the original dataset. By this we mean to adjust the data by dropping our irrelevant information and differentiating between numerical, ordinal, and categorical features. By doing so, we can design a better, more robust model. We also create a dummy model that using basic inference techniques for its predictions. We call this a baseline model; this is the model on which we can base our model’s accuracy on. If our developed and learned model has lower accuracy that the baseline model then there’s something wrong with our learning process, otherwise the learned model has the potential to be effective. 

We initially used a Linear Regression Model with hyperparameter tuning on the sample data. Linear regression models are a common type of model for predictive analysis in supervised machine learning. It is used to predict target values for a given continuous range. With our trained Linear Regression model, we obtained a recall score of 64% and a precision score of 37.5%. A recall score is based on the number of positive predictions made by the model out of al the positive samples in the dataset. A precision score is based on the number of positive predictions made by the model that are actually declared as positive. 
![image](https://user-images.githubusercontent.com/73089638/162645660-a87d31a1-08af-4ff7-aea8-8e82403ccb29.png)

