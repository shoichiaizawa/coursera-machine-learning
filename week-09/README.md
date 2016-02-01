Week 9
======

- Anomaly Detection
    - Density Estimation
        - Problem Motivation
        - Gaussian Distribution
        - Algorithm
    - Building an Anomaly Detection System
        - Developing and Evaluating an Anomaly Detection System
        - Anomaly Detection vs. Supervised Learning
        - Choosing What Features to Use
    - Multivariate Gaussian Distribution (Optional)
        - Multivariate Gaussian Distribution
        - Anomaly Detection using the Multivariate Gaussian Distribution
    - Review
        - Quiz: Anomaly Detection
- Recommender Systems
    - Predicting Movie Ratings
        - Problem Formulation
        - Content Based Recommendations
    - Collaborative Filtering
        - Collaborative Filtering
        - Collaborative Filtering Algorithm
    - Low Rank Matrix Factorization
        - Vectorization: Low Rank Matrix Factorization
        - Implementational Detail: Mean Normalization
    - Review
        - Quiz: Recommender Systems
        - Assignment: Anomaly Detection and Recommender Systems

--------------------------------------------------------------------------------

Anomaly Detection
=================

- Density Estimation
    - Problem Motivation
    - Gaussian Distribution
    - Algorithm
- Building an Anomaly Detection System
    - Developing and Evaluating an Anomaly Detection System
    - Anomaly Detection vs. Supervised Learning
    - Choosing What Features to Use
- Multivariate Gaussian Distribution (Optional)
    - Multivariate Gaussian Distribution
    - Anomaly Detection using the Multivariate Gaussian Distribution
- Review
    - Quiz: Anomaly Detection

\[Density Estimation] Problem Motivation
----------------------------------------

Just like in other learning algorithms, we are giving a dataset <i>x<sup>(1)</sup>, x<sup>(2)</sup>, ..., x<sup>(m)</sup></i>.

We are then giving a new example, <i>x<sub>test</sub></i>, and we want to know whether this new example is abnormal/anomalous.

We define a "model" *p(x)* that tells us the probability the examples is not anomalous. We also use a threshold *ε* (epsilon) as a dividing line so we can say which examples are anomalous and which are not.

A very common application of anomaly detection is detecting fraud:

- <i>x<sup>(i)</sup></i> = features of user *i*'s activities
- Model *p(x)* from the data.
- Identify unusual users by checking
- which have *p(x) < ε*.

If out anomaly detector is flagging **too many** anomalous examples, then we need to **decrease** our threshold *ε*.

\[Density Estimation] Gaussian Distribution
-------------------------------------------

TODO: TBA

\[Density Estimation] Algorithm
-------------------------------

TODO: TBA

\[Building an Anomaly Detection System] Developing and Evaluating an Anomaly Detection System
---------------------------------------------------------------------------------------------

TODO: TBA

\[Building an Anomaly Detection System] Anomaly Detection vs. Supervised Learning
---------------------------------------------------------------------------------

When do we use anomaly detection and when do we use supervised learning?

Use anomaly detection when...

- We have a very small number of positive examples (*y = 1* ... 0-20 example is common) and a large number of negative (*y = 0*) examples.
- We have many different "types" of anomalies and it is hard for any algorithm to learn from positive examples what the anomalies look like; future anomalies may look nothing like any of the anomalous examples we've seen so far.

Use supervised learning when...

- We have a large number of both positive and negative examples. In other words, the training set is more evenly divided into classes.
- We have enough positive examples for the algorithm to get a sense of what new positives examples look like. The future positive examples are likely similar to the ones in the training set.

\[Building an Anomaly Detection System] Choosing What Features to Use
---------------------------------------------------------------------

The features will greatly affect how well your anomaly detection algorithm works.

We can check that out features are **gaussian** by plotting a histogram of out data and checking for the bell-shaped curve.

Some **transforms** we can try on an example feature *x* that does not have the bell-shaped curve are:

- <i>log(x)</i>
- <i>log(x + 1)</i>
- <i>log(x + c)</i> for some constant
- <i>√x</i>
- <i>x<sup>1/3</sup></i>

We can play with each of these to try and achieve the gaussian shape in our data.

There is an **error analysis procedure** for anomaly detection that is very similar to the one in supervised learning.

Our goal is for *p(x)* to be large for normal examples and small for anomalous examples.

One common problem is when *p(x)* is similar for both types of examples. In this case, you need to examine the anomalous examples that are giving high probability in detail and try to figure out new features that will better distinguish the data.

In general, choose features that might take on usually large or small values in the event of an anomaly.

\[Multivariate Gaussian Distribution (Optional)] Multivariate Gaussian Distribution
-----------------------------------------------------------------------------------

