### Cross-validation
* Divide dataset into a fixed training set and a fixed test set can be problematic (if the test set is too small)
        * If the dataset has hundred of thousands of example or more, this is not a serious issue.
        * A small test set implies statistical uncertainty around the estimated average test error, making it difficult to claimthat one algorithm works better than another on the given task.
* We can repeat the training and testing processes on different randomly chosen subsets of the original dataset.
### Bootstrapping
* Similar technique for estimating the confidence in model parameters $\theta$
* Procedure:
        * Draw k hypothetical datasets from original data. Either via cross validation or sampling with replacement.
        * Fit the model for each dataset to compute parameters $\theta$ (k).
        * Return the standard deviation of $\theta$ (1), ..., $\theta$ (k).
* Leave-one-out (n-fold cross validation)
* k-fold cross-validation:
        * Split the dataset into k non-overlapping subset (can shuffle)
        * The test error can be estimated by taking the average test error across k trials.
### Estimator, Bias and Varience in Machine Learning (?????)
* Function estimation/ approximation
* Bias in ML: The sample mean is an unbiased estimator of Gaussian mean parameter & The sample variance is a biased estimator of the variance of a Gaussian distribution.
* Leverage Bias and Variance to Minimize Mean Squared Error
  * Bias and variance measure two different sources of error in an estimator.
  * Bias measures the expected deviation from the true value of the function or parameter.
  * Variance provides a measure of the deviation from the expected estimator value that any particular sampling of the ata is likely to cause.
A choice between 2 estimators, one with more bias and one with more variance, how do we choose between them => use cross-validation, also compare the mean square error (MSE).
In the case where generalization error is measured by the MSE, increasing capacity tends to increase variance and decrease bias.
