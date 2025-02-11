# Decision Tree and Random Forest
* A decision tree is an approach to predictive analysis that can help you make decisions.
* We can also build a tree from numeric data or ranked data.
* In ML world,
  * each node represents a Feature (Attribute)
  * Each link (branch) represents a decision (rule).
  * Each leaf represents an outcome.
=> Several ways to measure impurity: "Gini" impurity is the most popular one.
* Smallest Gini => separate the best.
* For decision tree with  numeric data:
  * Sort the patients by weight, lowest to highest.
  * Calculate the middle value between each value.
* Feature Selection
  * We can also create a threshold uch that the impurity reduction mút be large enough to make a big different.
  * Decision trees have disadvantages of being overfit. Simpler trees can avoid overfitting => each split can make a large reduction impurity.
* Common approaches to deal with missing data:
  * Skip the mising data.
  * Pick the most common option => replace with mean and median.
  * Find another column that has the highest correlation with this column and use that as a guide.
  * Decision trees are easy to build, easy to use, and easy to intepret.
  * They work great with the data used to create them, but they are not flexible when applied to new samples.
# Random Forest
* made of decision of trees, combining the simplicity of decision trees with flexibilty resulting in significant improvement in accuracy.
* Assuming there are only 4 samples in original dataset.
* Step 1: create a "bootstrapped" dataset => can pick the same sample more than one.
* Step 2: create a decision tree using the bootstrapped dataset, but only use subset of variables at each steps.
* Variety is what makes random forests more effective than individual trees.
* Bagging (Boostrap aggregating): Bootstrapping w data plus using the aggregate to make a decision => An ensemble technique mainly used to reduce the variance of our predictions by combining the result of multiple classifiers modelled on different sub-samples of the same dataset.
* Generally, 1/3 of the original data are not included in the bootstrapped .
# Support Vector Machine (SVM)
