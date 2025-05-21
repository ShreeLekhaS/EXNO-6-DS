# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```
### 1. LINE PLOT
```
x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]

plt.figure(figsize=(8, 5))
sns.lineplot(x=x, y=y1, label="Y1")
sns.lineplot(x=x, y=y2, label="Y2")
sns.lineplot(x=x, y=y3, label="Y3")
plt.title("Line Plot Example")
plt.xlabel("X Axis")
plt.ylabel("Y Values")
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/957f0fcc-2cd9-4ee1-8c02-b8be3375a308)

### 2. BAR PLOT
```
tips = sns.load_dataset('tips')

plt.figure(figsize=(8, 5))
sns.barplot(x="day", y="total_bill", data=tips, hue="sex", palette="pastel")
plt.title("Average Total Bill per Day (Grouped by Sex)")
plt.xlabel("Day")
plt.ylabel("Total Bill")
plt.show()
```
![image](https://github.com/user-attachments/assets/3ded0887-363b-4443-80b9-ee05ce26bfd5)

### 3.BAR PLOT 
```
tit = pd.read_csv("titanic_dataset.csv")

plt.figure(figsize=(8, 5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
plt.show()
```
![image](https://github.com/user-attachments/assets/41157aa9-8de2-4905-ba0b-e8a3bc5a2fb3)

```
plt.figure(figsize=(8, 5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
plt.show()
```
![image](https://github.com/user-attachments/assets/295fb3d7-53ce-43b9-8ad7-997aa8d63e62)

### 4. SCATTER PLOT
```
plt.figure(figsize=(8, 5))
sns.scatterplot(x='total_bill', y='tip', data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
plt.show()
```
![image](https://github.com/user-attachments/assets/ebc8a4df-cc0d-4da2-bb0a-834cdc0389fd)

### 5. VIOLIN PLOT
```
plt.figure(figsize=(8, 5))
sns.violinplot(x='Sex', y='Age', data=tit, palette='muted')
plt.title("Distribution of Age by Gender")
plt.show()
```
![image](https://github.com/user-attachments/assets/7ff3afa1-7741-49c4-9c5d-e6056c52cbd1)

### 6. HISTOGRAM
```
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)

plt.figure(figsize=(8, 5))
sns.histplot(marks, kde=True, bins=10, color='skyblue')
plt.title("Distribution of Marks")
plt.xlabel("Marks")
plt.ylabel("Frequency")
plt.show()
```
![image](https://github.com/user-attachments/assets/e6709694-fad5-45e3-ad4e-c9a54494c56e)

### 7. HISTPLOT
plt.figure(figsize=(8, 5))
sns.histplot(data=tit, x='Pclass', hue='Survived', kde=True, multiple='stack', palette='Set2')
plt.title("Passenger Class Distribution by Survival")
plt.xlabel("Passenger Class")
plt.ylabel("Count")
plt.show()

![image](https://github.com/user-attachments/assets/a740c579-a19b-4741-8d92-f49099b3ad0d)

### 8. KDE PLOT
```
plt.figure(figsize=(8, 5))
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='fill', linewidth=3, palette='Set2', alpha=0.8)
plt.title("KDE of Total Bill Grouped by Time")
plt.show()
```
![image](https://github.com/user-attachments/assets/eb02e60d-a098-4607-88df-1db56d50d166)

# Result:
 Thus Data Visualization using seaborn in python library executed successfully
