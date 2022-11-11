# andrewscurves [![PyPI version](https://badge.fury.io/py/andrewscurves.svg)](https://badge.fury.io/py/andrewscurves)
Official repository to create high quality andrews function data and high quality plots

https://towardsdatascience.com/simple-introduction-to-andrews-curves-with-python-e20d0620ed6b

# Installation 
```
pip install andrewscurves
```
# Importing
```
from andrewscurves import *
```
# Usage
```
andrewscurves(data, class_column, samples):
    """
    Parameters
    ----------
    data : pandas.DataFrame
        input a pandas dataframe
    class_column : str
        target or class column of your pandas dataframe
    samples : int
        integer representing number representative samples to generate

    Returns
    -------
    df : pandas.DataFrame
        output a pandas dataframe with andrews function spacing and covariates along with feature columns

```

Parameters
- 'data': pandas dataframe
- 'class_column': target variable string
- 'samples': number of samples to generate from your dataframe integer

# Examples
```
from andrewscurves import andrewscurves
import pandas as pd

csv_url = 'https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data'
col_names = ['Sepal_Length','Sepal_Width','Petal_Length','Petal_Width','Class']
iris =  pd.read_csv(csv_url, names = col_names)

ac_df = andrewscurves(iris, 'Class', 1000)
```
![image](https://user-images.githubusercontent.com/61998370/201253192-92cdc60b-98b1-4aa2-864f-1b015e308af0.png)
```
from andrewscurves import plotly_andrews_curves

plotly_andrews_curves(iris, 'Class',100)
```
![image](https://user-images.githubusercontent.com/61998370/201253413-608faf6a-cb71-4f64-ba6a-2e2c49b3127b.png)
```
from andrewscurves import seaborn_andrews_curves

seaborn_andrews_curves(iris, 'Class',50)
```
![image](https://user-images.githubusercontent.com/61998370/201253555-709b96a9-4dbb-41dd-a940-16340b0a4e0b.png)
```
from andrewscurves import mpl_andrews_curves
import matplotlib.pyplot as plt
plt.figure(figsize=(15,8)) ##set figsize with plt like a typical mpl plot

mpl_andrews_curves(iris, 'Class',100)
```
![image](https://user-images.githubusercontent.com/61998370/201253683-7844b1d5-ee9d-44d8-b958-fb744aeafbd3.png)
```
from andrewscurves import hvplot_andrews_curves

hvplot_andrews_curves(iris, 'Class',100)
```
![image](https://user-images.githubusercontent.com/61998370/201253764-77913a44-ec11-46d2-9092-c432dafcf4cf.png)
