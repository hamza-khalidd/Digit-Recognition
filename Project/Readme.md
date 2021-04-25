## AI 106393 Spring 2021: Course Repository ##

## PROJECT MEMBERS ##
StdID | Name
------------ | -------------
**64170** | **Hamza Khalid**
62210 | Muhammad Daniyal
62447 | Saad Khan

## Description ##
This folder in AI-393 Repository contains the complete Project with its working attached via Jupyter Notebook. The project was to make submission for Digit Recognizer Competition on Kaggle and try to achieve maximum accuracy.
  - Link to the competition: https://www.kaggle.com/c/digit-recognizer
Our aim was to achieve maximum accuracy as much as we can and then check kaggle score by submitting in correct format(provided in sample_submission.csv).

Note : This was a classification scenrio in which we need to classify 1-9 numbers (9 different classes) on the basis of its given pixels.

## Approach ##
We tried different approaches on this project.
### Approach 01 ###
  - In this we just upload csv into dataframe and split the data and target variable and apply ML models n it like SVM, Naive Bayes etc.
### Approach 02 ###
  - In this approach we used feature selection technique (SelectKBest) in which we were provided the most best columns from the data according to the number we provided. (Example: If we have 784  columns in total and we give 500 to SelectKBest and pass our data so it will return the top best 500 columns from 784 columns). Then we split that data of 500 columns and then apply models on this.
  - Same thing we done for testing data we select those 500 columns from testing data which were provided by SelectKBest.
  - Then make predictions on testing data and make a dataframe with correct format, then save into csv and make submission on kaggle.
### Approach 03 (Used In Project) ###
  - This is the approach which I used in Project.
  - In this approach I worked on Convolution of 4 different types 3x3, 5x5, 7x7, 9x9 with two types of filters Normal filter and Incremental filter.
  - I applied total 8 types of convolution on the data and saved the data into dataframe for later use.
  - Then I applied 4 ML Models KNN, SVM, Decision Tree, Multinomial Naive Bayes.
  - I then also applied Cross Validtion. This is basically a technique for evaluating Machine Learning Models by training models on the subsets of available data and evaluating them. This is used to check how accurate your model could be.
  - After applying ML models I checked which gives best accuracy.
  - Best accuracy was of SVM on 3x3 Incremental / Normal Filter of 98.20238095238095
  - Than I used this ML model and filter for testing data to make predictions and upload it on kaggle by formatting the dataframe and save into csv file.
### Any Other Approach ? ###
  - Yes, while I was traversing over the internet so seen many blogs of this that best things for working on images is using Keras and Tensorflow (Deep Learning Libraries).
  - This problem might be solved using CNN (Convolutional Neural Networks) by making convolutional layers.
  - This may lead us to 100% Accuracy score on Kaggle.

## How I Used Convolution ? ##
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
  
## Which Machine Learning Models Used ? ##
There are 4 types of Machine Learning Models Used In This Project.
  - SVM : This gives us best accuracy among all others in each approach with or without tuned parameters. This technique is used for Classification, Regression and Outliers Detection. This is capable of performing multi-class classification done here. 
  - KNN : After SVM, KNN gives us best accuracy for all convolutional data.
  - Decision Tree : This gives us third highest accuracy after SVM and KNN. This method is used for Classification and Regression. This works in the way that predicts a target value by some simple rules which raised from data features.
  - Multinomial Naive Bayes : This is the 4th model I used and gives lowest accuracy among all other models used.

## Best Accuracy ##
The best accuracy was using SVM on any approach.
  - If we any one approach and apply different ML Models on it, SVM gives us the highest accuracy.
  - In our case, Digit Recognizer Data we used convolution with ML models so we came at this point that SVM is the one of the best Models and we achieved hightest accuracy on SVM using 3x3 Conovlution on the data with Incremental Filter (Normal and Incremental Gives Same Accuracy).
  - Accuracy Score Is : 0.982024 (On Training Data)
  - Kaggle Score Is : 0.98157 (Prediction on Testing Data)
  - Cross Validation Mean Score : 0.972321 (On Training Data)
  - All the above scores are achieved by using 3x3 Convolution.
  #### SVM Classfier ####
    - SVM is a widely used SUpervised Machine Learning technique used for both classification and regression problems.
    - SVM kernel : Kernels is SVM are set of mathematical functions. There are many different Kernels in SVM. We used 'rbf' (Radial Basis Function) which works when we have no prior knowledge about the given data. By default its also 'rbf' if we dont set kernel parameter to any other kernel while Initializing.
    - C Parameter is a Regularization parameter. It is a hypermeter which is set before training the model and is used to control error. By default its 1.

## Problems ##
### In Training Data ###
   - In training data we have 784 columns which is a huge number of columns for training, so mainly we have to transform those 784 columns so they could be reduced and used for prediction. Then firstly Linear Regression gives less accuracy so I also used some other like SVM, Naive Bayes, KNN and Decision Tree but the best accuracy we obtained was from SVM. This was a bit challenging task. 
   - Convolution was a huge task and most of the project time was consumed while organizing data and csv files and predicting using models.
   - Organizing the Notebook was a bit challenging due to large dataset.
   - Time consuming work.
   - Convolution also was not working like it gives mostly alike accuracy in SVM like other approaches on 9x9 or 7x7 filters but as I change filters to 5x5 or 3x3 accuracy increases.
   Note: I noted that with a small filter accuracy increase as compare to large filter matrix like 3x3 > 5x5 > 7x7 > 9x9 (3x3 gives better accuracy than 5x5, 5x5 gives better than 7x7 and 7x7 gives better than 9x9).
### In Testing Data ###
   - Approach which I applied to training data, also applied to testing data then make prediction using SVM with 3x3 incermental filter. Also for submitting to kaggle formating of index was necessary as the index starts from 1 in sample submission file. So I make a dataframe with ImageId and Label in which ImageId starts from 1 till the length of predicted data.

## References ##
  - For Machine Learning Models : https://scikit-learn.org/stable/
  - For Convolution : 
    - 1) https://medium.com/analytics-vidhya/2d-convolution-using-python-numpy-43442ff5f381 (For Understanding)
    - 2) https://docs.scipy.org/doc/scipy/reference/generated/scipy.signal.convolve2d.html (For Working on Project)
  - For DataFrame Working : https://pandas.pydata.org/pandas-docs/stable/reference/frame.html
  - For Array Working (Some Help Taken) : https://numpy.org/doc/stable/user/basics.creation.html
  - Maybe Any Other website while traversing over the internet also.
  - For Study about SVM Kernel : https://data-flair.training/blogs/svm-kernel-functions/
