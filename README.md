Machine Learning - Stanford University, instructed by Andrew Ng
===============================================================

![Machine Learning](https://coursera.s3.amazonaws.com/topics/ml/large-icon.png)

### About this repository

This is my note repository for [Machine Learning - Stanford University](https://www.coursera.org/learn/machine-learning) course offered at [Coursera.org](https://www.coursera.org/). The notes are currently being used for the session between **2015-11-30** and **2016-02-22**.

At this time, the notes are very disorganised, as in the large part of the text is very exact copy (but typed by me) of the original one given by Professor Ng and other Coursera community members -- I will try to summarise all this as much as possible whenever I can.

### My objective for this course

I decided to take this course as a paid course so my minimum objective for this course is to complete the course successfully within the given time frame; this includes submitting every assignments by the due date.

My goal for this course is, likewise other learners of this course I came across on the internet, to implement the course materials taught using Octave/MATLAB into a different programing language -- **Python** will probably be my language of choice –– after the course completion.

### Terms of Use for Coursera.org

Please note that there is no assignment related file is stored within this repository; they are in my local computer but excluded with the `.gitignore` file.

I am believing that what I do in this repository is legit, however, that said, I would be grateful to anyone kindly enough to point me out any of my possible infringement of the [Honour Code](https://www.coursera.org/about/terms/honorcode) OR the other [Terms of Use](https://www.coursera.org/about/terms) at Coursera.org. In such cases, I will make an immediate action on those files.

Table of Contents
-----------------

- Week 1
    - Introduction
        - Environment Setup Instructions
            - Installing Octave
            - Machine Learning Honor Code
            - Course Resources
        - Introduction
            - Welcome
            - How to Use Discussion Forums
            - Supervised Learning
            - Unsupervised Learning
            - Who are Mentors?
            - Get to Know Your Classmates
            - Frequently Asked Questions
        - Review
            - Quiz: Introduction
        - Course Wiki Lecture Notes
            - Machine Learning Course Wiki
            - Introduction
            - Linear Regression with One Variable
            - Linear Algebra Review
    - Linear Regression with One Variable
        - Model and Cost Function
            - Model Representation
            - Cost Function
            - Cost Function - Intuition I
            - Cost Function - Intuition II
        - Parameter Learning
            - Gradient Descent
            - Gradient Descent Intuition
            - Gradient Descent For Linear Regression
        - Review
            - Quiz: Linear Regression with One Variable
    - Linear Algebra Review
        - Linear Algebra Review
            - Matrices and Vectors
            - Addition and Scalar Multiplication
            - Matrix Vector Multiplication
            - Matrix Matrix Multiplication
            - Matrix Multiplication Properties
            - Inverse and Transpose
        - Review
            - Practice Quiz: Linear Algebra5 questions
- Week 2
    - Linear Regression with Multiple Variables
        - Multivariate Linear Regression
            - Multiple Features
            - Gradient Descent for Multiple Variables
            - Gradient Descent in Practice I - Feature Scaling
            - Gradient Descent in Practice II - Learning Rate
            - Features and Polynomial Regression
        - Computing Parameters Analytically
            - Normal Equation
        - Review
            - Quiz: Linear Regression with Multiple Variables
            - Assignment: Linear Regression
    - Octave Tutorial
        - Octave Tutorial
            - Basic Operations
            - Moving Data Around
            - Computing on Data
            - Plotting Data
            - Control Statements: for, while, if statement
            - Vectorization
            - Normal Equation Noninvertibility
        - Submitting Programming Assignments
            - Working on and Submitting Programming Assignments
        - Review
            - Quiz: Octave Tutorial
- Week 3
- Week 4
- Week 5
- Week 6
- Week 7
- Week 8
- Week 9
- Week 10
- Week 11

--------------------------------------------------------------------------------

Week 1: Introduction
====================

Environment Setup Instructions
------------------------------

The assignments of this course requires [GNU Octave](https://www.gnu.org/software/octave/) or [MathWorks MATLAB](http://uk.mathworks.com/products/matlab/). I chose Octave because it is open-sourced. MATLAB is licensed software, the course takers given free access but this is only valid for 120 days.

### Installing Octave

Instead of installing GNU Octave using the given dmg file (`GNU_Octave_3.8.0-6.dmg`), I chose [Homebrew](http://brew.sh/) as my choice of Octave installation method.

TODO: Summarise my installation steps, possibly in a blog entry or something.

Here is a bunch of references I read upon the Octave installation:

- [Octave for MacOS X](http://wiki.octave.org/Octave_for_MacOS_X)
- [How to install Octave on OS X (Yosemite)](http://adampash.com/how-to-install-octave/)
- [Re: Octave for Mac OSX?](https://lists.gnu.org/archive/html/help-octave/2015-09/msg00060.html)
- [Install Octave on your Mac using Homebrew](http://gabrielsong.me/post/49198871075/install-octave-on-your-mac-using-homebrew)
- [Install Octave on Mac OS X 10.9](http://sumnous.github.io/blog/2014/07/13/install_octave/)
- [Installing Octave on OS X 10.9 Mavericks](http://jatinganhotra.com/blog/2014/01/21/installing-octave-on-os-x-10-dot-9-mavericks/)

### Machine Learning Honor Code

See: https://www.coursera.org/learn/machine-learning/supplement/nh65Z/machine-learning-honor-code

### Course Resources

- [GNU Octave Documentation](http://www.gnu.org/software/octave/doc/interpreter/)
- [Tips from Mentors](https://www.coursera.org/learn/machine-learning/supplement/SFKpu/tips-from-mentors)

Introduction
------------

### Welcome

> Machine Learning exists everywhere without you noticing

- Google/Microsoft's learning algorithms for how to rank web pages
- Face recognition in the iPhoto app
- Anti spam mails judgement

#### Machine Learning

- Grew out of work in AI
- New capability for computers

##### Examples:

- Database mining
    - Large datasets from grouth of automation/web
    - E.g.:
        - Web click data
        - Medical records
        - Biology
        - Engineering
- Applications can't program by hand.
    - E.g.:
        - Autonomous helicopter
        - Handwriting recognition
        - Most of Natural Language Processing (NLP)
        - Computer Vision
- Self-customisation programs
    - E.g.:
        - Amazon, Netflix product recommendations
- Understanding human learning (brain, real AI)

### How to Use Discussion Forums

TODO: See: https://www.coursera.org/learn/machine-learning/supplement/66jBd/how-to-use-discussion-forums

### Supervised Learning

#### Housing price prediction

<u>Supervised Learning</u>: "right answers" given

<u>Regression</u>: Predict continuous value output (price)

#### Breast cancer (malignant, benign)

<u>Classification</u>: Discrete valued output (0 or 1)

- [What is the difference between a benign and malignant tumour?](https://pancreaticcanceraction.org/about-pancreatic-cancer/diagnosis/faq/difference-benign-malignant-tumour/)

- Clump Thickness
- Uniformity of Cell Size
- Uniformity of Cell Shape

#### A quick wrap up question

You're running a company, and you want to develop learning algorithms to address each of two problems.

Problem 1: You have a large inventory of identical items. You want to predict how many of these items will sell over the next 3 months.
Problem 2: You'd like software to examine individual customer accounts, and for each account decide if it has been hacked/compromised.

Should you tree three as classification of as regression problems?

- [ ] Treat both as classification problems.
- [ ] Treat problem 1 as a classification problem, problem 2 as a regression problem.
- [x] Treat problem 2 as a regression problem, problem 2 as a classification problem.
- [ ] Treat both as regression problems.

### Unsupervised Learning

#### Example 1: Google News's data clustering

[Google News](https://news.google.com/) groups a set of news articles found on the web into set of articles about the same story.

##### References

- [Cluster analysis](https://en.wikipedia.org/wiki/Cluster_analysis)

#### Example 2: DNA microarray data

TODO: TBA

##### References

- [DNA microarray](https://en.wikipedia.org/wiki/DNA_microarray)
- [Identifying regulatory mechanisms using individual variation reveals key role for chromatin modification](http://www.c2b2.columbia.edu/danapeerlab/html/pub/pnas2006.pdf) -- a research paper

#### Some more of examples of unsupervised learning

- Organise computing clusters
- Social network analysis
- Market segmentation
- Astronomical data analysis

#### Cocktail party problem

##### Resources:

- [Cocktail party effect](https://en.wikipedia.org/wiki/Cocktail_party_effect)
- [Source separation](https://en.wikipedia.org/wiki/Source_separation)

##### Cocktail Party program algorithm

`[W,s,v] = svd((repmat(sum(x.*x,1),size(x,1).*x)*x'));`

#### A quick wrap up question

Of the following examples, which would you address using an <u>unsupervised</u> learning algorithm? (Check all that apply.)

- [ ] Given email labeled as spam/not spam, learn a spam filter.
- [x] Given a set of news articles found on the web, group them into set of articles about the same story.
- [x] Given a database of customer data, automatically discover market segments and group customers into different market segments.
- [ ] Given a dataset of patients diagnosed as either having diabetes or not, learn to classify new patients as having diabetes or not.

### Who are Mentors?

See: https://www.coursera.org/learn/machine-learning/supplement/JBzFm/who-are-mentors

### Get to Know Your Classmates

See: https://www.coursera.org/learn/machine-learning/supplement/dJCBb/get-to-know-your-classmates

### Frequently Asked Questions

XXX: Helpful info

https://www.coursera.org/learn/machine-learning/supplement/gBboB/frequently-asked-questions

Review
------

### Quiz: Introduction

See: https://www.coursera.org/learn/machine-learning/exam/wjqip/introduction

Course Wiki Lecture Notes
-------------------------

### Machine Learning Course Wiki

This Course Wiki was compiled by learners who took the session-based version of Machine Learning. Many learners took the time to help fellow classmates by sharing information on this site when they solved a tough installation issue or received helpful advice about a review question, programming exercise, or the video lectures. Eventually we'll be transcribing the information contained in the Wiki directly onto the On-Demand platform.

In the interim, please access the wiki here: [https://share.coursera.org/wiki/index.php/ML:Main](https://share.coursera.org/wiki/index.php/ML:Main).

### Introduction

See: https://www.coursera.org/learn/machine-learning/supplement/X64SM/introduction

#### What is Machine Learning?

Two definitions of Machine Learning are offered. Arthur Samuel described it as:

> "the field of study that gives computers the ability to learn without being explicitly programmed." This is an older, informal definition.

Tom Mitchell provides a more modern definition:

> "A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E."

Example: playing checkers.

E = the experience of playing many games of checkers
T = the task of playing checkers.
P = the probability that the program will win the next game.

#### Supervised Learning

In supervised learning, we are given a data set and already know what our correct output should look like, having the idea that there is a relationship between the input and the output.

Supervised learning problems are categorized into **"regression"** and **"classification"** problems. In a **regression** problem, we are trying to predict results within a continuous output, meaning that we are trying to map input variables to some continuous function. In a **classification** problem, we are instead trying to predict results in a discrete output. In other words, we are trying to map input variables into **discrete** categories.

##### Example:

Given data about the size of houses on the real estate market, try to predict their price. Price as a function of size is a *continuous* output, so this is a regression problem.

We could turn this example into a classification problem by instead making our output about whether the house "sells for more or less than the asking price." Here we are classifying the houses based on price into two *discrete* categories.

#### Unsupervised Learning

Unsupervised learning, on the other hand, allows us to approach problems with little or no idea what our results should look like. We can derive structure from data where we don't necessarily know the effect of the variables.

We can derive this structure by **clustering** the data based on relationships among the variables in the data.

With unsupervised learning there is no feedback based on the prediction results, i.e., there is no teacher to correct you. It’s not just about clustering. For example, associative memory is unsupervised learning.

##### Example:

*Clustering*: Take a collection of 1000 essays written on the US Economy, and find a way to automatically group these essays into a small number that are somehow similar or related by different variables, such as word frequency, sentence length, page count, and so on.

*Associative*: Suppose a doctor over years of experience forms associations in his mind between patient characteristics and illnesses that they have. If a new patient shows up then based on this patient’s characteristics such as symptoms, family medical history, physical attributes, mental outlook, etc the doctor associates possible illness or illnesses based on what the doctor has seen before with similar patients. This is not the same as rule based reasoning as in expert systems. In this case we would like to estimate a mapping function from patient characteristics into illnesses.

### Linear Regression with One Variable

See: https://www.coursera.org/learn/machine-learning/supplement/Mc0tF/linear-regression-with-one-variable

- Model Representation
- The Hypothesis Function
- Cost Function
- Gradient Descent
- Gradient Descent for Linear Regression
- What's Next

#### Linear Algebra Review

See: https://www.coursera.org/learn/machine-learning/supplement/NMXXL/linear-algebra-review

Khan Academy has excellent [Linear Algebra Tutorials](https://www.khanacademy.org/#linear-algebra).

This online [Linear Algebra text](https://en.wikipedia.org/wiki/Linear_least_squares_%28mathematics%29#Derivation_of_the_normal_equations) is also an excellent resource, particularly for a proof of the normal equation.

- Matrices and Vectors
- Addition and Scalar Multiplication
- Matrix-Vector Multiplication
- Matrix-Matrix Multiplication
- Matrix Multiplication Properties
- Inverse and Transpose
- Footnotes

Week 1: Linear Regression with One Variable
===========================================

- Model and Cost Function
    - Model Representation
    - Cost Function
    - Cost Function - Intuition I
    - Cost Function - Intuition II
- Parameter Learning
    - Gradient Descent
    - Gradient Descent Intuition
    - Gradient Descent For Linear Regression
- Review
    - Quiz: Linear Regression with One Variable

Week 1: Linear Algebra Review
=============================

- Linear Algebra Review
    - Matrices and Vectors
    - Addition and Scalar Multiplication
    - Matrix Vector Multiplication
    - Matrix Matrix Multiplication
    - Matrix Multiplication Properties
    - Inverse and Transpose
- Review
    - Practice Quiz: Linear Algebra5 questions

--------------------------------------------------------------------------------

Week 2
======

- Week 2: Linear Regression with Multiple Variables
    - Multivariate Linear Regression
        - Multiple Features
        - Gradient Descent for Multiple Variables
        - Gradient Descent in Practice I - Feature Scaling
        - Gradient Descent in Practice II - Learning Rate
        - Features and Polynomial Regression
    - Computing Parameters Analytically
        - Normal Equation
    - Review
        - Quiz: Linear Regression with Multiple Variables
        - Assignment: Linear Regression
- Week 2: Octave Tutorial
    - Octave Tutorial
        - Basic Operations
        - Moving Data Around
        - Computing on Data
        - Plotting Data
        - Control Statements: for, while, if statement
        - Vectorization
        - Normal Equation Noninvertibility
    - Submitting Programming Assignments
        - Working on and Submitting Programming Assignments
    - Review
        - Quiz: Octave Tutorial

Linear Regression with Multiple Variables
-----------------------------------------

TODO: TBA

Octave Tutorial
---------------

### Basic Operations

#### Launch Octave by typing `octave`

```sh
$ octave
GNU Octave, version 4.0.0
Copyright (C) 2015 John W. Eaton and others.
This is free software; see the source code for copying conditions.
There is ABSOLUTELY NO WARRANTY; not even for MERCHANTABILITY or
FITNESS FOR A PARTICULAR PURPOSE.  For details, type 'warranty'.

Octave was configured for "x86_64-apple-darwin15.0.0".

Additional information about Octave is available at http://www.octave.org.

Please contribute if you find this software useful.
For more information, visit http://www.octave.org/get-involved.html

Read http://www.octave.org/bugs.html to learn how to submit bug reports.
For information about changes from previous versions, type 'news'.

octave:1> 5+6
```

#### Basic arithmetic operators: `+`, `-`, `*`, `/`, `^`

```sh
octave:1> 5+6
ans =  11
octave:2> 3-2
ans =  1
octave:3> 5*8
ans =  40
octave:4> 1/2
ans =  0.50000
octave:5> 2^6
ans =  64
```

#### Logical operators: `==`, `~=`, `&&`, `||`, `xor(A,B)`

```sh
octave:6> 1 == 2    % false
ans = 0
octave:7> 1 ~= 2    % true, not `!=` used in other programming languages
ans =  1
octave:8> 1 && 0    % AND
ans = 0
octave:9> 1 || 0    % OR
ans =  1
octave:10> xor(1,0) % XOR, exclusive or
ans =  1
```

#### Prompt profile can be changed by PS1('>> '), pick your style in `''`

```sh
octave:11> PS1('>> ');
>>
>>
```

#### Assigning values in variables

```sh
>> a = 3
a =  3
>> a = 3;           % semicolon suppressing output
>> a=3
a =  3
>> a=3;
>> b = 'hi';
>> b
b = hi
>> c = (3>=1);
>> c
c =  1
```

#### Display a value and print formatting

```sh
>> a=pi;
>> a
a =  3.1416
>> disp(a);
 3.1416
>> disp(sprintf('2 decimals: %0.2f', a))
2 decimals: 3.14
>> disp(sprintf('6 decimals: %0.6f', a))
6 decimals: 3.141593
>> a
a =  3.1416
>> format long
>> a
a =  3.14159265358979
>> format short
>> a
a =  3.1416
```

#### Assigning values to a matrix

```sh
>> A = [1 2; 3 4; 5 6]
A =

   1   2
   3   4
   5   6

>> A = [1 2;
> 3 4;
> 5 6]
A =

   1   2
   3   4
   5   6

>> v = [1 2 3]
v =

   1   2   3

>> v = [1; 2; 3;]
v =

   1
   2
   3

>> v = 1:0.1:2
v =

 Columns 1 through 7:

    1.0000    1.1000    1.2000    1.3000    1.4000    1.5000    1.6000

 Columns 8 through 11:

    1.7000    1.8000    1.9000    2.0000

>> v = 1:6
v =

   1   2   3   4   5   6

>> ones(2,3)
ans =

   1   1   1
   1   1   1

>> C = 2*ones(2,3)
C =

   2   2   2
   2   2   2

>> C = [2 2 2; 2 2 2]
C =

   2   2   2
   2   2   2

>> w = ones(1,3)
w =

   1   1   1

>> w = zeros(1,3)
w =

   0   0   0

>> w = rand(1,3)
w =

   0.92298   0.45152   0.38449

>> w = rand(3,3)
w =

   0.254998   0.602767   0.964442
   0.956797   0.062504   0.885942
   0.441748   0.175175   0.631338

>> w = rand(3,3)
w =

   0.350853   0.848208   0.040288
   0.445533   0.884052   0.840742
   0.214455   0.123800   0.294939

>> w = randn(1,3)
w =

   0.598468  -0.077019  -2.597472

>> w = randn(1,3)
w =

  -0.80322   0.59338   1.68643
```

#### Plotting a graph

```sh
>> w = -6 + sqrt(10)*(randn(1,10000))
>> hist(w)
>> hist(w,50)
```

#### Some other useful functions

```sh
>> eye(4)
ans =

Diagonal Matrix

   1   0   0   0
   0   1   0   0
   0   0   1   0
   0   0   0   1

>> I = eye(4)
I =

Diagonal Matrix

   1   0   0   0
   0   1   0   0
   0   0   1   0
   0   0   0   1

>> I = eye(6)
I =

Diagonal Matrix

   1   0   0   0   0   0
   0   1   0   0   0   0
   0   0   1   0   0   0
   0   0   0   1   0   0
   0   0   0   0   1   0
   0   0   0   0   0   1

>> I = eye(3)
I =

Diagonal Matrix

   1   0   0
   0   1   0
   0   0   1

```

#### `help` command

```sh
>> help eye
>> help rand
>> help help
```

### Basic Operations

### Moving Data Around

### Computing on Data

### Plotting Data

### Control Statements: for, while, if statement

### Vectorization

### Normal Equation Noninvertibility

--------------------------------------------------------------------------------

Week 3
======

--------------------------------------------------------------------------------

Week 4
======

--------------------------------------------------------------------------------

Week 5
======

--------------------------------------------------------------------------------

Week 6
======

--------------------------------------------------------------------------------

Week 7
======

--------------------------------------------------------------------------------

Week 8
======

--------------------------------------------------------------------------------

Week 9
======

--------------------------------------------------------------------------------

Week 10
=======

--------------------------------------------------------------------------------

Week 11
=======

--------------------------------------------------------------------------------

