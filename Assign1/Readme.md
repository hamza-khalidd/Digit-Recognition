## AI 106393 Spring 2021: Course Repository ##

### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**64170** | **Hamza Khalid** <!--this is the group leader in bold-->
62210 | Muhammad Daniyal
62447 | Saad Khan
<!-- Replace name and student ids with acutally group member names and ids-->

## Description ##
This repository contains project which will be submitted for AI course (106393) offered in Spring 2021 at PafKiet.
The description is that: We have to take part in Digit Recognizer competition on Kaggle and do working on it. We first downloaded the train and test csv files from that competition and try to achieve maximum accuracy as much we can, using scikit-learn library and apply on the given data.

## Approach ##
There could be different approaches to achieve onething that:
   - Simple split the data and apply algorithms on it from scikit-learn like SVM, Naive Bayes etc.
   - Other approach could be using CNN Models from tensorflow and keras. (Just studied a little bit on internet so included here)
   - 3rd Approach is to apply feature selection technique to the given data than split the selected data and apply algorithms. (Approach I used in Assignment 01)
   - Last approach in my mind is to apply Convolution to the given data which will reduce features than apply algorithms. (Approach Used In Assignment 02 - Final Phase)

   ### Approach I Used ###
   #### Without Technique ####
   - First I import all the relevant libraries.
   - Then import the training data.
   - separate data and target variable(data in X and target column which is label in Y).
   - Then split the data for training and testing purpose with a test size of 0.2.
   - Then I first applied 2 classifiers on the data and predict accuracy without any technique.
   - Accuracy via SVM Classifier is 0.9734 (without any technique)
   - Accuracy via Naive Bayes is 0.8305 (without any technique)
   - Then I applied Cross Validation on both Algorithms and check their cross validated mean scores.
   #### With Feature Selection Technique ####
   - After that I predict data using selectKbest technique.
   - Firstly it is used to select top best features related with target.
   - Then I randomly passed 484 to get 484 best columns and separate them into a dataframe.
   - Then I split them at a size of 0.3 for further predictions.
   - Next I applied SVM and Naive Bayes again to check accuracy.
   - So SVM gives 0.975000 Accuracy and Naive Bayes gives 0.827262 accuracy.
  #### How To Submit On Kaggle ####
   - For kaggle submission we have to make predictions on test data.
   - So we predict test data using SVM via passing the same 484 columns which we get on Feature selection.
   - Then format the file with ImageId and Label.
   - Save into CSV File.
   - Submit on Kaggle.
   - Check Score, Take Screenshot and attached.

## Problem Faces ##
### In Training Data ###
   - In training data we have 784 columns which is a huge number of columns for training, so mainly we have to transform those 784 columns so they could be reduced and used for prediction. Then firstly Linear Regression gives less accuracy so I also used some other like SVM and Naive Bayes but the best accuracy we obtained was from SVM. This was a bit challenging task.
### In Testing Data ###
   - Same transformation which I applied to training data, also applied to testing data then make prediction using SVM. Also for submitting to kaggle formating of index was necessary as the index starts from 1 in sample submission file. So I make a dataframe with ImageId and Label in which ImageId starts from 1 till the length of predicted data.
## References ##
### For Models ###
- https://scikit-learn.org/stable/
- May Be any help from other resources.
### For Feature Selection ###
   - I am learning Data Science from Frontier Technology Institute.
   - From there I was able t know that there are feature selection techniques like Chi Square, SelectKBest etc.
   - So I applied SelectKBest using the learning from Frontier Technology Institute.

