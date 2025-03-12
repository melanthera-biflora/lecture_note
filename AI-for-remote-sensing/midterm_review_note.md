# Definition of learning algorithm (28/1/2025)
* A machine learning algorithm is the algorithm that is able to learn from data.
* A computer program is said to learn from experience E with respect to some class of task T and performance measure P, if its performance at task in T, as measured by P, improves with experience E.
* The task T, performance measure P, and experience E can be very broad => can be classification problem, estimation, prediction, etc.
## The task T
* The learning process is not the task. Learning is our means of obtaining the ability to perform the task.
* Machine learning task can be described in terms of how the machine learning system could process an example, i.e., a collection of features that have been quantitatively measured from some object or events that we want the machine learning system to process.
  * feature: the information we use in the model => input data itself is a feature. 
* Mathematically, an "example" can be represented by $x \in R^n$, and each entry $x_i$ of x is a feature.
  * In ML, we should create something that machine can recognize.
  * Machine Learning is a blackbox model (not a equation like traditional method).
* The task T can include:
  * **Classification**: The computer program is asked to specify which of k categories some input belongs to.
    * To solve this task, the learning algorithm will produce a function $f$: $R^n$ -> {1,...,k}, or y = f(x), where y can be numeric code or other variants of the classification, such as probability distribution over class.
    * When some of input might be missing, rather than providing a single classification function, the learning algorithm must learn a set of function. => If you have only few sample => quantify which one has more important role, what is the impact of input data.
  * **Regression (Estimation)**: the computer program is asked to predict a numerical value given some input.
    * To solve this task, the learning algorithm will produce a function: $R^n$ -> $R$. This type of task is similar to classification, except that the format of the output is different.
  * **Transcription**: the machine learning system will observe a relatively unstructured representation of data and transcribe it into discrete, textual form.
    * Google Street View use deep learning to process address number.
  * **Machine Translation**: The computer program will convert a sequence of symbol in some language to another language => encoder - decoder
  * **Anomaly Detection**: The computer program sifts through a set of events or object, and flags some of them as being unsual => cover picture/ include image resolution.
  * **Synthesis and sampling**: The ML algorithm is asked to generate new examples that are similar to those in training data. In some case, we want the sampling or synthesis procedure to generate a specific kind of output given the input.
## The performance measure, P
* The quantitative measure of machine learning performance shoul be specific to task T.
* These performance measure should be computed using a test set of data that is seperated from the data used for training the machine learning system.
* ML for tasks such as classification, classification with missing input, and transcription, we often measure the accuracy of the model: the proportion of examples for which the model produce the correct output. We also obtain equivalent information by measuring error rate (1-0 loss): the proportion of examples for which the model produce an incorrect output.
* For task such as density estimation, we must use a different performance metric that gives model a continuous-valued score for each example.
* MSE is usually used as loss function => The principle is to make sure that MSE is small. Typical approach: Stochastic Gradient Distance (SGD) => We have function, take the derirative which reflects to one of the parameters, force that to 0.
* Why we want to use NMAE more often than NME?
  * Ideally we want the regression line in our prediction is 1:1 line.
  * Sometimes we have overestimation when the estimate is higher than the truth, and sometimes we have underestimation.
  * If we use NME to calculate the mean difference of the estimate and the truth => they may cancel out => look like we have no errors but it's not true => very often we want to use NMAE.       
## Experience E
* The whole learning process is experience E.
* include:
  * **Supervised Learning**: Supervised learning algorithm experience a dataset containing features, but each example is also associated with a label or target. For example, rainfall estimation from satellite observations can use ground radar estimates as label => The learned patterns can predict the values of target attribute in future data instance => learn algorithm when we do have target.
    * involved observing several examples of a random vector $x$ and an associated value of vector $y$, and learn to estimate $y$ from $x$, usually by estimating $p(y|x)$.
    * Ex: regression, classification, structured output problem.
  * **Unsupervised learning**: Unsupervised learning algorithm learn useful properties of the structure of a dataset containing many features. Some unsupervised learning algorithm perform other roles, like clustering, which consists of dividing the dataset into cluster of similar examples. => the data has no target attributes. Ex: you want to separate people into different group/ rate a film.
    * involved observing several examples of a random vector $x$, and attemping to implicitly or explicitly learn the probability distribution p(x), or some interesting properties of that distribution.
    * Ex: density estimation, clustering => K-mean clustering.
* The line between them is often blurred.
  * The decomposition of joint distribution means that we can solve the unsupervised problem of modeling p(x) by splitting it into n supervised learning problems.
\[
p(\mathbf{x}) = \prod_{i=1}^{n} p(x_i \mid x_1, \dots, x_{i-1})
\]

\[
= p(x_1) p(x_2 \mid x_1) p(x_3 \mid x_1, x_2) \dots p(x_n \mid x_1, \dots, x_{n-1})
\]
  *  We can solve the supervised learning problem of \( p(y \mid \mathbf{x}) \) by using unsupervised learning technologies to learn the joint distribution \( p(\mathbf{x}, y) \) and inferring:

\[
p(y \mid \mathbf{x}) = \frac{p(\mathbf{x}, y)}{\sum_{y'} p(\mathbf{x}, y')}
\] 
