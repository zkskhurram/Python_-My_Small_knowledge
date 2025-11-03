💡 **Subject** : tip_tricks_01_using_libraries\
🖊️ **Author**  : Khurram Shahzad \
🎓 **Mentor**  : Dr. Aammar Tufail\
🔗 **Contact** : khurramamq@gmail.com // [https://github.com/zkskhurram/Python_-My_Small_knowledge/edit/main](https://github.com/zkskhurram/Python_-My_Small_knowledge/tree/main)

⚙️ Overview\
When working in Python, libraries make your life easier — they’re ready-made toolkits that save time, prevent code repetition, and bring powerful functions for data, AI, and automation.
---

# 📘 01 - How to find the version of pandas

```python
pip install -r requirements.txt
```

```python
# 1st way
import pandas as pd
pd.__version__
```

```python
# 2nd way
pd.show_versions ()
```

# 📘 02- Make a data frame

```python
# Primary Dataframe creation
df=pd.DataFrame({'A Col':[1,2,3,4,5,6],'B Col':[11,12,13,14,15,16]})
df
```

```python
# Numpy array use to create Primary Dataframe
import numpy as np

arr=np.array([[1,2,3],[4,5,6],[7,8,9]])
arr
pd.DataFrame(arr)
```

```python
# Numpy array Dataframe
pd.DataFrame(np.random.rand(4,8))
```

```python
# Numpy array Dataframe with Columns using list
pd.DataFrame(np.random.rand(4,8),columns=list('ABCDEFGH'))
```

# 📘 3- How to rename columns

```python
# Primary Dataframe using dictionary 
df=pd.DataFrame({'A Col':[1,2,3,4,5,6],'B Col':[11,12,13,14,15,16]})
df
```

```python
# 1st way to rename column
df.rename(columns={'A Col': 'Col_A', 'B Col':'Col_B'},inplace=True)
df
# To rename multiple columns at once, you can pass a dictionary to the rename() function.
# The keys of the dictionary are the current column names, and the values are the new column names.
```

```python
# 2nd way rename column
df.columns=[['column , a','column , b']]
df
# To get the column names as a list of lists
```

```python
# to replace any character, string
# df=df.columns.str.replace(",","-", inplace=True)
```

```python
# Adding Prefix to column
df=df.add_prefix('this is ')
df
```

```python
# Adding Suffix to column
df=df.add_suffix(' #')
df
```

```python
# Rename Column
df.columns=[['Column 1','Column2']]
df
# use the column names as a list of lists
```

# 📘 4- Using Template data

```python
import pandas as pd
import numpy as np
import seaborn as sns

kashti=sns.load_dataset('titanic')
kashti.head()
```

```python
kashti.to_csv('titanic_save.csv')
```

```python
import pandas as pd
import numpy as np
import seaborn as sns

phool=sns.load_dataset('iris')
phool.head()
```

```python
phool.to_csv('iris_save.csv')
```

```python
import pandas as pd
import numpy as np
import seaborn as sns

df=sns.load_dataset('tips')
df.head()
```

```python
# Summry 
df.describe
```

```python
# Saving a Dataset 
df.to_csv('tips_save.csv')
```

# 📘 5- Using your own data

```python
import pandas as pd

df=pd.read_csv('data.csv')
df.head(10)
```

# 📘 6- Reverse Row order

```python
# Import data using seaborn
import seaborn as sns   
import pandas as pd

dif = sns.load_dataset('titanic')
dif.head()
```

```python
# Reverse all rows bottom to top 
dif.loc[::-1].head(10)
```

```python
# Reverse rows bottom to top start from the 5th row from bottom except last row
dif.loc[::-5].head()
```

```python
# Reset all rows top to bottom
dif.loc[::-1].reset_index(drop=True).head()
```

# 📘 7- Reverse Column Order

```python
# Reverse all column names in a given DataFrame
dif.loc[:,::-1]
```

