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

What data is available (structured (xls) or unstructured (images for example)).

### 3. Evaluation

What is the success criteria? For example, the model must be 95% accurate at predicting heart disease.

### 4. Features

What do you know about the data? For example, if a scientific study shows that weight over x leads to a higher chance of heart disease, you can use that as part of the algorithm.

### 5. Modelling

Which model (supervised, unsupervised or reinforcement) should you use?

### 6. Experimentation

What have you tried and what could you try?
