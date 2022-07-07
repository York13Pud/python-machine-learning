# Data Science and Machine Learning Notes

Reference: Learning started on Friday, first of July 2022 (01/07/2022).

## What is AI, Data Science and Machine Learning?

- AI: Human intelligence replicated by a computer. This is currently limited to narrow-AI, which means it is single purpose with no real adaptability to do other things, which is termed general AI.
- Data Science: Data analysis that looks at ways to make use of data.
- Machine Learning: An ability to find patterns in a collection of data and make predictions / recommendations based on that data. It uses an algorithm (called a model) to do analysis against a data set and look for patterns and make predictions based on that models analysis.
- Deep Learning: An algorithm used in machine learning.

![AI, DS and ML](/assets/images/notes/001-what-is-ai-ds-ml.png)

## Types of MAchine Learning

![ML Types](/assets/images/notes/002-ml-types.png)

### Supervised Learning

Using data that has structure, such as a spreadsheet, CSV file or database and will attempt to label the data. There are two types:

- Classification: Is this data one thing or another? Is binary (this or that - has or hasn't got heart disease) or has multiple classification possibilities (multiple labels (dog breads)).
- Regression: Trying to predict a number. For example, the price of a house based on its attributes.

### Unsupervised Learning

Using data that has no defined structure / labels, such as a CSV file with no column names. ML will be used to create categories for the data and group up alike data points into those categories (clustering).

It can also use multiple data points that can be used together to create associations that can be used by ML to make recommendations based on a number of data points.

### Transfer Learning

Allows another machine learning model to make use of the results from another machine learning model. For example using one model to determine the type of car in a photo and then sending that result to another model to determine if the car has a chip in the windscreen that needs fixing or it's missing a wing mirror.

### Reinforcement Learning

Teaching a model to learn by repeating something, such as playing a game until it gets good at it. Also called skill acquisition and real-time learning.

## ML Framework

![ML Framework](/assets/images/notes/003-ml-framework.png)

The three main stages are:

- Data collection - Where will the data come from?
- Data modelling - This is the main focus of the machine learning framework  and has six steps.
- Deployment

Data modelling steps:

### 1. Problem Definition: What problem are you looking to solve?

Is machine learning the right approach? If not, don't use it.

If ML is the right thing, you then need to decide which type of learning (supervised, unsupervised, transfer or reinforcement) you should use based on the problem you are needing to solve.

### 2. Data

What data is available (structured (xls/csv for example) or unstructured (images or text for example)).

In addition, there is static data, meaning data that doesn't change its values or schema. This is the type of data you typically start with whilst starting out in data science.

Streaming data is data that changes constantly. For example, stock prices.

A typical starter data science workflow will look like the below.

![DS Workflow](/assets/images/notes/004-ds-typical-workflow.png)

### 3. Evaluation

What is the success criteria? For example, the model must be 95% accurate at predicting heart disease.

![Types of Metrics](/assets/images/notes/005-metric-types.png)

### 4. Features

What do you know about the data? For example, if a scientific study shows that weight over x leads to a higher chance of heart disease, you can use that as part of the algorithm.

![Features of Data](/assets/images/notes/006-features-of-data.png)

- Numerical features: Data that is numerical.
- Categorical features: Data that can be categorised, such as gender.
- Derived features: Data that is created from existing data. For example, adding two columns together, with the result stored in a column you created.

Feature coverage is where samples of data have the same data points (columns for example) filed in. If not, this can skew the results in a model and may mean that some data needs to be removed, which can result in a model that doesn't work. The fix for that is to get more data, ideally the data points that were missing.

### 5. Modelling

Which model (supervised, unsupervised or reinforcement) should you use?

There are three parts to modelling:

1. Choosing and training a model
2. Tuning a model
3. Model comparison

#### Choosing and training a model

![Model Split](/assets/images/notes/007-model-split.png)

Generalisation is the ability for a machine learning model to perform well in a data set it hasn't seen before. Think of it like an exam, you go over the course materials (training set), you then do a practice exam (validation set) and then do the final exam (test set) with the final exam taking elements from the validation and test sets to hopefully pass.

![Model Split Example](/assets/images/notes/008-model-split-2.png)

When training models, start with a small subset of the data to see how it goes. All being well, add more data and do it again. If not, perhaps you can change the model you're using.

Don't be afraid to experiment.

#### Tuning a model

An example of this could be changing the temperature you use to cook something, along with the time it should take to cook.

- ML models have hyperparameters you can adjust
- the first results of a model are not the last
- Tuning can take place on training or validation data sets

#### Model comparison

![Modelling Stages Final](/assets/images/notes/009-modelling-stages.png)

Results from the training and test data sets should be close to each other within a small margin of different.

![Over and Under Fitting](/assets/images/notes/010-over-under-fitting.png)

If the training results performance is higher than the tests performance, this is called underfitting. The opposite of this (Test is higher than training) is called overfitting.

The ideal situation is called balanced. This is in between under and over fitting.

![Balanced Fitting](/assets/images/notes/011-balanced.png)

Data leakage occurs when data leaks between the steps. For example, data in the training data is also present in the test data.

Data mismatch is where you have different data in the training and testing sets.

![Under / Over Fitting Fixes](/assets/images/notes/012-fitting-fixes.png)

Things to Remember:

- Avoid over and under fitting
- Keep the test set separate
- Compare apples to apples
- Once best performance metric does not equal the best model

### 6. Experimentation

What have you tried and what could you try?

## Tools to Use

![Tools](/assets/images/notes/013-tools.png)

### Software Distribution Options

- Anaconda: Big installer, one and done.
- Mini-Conda: Smaller installer with less installed by default. This will be what is used for the course.

### Package Manager Options

- Conda: It is a CLI package manager for both Anaconda and Mini-Conda. This will be what is used for the course.
- Anaconda Navigator: A GUI package manager.

### Installing Mini-Conda

Download it and go next, next, next and finish!

### Using Conda

Once installed, open a terminal and you will see base as the source environment. Mini-Conda creates an environment called base by default. To get back to the normal environment, use `source ~/.zshrc` in the cli.

## Using Mini-Conda and Conda

### Create New Environment

Create a new conda (virtual) environment, with packages put in ./env and install a list of packages.

``` console
conda create --prefix ./env pandas numpy matplotlib scikit-learn
```

Another option to create a conda environment is to use --name instead.

``` console
conda create --name sample-project pandas numpy matplotlib scikit-learn
```

Be aware though that using --name will put it into the location you installed miniconda to.

### Activate and Deactivate a New Environment

To activate the environment, run either:

``` console
# If you used the --prefix to create the env
conda activate /path/to/env
```

Or

``` console
# If you used the --name to create the env
conda activate name-of-env
```

To deactivate an env, run

``` console
conda deactivate
```

### Install / Uninstall Additional Packages

Install packages:

``` console
conda install package-1 package-2
```

Remove packages:

``` console
conda remove package-1 package-2
```

### Exporting a Conda Environment

Similar process 

``` console
conda env export --prefix ./Desktop/project_1/env > environment.yml
```

### Create a Conda Environment from an Export

conda env create --file environment.yml --name env_from_file