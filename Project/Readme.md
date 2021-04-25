## AI 106393 Spring 2021: Course Repository ##

### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**64170** | **Hamza Khalid**
62210 | Muhammad Daniyal
62447 | Saad Khan

### Description ###
This folder in AI-393 Repository contains the complete Project with its working attached via Jupyter Notebook. The project was to make submission for Digit Recognizer Competition on Kaggle and try to achieve maximum accuracy.
  - Link to the competition: https://www.kaggle.com/c/digit-recognizer
Our aim was to achieve maximum accuracy as much as we can and then check kaggle score by submitting in correct format(provided in sample_submission.csv).

### Approach ###
We tried different approaches on this project.
#### Approach 01 ####
  - In this we just upload csv into dataframe and split the data and target variable and apply ML models n it like SVM, Naive Bayes etc.
#### Approach 02 ####
  - In this approach we used feature selection technique (SelectKBest) in which we were provided the most best columns from the data according to the number we provided. (Example: If we have 784  columns in total and we give 500 to SelectKBest and pass our data so it will return the top best 500 columns from 784 columns). Then we split that data of 500 columns and then apply models on this.
  - Same thing we done for testing data we select those 500 columns from testing data which were provided by SelectKBest.
  - Then make predictions on testing data and make a dataframe with correct format, then save into csv and make submission on kaggle.
#### Approach 03 ####
  - This is the approach which I used in Project.
  - In this approach I worked on Convolution of 4 different types 3x3, 5x5, 7x7, 9x9 with two types of filters Normal filter and Incremental filter.
  ##### Convolution #####
  Convolution is a type of Image filter which works on Pixels of an Image to compress its pixels using a matrix.
    - I used convolution in a way like first import data then convert into 1d array then in a loop convert each image in data to 2d array, apply convolution of different types 3x3, 5x5, 7x7, 9x9 and  using filters get the desired reduced data,then I flatten the data and save into dataframe.

### Problems ###
This repository contains project which will be submitted for AI course (106393) offered in Spring 2021 at PafKiet.

### References ###
This repository contains project which will be submitted for AI course (106393) offered in Spring 2021 at PafKiet.
