# DS-SA-8
# A08-IMPLEMENT KDE PLOT WITH ANY ONE OF YOUR OWN DATA SET
```
Developed By : Sowmiya N
Register Number : 212221230106
```
### KDE Plot:
```
KDE Plot described as Kernel Density Estimate is used for visualizing the Probability Density of a continuous variable. It depicts the probability density at different values in a continuous variable. We can also plot a single graph for multiple samples which helps in more efficient data visualization.
```
## CODE:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("titanic_dataset.csv")

df

#Create KDE for all the numeric variables in dataframe
sns.kdeplot(data=df)

sns.kdeplot(data=df, x='Pclass')

sns.kdeplot(data=df, x='Age')

sns.kdeplot(data=df, x='Fare')

sns.kdeplot(data=df,x='Survived',hue='Sex')

sns.kdeplot(data=df,x='Fare',hue='Sex')

sns.kdeplot(data=df,x='Survived',hue='Age')

sns.kdeplot(data=df,x='SibSp',hue='Age')

sns.kdeplot(data=df,x='Survived',hue='Pclass')

#Stack KDE on a category using MULTIPLE argument
sns.kdeplot(data=df,x='Survived',hue='Sex',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Sex',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)

sns.kdeplot(data=df,x='Fare',hue='Sex',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Pclass',multiple='stack')

sns.kdeplot(data=df,x='Survived',hue='Pclass',multiple='stack',linewidth=5,palette='Dark2',alpha=0.5)

sns.kdeplot(data=df,x='Fare',hue='Pclass',multiple='stack')

#Create a bivariate KDE
sns.kdeplot(data=df, x='Survived',y='SibSp')

sns.kdeplot(data=df, x='Survived',y='Fare')

sns.kdeplot(data=df, x='Age',y='Fare')

sns.kdeplot(data=df, x='Age',y='Pclass')

```
## OUTPUT:
### Initial Dataframe:
![op](./s81.png)
### KDE for all numeric variables of the Dataframe:
![op](./s82.png)
### Basic KDE plot for Pclass column:
![op](./s83.png)
### Basic KDE plot for Age column:
![op](./s84.png)
### Basic KDE plot for Fare column:
![op](./s85.png)
### Basic KDE plot for Survived column:
![op](./s88.png)
### Basic KDE plot for SibSp column:
![op](./s89.png)
### KDE on a category using MULTIPLE argument:
### Survived Vs Sex:
![op](./s86.png)
### Fare Vs Sex:
![op](./s87.png)
### Survived Vs Pclass:
![op](./s810.png)
### KDE on a category using MULTIPLE argument(Using additional Parameter- stack):
### Survived Vs Sex
![op](./s811.png)
### Fare Vs Sex
![op](./s813.png)
### Survived Vs Pclass:
![op](./s814.png)
### Fare Vs Pclass:
![op](./s816.png)
### KDE on a category using MULTIPLE argument(Using additional Parameter- stack,line width):
### Survived Vs Sex:
![op](./s812.png)
### Survived Pclass:
![op](./s815.png)

### Bivariate KDE:
### Survived Vs SibSp:
![op](./s817.png)
### Survived Vs Fare:
![op](./s818.png)
### Age Vs Fare:
![op](./s819.png)
### Age Vs Pclass:
![op](./s820.png)
