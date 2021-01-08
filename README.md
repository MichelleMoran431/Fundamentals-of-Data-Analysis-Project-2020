# Fundamentals-of-Data-Analysis-Project-2020


## Project 2020 - Fundamentals of Data analysis. Using the Powerproduction dataset and jupyter notebook

#### NB: All references for this project can be located in the project notebook file project 2020.ipynb


#### Task
To perform and explain simple linear regression using Python on the powerproduction dataset available on Moodle.

The goal is to accurately predict wind turbine power from wind speed values using the data set as basis. It must contain the following : 

- Jupyter notebook that performs simple linear regression on the dataset
- An explanation of your regresssion and an analysis of its accuracy
- Standard items in a git repository such as a README

Further information to enhance submission : To compare the simple linear regression to other types of regression on this data set.

#### Packages

The following packages were used to run statistical analysis and visualise the graphs for this project.

Python https://www.python.org/downloads/

Anaconda https://www.anaconda.com/distribution/ - is the easiest way to perfrom Python data science machine learning on Linux, Windows and Mac OS.

Pandas https://pandas.pydata.org/ - pandas is an "open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tool."

Scripy https://pypi.org/project/Scripy/ - which allows the user to run system commands in the same shell through it's main tool *shell.Run().

Numpy http://www.numpy.org/ - is the fundamental package for scientific computing within Python.

Matplotlib https://matplotlib.org/ - is a 2D plotting library within Python within which the user can generate a wide variety of figures, including plots, histograms, scetterplots etc.

Seaborn https://seaborn.pydata.org/ - is a Python data visualisation library based on matplotlib. It provides a high level interface for drawing infromative statistical graphs.

Ploty https://plot.ly/ - Plotly provides online graphing, analytics, and statistics tools for individuals and collaboration, as well as scientific graphing libraries for Python, R, MATLAB, Perl etc.

Cufflinks https://plot.ly/python/v3/ipython-notebooks/cufflinks/

Scikit-learn https://scikit-learn.org - Scikit-learn is a simple and effecient tool for data mining and data analysis.

#### Importing packages
The above packages can be imported into Python. Use Import function in Python as follows:

Import libaries that will be used in this project

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import scikit-learn as sklearn
Importing the data


#### Contents of GitHub Respository

The GitHub Respository associated with this project contains the following:


Project 2020.ipynb - Jupyter Notebook outlining the analysis of the powerproduction.csv database containing python code and description of the analysis.
Project 2020 Folder - Contains the powerproduction.csv file
PDF files : Reference literature relating to windturbines analysis
Various images

#### Project Notebook Synopsis

##### Introduction 

- A definition of what simple linear regression is and its variables in terms of the powerproduction dataset

- The 4 assumptions of Linear regression defined and their importance

- The 4 steps of building a Simple linear regression model : setting the analysis of the powerproduction dataset

##### Simple Linear Regression of the powerproduction dataset applied : 


       1. Importing the PowerProduction dataset - Using pandas library to import. Called dfpower

       2. Data Checking and pre-processing - Making sure that the dataset import correctly and fully. using .head() and .tail() functions.Using .describe() to review the statistics of the dataset.
         - DataProcessing looked at the presence of outliers using scipy-stats package containing z-score and interquartile range calculations.
 
        3. Visualisation of the dataset - using matplotli.plot as plt ,and scatter plot to show the relationship between the variables windspeed and power. Setting the graphing parameters :style and size

        Included here was a short note on the workings of numpy.polyfit and its importance in the regression calculations of this project.

        4. The Coefficients m and c were calculated using numpy,polyfit and then used to fit the best line to the data 
   
 - Correlation Coefficients - the various types described and calculated using scipy.stats
 
##### Conclusion


Advanced Statistical parameters and residual plots for a linear regression model : Further information using OLS() and residual plots to determine if simple linear regression is the best type to use for these variables


##### Other Regression  and methods 

The other regression model choosen is the polynomical model. 

3 degrees of polynomical regression was determined, coded and plotted and compared. 

linear, cubic and quadratic , each with increasing constants

The code was the same for each type , with the last argument been the degree of polynomial and this changed

z = np.polyfit(x,y,2)
poly1d_fn = np.poly1d(z) 
print(poly1d_fn)
#poly1d_fn is a function which takes in x and returns an estimate for y

Each was plotted and using sklearn.metrics the r2 score calculated

A comparison was completed of the r2 values and observing the data points on the actual curve. The Quadratic polynomial looked accurate

##### Comparison of Linear regression and Polynomial regression 

Importing the following : 

import numpy as np
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures
import pandas as pd

import matplotlib.pyplot as plt


Importing the dataset and reshaping it to convert forn 1-d to 2-d arrays

A linear regression model and polynomial regression model was fitted to the dataset dfpower using sklearn packages and a prediction was done using a random value for windspeed.

The class poly_reg imported from PolynomialFeatures ,is a transformer tool , where it transform  x ( 1 column)into x_poly ( 3 columns).

and x_poly is used in the prediction of the y values.







