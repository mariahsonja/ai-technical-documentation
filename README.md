# Technical Basics Documentation

- [Machine Learning](#machine-learning-review)
- [Validation Techniques](#validation-techniques)
- [Deep Learning](#deep-learning-review), 

## Machine Learning Review

[Supervised Learning](#supervised-learning), [Unsupervised Learning](#unsupervised-learning), [Reinforcement Learning](#reinforcement-learning)
  
### Supervised Learning

- **Data:** structured and labelled

- **Techniques:** classification(category) and regression(value)

- **Algorithms**
  - Logistic Regression
  - Linear Regression
  - Random Forest (regression and classification)
  - Decision Tree (classification and regression)
  - Support Vectors Machines(SVM – classification)
  - NaïveBayes (classification)

### Unsupervised Learning

- **Data:** not structured or labelled

- **Techniques:** clustering (to discover inherent groups) and association (identify rules).

- **Algorithms**
  - K-means(clustering)
  - Apriori (association)

### Reinforcement Learning

- **Data:** data used to train an agent to learn to make decisions.

- **Techniques:** model-base  RL  (use  experience to  construct  an  internal  model)  and model-free RL (use experienceto learn directly one or both of two simpler quantities without use of a world model.

- **Algorithms**
  - Q-learning
  - SARSA (state-action-reward-state-action)
  
## Validation Techniques
[Resubstitution](#resubstitution), [Hold-out](hold-out), [K-fold Cross-Validation](#K-fold-cross-validation), [LOOCV](#LOOCV), [Random Subsampling](#random-subsampling), [Bootstrapping](#bootstrapping)

Used to get the error rate of the ML model, which can be considered as close to the true error rate of the population. If the data volume is large enough to be representative of the population, you may not need the validation techniques. 

#### Resubstitution 

If all the data is used for training the model and the error rate is evaluated based  on  outcome  vs. actual  value  from  the  same  training  data  set,  this  error  is  called the resubstitution error. 

#### Hold-out

To  avoid  the  resubstitution  error,  the  data  is  split  into  two  different  datasets labeled as a training and a testing dataset. This can be a 60/40 or 70/30 or 80/20 split. In this case, there is a likelihood that uneven distribution of different classes of data is found in training and test dataset. To fix this, the training and test dataset is created with equal distribution of different classes of data. This process is called stratification.

#### K-fold Cross-Validation

In  this  technique,  k-1  folds  are  used  for  training  and  the remaining one is used for testing. The advantage is that entire data is used for training and testing.  The  error  rate  of  the  model is  average  of  the  error  rate  of  each  iteration.  This technique can also be called a form the repeated hold-out method. The error rate could be improved by using stratification technique.

#### LOOCV

In Leave-One-Out Cross-Validation, all of the data except one record is used for training and one record is used for testing. This process is repeated for N times if there are N records. The advantage is that entire data is used for training and testing. The error rate of the model is average of the error rate of each iteration. Costly.

#### Random Subsampling

In this technique, multiple sets of data are randomly chosen from the  dataset  and  combined  to  form  a  test  dataset.  The  remaining  data  forms  the  training dataset. The error rate of the model is theaverage of the error rate of each iteration.

#### Bootstrapping

In   this   technique,   the   training   dataset   is   randomly   selected   with replacement.  The  remaining  examples  that  were  not  selected  for  training  are  used  for testing. Unlike K-fold cross-validation, the value is likely to change from fold-to-fold. The error rate of the model is average of the error rate of each iteration.
