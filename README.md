---------------------------
Machine-learning-examples
---------------------------

Some work on machine-learning using R, Python , Rstudio and Anaconda

---------------------
Setup the environment.
---------------------

	Step1 - Download and install R. 
		- sudo nano /etc/apt/sources.list
		- add the following line to the list. 
			deb https://ftp.iitm.ac.in/cran/bin/linux/ubuntu xenial/
		- sudo apt-get update
		- sudo apt-get install r-base

	Step2 - Install RSudio
		- download and install on Ubuntu " https://download1.rstudio.org/rstudio-xenial-1.0.153-amd64.deb

	Step3 - Start Anaconda
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
	
	- in Python , import a dataset, declare the working directory and specify the data in the variables
		dataset = pd.read_csv('Data.csv')
		#matrix of features and dependent variable vector
		# we are going to create a matrix of 3 independent variable. 
		X = dataset.iloc[:, :-1].values # ":" means take all the columns except the last one. 
		# create the dependent variable venctor
		Y = dataset.iloc[:,3].values
	- in R
		#import the dataset
		dataset = read.csv('Data.csv')

4.> Missing Data
	- Handle the case of missing data. 
		- one option is to remove the whole row. but thats not good as it contains of crucial data. 
		- option two is to take a mean of values in the column.
		- we'll take option two. Find the mean of the values and fill empty data with that value.  
	- Finding mean with Python.
		- #taking care of missing data. 
		from sklearn.preprocessing import Imputer #to take care of the missing data.
		imputer = Imputer(missing_values= 'NaN', strategy = 'mean', axis = 0) #check what parameters are required to be present here 
		#fit the imputer object in the matrix
		imputer = imputer.fit(X[:,1:3])

		#replace the missing data by the mean of value X
		X[:, 1:3] = imputer.transform(X[:, 1:3]) #method to replace the nan value with the mean of the column.

		#we can take multiple strategies to remove nan values, Mean, Median or most frequently occuring.
	- Finding mean with R
		dataset$Age = ifelse(is.na(dataset$Age),ave(dataset$Age, FUN = function(x) mean(x,na.rm = TRUE)),dataset$Age)



5.> Categorical Data


6.> Splitting the dataset into the Training set and Test set


7.> Feature Scaling 


8.> Data Preprocessing Template

