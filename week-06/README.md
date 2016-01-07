Week 6
======

- Advice for Applying Machine Learning
    - Evaluating a Learning Algorithm
        - Deciding What to Try Next
        - Evaluating a Hypothesis
        - Model Selection and Train/Validation/Test Sets
    - Bias vs. Variance
        - Diagnosing Bias vs. Variance
        - Regularization and Bias/Variance
        - Learning Curves
        - Deciding What to Do Next Revisited
    - Review
        - Quiz: Advice for Applying Machine Learning
        - Assignment: Regularized Linear Regression and Bias/Variance
- Machine Learning System Design
    - Building a Spam Classifier
        - Prioritizing What to Work On
        - Error Analysis
    - Handling Skewed Data
        - Error Metrics for Skewed Classes
        - Trading Off Precision and Recall
    - Using Large Data Sets
        - Data For Machine Learning
    - Review
        - Quiz: Machine Learning System Design

--------------------------------------------------------------------------------

Advice for Applying Machine Learning
====================================

- Evaluating a Learning Algorithm
    - Deciding What to Try Next
    - Evaluating a Hypothesis
    - Model Selection and Train/Validation/Test Sets
- Bias vs. Variance
    - Diagnosing Bias vs. Variance
    - Regularization and Bias/Variance
    - Learning Curves
    - Deciding What to Do Next Revisited
- Review
    - Quiz: Advice for Applying Machine Learning
    - Assignment: Regularized Linear Regression and Bias/Variance

See: https://share.coursera.org/wiki/index.php/ML:Advice_for_Applying_Machine_Learning

Evaluating a Learning Algorithm
-------------------------------

### Deciding What to Try Next

Errors in your predictions can be troubleshooted by:

- Getting more training examples
- Trying smaller sets of features
- Trying additional features
- Trying polynomial features
- Increasing or decreasing λ

Don't just pick one of these avenues at random. We'll explore diagnostic techniques for choosing one of the above solutions in the following sections.

### Evaluating a Hypothesis

TODO: TBA

### Model Selection and Train/Validation/Test Sets

TODO: TBA

Bias vs. Variance
-----------------

TODO: TBA

### Diagnosing Bias vs. Variance

TODO: TBA

![Diagnosing Bias vs. Variance](../images/features-and-polynom-degree.png)

### Regularization and Bias/Variance

TODO: TBA

![Regularization and Bias/Variance](../images/features-and-polynom-degree-fix.png)

### Learning Curves

TODO: TBA

![Typical learning curve for high bias](../images/learning-curve-high-bias.png)

![Typical learning curve for high variance](../images/learning-curve-high-variance.png)

### Deciding What to Do Next Revisited

Our decision process can be broken down as follows:

- Getting more training examples
    - → Fixes **high variance**
- Trying smaller sets of features
    - → Fixes **high variance**
- Adding features
    - → Fixes **high bias**
- Adding polynomial features
    - → Fixes **high bias**
- Decreasing λ
    - → Fixes **high bias**
- Increasing λ
    - → Fixes **high variance**

#### Diagnosing Neural Networks

- A neural network with fewer parameters is **prone to underfitting**. It is also **computationally cheaper**.
- A large neural network with more parameters is **prone to overfitting**. It is also **computationally expensive**. In this case you can use regularization (increase λ) to address the overfitting.

Using a single hidden layer is a good stating default. You can train your neural network on a number of hidden layers using your cross validation set.

TODO: TBA

Review
------

### Quiz: Advice for Applying Machine Learning

### Assignment: Regularized Linear Regression and Bias/Variance

--------------------------------------------------------------------------------

Machine Learning System Design
==============================

- Building a Spam Classifier
    - Prioritizing What to Work On
    - Error Analysis
- Handling Skewed Data
    - Error Metrics for Skewed Classes
    - Trading Off Precision and Recall
- Using Large Data Sets
    - Data For Machine Learning
- Review
    - Quiz: Machine Learning System Design

Building a Spam Classifier
--------------------------

### Prioritizing What to Work On

### Error Analysis

Handling Skewed Data
--------------------

### Error Metrics for Skewed Classes

### Trading Off Precision and Recall

Using Large Data Sets
---------------------

### Data For Machine Learning

Review
------

### Quiz: Machine Learning System Design

