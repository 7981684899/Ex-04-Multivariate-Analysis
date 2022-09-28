                       EX NO 4 : Multivariate Analysis
AIM:

   To Perform Multivariate Analysis
Algorithm:

1.Read the given data

2.Get information from the data

3.Perform the Multivariate Analysis

4.Save the clean data to file

Program:

reading the file
import pandas as pd

import seaborn as sns

df=pd.read_csv("/content/SuperStore.csv")

data=df

Scatterplot
import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

sns.scatterplot (df['Postal Code'],df['Sales'])

image

Barplot
import pandas as pd

import seaborn as sns

sns.barplot (x=df["Postal Code"], y=df["Sales"], data=df)

image

Scatterplot
import pandas as pd

import seaborn as sns

sns.scatterplot(df["Postal Code"], y=df["Sales"], hue=df['Row ID'])

image

df.info()

image

states=df.loc[:,["Postal Code","Sales"]]

states=states.groupby(by=["Postal Code"]).sum().sort_values(by="Sales")

sns.barplot(x=states.index,y="Sales",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Postal Code")

plt.ylabel=("SALES")

plt.show()

image

states=df.loc[:,["Segment","Sales"]]

states=states.groupby(by=["Segment"]).sum().sort_values(by="Sales")

#plt.figure(figsize=(10,7))

sns.barplot(x=states.index,y="Sales",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Segment")

plt.ylabel=("Sales")

plt.show()

image

import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/SuperStore.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()

image

Result: Multivariate-Analysis is performed on given data and saved


