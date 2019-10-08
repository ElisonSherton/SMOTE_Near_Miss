# SMOTE Near-Miss
 Handling Class/Label Imbalance in Classification tasks.
 
It commonly happens that in a classification task, there's a huge class imbalance or a label imbalance. For example, in a study involving a population with regards to presence or absence of cancer, the number of people who don't have cancer will far outnumber those who do have cancer. 
 
In such cases, the classifier learns the rules for majority class very well but for minority class, it performs poorly. In order to overcome that problem, we have two methods

- **Oversampling**

In this method, we synthetically create observations pertaining to the minority class with the data we already have until we have the same number of values for both the classes (i.e. 50-50) and then run a classifier on this new synthetic dataset. This method is also called **SMOTE (Synthetic Minority Oversampling Technique).** 

- **Undersampling**

In this method, we drop the majority label points until their number matches the number of minority label points. This is another way of making sure we have 50-50 label distribution in the target values. It is also called **NearMiss**. But here, we're losing out on a lot of variation in the data (especially if the imbalance is very high).

The notebook SMOTE.ipynb implements both SMOTE and Near-Miss techniques on a prebuilt e-coli dataset. The library that allows us to accomplish this task is called imblearn and can be installed by both pip and conda.

For more detailed explanation, please refer these resources:

https://medium.com/@saeedAR/smote-and-near-miss-in-python-machine-learning-in-imbalanced-datasets-b7976d9a7a79
https://en.wikipedia.org/wiki/Oversampling_and_undersampling_in_data_analysis
