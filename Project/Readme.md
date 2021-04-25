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
#### Approach 03 (Used In Project) ####
  - This is the approach which I used in Project.
  - In this approach I worked on Convolution of 4 different types 3x3, 5x5, 7x7, 9x9 with two types of filters Normal filter and Incremental filter.
  - I applied total 8 types of convolution on the data and saved the data into dataframe for later use.
  - Then I applied 4 ML Models KNN, SVM, Decision Tree, Multinomial Naive Bayes.
  - I then also applied Cross Validtion. This is basically a technique for evaluating Machine Learning Models by training models on the subsets of available data and evaluating them. This is used to check how accurate your model could be.
  - After applying ML models I checked which gives best accuracy.
  - Best accuracy was of SVM on 3x3 Incremental / Normal Filter of 98.20238095238095
  - Than I used this ML model and filter for testing data to make predictions and upload it on kaggle by formatting the dataframe and save into csv file.

### How I Used Convolution ? ###
Convolution is a type of Image filter which works on Pixels of an Image to compress its pixels using a matrix.
I used this in a way like:
  - Importing Data
  - Splitting target column from data
  - Converting data into 1d array
  - Runs a loop.
  - In loop, each row of data (represents 1 image) converts into 2d array.
  - Passed into convolve2d function with filter (3x3,5x5,7x7,9x9) provided.
  - Gives the 2d array with reduced data.
  - Flatten the array
  - Save into dataframe using transpose.
  - In Convolution filter works as a matrix an traverse to the 2d array and reduced the data.
  - 
### Which Machine Learning Models Used ? ###
There are 4 types of Machine Learning Models Used In This Project.
  - SVM : This gives us best accuracy among all others in each approach with or without tuned parameters. This technique is used for Classification, Regression and Outliers Detection. This is capable of performing multi-class classification done here. 
  - KNN : After SVM, KNN gives us best accuracy for all convolutional data.
  - Decision Tree : This gives us third highest accuracy after SVM and KNN. This method is used for Classification and Regression. This works in the way that predicts a target value by some simple rules which raised from data features.
  - Multinomial Naive Bayes : This is the 4th model I used and gives lowest accuracy among all other models used.

### Problems ###
This repository contains project which will be submitted for AI course (106393) offered in Spring 2021 at PafKiet.

### References ###
This repository contains project which will be submitted for AI course (106393) offered in Spring 2021 at PafKiet.
