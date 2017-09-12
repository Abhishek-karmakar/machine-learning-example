---------------------------
Machine-learning-examples
---------------------------

Some work on machine-learning using R, Python , Rstudio and Anaconda

---------------------
Setup the environment.
---------------------

Step1 - Download and install R. 
	- sudo nano /etc/apt/sources.list
	- Add the following line to the list. 
		deb https://ftp.iitm.ac.in/cran/bin/linux/ubuntu xenial/
	- sudo apt-get update
	- sudo apt-get install r-base

Step2 - Install RSudio
	- Download and install on Ubuntu " https://download1.rstudio.org/rstudio-xenial-1.0.153-amd64.deb

Step3 Start Anaconda
	- type "anaconda-navigator" in the terminal.

----------------------
Get the data sets 
---------------------- 
	https://www.superdatascience.com/machine-learning/

------------------------
Data Preprocessing ToDos
------------------------

1.> Get the dataset

	- In every dataset. There is dependent data and independent data. 
	- Using a machine learning model we will try to use the independent data to predict the outcome of the dependent data. 
	- We will do it for all the machine learning models. 
	- Try to make a template so that you can use it to create PreProcess data from all the machine learning models. 


2.> Import the libraries
	- Spread in two parts. Python and R
	- Import Library in Python. 
		import numpy as np #name of the linrary i numpy and shortcut is np
		import matplotlib.pyplot as plt # help to plot nice charts. Intuitive and useful tools. 
		import pandas as pd # library to import and manage datasets.
	- Import Libraries in R
		Dont need to import in the library, Present in the packages tab of RStudio


3.> Import the Dataset


4.> Missing Data


5.> Categorical Data


6.> Splitting the dataset into the Training set and Test set


7.> Feature Scaling 


8.> Data Preprocessing Template

