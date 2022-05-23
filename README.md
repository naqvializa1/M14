# Columbia_Fintech_Module14


# Project Title

This program demonstrates Algo Trading with Machine Learning algorithms 

---

## Technologies

This project is written in python. The required libraries are as follows
pathlib, pandas, numpy, hvplot, sklearn.preprocessing, sklearn.metrics, sklearn.svm.SVC, sklearn.ensemble.AdaBoostClassifier, sklearn.tree.DecisionTreeClassifier


---

## Usage

This program demonstrates using Machine Learning Algorithms to predict the buy / sell signals. It also demonstrates using variety of Machine Learning Algorithms and also fine-tuning different Machine Algorithm parameters to better predict the outcomes.

## Analysis Report

## Tuning the Algo by changing the training dataset period

The training window was increased to 12 months, 24 months, 36 months and 48 months.
The classification report was run after each parameter change and recorded below. The performance graphs are saved in png files and also recorded. The names of the png files are also listed below.

Across all the time window changes, the accuracy is best with 24 months. However, there is not much difference in accuracy across other time windows. They all hover around 55% accuracy
All the models perform well for predicting or signalling 'buy'. However, none of the parameters help with predicting or signaling 'Sell'. Once again, 24 months trainng window shows the best result with recall score of 1 and f1-score of 0.72 for predicting 'Buy' signal.

Third point of comparing the strategy results with actual results. 
Based on the cumulative returns and the graphs, setting the training set for 24 months provides the best predicting results.


## Tuning the Algo by adjusting the SMA input features

The SMA periods were adjusted in three different experiments as shown below
1 - Short window was changed to 50
2 - Long window was changed to 200
3 - Short window was changed to 50 and long window was changed to 200

The classification reports are shown below. 
The accuracy of all the three parameters is best for option 1
Interestingly, for option 2 (short window is 4 and long window is 200), the model improves for Sell signal. The recall is 0.85 and f1-score is 0.58, which is one of the best among all the parameters for 'Sell' signal predictability. But the predictability for 'Buy' signal drops for Option 2.

Other than that, Option 1 (short window is 50 and long wingow is 100) is best for predicting 'Buy' signal.
Recall is 1 and f1-score is 0.72


## Original Algo

          precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy                           0.55      4092
   macro avg       0.49      0.50      0.39      4092
weighted avg       0.50      0.55      0.43      4092

### Graph file - 'Initial_algo.png'


## Training period 12 months
            precision    recall  f1-score   support

        -1.0       0.00      0.00      0.00      1497
         1.0       0.56      1.00      0.72      1931

    accuracy                           0.56      3428
   macro avg       0.28      0.50      0.36      3428
weighted avg       0.32      0.56      0.41      3428

### Graph file - 'Tune1_12months_algo.png'

## Training period 24 months
              precision    recall  f1-score   support

        -1.0       0.80      0.00      0.01      1229
         1.0       0.56      1.00      0.72      1565

    accuracy                           0.56      2794
   macro avg       0.68      0.50      0.36      2794
weighted avg       0.67      0.56      0.41      2794

### Graph file - 'Tune1_24months_algo.png'

## Training period 36 months
              precision    recall  f1-score   support

        -1.0       0.00      0.00      0.00       772
         1.0       0.55      1.00      0.71       948

    accuracy                           0.55      1720
   macro avg       0.28      0.50      0.36      1720
weighted avg       0.30      0.55      0.39      1720

### Graph file - 'Tune1_36months_algo.png'


## Training period 48 months
              precision    recall  f1-score   support

        -1.0       0.00      0.00      0.00       404
         1.0       0.56      1.00      0.72       522

    accuracy                           0.56       926
   macro avg       0.28      0.50      0.36       926
weighted avg       0.32      0.56      0.41       926

### Graph file - 'Tune1_48months_algo.png'



###### ------------------------------- 




## Short window 50 Long window 100
              precision    recall  f1-score   support

        -1.0       0.00      0.00      0.00      1804
         1.0       0.56      1.00      0.72      2288

    accuracy                           0.56      4092
   macro avg       0.28      0.50      0.36      4092
weighted avg       0.31      0.56      0.40      4092

### Graph file - 'Tune2_shortwindow.png'

## Short window 4 Long window 200
             precision    recall  f1-score   support

        -1.0       0.44      0.85      0.58      1740
         1.0       0.58      0.16      0.25      2227

    accuracy                           0.47      3967
   macro avg       0.51      0.51      0.42      3967
weighted avg       0.52      0.47      0.40      3967

### Graph file - 'Tune2_longwindow.png'

## Short window 50 Long window 200
              precision    recall  f1-score   support

        -1.0       0.45      0.20      0.28      1740
         1.0       0.56      0.81      0.67      2227

    accuracy                           0.54      3967
   macro avg       0.51      0.51      0.47      3967
weighted avg       0.52      0.54      0.50      3967

### Graph file - 'Tune2_shortwindowlongwindow.png'



## Testing with Alternative Machine Learning Algorithms
Two other classifier machine learning algorithms were implemented as shown below
1) AdaBoostClassifier algorithm
2) DecisionTreeClassifier algorithm
The classification reports along with original algorithm classification report are shown below.
Based on the classification reports and cumulative return plots, one can summarize and conclude that the other two classifier models implemented do not enhance the predictability for either 'Buy' or 'Sell signal.




## Original Algo

          precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy                           0.55      4092
   macro avg       0.49      0.50      0.39      4092
weighted avg       0.50      0.55      0.43      4092

### Graph file - 'Initial_algo.png'

## AdaBoostClassifier -- New Machine Learning Classifier
AdaBoost Classifier 
              precision    recall  f1-score   support

        -1.0       0.44      0.08      0.13      1804
         1.0       0.56      0.92      0.70      2288

    accuracy                           0.55      4092
   macro avg       0.50      0.50      0.41      4092
weighted avg       0.51      0.55      0.45      4092

### Graph file - 'AdaBoostClassifier.png'

## DecisionTreeClassifier -- New Machine Learning Classifier

DecisionTree Classifier 
               precision    recall  f1-score   support

        -1.0       0.44      0.08      0.13      1804
         1.0       0.56      0.92      0.70      2288

    accuracy                           0.55      4092
   macro avg       0.50      0.50      0.41      4092
weighted avg       0.51      0.55      0.45      4092

### Graph file - 'DecisionTreeClassifier.png'