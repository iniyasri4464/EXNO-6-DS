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
### Register no-212223230081
### Developed By-INIYASRI S

```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```

![image](https://github.com/user-attachments/assets/0b7a6e45-f701-49c0-9ef3-d1e731b722e4)

```
df=sns.load_dataset("tips")
df
```

![image](https://github.com/user-attachments/assets/3df0a554-137a-4c54-80c2-a0df7d156eaa)


```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/user-attachments/assets/c3d22cfb-6dd3-417c-a5d9-678a4b633afe)

```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.xlabel('X Label')
plt.ylabel('Y Label')
```

![image](https://github.com/user-attachments/assets/af108e69-eb5a-4572-a98c-fc70900a4fb1)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tips=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2=plt.bar(avg_tips.index, avg_tips, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

![image](https://github.com/user-attachments/assets/b743d41c-ce4b-40ce-b7da-9789b5a96358)

```
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tips=tips.groupby('day')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill, label='Total Bill',width=0.4)
p2=plt.bar(avg_tips.index,avg_tips,bottom=avg_total_bill, label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

![image](https://github.com/user-attachments/assets/99dd40c0-b090-4cb4-b764-21a6065b5519)

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.937,0.9375,0.9372,0.939,0.9392]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```

![image](https://github.com/user-attachments/assets/937d6b07-d72d-4553-a2ce-189532867343)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of te week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/0ab51186-37da-4fe6-ada5-4427fbb7b83a)

```
import pandas as pd
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/dec3ed99-abb2-4d1e-9428-158d8bd0da1a)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/8a3e26f9-cdf0-4493-86f7-7dc4639de1a9)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")

```

![image](https://github.com/user-attachments/assets/076ab6ee-0b57-41a9-b4cc-642fb8c1ad0e)

```
import seaborn as sns
tips= sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y = 'tip',hue='sex',data=tips)
plt.ylabel('Tip Amount')
plt.xlabel('Total Bill')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/845a764a-3ecd-4744-bf5e-e05633293ea2)

```
import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(1)
num_var = np.random.randn(1000)
num_var = pd.Series(num_var, name="Numerical Variable")
num_var
```

![image](https://github.com/user-attachments/assets/467be0d4-ce69-48eb-ba0c-480350a648a1)

```
sns.histplot(data = num_var, kde=True)
```

![image](https://github.com/user-attachments/assets/22ba94e4-d57f-4e8c-a1dd-11401aa4ddc0)


```
import pandas as pd
df=pd.read_csv("titanic_dataset.csv")
df
```

![image](https://github.com/user-attachments/assets/8df8ab5c-b33c-4baf-b4f3-0c7c1b182ad2)

```
sns.histplot(data = df,x = "Pclass",hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/d209b101-f24e-4bdb-8322-4e545961edcb)

```
import seaborn as sns
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)
marks
```
![image](https://github.com/user-attachments/assets/b6037be8-2e1e-461a-88c4-f40f5ac3ab93)

```
sns.histplot(data = marks, bins=10,kde=True,stat='count', cumulative=False, multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Students Marks')
```
![image](https://github.com/user-attachments/assets/78412624-da1c-4834-83ee-5845271af231)


```
import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```

![image](https://github.com/user-attachments/assets/a2927b56-7252-4183-94b2-61d87a01d129)

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```

![image](https://github.com/user-attachments/assets/ee47623f-d438-49bb-9d4e-520b103a7ff1)

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age by Passenger Class,Titanic")
```
![image](https://github.com/user-attachments/assets/a9855443-8672-460a-bc2d-a6af079c33e8)

```
sns.violinplot(x='day',y='total_bill',hue='smoker',data=tips,linewidth=2,width=0.6)

plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Pot of Total Bill by Day and Smoker status")
```
![image](https://github.com/user-attachments/assets/17788a22-c29b-42a1-b7ed-65ac710a2bc5)

```
import seaborn as sns

sns.set_theme(style='whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x='day', y='tip', data=tip, palette="hsv")
```

![image](https://github.com/user-attachments/assets/9a197ffc-3a89-4a90-9a05-4f679d3cf265)

```
sns.set_theme(style='whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/user-attachments/assets/ebc9a2cb-3c5e-41ed-bb89-b814c395bd59)

```
import seaborn as sns

sns.set_theme(style='whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x='tip', y='day', data=tip, palette="Spectral")
```
![image](https://github.com/user-attachments/assets/86d361b4-afac-481e-9dd5-178fcd86b689)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack', linewidth=3,palette='colorblind',alpha=0.8)
```

![image](https://github.com/user-attachments/assets/7358e885-0154-4e1c-a895-33c768687208)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='dark',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/fb962ba0-336b-4154-b5c5-ef84c83229f4)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='crest',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/f78323ab-d791-4c45-a035-08e28c700e5b)

```
tips=sns.load_dataset("tips")
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)
```

![image](https://github.com/user-attachments/assets/9783c461-6c25-4f42-a74d-53d61d000f7f)

```
data=np.random.randint(low=1,high=100,size=(10,10))

hm=sns.heatmap(data=data,annot=True)
```

![image](https://github.com/user-attachments/assets/072b0e5d-42b8-47b1-b5cf-a400b04f0c1d)

```
sns.heatmap(data=data)
```

![image](https://github.com/user-attachments/assets/5812ffa2-a99c-41a8-9a70-44b3d7d92f63)

# Supermarket.csv data:
```
mart=pd.read_csv("supermarket.csv")
mart
```
![image](https://github.com/user-attachments/assets/d328ff01-5c5e-4b3d-a851-e0a55585f818)


```
mart=mart[['Gender','Payment','Unit price','Quantity','Total','gross income']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/547e8d68-92d7-490a-8756-7048108f156f)

```
sns.kdeplot(data=mart,x='Total')
```
![image](https://github.com/user-attachments/assets/8ccfb411-cf99-4b57-98a5-14b0cb4cdd53)

```
sns.kdeplot(data=mart,x='Unit price')
```
![image](https://github.com/user-attachments/assets/cc475941-f64b-4ac9-bb8d-55b38cba63d3)

```
sns.kdeplot(data=mart)
```

![image](https://github.com/user-attachments/assets/72fed8a0-6c2d-4e29-90d2-b719dff422a5)

```
sns.kdeplot(data=mart,x='Total',hue='Payment',multiple='stack')
```

![image](https://github.com/user-attachments/assets/0440f7dd-8ac4-413a-b461-ecd4f7e1ce9b)

```
sns.kdeplot(data=mart,x='Total',hue='Payment',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)
```

![image](https://github.com/user-attachments/assets/e6737225-da67-482f-991d-86d8e43b16ec)


```
sns.kdeplot(data=mart,x='Unit price',y='gross income')
```

![image](https://github.com/user-attachments/assets/da39a61c-c593-4d17-8a1f-e471ef3a8c18)


# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
