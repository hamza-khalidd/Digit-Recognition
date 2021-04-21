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
There are some problems faced by me and my group which were:
   -
## References ##
This repository contains assignments and project submitted to DM course offered in Fall 2020 at PafKiet.
