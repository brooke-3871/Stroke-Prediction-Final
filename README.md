# Stroke Prediction Model

*In the United States, someone suffers a stroke every 40 seconds, and every 4 minutes someone dies from a stroke. These statistics gathered by the [CDC](https://www.cdc.gov/stroke/facts.htm) help illustrate the frequency and severity of this ailment. With strokes being one of the leading causes of death in the United States, a predictive model created from demographic information has potential to keep at risk individuals preemptive care to mitigate fatalities*

## 1. Data
The data set acquired is from Kaggle is demographic information on 5110 individuals and should be sufficient to begin to identify key factors that contribute to stroke occurance. To view the initial data set follow the link below:

> * [Kaggle Data Set](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset)


## 2. Method

The stroke occurance can be thought of as a classification problem, either a patient has a stroke, or does not. This type of problem lends itself to multiple types of predictive models, I will be exploring the Decision Tree, Random Forest Classifier, K Nearest Neighbor, and Gradient Boosting Classifier. 


## 3. EDA
The exploratory data analysis jupyter notebook can be reviewed here: [Stroke Data EDA](https://github.com/brooke-3871/Stroke-Prediction-Final.git)
    When exploring the data, there were a few problems to note that may effect the overall predictive power of the model.
    
   >*__Problem 1__: The count of stroke patients and non stroke patients is quite unbalanced with the majority of data points being patients that have not experienced a stroke. This may detract from the predictive power of any model since only 5% of patients in data set have had a stroke, even predicting all zeros for a test set would still portray the idea of 95% accurate. To counteract this, I will compare the final model's predicitve power against a random binary array to ensure that the model is making accurate predictions, not just defaulting to the data patterns.*
  
  
  >*__Problem 2__: While this data set is large enough to make some educated inferences about the total population, 5110 individuals make up only 0.000015% of the total US population. Therefore any conclusions made, must be taken with a grain of salt and can be used in future studies.*
  
 
The highlights from this EDA is that the health demographics included were all statistically significant when testing independance between variables. This lets us know that pre-existing health conditions can be a significant factor in stroke occurance.

## 4. Machine Learning

As previously mentioned this is a classification problem, I used the sklearn library to import and use the Random Forest Classifier, Decision Tree Classifier, K Nearest Neighbor, and Gradient Boosting Classifier. I tested and tuned all 4 models to determine which has the best predicting power. In this phase of analysis I also determined which performance metric to focus on. In this instance we want to focus on the True positives, or those who are predicted to have a stroke as those are the at risk patients. This leads to focusing on the recall or sensitivity of the model opposed to the precision. 

[![Screen-Shot-2021-10-27-at-3-38-19-PM.png](https://i.postimg.cc/wMTXJj9N/Screen-Shot-2021-10-27-at-3-38-19-PM.png)](https://postimg.cc/r03R2c0y)

Above is the comparison of recall scores after tuning the models. It is clear the that winner in this scenario is the Random Forrest Classifier. 


## 5. Improvements

Improvements that can be made definitely start with the amount of data. 5110 is a decent sample size but is not large enough to be representative of the entire population. I also believe there are other demographic features in the data that could be expanded on for more analysis such as broadening Rural and Urban to more specific geographic locations as well as included race and income features as well. 




 
 
