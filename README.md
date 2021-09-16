# Pandas-Profiling
An example to visualize the correlations and heatmaps of a Scikitlearn dataset using Pandas Profiling library.

#Libraries used:
`code`
import numpy as np
import pandas as pd
from pandas_profiling import ProfileReport

#Dataset import:
`code`
from sklearn.datasets import load_diabetes
diab_data = load_diabetes()

#Creating a DataFrame and storing the dataset:
`code`
df = pd.DataFrame(data = diab_data.data, columns = diab_data.feature_names)

#Inspection of Data:
`code`
df.head()
df.columns
df.shape
df.describe()

#Creating a Pandas Profile:
`code`
profile = ProfileReport(df, title = 'Pandas Profiling Report', explorative = True)

#Visualising a Pandas Profile of the Dataset in the Jupyter Notebook:
`code`
profile.to_widgets()

#Visualising a Pandas Profile of the Dataset on a locally hosted server as a webpage: 
`code`
profile.to_file("output.html")
