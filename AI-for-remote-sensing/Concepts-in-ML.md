# The Task T  

## Classification  
Computer programs are asked to specify which of *k* categories some input belongs to.  
**Note:** When some of the inputs may be missing, rather than providing a single classification function, it examines a set of functions.  

## Regression  
Computer programs are asked to predict a numerical value given some input.  

## Transcription  
The system observes a relatively unstructured representation of data and transcribes it into discrete, textual form.  

## Machine Translation  
Convert a sequence of symbols in one language to another language.  

## Anomaly Detection  
Flag unusual events or objects within a set.  

## Synthesis and Sampling  
The algorithm generates new examples similar to those in the training data.  
**Example:** Creating super-resolution radar/satellite data.  

# The Performance Measure  

# The Experience  

## Supervised Learning  
- Dataset associated with a label or target.  
- Involves observing random vector *x* and its associated value *y*.  
- Examples: Regression, Classification.  

## Unsupervised Learning  
- No target attributes.  
- Observes random vector *x* and attempts to implicitly or explicitly learn the probability distribution *p(x)*.  
- Example: Clustering.  

### **Note:** The Line Between Supervised and Unsupervised Learning is Blurred  
- The unsupervised problem of *p(x)* can be solved by splitting it into *n* supervised learning problems (decomposition of joint distribution).  
- Supervised learning problems can leverage unsupervised techniques to learn the joint distribution.  

## Semi-Supervised Learning  
- Some examples include a supervision target/label, while others do not.  

## Reinforcement Learning  
- Not just experiencing a fixed dataset, but involving a feedback loop between the learning system and its experiences.  

# Dataset  
A collection of examples.  
# Overfitting and underfitting
* what has been calculated and reduced was base on the training set => **training error**.
* Low training MSE does not mean good performance.
* **Generalization** is the central challenge in machine learning => model will work with new data.
=> We typically estimate the generalization error of machine learning model using a test set of examples that were collected separately from the training set.
**Notes: Train and test data generating process**:
* i.i.d. assumption: examples in each dataset are independent from each other, and that the train set and test set are identically distribute, drawn from the same probability distribution as each other.
* The expected training error of a randomly selected model is equal to the expecte test error of that.
* Factors determining machine learning performance: make the training error small and make the gap between train and test error small.
* **Underfitting**: when the model is not able to obtain a sufficiently low error value on the training set.
* **Overfitting**: when the gap between the training error and testing error is too large.
# No Free Lunch (NFL) theorems for machine learning
* No ML algorithm is universally any better than any other.
# Regularization:
# Hyperparameter & Validation Sets: 
* setting to control the behavior of the learning algorithm.
* are not adapted by the learning algrothim itself.
* should NOT be learned from the training set.
* A validation set that the training algorithm does not observe can be used to tune model hyperparameters => part of training dataset
# Some common terminology:
* Input
* Output
* Parameter
* Capacity
* Hypothesis space
* Features
* Training set
* Validation set
* Test set
