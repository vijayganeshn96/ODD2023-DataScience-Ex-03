# Ex03-Univariate-Analysis

## AIM:

To perform Univariate EDA on the given data set

## Explanation:

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis

## ALGORITHM:

### STEP 1:
Import the built libraries required to perform EDA and outlier removal.

### STEP 2:
Read the given csv file

### STEP 3:
Convert the file into a dataframe and get information of the data.

### STEP 4:
Return the objects containing counts of unique values using (value_counts()).

### STEP 5:
Plot the counts in the form of Histogram or Bar Graph.

### STEP 6:
Use seaborn the bar graph comparison of data can be viewed.

### STEP 7:
Save the final data set into the file

## PROGRAM:
```py
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv("iris.csv")
df.head()
df.tail()
df.nunique()
df.iloc[:,4].value_counts()
for i in range(0,df.shape[1]):
  print("-------------",df.columns[i],"-------------")
  print(df.iloc[:,i].value_counts())
  print("-------------------------------------------")
sns.countplot(x='species',data = df)
dfv = df.loc[df['species']=='virginica']
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
dfs = df.loc[df['species']=='sentosa']
dfc = df.loc[df['species']=='versicolor']
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'*')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'*')
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()
```

## OUTPUT:


![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/3cd5cdee-321e-4279-a03e-1c4630e04d43)

![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/8a4a1a8b-cfd6-4bc1-bf82-937d28cda633)

![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/811f6e2a-8237-483c-b1c9-63a435818940)

![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/92e61b43-d3f2-41e2-993c-f262d37aff29)

![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/a6be20ed-da4e-4f2e-9f94-5dcf6ff2282e)

![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/75b39eee-719e-477c-bc90-795b5efc09db)

![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/393b88e8-3f7b-4e6d-ba3f-087c1bd84009)

![image](https://github.com/Anbuselvan04/Ex03-Univariate-Analysis/assets/119410896/7b4164fd-9197-4f0a-b6ab-b55f983697d7)



## RESULT:

Thus the program to perform EDA on the given data set is successfully executed
