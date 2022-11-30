# Weather-analysis.
## Aim:
To implement data science techniques in weather prediction dataset
## Algorithm:
```
1.Import necessary packages.
2.Implement univariate techniques.
3.Implement bivariate techniques.
4.Implement data visualization techniques.
5.Close the program.
```
## Program with output:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("weather.csv")
df
```
![Output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l1.png?raw=true)
df.head()
![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l2.png)
df.info()
![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l3.png)
df.tail()
![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l4.png)
df.describe()
![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l5.png)
df.shape
![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l6.png)
df['weather'].value_counts()
![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l7.png)
## label encoder:
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

df['wind'] = le.fit_transform(df['weather'])
df.head(10)
![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l8.png)
