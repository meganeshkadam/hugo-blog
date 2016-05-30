+++

author = "Ganesh Kadam"
categories = ["Meetups and Events"]
date = "2016-05-28T4:30:12+05:30"
description= "May Python Pune Meetup 2016"
linktitle = "/categories/Meetups and Events/"
title = "Data Analysis using Python Pandas"
type = "post"
tags = ["Python-Pune","Data Science","ML"]

+++

Python Pune meetup was held at Amazatic solutions, on 28th May 2016. This meetup was focused on Data Analysis using Python Pandas for Data Science Series.Below are some of the highlights of this workshop which were covered using Case Study :

• Numpy basics

• Pandas Data Structures and basics

• Data Loading

• Data Wrangling (Clean, Transform, Merge)

• Data Aggregation and grouping operations

• Exploratory Data Analysis and Descriptive Statistics

• Plotting and Visualization

[@sudarshan](https://twitter.com/sudarshan1989) was the speaker for this workshop. He is a Data Engineer at NEC Corporation of America and also a regular member of Python Pune Meetup and Data Scientist Meetup of Pune. I missed the first session on Data Science in last month which mainly focused on the basics of Data Science, Machine Learing and Algorithms and related concepts. Thanks to [@sudarshan](https://twitter.com/sudarshan1989) he covered few of the basic concepts in this meetup again.

Datascience is full framework.Machine learning deals with building models.Two major languages used in Datascience are : # R and Python
Apart from some syntactical differences in R and Python, both the languages offer the datastructure most oftenly used in Datacience i.e
Dataframe.

In a typical Datascience workflow, most of the time of Data Scientists is consumed to get the data,analyze the data,sepeartion of data,and cleaning of data, that means almost 70% of the total work in intial phase. Later comes the actual business logic and model building.[@sudarshan](https://twitter.com/sudarshan1989) cleared this understanding about the Data Science.Most of the people wind up enrolling in to some classes and generally don't understand the actual concepts, there is really a need of efforts if you want to be a Data Scientist.

We faced few technical issues during the meetup, in the mean time [@sudarshan](https://twitter.com/sudarshan/1989) started with the basics of numpy. The learning curve to be a good Data Scientist, includes the understanding of python libraries:

- numpy
- python-pandas
- matplotlib
- scikitlearn

Following are few comparisions between numpy and python pandas:

### numpy:

- built for fast array processing, vector operations
- 15 times faster then list
- made for scientific calculations

eg :

```
import numpy as np
imprt pandas as pd

ni = np.array(list)
 type (n1) gives o/p :numpy.ndarray

```
numpy function arrange:

```
7np.arrange(10)  # bydefault int
for float use : np.arrange(10, dtype=np.64)
```

### python pandas :

- Datastructure series - 1d numpy array stores data. its like column in dataframe context
- series also has the index and the value
- To access values in series :

```
ser1.values

```
- To acess the value in index :

```
ser1.index

```
- We can customize the indexes, and can also have duplicates

```
ser2=[1,211,2,1,2,1,2], index=[a,d,d,s,a,s]

```
- We can change the values in series using index
- Dataframe is collection of series like excel sheet
- More the memory More data can be analysed in python pandas

To learn more about python pandas, here is the beautiful website for beginners which has the cook book by [Julia Evans](https://twitter.com/b0rk) and lots of tutorials as well: [Python Pandas](http://pandas.pydata.org/pandas-docs/version/0.15.2/tutorials.html)

We also discussed about the Matplotlib, in one of the case studies.This case study was taken from the website [Kaggle](https://www.kaggle.com/),a website focused on learning Data Science and also has hackathons for the same.Case Study was about the Titanic-Machine Learning from Disaster.[@sudarshan](https://twitter.com/sudarshan1989) explained python pandas can be used effectively to extract the data from the available resources, and build the usefull models.Matplotlib is the library used to mainly produce the charts related to the data. You can generate plots, histograms, power spectra, bar charts, errorcharts, scatterplots, etc, with just a few lines of code.

Finally we disscusssed about the next meetup in which we will be conducting a Hackathon,in continuation with this meetup and try to do some hands on wiht Python Pandas.

Thanks to [@ciypro](https://twitter.com/ciypro) and [@sudarshan](https://twitter.com/sudarshan1989) for giving us the opportunity to learn and volunteer for this meetup.

Here are few resources from [@sudarshan](https://twitter.com/sudarshan1989) that we used for this meetup:

1. [Python Pune Data Analysis with Pandas](https://github.com/sudarshan1413/python_pandas_meetup_2016)
2. [Python for Data Analysis Book](http://www.cin.ufpe.br/~embat/Python%20for%20Data%20Analysis.pdf)
