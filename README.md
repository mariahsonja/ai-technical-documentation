# Technical Documentation

- [Machine Learning Review](#machine-learning-review)
- [Validation Techniques](#validation-techniques)
- [Performance Measurements](#performance-measurements)
- [Deep Learning Review](#deep-learning-review)
- [Open Source Technologies](#open-source-technologies)
- [Natural Language Processing](#natural-laguage-processing)

  


## Performance Measurements
[Confusion Matrix](#confusion-matrix), [Accuracy](#accuracy), [Error Rate](#error-rate), [Precision](#precision), [Recall](#recall), [Specificity](#specificity), [F1-score](#f1-score), [Precision-Recall](#precision-recall), [ROC Curve](#roc-curve), [PR vs ROC Curve](#pr-vs-roc-curve)

From a binary classification problem:
- **True positives (TP):** Predicted positive and are actually positive.
- **False positives (FP):** Predicted positive and are actually negative.
- **True negatives (TN):** Predicted negative and are actually negative.
- **False negatives (FN):** Predicted negative and are actually positive.

There are multiple techniques that can be used to measure performance:

#### Confusion Matrix
Representation of parameters in a matrix formatfor a classification model.

IMAGE
  
#### Accuracy

It calculates how often the model is correct. The most commonly used metric to judge a model and is actually not a clear indicator of the performance. The worse happens when classes areimbalanced.Take for example a cancer detection model. The chances of actually  having  cancer  are  very  low.  Let’s  say  out  of  100,  90  of  the  patients  don’t  have cancer  and  the  remaining  10  actually  have  it.  We  don’t  want  to  miss  on  a  patient  who  is having cancer but goes undetected (false negative). Detecting everyone as not having cancer gives an accuracy of 90% straight. The model did nothing here but just gave cancer free for all the 100 predictions.

IMAGE


#### Error Rate

Also known as *Misclassification Rate*, it calculates how often the model is wrong. 

`1 - accuracy`

#### Precision

Percentage  of  positive  instances  out  of  the total  predicted  positive instances. Here denominator isthe model prediction done as positive from the whole given dataset. Take it as to find out ‘how much the model is right when it says it is right’.

IMAGE

#### Recall

Percentage of positive instances out of thetotal actual positiveinstances. Therefore denominator  (TP  +  FN)here  is  theactualnumber  of  positive  instances  present  in  the dataset. Take it as to find out “how much extra right ones, the model missed when it showed the right ones”.

IMAGE

#### Specificity

Percentage  of  negative  instances  out  of  the total  actual  negative instances. Therefore denominator (TN + FP)is theactualnumber of negative instances present in the dataset. It is similar to recall but the shift ison the negative instances.Like finding out how many healthy patients were not having cancer and were told they don’t have cancer. Kind of a measure to see how separate the classes are.

IMAGE

#### F1-score

It is  the  harmonic  mean  of  precision  and  recall.  This  takes  the  contribution  of both, so higher the F1 score, the better. See that due to the product in the numerator if one goes low, the final F1 score goes down significantly. So a model does well in F1 score if the positive predicted are actually positives (precision) and doesn't miss out on positives and predicts  them  negative  (recall). One  drawback  is  that  both  precision  and  recall  are  given equal importance due to which according to our application we may need one higher than the other and F1 score may not be the exact metric for it. Therefore either weighted-F1 score or seeing the PR or ROC curve can help.

IMAGE

#### Precision-Recall

Also known as PR  curve, it  is  the  curve  between  precision  and  recall  for  various threshold values. Based on our application we can choose the predictor and the threshold value. PR AUC is just the area under the curve. The higher its numerical value the better.

#### ROC Curve 

Also known as Receiver Operating Characteristics, is a graphical representation plotted against TPR and FPR for  various  threshold  values.  As  TPR  increases  FPR  also  increases. Comparing  different predictors (here 3) on a given dataset also becomes easy. ROC AUC is just the area under the curve, the higher its numerical value the better.

#### PR vs ROC Curve

Both the metrics are widely used to judge a model performance. Which one to use PR or ROC? The answer lies in TRUE NEGATIVES. 

IMAGE

**Due  to  the  absence  of  TN  in  the  precision-recall  equation,  they  are  useful  in imbalanced classes.** In the case of class imbalance when there is a majority of the negative class.  The  metric  doesn’t  take  much  into  consideration  the  high  number  of  TRUE NEGATIVES  of  the  negative  class  which  is  in  majority,  giving  better  resistance  to  the imbalance. This is important when the detection of the positive class is very important. Like to detect cancer patients, which has a high class imbalance because very few have it out  of  all  the  diagnosed.  We  certainly  don’t  want  to  miss  on  a  person  having  cancer  and going undetected (recall) and be sure the detected one is having it (precision).

**Due to the consideration of TN or the negative class in the ROC equation, it is useful when  both  the  classes  are  important  to  us.** Like  the  detection  of  cats  and  dog.  The importance of true negatives makes sure that both the classes are given importance, like the output of a CNN model in determining the image is of a cat or a dog.


## Deep Learning Review

Deep learning is a term to describe certain types of neural networks and related algorithms that consume  often  very  raw  input  data.  The  process  involves  sending  data  through  many  layers  of nonlinear transformations in order to calculate a target output. Neural networks and deep learning provide the best solutions to many problems in image recognition, speech recognition, and natural language processing. 

There are multiple types of algorithms:

#### Convolutional Neural Network (CNN)

- **How it works:** A convolutional neural network consists of an input layer, hidden layers and an output layer. In any feed-forward neural network, any middle layers are  called  hidden  because  their  inputs  and  outputs  are  masked  by  the  activation function and final convolution. 
- **Application:** image processing


#### Recurrent Neural Networks (RNNs)

- **How it works:** it is a class of artificial neural networks where connections between nodes  form  a directed  graph along  a  temporal  sequence.  This  allows  it  to  exhibit temporal dynamic behavior.
- **Application:** text generation, text summarization, chatbots, translation.

IMAGE

 
#### Long Short-Term Memory Networks (LSTMs)

- **How it works:** It is a type of recurrent neural networks capable of learning order dependence in sequence  predictions  problems. It  is  well-suited  to  classifying, processing and making predictions based on times series data, since there can be lags of unknown duration between important events in a time series.
- **Application:** machine translation,speech recognitionanomaly detection.

#### Other algorithms
- **Stacked Auto-Encoders**
- **Deep Boltzmann Machine (DBM)**
- **Deep Belief Networks (DBN)**


## Open Source Technologies

- **TensorFlow (Google):** The  framework  allows  us  to  develop  neural  networks  (and computationalmodels) using flowgraphs.

- **Keras:** Designed tosimplify the creation of deep learning models. It is written in Python and  can  be  deployed  on  top  of  TensorFlow,  Microsoft  Cognitive  Toolkit  (CNTK)  and Theano.  It  is known for  its  user-friendliness,  modularity  and  ease  of  extensibility.  It supports both convolutional and recurrent networks and runs onCPUs and/orGPUs.

- **Scikit-learn:** It features classification,regressionandclustering models.It is focused on data mining and data analysis. 

- **Microsoft  Cognitive  Toolkit:** It  trains  deep  learning algorithms  and  has  features  that includeoptimized  components  capable  of  handling  data  from  Python,  C++,  ability  to provide efficient resource usage and ease integration with Microsoft Azure.

- **Torch:** It  offers  a  widearray  of  algorithms for  deep  learning.  Provides  with  optimized flexibility and speed.GPU, iOS and Androidsupport.


