Week 10
=======

- Large Scale Machine Learning
    - Gradient Descent with Large Datasets
        - Learning With Large Datasets
        - Stochastic Gradient Descent
        - Mini-Batch Gradient Descent
        - Stochastic Gradient Descent Convergence
    - Advanced Topics
        - Online Learning
        - Map Reduce and Data Parallelism
    - Review
        - Quiz: Large Scale Machine Learning

--------------------------------------------------------------------------------

Large Scale Machine Learning
============================

- Gradient Descent with Large Datasets
    - Learning With Large Datasets
    - Stochastic Gradient Descent
    - Mini-Batch Gradient Descent
    - Stochastic Gradient Descent Convergence
- Advanced Topics
    - Online Learning
    - Map Reduce and Data Parallelism
- Review
    - Quiz: Large Scale Machine Learning

\[Gradient Descent with Large Datasets] Learning With Large Datasets
--------------------------------------------------------------------

We mainly benefit from a very large dataset when out algorithm has high variance when *m* is small. Recall that if our algorithm has high bias, more data will not have any benefit.

Datasets can often approach such sizes as m = 100,000,000. In this case, our gradient descent step will have to make a summation over all one hundred million examples. We will want to try to avoid this -- the approaches for doing so are described below.

\[Gradient Descent with Large Datasets] Stochastic Gradient Descent
-------------------------------------------------------------------

TODO: TBA

\[Gradient Descent with Large Datasets] Mini-Batch Gradient Descent
-------------------------------------------------------------------

TODO: TBA

\[Gradient Descent with Large Datasets] Stochastic Gradient Descent Convergence
-------------------------------------------------------------------------------

How do we choose the learning rate *α* for stochastic gradient descent? Also, how do we debug stochastic gradient to make sure it is getting as close as possible to the global optimum?

One strategy is to plot the average cost of the hypothesis applied to every 1000 or so training examples. We can compute and save these costs during the gradient descent iterations.

With a smaller learning rate, it is **possible** that you may get a slightly better solution with stochastic gradient. That is because stochastic gradient descent will oscillate and jump around the global minimum, and it will make smaller random jumps with ta smaller learning rate.

If you increase the number of examples you average over to plot the performance of you algorithm, the plot's line will become smoother.

With a very small number of examples for the average, the line will be too noisy and it will be difficult to find the trend.

One strategy for trying to actually converge at the global minimum is to **slowly decrease *α* over time**.

For example,

```
            const1
α = ------------------------
    iterationNumber + const2
```

However, this is not often done because people don't want to have to fiddle with even more parameters.

\[Advanced Topics] Online Learning
----------------------------------

With a continuous stream of users to a website, we can run an endless loop that gets (*x, y*), where we collect some user actions for the features in *x* to predict some behaviour *y*.

You can update *θ* for each individual (*x, y*) pair as you collect them. This way, you can adapt to new pools of users, since you are continuously updating theta.

\[Advanced Topics] Map Reduce and Data Parallelism
--------------------------------------------------

TODO: TBA

\[Review] Quiz: Large Scale Machine Learning
--------------------------------------------

TODO: TBA