# 📘 8- select a Column by datatype

```python
# All datatypes in Dataset
dif.dtypes
```

```python
# Only Select Numeric Columns
dif.select_dtypes(include='number').head()
```

```python
# Only Select object Columns
dif.select_dtypes(include='object').head()
```

```python
# Only Select character Columns
dif.select_dtypes(include='character')
```

```python
# Only Select multiple Columns
dif.select_dtypes(include=['object','character']).head()
```

```python
# Only Select multiple Columns
dif.select_dtypes(include=['number','character']).head()
```

```python
# Only Select multiple Columns
dif.select_dtypes(exclude=['number','character']).head()
```

# 📘 9- Convert string to number

```python
# Create Primary data using dictionary
diff = pd.DataFrame ({'A': [1, 2, 3], 'B': [4, 5,6] , 'C': [7, 8, 9]})
diff
```

```python
# All Datatypes
diff.dtypes
```

```python
# Covert all data types to string
diff.astype({'A':'object','B':'object','C':'object'}).dtypes
```

```python
# Reverse all datatypes in the dataframe
pd.to_numeric(diff['A'], errors='coerce')
diff.dtypes
```

# 📘 10- Reduce dataframe size

```python
# Load secondary data using the `load_secondary_data` function  
kashti=sns.load_dataset('titanic')
kashti.shape
```

```python
# Check fraction of data with function by percent 
kashti.sample(frac=0.1).shape
```

```python
kashti.info()
```

# 📘 11- Copy data from clipboard

```python
# data downloas
import pandas as pd
import seaborn as sns

df=sns.load_dataset('titanic')
df.to_excel('titanic.xlsx')
```

```python
# read clipboard in Python it return latest data in clipboard copied by you
df=pd.read_clipboard()
df
```

```python
df=pd.read_clipboard()
df.head()
```

# 📘 12- Split data into two sets

```python
import pandas as pd
import seaborn as sns

kashti=sns.load_dataset('titanic')
kashti.head(11)
```

```python
# Length of dataset function show rows in dataset
len(kashti)
```

```python
# shape of dataset function show rows and columns
kashti.shape
```

```python
# Use random number generator to generate a random number between 1 and 100
from random import random
kashti_1=kashti.sample(frac=0.50, random_state=1)
kashti_1.shape
# Data split into half
```

```python
# Retrive left split data 
kashti_2=kashti.drop(kashti_1.index)
kashti_2.shape
```

```python
# random head data of split 1st dataset
kashti_1.head()
```

```python
# random head data of split 2nd dataset
kashti_2.head()
```

```python
# Column Length of each split dataset
len(kashti_2) + len(kashti_1)
```

# 📘 13- Join two data sets

```python
# Concat function join split data rows show disorder
kashti=pd.concat([kashti_1,kashti_2])
kashti
```

```python
# Reorders rows in dataset from most recent to oldest base on index
kashti.sort_index(ascending=True)
```

```python
# Reorders rows in dataset from highest to lowest based on index
kashti.sort_index(ascending=False)
```

# 📘 14- Filtring a Dataset

```python
import pandas as pd
import numpy as np
import seaborn as sns

df=sns.load_dataset('titanic')
df.head()
# returns :First 5 rows of the dataframe head
```

```python
df.shape
```

```python
df.sex.unique()
df  
# Return array of unique sex values
```

```python
df[(df.sex=='male')]
# Return the array of male individuals
```

```python
df.age.unique()
# Return the array of unique ages
```

```python
print (df.embark_town.unique())
# Return the number of unique embark towns
df[(df.embark_town=='Southampton')].shape
# Return the number of passengers who embarked from Southampton
```

```python
df[(df.embark_town=='Southampton')
   & (df.sex=="female")]
# Return the number of female passengers who embarked at Southampton
```

```python
df[((df.embark_town=='Southampton') | 
   (df.embark_town=='Queenstown') )
   & (df.sex=="female")]
# Return the number  of female passengers who embarked at Southampton and Queenstown
```

