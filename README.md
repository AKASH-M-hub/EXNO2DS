# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT

from google.colab import drive

drive.mount('/content/drive')

![image](https://github.com/user-attachments/assets/b0726552-c363-41e3-babf-81dfb8da711c)

ls /content/drive/MyDrive/Akash/titanic_dataset

![image](https://github.com/user-attachments/assets/03601eba-357c-4851-af3c-7c21d64d4a91)

import pandas as pd

import numpy as np

df=pd.read_csv("/content/drive/MyDrive/Akash/titanic_dataset")

df

![image](https://github.com/user-attachments/assets/d28c9541-3d05-4c2c-970d-11af5e95f71a)

df.isnull()

![image](https://github.com/user-attachments/assets/b0c9e4b8-6bfa-41de-ab14-886683f571d5)

df.info()

![image](https://github.com/user-attachments/assets/9eee972e-2db3-4f15-841b-095ea370d473)

df.shape

![image](https://github.com/user-attachments/assets/f79f72e3-eae6-4d0d-b41b-c99a0110ff1a)

df.nunique()

![image](https://github.com/user-attachments/assets/569c101d-31f2-419a-84ba-06185b018dd0)

df["Survived"].value_counts()

![image](https://github.com/user-attachments/assets/0db15723-113e-4924-adeb-dcfd8a0172d6)

per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)

per

![image](https://github.com/user-attachments/assets/75fc196a-5ded-4280-aca1-298568ab5f8a)

import matplotlib.pyplot as plt

import seaborn as sns

sns.countplot(data=df,x="Survived")

![image](https://github.com/user-attachments/assets/634d68e3-49a9-49e1-8a40-1934d7b09c18)

![image](https://github.com/user-attachments/assets/46208ff6-c624-4873-b973-7e63fec36417)

df.Pclass.unique()

![image](https://github.com/user-attachments/assets/b4afa8c6-7e07-4a6e-b24b-fb84a6037b57)

df.rename(columns={"sex":"Gender"},inplace=True)

df

![image](https://github.com/user-attachments/assets/d93adffd-bcdf-47ca-8b9a-2b2162034721)

df.boxplot(column="Age",by="Survived")

![image](https://github.com/user-attachments/assets/20db8125-26b4-4355-a84d-8b359456318d)

sns.scatterplot(x = df["Age"],y = df["Fare"])

![image](https://github.com/user-attachments/assets/9c03483a-4943-47ea-b87c-3121ca8bca08)

fig,ax1=plt.subplots(figsize=(8,5))

pt=sns.boxplot(ax=ax1,x="Pclass",y="Age",hue="Gender",data=df)

sns.pairplot(df)

![image](https://github.com/user-attachments/assets/b9cd56db-b087-47f1-9a1b-e320f90b7f17)

![image](https://github.com/user-attachments/assets/d11e8b56-2ed2-4fd3-a2c6-90d69faa12ce)


# RESULT
      THUS THE ABOVE CODE IS EXECUETED SUCCESSFULLY....
