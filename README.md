# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

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
import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset('titanic')

sns.countplot(x='survived', data=df)
plt.title('Survival Count')
plt.xlabel('Survived (0 = No, 1 = Yes)')
plt.ylabel('Count')
plt.show()
```
<img width="637" height="512" alt="DS Ex5 - Output 1" src="https://github.com/user-attachments/assets/484d8ab3-2d0f-400d-ba69-745030f77776" />
```
sns.countplot(x='sex', hue='survived', data=df)
plt.title('Survival by Gender')
plt.show()
```
<img width="642" height="510" alt="DS Ex5 - Output 2" src="https://github.com/user-attachments/assets/51c34346-9e59-4295-9226-cc2ba5babc18" />
```
sns.countplot(x='pclass', hue='survived', data=df)
plt.title('Survival by Passenger Class')
plt.show()
```
<img width="638" height="508" alt="DS Ex5 - Output 3" src="https://github.com/user-attachments/assets/976e501a-98c3-4da1-ae91-5858b0cc0e4c" />
```
sns.histplot(df['age'].dropna(), bins=30, kde=True)
plt.title('Age Distribution')
plt.xlabel('Age')
plt.show()
```
<img width="632" height="512" alt="DS Ex5 - Output 4" src="https://github.com/user-attachments/assets/78043c9f-facb-41c4-b1e4-787fa34810e7" />
```
sns.boxplot(x='pclass', y='age', data=df)
plt.title('Age Distribution by Class')
plt.show()
```
<img width="631" height="510" alt="DS Ex5 - Output 5" src="https://github.com/user-attachments/assets/2775e0d6-41f3-42af-91b3-713c238de75e" />
```
corr = df.corr(numeric_only=True)
sns.heatmap(corr, annot=True, cmap='coolwarm')
plt.title('Feature Correlation')
plt.show()
```
<img width="662" height="557" alt="DS Ex5 - Output 6" src="https://github.com/user-attachments/assets/1de7e62e-8872-46dd-a5f2-6e6c2e45a147" />
```
sns.scatterplot(x='age', y='fare', hue='survived', data=df)
plt.title('Fare vs Age (Colored by Survival)')
plt.show()
```
<img width="638" height="510" alt="DS Ex5 - Output 7" src="https://github.com/user-attachments/assets/804cc11e-06ec-4c12-aa1b-bdd2e5a7c19f" />
```
df['embarked'].value_counts().plot.pie(autopct='%1.1f%%')
plt.title('Embarkation Distribution')
plt.ylabel('')
plt.show()
```
<img width="437" height="458" alt="DS Ex5 - Output 8" src="https://github.com/user-attachments/assets/4ab05775-22a6-4ed1-928d-f447c0d8a29c" />
```
sns.pairplot(df[['age', 'fare', 'pclass', 'survived']], hue='survived', palette='coolwarm') 
plt.suptitle("Pairwise Relationships", y=1.02) 
plt.show()
```
<img width="815" height="768" alt="DS Ex5 - Output 9" src="https://github.com/user-attachments/assets/39293184-0f81-45e0-8607-c9ea1541fe10" />

# Result:
Thus, the program to Perform Data Visualization using seaborn python library for the given data was implemented.
