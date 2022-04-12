# Applied-Machine-Learning
## Applying supervised machine learning methods

The purpose of this assignment was to apply knowledge of supervised machine learning to toy datasets. 

The purpose of the assignment was to look at the Credit Card Clients Dataset  to determine whether or not a credit card client will default on their payments. Initially, just by observing the dataset we noticed that there were no missing values as well as enough data for a good 80-20 split. To explain what an 80-20 split means we must first understand how supervised learning is carried out. In supervised machine learning we are given some data and a question; for example, given this dataset of different flower and the associated number of petals per flower form previous years, predict the number of petals for the new flowers that will bloom this season (this will be our target data). So using the dataset from previous years we can develop an intelligent model that can accurately predict our target data. Therefore, we split our data into two sets; one to learn and develop the model from, the other to test the model on so that we can have some certainty and assurance that our model will work for real life data. 

So the 80-20 split means that one set contained 80% of the original dataset, the other 20%. The 80% set was used to train the machine learning models and the 20% set was used to test the model. The original dataset contained various pieces of information such as sex, education, marriage, various bill amounts, various pay amounts and more. A reference picture has been provided below. 

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/73089638/162645760-b256d747-e699-4c3e-9d9b-b06bcf9d4443.png">

We performed some initial exploratory data analysis to observe that credit card default rates were highest in university graduates.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/73089638/162645723-06ce2374-fd13-4ce0-92cf-c01aff5ff808.png">


Afterwards, we proceeded to clean up the original dataset. By this we mean to adjust the data by dropping our irrelevant information and differentiating between numerical, ordinal, and categorical features. By doing so, we can design a better, more robust model. We also create a dummy model that using basic inference techniques for its predictions. We call this a baseline model; this is the model on which we can base our model’s accuracy on. If our developed and learned model has lower accuracy that the baseline model then there’s something wrong with our learning process, otherwise the learned model has the potential to be effective. 

We initially used a linear model to for predictive analysis. Linear models predict target values for a given continuous range. We used a very common approach to this by using the Linear Regression Model. It is however, common to try different models on your sample data to find the best fit so we tried various other models. The table below shows the different models we attempted to work with including all scores necessary. The most important (not always) measurnment to look out for is the recall score and according to the table below Linear Regression and Light GBM are the best models for this data. 

<img width="1000" alt="image" src="https://user-images.githubusercontent.com/73089638/162869387-25427eef-f08e-4adc-91f0-309c2423ba67.png">


Now these results can be misleading since we did not consider certain things like category importance. The categories (column headers) in machine learning  are called features. Should the EDECATION and MARRIAGE features be considered equally important in this data? Will this cause any biases? 

We took a look at feature importance and came to the conclusion that PAY_1 was the top  feature for LightGBM whereas it was no.2 for Linear Regression. This just shows that different models take different things into account and you need to use your data properly without any biases.  

After a few other tests, we ended up choosing LightGBM as the model of our choice because of its high recall score compared to the others. We came to this conclusion by ignoring all biases and by not training our model more than once on the data set which his avoids overfitting (where the model leanrns too many specificities of the training set such that it cannot be applied to any training or real life data set without giving bad/biases results). 


