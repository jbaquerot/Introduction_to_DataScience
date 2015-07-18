# Introduction_to_DataScience
Material to Introduction to DataScience Course

## Aims and outcomes
The Introduction to Data Science course will provide you with an in-depth understanding of practice of Data Science and its application in Big Data projects. You will also gain practical skills in handling structured and unstructured data, analysing and visualising data, data mining, machine learning, as well as gaining hands-on experience of software tools used and their use in real-world settings.

## Course Themes:
Machine learning and data mining algorithms; prediction vs. description; exploratory data analysis; Big Data; Data Visualisation; data processing; munging and engineering; asking good questions; business / problem understanding; storytelling; communication.

## Syllabus

### Introduction to Data Science
* What Data Science is?
* New skill: Data Scientist
* Data Science Areas
* Problems that solve Data Science

### Data Science Process
* Data Science is a Science (not an Engineering)
* The Scientific Method
* Data Mining Process
* Data Science Process Explained


### Business/Problem Understanding
* The importance of understand the business
* How to understand the business?
* Tips in developing business knowledge

### Data Management
* Getting data from Databases, Text files, MS Excel files, JSON
* Getting data from WWW: bulk download, API access (Twitter), Web Scrapping
* Data Cleanup
* Data Manipulation: Filtering, Transforming, Aggregating and Sorting

### Data Exploration
* Visual Analytics Process
* Exploratory Data Analysis
* Data Types
* Data Visualisation
* Graph Types

### Modeling
* What is a Model?
* The learning problem
* Types of learning
* The linear model
* Error and noise
* Bias-Variance tradeoff
* Learning Curves
* A Key Analytical Framework: Expected Value
* Overfitting, Regularisation and Validation
* Learning Principles
* Learning Aides: 
  * Data Transformations
  * Dimension Reduction and Feature Selection (PCA)
* Models:
  * Logistic Regression
  * Decision Trees
  * Random Forests
  * Neural Networks
  * Support Vector Machine
  * K-means
  * Hierarchical Clustering
* Aggregation Methods

### Storytelling
* Effective Communication
* Visual Design
* Visual Storytelling

###Introduction to Big Data
* The origin of Big Data
* What is Big Data?
* Introduction to Hadoop HDFS, Map Reduce and Hadoop 2.0
* Introduction to Apache Spark
* Big Data project management




Dockerized Notebook Data Science
======================

Docker container with Python data science tools (particularly, pandas, numpy, matplotlib, plotly, sklearn, scikit-image, nltk, gensim, psycopg2) the IPython notebook (single user). 

## Creating docker image

Creating ipython docker image

```
cd docker
docker build -t  datascience-base .
``` 

## Runing the container

```
cd ..
docker run -d -p 80:8888 -v "$(PWD)"/data:/workspace/data -v "$(PWD)"/notebooks:/workspace/notebooks/ -e "PASSWORD=<TO_CHANGE>" datascience-base
```


If you are on OSX, you'll need to know the name of your VM from boot2docker:

```
 boot2docker ip
```

You'll then connect via `http://<ip>`