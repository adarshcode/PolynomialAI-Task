# PolynomialAI-Task

----

This is my submission for ML/NLP task for polynomial.ai.

----

## Introduction of the problem:-
- We are provided with a dataset of Amazon customer reviews for Cell Phones and Accessories. The task is to create a model that can classify each review into 'positive', 'negative' and 'neutral' review.
 
 ## Approach used:- 
 - The given dataset is in json format so I have converted the data into csv format for my convenience. Also, the given dataset has nearly 9.6 million rows and 9 columns which makes the dataset unloadable into the memory directly. In order to resolve this issue 'chunksize' is used to divide the dataset into smaller datasets with number of rows as 'chunksize' and number of columns remain same i.e. 9.
 
 - I have chosen chunksize=10^6 so I have 10 chunks(smaller datasets)
 
 - Now, each chunk is basically a dataset, which is then appended to a list named 'chunks' so that operations can be performed on each chunk using a loop.
 
 ## Model details:-
 - The model that I have used for classification is Logistic Regression.
 - The model is applied on each of the chunks(smaller datasets) and the chunk with the best accuracy is chosen for confusion matrix and classification report.
 
 ## Model metrics:- 
 Chunk 4 was chosen for confusion matrix and classification report.
 

|                      | precision | recall | f1-score | support |
|----------------------|-----------|--------|----------|---------|
| negative(-1)         | 0.78      | 0.68   | 0.73     | 43035   |
| neutral(0)           | 0.49      | 0.20   | 0.28     | 18990   |
| positive(1)          | 0.89      | 0.97   | 0.93     | 184920  |
|                                                                |
| accuracy             |           |        | 0.86     | 246945  |
| macro avg            | 0.72      | 0.62   | 0.65     | 246945  |
| weighted avg         | 0.84      | 0.86   | 0.84     | 246945  |
------------------------------------------------------------------

 
