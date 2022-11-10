# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SANJAY S
RegisterNumber: 22007761 
*/
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers (1).csv")
data.info()
data.head()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No of Clusters")
plt.ylabel("wcss")
plt.title("Elbow method")
plt.plot(range(1,11),wcss)
plt.xlabel("No of Clusters")
plt.ylabel("wcss")
plt.title("Elbow method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
```

## Output:
![ml8op1](https://user-images.githubusercontent.com/115128955/200996309-21cf7615-3670-4b4e-87c7-969ba782954c.png)

![ml8op2](https://user-images.githubusercontent.com/115128955/200996352-d07d3e37-10ab-4861-b4de-f91cc820d458.png)

![ml8op3](https://user-images.githubusercontent.com/115128955/200996370-7a7b12c7-3c65-4a0e-99d0-df13029ab793.png)

![ml8op4](https://user-images.githubusercontent.com/115128955/200996393-59ded61b-80fc-4574-bddf-5cfc50a539a0.png)

![ml8op5](https://user-images.githubusercontent.com/115128955/200996413-f44f4cfa-8e8e-43de-adc1-a56c321cde33.png)

![ml8op6](https://user-images.githubusercontent.com/115128955/200996433-ac426669-3e3b-4e58-9415-4aab8d8313f1.png)

![ml8op7](https://user-images.githubusercontent.com/115128955/200996448-eec236fa-2333-48d4-81ef-ee3939938317.png)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
