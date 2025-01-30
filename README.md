## Predicting Survival of Passengers using Titanic Dataset:  

Here, we use three different supervised machine learning algorithms to predict the survival of passengers in Titanic dataset.  

-  Logistic Regression 
- Random Forest 
- Neural Network (Pytorch)

## Dependencies:  
After cloning this repository, install all the required dependencies from the requirements.txt file.

```pip install -r requirements.txt```   
The Titanic dataset consists of 891 data and 12 columns:  

    PassengerId - Indicates the passenger number
    Survived - Indicates if the passenger travelled survived or not.
    Pclass - Indicates which class passenger belongs to
    Name - Provides Names of passenger
    Sex - Indicates sex/gender of passenger
    Age - Indicates age of passenger
    SibSp - Provides information about number of sibiling/spouse accompaning
    Parch - Provides information about number of parents / children aboard the Titanic
    Ticket - Ticket number
    Fare - Passenger fare
    Cabin - Provides information about Cabin number, NaN specifies no cabin allocated
    Embarked - Port of Embarkation 


From these columns or features, after EDA and feature selection, we select [Pclass	Age	SibSp	Parch	Fare	Sex_male	Embarked_Q	Embarked_S]  
The Survived column is the target. 
The models are evaluated based on accuracy, precision, recall and F1 scores.  

### Logistic Regression:   
<img src="metrics/metrics_logistic_regression.png" width="500" style="vertical-align:middle;margin:0px 50px">  
<p>  </p>   
   
    Precision: 0.7714 
    Recall:  0.7826
    F1 Score: 0.7769

### Random Forest:   
<img src="metrics/metrics_random_forest.png" width="500" style="vertical-align:middle;margin:0px 50px">  
<p>  </p>   
   
    Precision: 0.8867 
    Recall:  0.6811
    F1 Score: 0.7704

### Neural Network:   
<img src="metrics/metrics_NN.png" width="500" style="vertical-align:middle;margin:0px 50px">  
<p>  </p>
   
    Precision: 0.8475 
    Recall: 0.7246
    F1 Score: 0.7812 


From this we can see that, all models have similar accuracy. Since the Survived class is imbalanced i.e, the number of people who did not survive(denoted by 0) is greater than the number of people who survived (denoted by 1), the precision, recall and F1 score of class 0 of all three models is better than the scores of class 1 respectively.   

The Logistic Regression model performs better in terms of recall 78.26%,  correctly identified all of the actual positive instances within the dataset. 

 In terms of precision, the Random Forest model performed the best with 88.67%, correctly predicted positive instances. 

And the Neural Network performed best in terms of F1-score 78.12% 