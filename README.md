This repository consists of code samples of some of the ML projects I have done while learning and exploring this domain.

![image](https://user-images.githubusercontent.com/77841499/132994175-39edfec2-aa06-4b94-9c80-7e1289a282ff.png)


Machine Learning
>Machine Learning (or ML) is an area of Artificial Intelligence (AI) that is a set of statistical techniques for problem solving.These techniques can be applied to a wide variety of problems which are not limited to - vision based research, fraud detection, price prediction, and even NLP.

Natural Language Processing
> Natural Language Processing (or NLP) is an area that is a confluence of Artificial Intelligence and Linguistics.NLP has many tasks such as Text Generation, Text Classification, Machine Translation, Speech Recognition, Sentiment Analysis, etc. 

Data Learning
>Deep Learning (which includes Recurrent Neural Networks, Convolution Neural Networks and others) is a type of Machine Learning approach. It is an extension of Neural Networks.It can also be used for vision based classification and can be used in NLP.

# Flow Chart of everthing ML

![ml flowchart](https://user-images.githubusercontent.com/77841499/132993807-b0a69d7a-e11f-4050-b1a5-7a7c41ec1a64.jpeg)

# Naive Bayes Classifier

Bayes Theorem
P(A|B)-  how often A happens given that B happens= P(B|A)P(A)/P(B)
P(B|A)-  how often B happens given that A happens

> Naive Bayes classifier calculates the probabilities for every factor.This classifier assumes the features (in this case we had words as input) are independent. Hence the word naive.

Sklearn Naive Bayes provides three alternatives for model training:
1. Gaussian- it assumes that features follow a normal distribution
2. Multinomial- used for discrete counts (eg: number of times outcome number x_i is observed over the n trials)
3. Bernoulli- useful if your feature vectors are binary (i.e. zeros and ones), text classification with ‘bag of words’ model where 1s are word that occur in the document & 0s are words that do not.
 
# Support Vector Machines(Classifier)

*Separation of classes*

> Given a labelled training data, the algorithm outputs an optimal hyperplane which categorises new examples.

**Tuning Parameters in SVM Classifier**

( by varying these parameters we can achieve considerable non linear classification line with more accuracy in reasonable amount of time )

1. Regularization Parameters

  > The Regularization parameter (C parameter in python’s sklearn library) tells the SVM optimization how much you want to avoid misclassifying each training example

2. Gamma

  > The gamma parameter defines how far the influence of a single training example
  * low gamma-points far away from plausible seperation line are considered in calculation for the seperation line
  * high gamma-the points close to plausible line are considered in calculation.


3. Margin

  *SVM to core tries to achieve a good margin.*

   > A margin is a separation of line to the closest class points.

   1.Good Margin 2. Bad Margin

4. Kernel

   > The learning of the hyperplane in linear SVM is done by transforming the problem using some linear algebra. 

   For linear kernel the equation for prediction for a new input using the dot product between the input (x) and each support vector (xi) is calculated as follows:

  ` f(x) = B(0) + sum(ai * (x,xi))` 

  > Other kernels can be used that transform the input space into higher dimensions such as a Polynomial Kernel and a Radial Kernel. This is called the Kernel Trick.

  1. Polynomial Kernel

    K(x,xi) = 1 + sum(x * xi)^d

    (the degree d must be specified by learning algorithm)

  2. Radial Kernel

    K(x,xi) = exp(-gamma * sum((x – xi^2))

    (gamma must be specified, a good value of gamma=0.1, must be between 0 and 1)
    
 > SVC takes more training time than the Naive Bayes but the prediction is faster. However, it totally depends on scenario and data set which one performs best.
 
 
