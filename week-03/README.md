Week 3
======

- Logistic Regression
    - Classification and Representation
        - Classification
        - Hypothesis Representation
        - Decision Boundary
    - Logistic Regression Model
        - Cost Function
        - Simplified Cost Function and Gradient Descent
        - Advanced Optimization
    - Multiclass Classification
        - Multiclass Classification: One-vs-all
    - Review
        - Quiz: Logistic Regression
        - Assignment: Logistic Regression
- Regularization
    - Solving the Problem of Overfitting
        - The Problem of Overfitting
        - Cost Function
        - Regularized Linear Regression
        - Regularized Logistic Regression
    - Review
        - Quiz: Regularization

--------------------------------------------------------------------------------

### Logistic Regression Model

#### Advanced Optimization

- Optimisation algorithms:
    - [Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent)
    - More advanced and sophisticated algorithms, such as:
        - [Conjugate gradient](https://en.wikipedia.org/wiki/Conjugate_gradient_method)
        - [BFGS algorithm](https://en.wikipedia.org/wiki/Broyden%E2%80%93Fletcher%E2%80%93Goldfarb%E2%80%93Shanno_algorithm)
        - [L-BFGS](https://en.wikipedia.org/wiki/Limited-memory_BFGS)
        - etc

##### Advantages and Disadvantages of these advanced algorithms:

- Advantages:
    - No need to manually pick α (learning rate)
        - Have a clever inner loop (line search algorithm) which tries a bunch of alpha values and picks a good one
    - Often faster than gradient descent
        - Do more than just pick a good learning rate
    - Can be used successfully without understanding their complexity
- Disadvantages:
    - More complex, such as:
        - Could make debugging more difficult
        - Should not be implemented yourself (unless you are an expert in numerical computing)
        - Different libraries may use different implementations – may hit performance

##### Cost Function for logistic regression

```octave
function [jVal, gradient] = costFunction(theta)

jVal = (theta(1)-5)^2 + (theta(2)-5)^2;

gradient = zeros(2,1);
gradient(1) = 2*(theta(1)-5);
gradient(2) = 2*(theta(2)-5);
```

##### Use the `fminunc` function implement this cost function

`fminunc` stands for **Function Minimisation Unconstrained**

```octave
options = optimset ('GradObj', 'on', 'MaxIter', '100');
initialTheta = zeros(2,1)

% `@` symbol in `@costFunction` represents a pointer to the cost funciton
% `fminunc` stands for Function Minimisation Unconstrained
[optTheta, functionVal, exitFlag] = fminunc (@costFunction, initialTheta, options)
```

##### In Octave command line

```octave
>> options = optimset ('GradObj', 'on', 'MaxIter', '100');
>> initialTheta = zeros(2,1)
initialTheta =

   0
   0

% `@` symbol in `@costFunction` represents a pointer to the cost funciton
% `fminunc` stands for Function Minimisation Unconstrained
>> [optTheta, functionVal, exitFlag] = fminunc (@costFunction, initialTheta, options)
optTheta =

   5
   5

functionVal = 0
exitFlag =  1
```

###### References

Octave:

- [20.2 Minimizers – fminunc](https://www.gnu.org/software/octave/doc/interpreter/Minimizers.html#XREFfminunc)

MATLAB:

- [fminunc](http://uk.mathworks.com/help/optim/ug/fminunc.html)