```python
df[df.embark_town.isin(['Queenstown'])].head()
# Return the number of passengers who embarked in Queenstown
```

```python
print(df.shape)
# Return the shape of the DataFrame Total number of rows and columns
print(df[df.age>30].shape)
# Return the shape of the DataFrame where age is greater than 30
print(df[df.age<30].shape)
# Return the shape of the DataFrame where age is less than 30
print(df[df.age>15].shape)
# Returns the shape of the DataFrame where age is greater than 15
```

# 📘 15- filtering with by large categories

```python
print(df.embark_town.value_counts())
# Return the number of rows passnegers who embarked in each town
print(df.sex.value_counts())
# Return the number of rows passnegers who are male and female
print(df.age.value_counts().head(20))
# Returns the number of rows passnegers who are in each age group
```

```python
print(df.embark_town.value_counts().nlargest(2))
# Return the number of rows passnegers who embarked in each town
# nlargest returns the n largest elements from the series
print(df.sex.value_counts().nlargest(2))
# Return the number of rows passnegers who are male and female
# nlargest returns the n largest elements from the series
print(df.age.value_counts().nlargest(2))
# Returns the number of rows passnegers who are in each age group
# nlargest returns the n largest elements from the series
```

```python
# Second way
count=df.embark_town.value_counts()
# Returns : {'Southampton': 2, 'Cherbourg': 1, 'Queenstown': 1} 
count.nlargest(2).index
# Returns 2
```

```python
df[df.embark_town.isin(count.nlargest(1).index)].head()
# Returns the first row of the dataframe where the embark_town is the most common embark_town.
```

```python
df[df.embark_town.isin(count.nlargest(3).index)].head(10)
# Returns the top 3 embark towns with the most passengers.
```

```python
df[df.embark_town.isin(count.nsmallest(1).index)].head(10)
# Returns the first 5 rows of the dataframe where the embark_town is in the 3 smallest towns
```

# 📘 16- Spliting a string into multiple columns

```python
# import libraries
import pandas as pd
# Create a Primary Dataframe using dictionaries 
dfn=pd.DataFrame({'name':['Muhammad Kashif','Muhammad Hanif','Khurram Shahzad','Wazir Ahmed'],
                 'Age':[20,21,19,22],
                 
                 'Marks':[90,85,88,92],
                 'locations':['Farwaniya,Kuwait','Dubai,UAE','Qatar,Qatar','Karachi,Pakistan']
                })
dfn
```

```python
# Splitting Name data frame into Two Column  
dfn.name.str.split(' ',expand=True)
```

```python
# Adding those splits into new cloumn
dfn[["First Name","Second Name"]]=dfn.name.str.split(' ',expand=True)
dfn
```

```python
# Splitting Locations data frame into Two Column  
dfn.locations.str.split(',',expand=True)
```

```python
# Adding those splits into new cloumn
dfn[["City","Country"]]=dfn.locations.str.split(',',expand=True)
dfn
```

```python
# Refine data manipulation
dfn_new = dfn[["First Name","Second Name", "Age","Marks","City","Country"]]
dfn_new
```

# 📘 17- Aggregate by multiple group/function

```python
import pandas as pd
import numpy as np  
import seaborn as sns
import matplotlib.pyplot as plt

df=sns.load_dataset('titanic')
df
```

```python
df.groupby('who').count()
# Return the count of group by object 'who'
```

```python
df.groupby('sex').count()
# Return the count of each sex
```

```python
print(df.groupby('pclass')['age'].sum())
# Return the sum of 'age' for each 'pclass' in the DataFrame df.
print(df.groupby('pclass')['age'].mean())
# Return the mean of 'age' for each 'pclass' group.  # noqa: E501
```

```python
len(df.groupby('who'))
# Returns numbers of rows in group by 'who' column
```

```python
len(df.groupby('fare'))
# Returns numbers of rows in group by fare column
```

