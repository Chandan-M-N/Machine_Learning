# Spam message classifier

  # Problem Statement:
   To determine if a text message is classified as spam or not spam.

   # Project Planning

   # Imports:

•	Contains necessary imports required for visualisations and reading data.

•	Extracting data from UCI dataset.

   # Data Analysis:
•	Evaluate the nature of data .info() .describe()

•	Determine the target labels distribution.

•	Analysing graphs to gain insights about the relationship between the new column length, spam, and non-spam messages.

# Constructing an Algorithm:
•	The data is divided into test and train messages.

•	Text messages are first transformed using CountVectorizer and TfidfTransformer into a Bag-of-words representation, and then into a Model.

**Pipeline -**

 Deploying a pipeline that was built utilising the three procedures shown below.

1.	**Count Vectorizer** -
  
    o	Using stop_words, eliminate English words.

    o	Tokenization: Each document is divided into the words that are present in it, by considering punctuation and white space.

    o	Vocabulary building: Make a list of every word that appears in any of the documents and assign numbers to it.
    
    
2.	 **Tf-idf Transformer -**
  
     o	Count Vectorizer's sparse matrix output is taken, and it is transformed by giving a high weight to any term that occurs frequently in a specific document.
  
    
3.	**Model -**
  
     o	To classify messages (tf-idf sparse matrix) as spam or not spam, logistic regression and multinomial naive bayes classifiers are used.


**GridSearchCV -**

•	Incorporating a grid search using a pipeline, adjusting the parameters, and applying five folds of cross-validation.

•	Getting the best cross-validation score and best parameters by fitting the constructed grid with train data.

•	Exploring stop words, TFIDF vocabulary, and created vocabulary.

#  Prediction and Evaluation of model:

•	Predictions made on test text data.

•	Using classification report and confusion matrix to evaluate the model.

#  Spam message classifier for user:

•	Constructing a full model on entire dataset (X and Y) without splitting by using the best parameters and estimator from GridSearchCV.

•	Creating a function called 'classify' that can categorise user provided message as spam or not spam.

•	The user has the advantage of entering any text message and checking model predictions on SMS.
  
# Data set

Link for data set used -> https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection/
