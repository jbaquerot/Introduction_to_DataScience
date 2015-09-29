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
 
### Introduction to Technologies:
*	iPython / Jupyter
*	Pandas (Data Analysis Library for Python)
*	Apache Spark with Python


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
  * Support Vector Machine
  * K-means
* Aggregation Methods

### Storytelling
* Effective Communication
* Visual Design
* Visual Storytelling

###Introduction to Big Data
* The origin of Big Data
* What is Big Data?
* Introduction to Hadoop HDFS, Map Reduce and Hadoop 2.0
* Big Data project management


## Hardware and Software Requirements

### Minimun Hardware Requirements

You should use a machine with the following minimum hardware requirements:

* Free disk space: 3.5 GB 
* RAM memory: 2.5 GB (4+ GB preferred)
* Processor:  Any recent Intel or AMD multicore processor should be sufficient.

### Supported Operating Systems

We support the following Operating Systems:

* 64-bit (preferred) Windows 7 or later
* 64-bit (preferred) Mac OS X 10.9.5 or later
* 64-bit (preferred) Linux (CentOS 6 or later, or Ubuntu 14.04 or later)
* 32-bit Windows 7 or later
* 32-bit Linux (CentOS 6 or later, or Ubuntu 14.04 or later)

NOTE for Linux users: Based on our testing, please make sure you are using Vagrant 1.7 or newer with Linux. The default Vagrant version packaged with most Linux distributions does not seem to work properly.

(Optional) For the best performance with VirtualBox, we recommend using a machine that supports hardware virtualization features: Intel VT-X or AMD AMD-V. Note that on many systems, the hardware virtualization features first need to be enabled in the BIOS before VirtualBox can use them.

### Required Software Packages

There are two required free software packages:

* Oracle's Virtual Box (https://www.virtualbox.org/)
* Vagrant automatic VM configuration (https://www.vagrantup.com/)

Note: If you already have either software package installed, makes sure that the versions are VirtualBox 4.3.28 (or later) and Vagrant 1.7.2 (or later).

### How to prepare your environment

First of all, download the GitHub project at your local disk.

Then you have two options:
* If you don't have the vagrant box file just run in your console

```vagrant up```

* If you have the vagran box file (package.box) run in your console

```vagrant box add jbaquerot/IntroDataScience path_to\package.box```

```vagrant init jbaquerot/IntroDataScience```

```vagrant up```

###How to access to course notebooks

Open a web browser and write: http:\\localhost:8001
