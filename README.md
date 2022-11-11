# acdata [![PyPI version](https://badge.fury.io/py/acdata.svg)](https://badge.fury.io/py/acdata)
Andrews Curves Data Generator: acdata
A repository to create high quality andrews curve data frames, plots, and more!

https://towardsdatascience.com/simple-introduction-to-andrews-curves-with-python-e20d0620ed6b

# Installation 
```
pip install acdata
```
# Importing
```
from acdata import acdata
```
# Usage
```
ac_df = acdata(data, class_column, samples)
```

Parameters
- 'data': pandas dataframe
- 'class_column': target variable string
- 'samples': number of samples to generate from your dataframe integer

# Example
```
from acdata import *

csv_url = 'https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data'
col_names = ['Sepal_Length','Sepal_Width','Petal_Length','Petal_Width','Class']
iris =  pd.read_csv(csv_url, names = col_names)

ac_df = acdata(iris, 'Class', 1000)
```
![image](https://user-images.githubusercontent.com/61998370/200385776-6b6a38a1-3c5b-4a4f-bd3b-07cf0a3dee68.png)


