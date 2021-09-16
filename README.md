# Pandas-Profiling
An example to visualize the correlations and heatmaps of a Scikitlearn dataset using Pandas Profiling library.

## Libraries used:

`
import numpy as np
`
<br>
`
import pandas as pd
`
<br>
`
from pandas_profiling
`
<br>
`
import ProfileReport
`

## Dataset import:

`
from sklearn.datasets import load_diabetes
diab_data = load_diabetes()
`

## Creating a DataFrame and storing the dataset:

`
df = pd.DataFrame(data = diab_data.data, columns = diab_data.feature_names)
`

## Inspection of Data:

`
df.head()
`
<br>
`
df.columns 
`
<br>
`
df.shape
`
<br>
`
df.describe()
`

## Creating a Pandas Profile:

`
profile = ProfileReport(df, title = 'Pandas Profiling Report', explorative = True)
`
## Visualising a Pandas Profile of the Dataset in the Jupyter Notebook:

`
profile.to_widgets()
`

## Visualising a Pandas Profile of the Dataset on a locally hosted server as a webpage: 

`
profile.to_file("output.html")
`
