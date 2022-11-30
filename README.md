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
![Output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l1.png)

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
## data cleaning:
df.isnull().sum()
missing_percentage = (df.isnull().sum())/(df.shape[0])*100
missing_percentage


![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l9.png)

df.duplicated().value_counts()

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l10.png)

## Univariate Analysis:
sns.boxplot(y="wind",data=df)

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l11.png)

sns.countplot(y="weather",data=df)

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l12.png)

sns.histplot(y="wind",data=df)

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l13.png)

## Multivariate Analysis:
sns.scatterplot(df['wind'],df['weather'])

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l14.png)
sns.barplot(data=df, x='wind', y='precipitation')

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l15.png)

df.corr()

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l16.png)
sns.heatmap(df.corr(),annot=True)

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l17.png)

## Data Visualization:
plt.figure(figsize=(20, 7))
sns.lineplot(data=df, x='temp_min', y='temp_max')
plt.show()

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l18.png)
sns.pointplot(x=df['temp_max'],y=df['temp_min'])

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l19.png)
sns.kdeplot(x=df['wind'],data=df)

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l20.png)

sns.countplot(y="precipitation",data=df)

![output](https://github.com/Hemapriya-2004/Mini-Project/blob/main/l21.png)

