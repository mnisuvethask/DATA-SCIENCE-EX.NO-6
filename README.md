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
  import pandas as pd
  
 import seaborn as sns
 
 import matplotlib.pyplot as plt
 
 df=pd.read_csv("titanic_dataset.csv")


 df.head()
<img width="929" height="498" alt="image" src="https://github.com/user-attachments/assets/a0d76ff7-78ac-461e-a122-1556e610117b" />


1.Lineplot:
 x=[1,2,3,4,5]
 
 y=[3,6,2,7,1]
 
 sns.lineplot(x=x,y=y)
 
 plt.title('Line Plot')
<img width="939" height="572" alt="image" src="https://github.com/user-attachments/assets/ce02b3b2-0569-4a0e-9892-8fc7f5a3b3f1" />

2.Multi Line Plot:
 x=[1,2,3,4,5]
 
 y1=[3,5,2,6,1]
 
 y2=[1,6,4,3,8]
 
 y3=[5,2,7,1,4]
 
 sns.lineplot(x=x,y=y1)
 
 sns.lineplot(x=x,y=y2)
 
 sns.lineplot(x=x,y=y3)
 
 plt.title('Multi Line Plot')
 
<img width="922" height="641" alt="image" src="https://github.com/user-attachments/assets/c5642b65-1347-4ad5-b891-5e16f29e7a97" />

TO VISUALIZE RELATIONSHIPS

1.Bar Chart:


 plt.figure(figsize=(8,5))
 
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 
 plt.title("Fare Of Passenger By Embarked Town")
 
<img width="932" height="694" alt="image" src="https://github.com/user-attachments/assets/e7298e40-ee46-4595-9c6b-77179a60d0d1" />

2.Scatter Plot:

 sns.scatterplot(x="Age", y="Fare", data=df)



 plt.title('Scatterplot of Age vs Fare')
 
 plt.show()
 
<img width="914" height="549" alt="image" src="https://github.com/user-attachments/assets/8a4421ab-7b9d-4d02-b039-ea5197f85b1f" />

3.Bubble Chart:

 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 
 plt.show()
<img width="922" height="543" alt="image" src="https://github.com/user-attachments/assets/990402bc-3ca2-44fd-8520-1e96fce0c18c" />

TO CAPTURE DISTRIBUTIONS

1.Histogram

 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
<img width="909" height="520" alt="image" src="https://github.com/user-attachments/assets/bbca0ece-ce61-4948-a6b9-a1becc1e1676" />

2.Boxplot

 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')

 
 plt.title("Age By Passenger Class")
 <img width="931" height="655" alt="image" src="https://github.com/user-attachments/assets/0738a181-2b77-41cb-a872-2c134b89fa73" />

3.Violin Plot

 sns.violinplot(x="Pclass", y="Fare", data=df)
 
 plt.title('Violin Plot of Fare by Passenger Class')
 
 plt.show()
 
<img width="898" height="550" alt="image" src="https://github.com/user-attachments/assets/7a2e58c9-f83d-4978-9e59-493ea4b6d0de" />

4.Density Plot

 sns.kdeplot(data=df['Age'], shade=True)
 
 plt.title('Density Plot of Passenger Ages')
 
 plt.show()
 
<img width="929" height="653" alt="image" src="https://github.com/user-attachments/assets/2daf732b-244c-45b7-9982-2e33fa79d09a" />

5.Heatmap

 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 
 corr_matrix = numeric_df.corr()
 
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 
 plt.title('Heatmap of Titanic Dataset')

 plt.show()
 <img width="942" height="642" alt="image" src="https://github.com/user-attachments/assets/76dca4b7-f032-4b5e-ae71-fb48570587cc" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
