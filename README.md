# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import dataset and print head,info of the dataset
2.check for null values
3.Import kmeans and fit it to the dataset
4.Plot the graph using elbow method
5.Print the predicted array
6.Plot the customer segments

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: KARTHIKEYAN S
RegisterNumber:  212224230116
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
```
```
data = pd.read_csv('Mall_Customers.csv')
df = pd.DataFrame(data)
df.head()
```
```
df.info()
```
```
df.isnull().sum()
```
```
plt.plot(range(1, 11), wcss)
plt.xlabel("No_of_Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
```
```
km = KMeans(n_clusters=5)
km.fit(df.iloc[:, 3:])
y_pred = km.predict(data.iloc[:, 3:])
y_pred
```
```
df["cluster"] = y_pred
```
```
df0 = df[df["cluster"] == 0]
df1 = df[df["cluster"] == 1]
df2 = df[df["cluster"] == 2]
df3 = df[df["cluster"] == 3]
df4 = df[df["cluster"] == 4]
```
```
plt.scatter(df0["Annual Income (k$)"], df0["Spending Score (1-100)"], c="red", label="cluster0")
plt.scatter(df1["Annual Income (k$)"], df1["Spending Score (1-100)"], c="black", label="cluster1")
plt.scatter(df2["Annual Income (k$)"], df2["Spending Score (1-100)"], c="blue", label="cluster2")
plt.scatter(df3["Annual Income (k$)"], df3["Spending Score (1-100)"], c="green", label="cluster3")
plt.scatter(df4["Annual Income (k$)"], df4["Spending Score (1-100)"], c="magenta", label="cluster4")

plt.legend()
plt.title("Customer Segment")
```

## Output:
### Dataset
![Screenshot 2025-05-15 092421](https://github.com/user-attachments/assets/5241687b-e362-468c-ac09-9646b2caa6c1)

### Dataset Info
![Screenshot 2025-05-15 092428](https://github.com/user-attachments/assets/9f53150b-5570-47ae-bb8f-9f5f60839661)

### Elbow Graph
![Screenshot 2025-05-15 092442](https://github.com/user-attachments/assets/681810c6-a7e9-4d6a-ae26-b9a5f397890a)

### Predicted Value
![Screenshot 2025-05-15 093310](https://github.com/user-attachments/assets/b78a7566-14c3-4864-8273-2fa6ccb3b234)

### Customer Segement Plot
![Screenshot 2025-05-15 092453](https://github.com/user-attachments/assets/e8ec7fe9-6398-4432-a4b1-274d9f839a85)





## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
