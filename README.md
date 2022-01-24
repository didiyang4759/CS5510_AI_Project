# CS5510_AI_Project
## Overview
This project is Identifying Personal Attacks in Wikipedia Comments, in this project build 3 ML model to anlaysis the relationship between non-tack and tack comments

## [Modeling and Result](https://github.com/didiyang4759/CS5510_AI_Project/blob/main/AI_Project/DiYang_Project.ipynb)

1. Text cleanup: Often, the biggest chunk of time and effort spent in machine learning and big data 
projects is to get the data cleaned up and ready to be used. The strawman code does some simple 
cleaning of data, replacing newlines and tabs with spaces. See if you can come up with other, better 
ways you can clean up the data to improve performance and accuracy. 
 
2. Metrics: In the strawman code, we have metrics for precision & recall, F1 score etc. You must add  
confusion matrix  as well. See sklearn.metrics.precision_recall_fscore_support as an alternative to 
classification_report (if you prefer this), and also see sklearn.metrics.confusion_matrix.  Note that 
the rows in the attack_annotated_comments.tsv file have a ‘split’ column indicating if they are in the 
training, test or validation (dev) set. Combine the training and test sets and use k-fold cross-
validation. What value of k do you think will be good? Why? 
 
3. Feature Extraction: This is where you decide which features you will use to classify the comments 
and related data. Start with using a bag of words representation using words from the comments by 
themselves (word unigrams). Try word and character n-grams, individually, and together, in various 
combinations. The strawman code uses two feature extraction methods (CountVectorizer and 
TfidfTransformer). You could use TfidfVectorizer as a single alternative to the combination of these 
two, to generate features. You may need to use FeatureUnion as well. 
Try adding other meaningful non-word features and see how they affect the accuracy. For example, 
is ‘year’ useful as a feature? Why or why not? Your Section 2 visualization may also give you some 
useful information to decide this. 

5. Tuning hyperparameters: Once you find a classifier model that gives you great results, try optimizing 
the classifier’s parameters – we call this hyperparameter tuning. For example, assume that LinearSVC 
gave you the best results with default hyperparameters. LinearSVC has hyperparameters like C, 
class_weight and kernel. A different combination of values for these parameters may improve 
performance even more. How would you identify the best combination(s)?  Check out hyper-
parameter tuning methods such as GridSearchCV and RandomizedSearchCV. Again, keep track of 
your work. 