TODO: TBA

\[Multivariate Gaussian Distribution (Optional)] Anomaly Detection using the Multivariate Gaussian Distribution
---------------------------------------------------------------------------------------------------------------

TODO: TBA

\[Review] Quiz: Anomaly Detection
---------------------------------

TODO: TBA

--------------------------------------------------------------------------------

Recommender Systems
===================

- Predicting Movie Ratings
    - Problem Formulation
    - Content Based Recommendations
- Collaborative Filtering
    - Collaborative Filtering
    - Collaborative Filtering Algorithm
- Low Rank Matrix Factorization
    - Vectorization: Low Rank Matrix Factorization
    - Implementational Detail: Mean Normalization
- Review
    - Quiz: Recommender Systems
    - Assignment: Anomaly Detection and Recommender Systems

\[Predicting Movie Ratings] Problem Formulation
-----------------------------------------------

Recommendation is currently a very popular application of machine learning.

Say we are trying to recommend movies to customers. We can use the following definitions:

- <i>n<sub>u</sub></i> = number of users
- <i>n<sub>m</sub></i> = number of movies
- <i>r(i, j)<sub>m</sub></i> = 1 if user <i>j</i> has rated movie <i>i</i>
- <i>y(i, j)<sub>m</sub></i> = rating given by user <i>j</i> to movie <i>i</i> (defined only if <i>r(i, j)<sub>m</sub></i> = 1)

\[Predicting Movie Ratings] Content Based Recommendations
---------------------------------------------------------

TODO: TBA

\[Collaborative Filtering] Collaborative Filtering
--------------------------------------------------

TODO: TBA

\[Collaborative Filtering] Collaborative Filtering Algorithm
------------------------------------------------------------

TODO: TBA

\[Low Rank Matrix Factorization] Vectorization: Low Rank Matrix Factorization
-----------------------------------------------------------------------------

TODO: TBA

\[Low Rank Matrix Factorization] Implementational Detail: Mean Normalization
----------------------------------------------------------------------------

TODO: TBA

\[Review] Quiz: Recommender Systems
-----------------------------------

TODO: TBA

\[Review] Assignment: Anomaly Detection and Recommender Systems
---------------------------------------------------------------

### An error in `ex8_cofi.m`

There is one error in the second part of Week 9 assignment starter code, `ex8_cofi.m`, for the Recommender Systems questions. A course mentor answered in [a course discussion forum thread](https://www.coursera.org/learn/machine-learning/discussions/YI_8-NrxEeSIcSIAC0EU3g) is that this is a typographical error for a variable used for `fmincg()` and `cofiCostFunc()`. In the original `ex8_cofi.m` file, the second variable in `cofiCostFunc()` is `Y`, but this has to be `Ynorm` instead. Because prior to the function call, we perform normalization on `Y`, creating `Ynorm`, but it is never used. This error does not halt Octave in the middle of its execution, but this error can cause the predicting rating values obtained for the top movie recommendations to be greater than 5, instead they are to be rated between 0 and 10.

Here is the relevant text extract from the [Errata section of the Course Wiki](https://share.coursera.org/wiki/index.php/ML:Errata:_Week_9):

> In ex8_cofi.m at line 199, where theta is trained using fmincg() for the movie ratings, the use of "Y" in the function call should be "<u><b>Ynorm</b></u>". Y is normalized in line 181, creating <u><b>Ynorm</b></u>, but then it is never used. The video lecture "Implementation Detail: Mean Normalization" at 5:34 makes it pretty clear that the normalized Y matrix should be used for calculating theta.

#### Solution

As explained in the text extract above, the second variable of `cofiCostFunc()` in `ex8_cofi.m` needs to be replaced from `Y` to `Ynorm`.

Replace the second variable at line 199 in `ex8_cofi.m` from:

```octave
theta = fmincg (@(t)(cofiCostFunc(t, Y, R, num_users, num_movies, ...
                                num_features, lambda)), ...
                initial_parameters, options);
```

, to:


```octave
theta = fmincg (@(t)(cofiCostFunc(t, Ynorm, R, num_users, num_movies, ...
                                num_features, lambda)), ...
                initial_parameters, options);
```

With this fix, the movie rating values are correctly shown.

##### References

- [Mean Normalization: Why are predictions higher than maximum possible rating?](https://www.coursera.org/learn/machine-learning/discussions/YI_8-NrxEeSIcSIAC0EU3g) -- Machine Learning Course Discussion Forums
- [ML:Errata: Week 9](https://share.coursera.org/wiki/index.php/ML:Errata:_Week_9) -- Machine Learning Course Wiki