```python
df.groupby(['sex','who','pclass','embarked']).count()
# Returns a DataFrame with the count of each unique combination of the specified columns.
```

# 📘 18- Select Specific Rows and Column

```python
df
# Print Dataframe
```

```python
df.head()
# Print the first 5 rows of the DataFrame
```

```python
# select Column
df[['sex','class']].head(10)
```

```python
df.describe()
# Returns description  of the data
```

```python
print(df.describe().loc[['min','25%','50%','75%','max']])
# Return the summary statistics of the DataFrame, excluding the mean and standard deviation
# Or
print(df.describe().loc['min':'max'])
# Return the summary statistics of the DataFrame, excluding the mean and standard deviation
```

```python
print(df.describe().loc['min':'max','survived':'age'])
# Return the summary statistics for the 'survived' , 'pclass' and 'age' columns of the DataFrame df, excluding th
```

```python
print(df.describe().loc['min':'max',['survived','age']])
# return the summary statistics for the 'survived' and 'age' columns of the dataframe
```

# 📘 19- Reshape mutiindex seies

```python
df
```

```python
df.survived.mean()
# Return the mean of the survived column in the df dataframe
```

```python
df.groupby('sex').survived.mean()
# Return the mean survival rate for each sex
```

```python
df.groupby(['sex','class']).survived.mean()
# Return the mean survival rate for each sex and class
```

```python
df.groupby(['sex','class']).survived.mean().unstack
# Return the mean survival rate for each sex and class
```

# 📘 20- Continous to categorical data convesion

```python
df.head()
# Return the first 5 rows of the DataFrame
```

```python
print(df.age.head())
print(df.shape)
```

```python
pd.cut(df.age, bins= [0,18,25,50,99], labels=['child','young_adult','Adult','old']).head()
# Return the bins and labels
df['New _Age'] = pd.cut(df.age, bins= [0,18,25,50,99], labels=['child','young_adult','Adult','old'])
# Add a new column with the age group
df.head(10)
```

```python
df.shape
```

# 📘 21- Covert one set vlue to another set value

```python
df.sex.head()
```

```python
df['sex_num']=df.sex.map({'male':0,'female':1})
# Return the dataframe with the new column sex _num
# Intialize sex with 0 and 1
df.head()
```

```python
df.shape
```

```python
df.embarked.count()
```

```python
df['embarked_num']=df.embarked.factorize()[0]
# Return the dataframe with the new column embark _num
# Intialize embark 0 as 0 and embark 1 as 1 and embark 2 as 2
df.head(15)
```

# 📘 22- Transpose a wide dataframe

```python
import pandas as pd
import numpy as np
```

```python
# Creating dataframe
dft=pd.DataFrame(np.random.rand(200,25),columns=list('abcdefghijklmnopqrstuvwxy'))
# Return new dataframe with specified columns
dft.head()
```

```python
dft.head(10).T
```

```python
dft.shape
```

```python
df.describe()
```

# 📘 23- Reshaping a dataframe

```python
fasla=pd.DataFrame([['12345',100,200,300],['34567',400,500,600],['67890',700,800,900]],columns=['zip','factory','warehouse','retail'])
fasla.head()
# return the first 5 rows of the dataframe
```

```python
fasla.head().T
```

```python
fasla2=pd.DataFrame([[1,'12345','factory'],[2,'34567','warehouse'],[3,'67890','retail']],columns=['user_id','zip','location_type'])
fasla2
```

```python
fasla.melt(id_vars='zip',var_name='location_type',value_name='distance')
```

```python
import seaborn as sns
sns.barplot(x='zip',y='factory',data=fasla)
```

```python
fasla_long=fasla.melt(id_vars='zip',var_name='location_type',value_name='distance')
# Return the result of the melt operation 
fasla_long
```

```python
import seaborn as sns
sns.barplot(x='zip',y='distance',hue='location_type',data=fasla_long)
```
