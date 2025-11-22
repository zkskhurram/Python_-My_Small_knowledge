-💡 **Subject** : tip_tricks_01_using_libraries\
- 🖊️ **Author:** Khurram Shahzad  
- 🎓 **Mentor:** Dr. Aammar Tufail  
- ✉️ **Email:** [khurramamq@gmail.com](mailto:khurramamq@gmail.com)  
- 💻 **GitHub:** [zkskhurram](https://github.com/zkskhurram/Python_-My_Small_knowledge/tree/main)
  
⚙️ Overview\
When working in Python, libraries make your life easier — they’re ready-made toolkits that save time, prevent code repetition, and bring powerful functions for data, AI, and automation.

# 01 - How to find the version of pandas

```python
# First cell to check pandas version

import pandas as pd
pd.__version__
```

```python
# Second cell to show pandas version details

pd.show_versions ()
```

# 02- Make a data frame
Here I am using `df` as variable for my primary dataset.

```python
# primary dataframe creation

df=pd.DataFrame({'A Col':[1,2,3,4,5,6,7,8],'B Col':[11,12,13,14,15,16,17,18]})

df
```

```python
# Numpy array use to create Primary Dataframe

import numpy as np

arr=np.array([[1,2,3],[4,5,6],[7,8,9]]) # 3x3 array in numpy list format

print(arr) # print numpy array

pd.DataFrame(arr) # convert numpy array to dataframe
```

```python
# Numpy array Dataframe

pd.DataFrame(np.random.rand(4,8)) 

# Create DataFrame from random numbers using numpy array
```

```python
# Numpy array Dataframe with Columns using list

pd.DataFrame(np.random.rand(4,8),columns=list('ABCDEFGH'))

# Create DataFrame from random numbers using numpy array with column names assigned
```

# 3- How to rename columns
Here I am using `rename_column` as variable for my primary dataset.

```python
# Primary Dataframe using dictionary

rename_column=pd.DataFrame({'A Col':[1,2,3,4,5,6],'B Col':[11,12,13,14,15,16]})
rename_column
```

```python
# First way to rename column

rename_column.rename(columns={'A Col': 'Col_A', 'B Col':'Col_B'},inplace=True)
rename_column

# To rename multiple columns at once, you can pass a dictionary to the rename() function.
# The keys of the dictionary are the current column names, and the values are the new column names.
```

```python
# Second way to rename column

rename_column.columns=['column _ a','column _ b']
rename_column

# To get the column names as a list of lists 
```

```python
# to replace any character, string

rename_column.columns = rename_column.columns.str.replace('_', '*', regex=False)
print(rename_column)

# Use the str.replace() method on the columns attribute to replace characters in column names.


```

```python
# Adding Prefix to column

rename_column=rename_column.add_prefix('this is ') # adding prefix to column names
rename_column
```

```python
# Adding Suffix to column
rename_column=rename_column.add_suffix(' #') # adding suffix to column names
rename_column
```

```python
# Rename Column
rename_column.columns=['Column 1','Column 2']
rename_column
# use the column names as a list of lists
```

# 4- Using template data
Here I am using  `boat` as variable for `seaborn` librariry dataset `titanic`.\
Here I am using  `flower` as variable for `seaborn` librariry dataset `iris`.\
Here I am using  `tip` as variable for `seaborn` librariry dataset `tips`.

```python
import pandas as pd
import numpy as np
import seaborn as sns

boat=sns.load_dataset('titanic')
boat.head()


```

```python
# summary statistics

boat.describe()

# columns of dataframe

boat.columns
```

```python
# Save DataFrame to CSV

boat.to_csv('titanic_save.csv')

# save DataFrame to Excel

boat.to_excel('titanic_save.xlsx')

boat.to_markdown('titanic_save.md')
```

```python
import pandas as pd
import numpy as np
import seaborn as sns

flower=sns.load_dataset('iris')
flower.head()

```

```python
# Save DataFrame to CSV

flower.to_csv('iris_save.csv')
```

```python
import pandas as pd
import numpy as np
import seaborn as sns

tip=sns.load_dataset('tips')
tip.head()
```

```python
# Summry statistics

tip.describe
```

```python
# Saving a Dataset to CSV
 
tip.to_csv('tips_save.csv')
```

# 5- Using your own data
Here I am using  `own_data` as variable for `seaborn` librariry dataset `titanic`..

```python
import pandas as pd

own_data=pd.read_csv('titanic_save.csv')
own_data.head(10)
```

# 6- Reverse Row order
Here I am using `reverse_order` as variable for `seaborn` librariry dataset `titanic`.

```python
# Import libraries and load dataset using seaborn

import seaborn as sns   
import pandas as pd

reverse_order = sns.load_dataset('titanic')
reverse_order.head()

```

```python
# Reverse all rows bottom to top without skipping

reverse_order.loc[::-1].head(10)

# we reverse all rows from bottom to top using .loc with slicing.
```

```python
# Reverse rows bottom to top with skipping 5 rows

reverse_order.loc[::-5].head(10)
```

```python
# Reset all dataframe index after reversing

reverse_order.loc[::-1].reset_index(drop=True).head(10)
```

# 7- Reverse Column Order
Here I am using `reverse_order` as variable for `seaborn` librariry dataset `titanic`.

```python
# Reverse all column names in a given DataFrame

reverse_order.loc[:,::-1]

```

# 8- select a Column by datatype
Here I am using `select_column` as variable for `seaborn` librariry dataset `titanic`.

```python
# Import libraries and load dataset using seaborn

import seaborn as sns   
import pandas as pd

select_column = sns.load_dataset('titanic')

select_column.dtypes

# We use variable select_column to load the 'titanic' dataset from seaborn and display the data types of each column using the dtypes attribute.
```

```python
# Only Select Numeric types

select_column.select_dtypes(include='number').head()
```

```python
# Only Select object types

select_column.select_dtypes(include='object').head()
```

```python
# Only Select character types

select_column.select_dtypes(include='character')
```

```python
# Only Select multiple datatypes

select_column.select_dtypes(include=['object','character']).head()
```

```python
# Only Select multiple Cdatatypes

select_column.select_dtypes(include=['number','object']).head()
```

```python
# exclude multiple datatypes

select_column.select_dtypes(exclude=['number','character']).head()
```

# 9- Convert string to number
Here I am using `type_casting` as variable for primary dataset.

```python
# Create Primary data using dictionary

type_casting = pd.DataFrame ({'A': [11, 12, 13], 
                              'B': [14, 15,16] , 
                              'C': [17, 18, 9]})
type_casting
```

```python
# All Datatypes

type_casting.dtypes
```

```python
# Covert all data types to string

type_casting.astype({'A':'object','B':'object','C':'object'}).dtypes
```

```python
# convert dataset to original data types

type_casting.astype({'A':'int','B':'int','C':'int'}).dtypes
```

```python
# Second way to convert dataset to original data types

pd.to_numeric(type_casting['A'], errors='coerce')
# type_casting.dtypes
```

# 10- Reduce dataframe size
Here I am using `boat_01` as variable for `seaborn` librariry dataset `titanic`.

```python
# Load secondary data using the `load_secondary_data` function  

boat_01=sns.load_dataset('titanic')
boat_01.shape
```

```python
# to check memory usage of dataframe 

boat_01.info(memory_usage='deep')
```

```python
# Check fraction of data with function by fraction 

boat_01.sample(frac=0.1).shape

# boat_01.sample(frac=0.1).shape --- IGNORE ---
```

# 11- Copy data from clipboard
Here I am using `copy_board` as variable for `seaborn` librariry dataset `titanic`.

```python
# import libraries and load dataset using seaborn

import pandas as pd
import seaborn as sns

copy_board=sns.load_dataset('titanic')
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

# 12- Split data into two sets
Here I am using `split_data` as variable for `seaborn` librariry dataset `titanic`\
Here I am using `split_data_1` as variable for `seaborn` librariry dataset `titanic`\
Here I am using `split_data_2` as variable for `seaborn` librariry dataset `titanic`

```python
import pandas as pd
import seaborn as sns

split_data=sns.load_dataset('titanic')
split_data.head(11)
```

```python
# Length of dataset function show rows in dataset

len(split_data)  
```

```python
# shape of dataset function show rows and columns
split_data.shape
```

```python
# Use random number generator to generate a random number between 1 and 100

from random import random
split_data_1 = split_data.sample(frac=0.50, random_state=1)
split_data_1.shape

# Data split into half 
```

```python
# Retrive left split data 

split_data_2=split_data.drop(split_data_1.index)
split_data_2.shape
```

```python
# random head data of split 1st dataset

split_data_1.head()
```

```python
# random head data of split 2nd dataset

split_data_2.head()
```

```python
# Column Length of each split dataset

len(split_data_2) + len(split_data_1)
```

# 13- Join two data sets

```python
# Combine both split datasets to get original dataset

split_data_join = pd.concat([split_data_1, split_data_2])
split_data_join.shape
```

```python
# Reorders rows in dataset from most recent to oldest base on index

split_data_join.sort_index(ascending=True)
```

```python
# Reorders rows in dataset from highest to lowest based on index

split_data_join.sort_index(ascending=False)
```

# 14- Filtring a Dataset
Here I am using `filter_data` as variable for `seaborn` librariry dataset `titanic`

```python
import pandas as pd
import numpy as np
import seaborn as sns

filter_data=sns.load_dataset('titanic')
filter_data.head()

# returns :First 5 rows of the dataframe head
```

```python
filter_data.shape
```

```python
filter_data.sex.unique()
```

```python
filter_data.sex.unique()
filter_data

# Return array of unique sex values
```

```python
filter_data[(filter_data.sex=='male')]

# Return the array of male individuals
```

```python
filter_data.age.unique()

# Return the array of unique ages
```

```python
filter_data.embark_town.unique()

# Return the number of unique embark towns
```

```python

filter_data[(filter_data.embark_town=='Southampton')].shape

# Return the number of passengers who embarked from Southampton
```

```python
filter_data[(filter_data.embark_town=='Southampton')
   & (filter_data.sex=="female")]

# Return the number of female passengers who embarked at Southampton
```

```python
filter_data[((filter_data.embark_town=='Southampton') | 
   (filter_data.embark_town=='Queenstown') )
   & (filter_data.sex=="female")]

# Return the number  of female passengers who embarked at Southampton and Queenstown
```

```python
filter_data[filter_data.embark_town.isin(['Queenstown'])].head()

# Return the number of passengers who embarked in Queenstown 
```

```python
print(filter_data.shape)

# Return the shape of the DataFrame Total number of rows and columns

print(filter_data[filter_data.age>30].shape)

# Return the shape of the DataFrame where age is greater than 30

print(filter_data[filter_data.age<30].shape)

# Return the shape of the DataFrame where age is less than 30

print(filter_data[filter_data.age>15].shape)

# Returns the shape of the DataFrame where age is greater than 15

print(filter_data[filter_data.age<15].shape)

# Returns the shape of the DataFrame where age is greater than 15
```

# 15- filtering with by large categories
Here I am using `filter_data` as variable for `seaborn` librariry dataset `titanic`

```python
print(filter_data.embark_town.value_counts())

# Return the number of rows passnegers who embarked in each town

print(filter_data.sex.value_counts())

# Return the number of rows passnegers who are male and female

print(filter_data.age.value_counts().head(6))

# Returns the number of rows passnegers who are in each age group
```

```python
print(filter_data.embark_town.value_counts().nlargest(2))

# Return the number of rows passnegers who embarked in each town
# nlargest returns the n largest elements from the series

print(filter_data.sex.value_counts().nlargest(2))

# Return the number of rows passnegers who are male and female
# nlargest returns the n largest elements from the series

print(filter_data.age.value_counts().nlargest(3))

# Returns the number of rows passnegers who are in each age group
# nlargest returns the n largest elements from the series
```

```python
# Second way

count=filter_data.embark_town.value_counts(2)

# Returns : {'Southampton': 2, 'Cherbourg': 1, 'Queenstown': 1} 

count.nlargest(2).index

# Returns 2
```

```python

filter_data[filter_data.embark_town.isin(count.nlargest(1).index)].head()

# Returns the first row of the dataframe where the embark_town is the most common embark_town.
```

```python
filter_data[filter_data.embark_town.isin(count.nlargest(2).index)].head(10)

# Returns the top 3 embark towns with the most passengers.
```

```python
filter_data[filter_data.embark_town.isin(count.nsmallest(1).index)].head(10)

# Returns the first 5 rows of the dataframe where the embark_town is in the 3 smallest towns
```

# 16- Spliting a string into multiple columns
Here I am using `pm_df` as variable for my primary dataset.

```python
# import libraries
import pandas as pd
# Create a Primary Dataframe using dictionaries 

pm_df=pd.DataFrame({'name':['Muhammad Kashif','Muhammad Hanif','Khurram Shahzad','Wazir Ahmed'],
                 'Age':[20,21,19,22],
                 'Marks':[90,85,88,92],
                 'locations':['Farwaniya,Kuwait','Dubai,UAE','Qatar,Qatar','Karachi,Pakistan']
                })
pm_df
```

```python
# Splitting Name data frame into Two Column  

pm_df.name.str.split(' ',expand=True)
 
```

```python
# Adding those splits into new cloumn

pm_df[["First Name","Second Name"]]=pm_df.name.str.split(' ',expand=True)
pm_df
```

```python
# Splitting Locations data frame into Two Column  

pm_df.locations.str.split(',',expand=True)

```

```python
# Adding those splits into new cloumn

pm_df[["City","Country"]]=pm_df.locations.str.split(',',expand=True)
pm_df
```

```python
# Refine data manipulation

pm_df = pm_df[["First Name","Second Name", "Age","Marks","City","Country"]]
pm_df
```

# 17- Aggregate by multiple group/function
Here I am using `agg_data` as variable for `seaborn` librariry dataset `titanic`

```python
import pandas as pd
import numpy as np  
import seaborn as sns
import matplotlib.pyplot as plt

agg_data=sns.load_dataset('titanic')
agg_data
```

```python
agg_data.groupby('who').count()

# Return the count of group by object 'who'
```

```python
agg_data.groupby('sex').count()

# Return the count of each sex 
```

```python
print(agg_data.groupby('pclass')['age'].sum())

# Return the sum of 'age' for each 'pclass' in the DataFrame .

print(agg_data.groupby('pclass')['age'].mean())

# Return the mean of 'age' for each 'pclass' group.  # noqa: E501
```

```python
len(agg_data.groupby('who'))

# Returns numbers of rows in group by 'who' column
```

```python
len(agg_data.groupby('fare'))

# Returns numbers of rows in group by fare column
```

```python
agg_data.groupby(['sex','who','pclass','embarked']).count()

# Returns a DataFrame with the count of each unique combination of the specified columns.
```

# 18- Select Specific Rows and Column
Here I am using `row_column` as variable for `seaborn` librariry dataset `titanic`

```python
import pandas as pd
import numpy as np  
import seaborn as sns
import matplotlib.pyplot as plt

row_column=sns.load_dataset('titanic')
row_column
```

```python
row_column.head()

# Print the first 5 rows of the DataFrame
```

```python
# select Column

row_column[['sex','class']].head(10)
```

```python
row_column.describe()

# Returns description  of the data
```

```python
print(row_column.describe().loc[['min','25%','50%','75%','max']])

# Return the summary statistics of the DataFrame, 
# excluding the mean and standard deviation

# Or

print(row_column.describe().loc['min':'max'])

# Return the summary statistics of the DataFrame, 
# excluding the mean and standard deviation

print(row_column.describe().loc[['min','max']])

# Return the summary statistics of the DataFrame, 
# only min and max values
```

```python
print(agg_data.describe().loc['min':'max','survived':'age'])

# Return the summary statistics for the 'survived' , 'pclass' and 'age' columns of the DataFrame df, excluding th
```

```python
print(agg_data.describe().loc['min':'max',['survived','age']])

# return the summary statistics for the 'survived' and 'age' columns of the dataframe
```

# 19- Reshape multi index seies
Here I am using `reshape` as variable for `seaborn` librariry dataset `titanic`

```python
import pandas as pd
import numpy as np  
import seaborn as sns
import matplotlib.pyplot as plt

reshape=sns.load_dataset('titanic')
reshape
```

```python
reshape.survived.mean()

# Return the mean of the survived column in the titanic dataframe
```

```python
reshape.groupby('sex').survived.mean()

# Return the mean survival rate for each sex
```

```python
reshape.groupby(['sex','class']).survived.mean()

# Return the mean survival rate for each sex and class 
```

```python
agg_data.groupby(['sex','class']).survived.mean().unstack()

# Return the mean survival rate for each sex and class as a reshaped DataFrame
```

# 20- Continous to categorical data convesion
Here I am calling again `boat ` as variable for `seaborn` librariry dataset `titanic`.

```python
boat.head()

# Return the first 5 rows of the DataFrame
```

```python
print(boat.age.head())
print(boat.shape)
```

```python
pd.cut(boat.age, bins= [0,10,18,25,50,99], labels=['Infant','child','young_adult','Adult','old']).head()

# Return the bins and labels

boat['New _Age'] = pd.cut(boat.age, bins= [0,10,18,25,50,99], labels=['Infant','child','young_adult','Adult','old'])

# Add a new column with the age group

boat.head(10)
```

```python
boat.shape
```

# 21- Covert one set vlue to another set value
Here I am calling again `boat ` as variable for `seaborn` librariry dataset `titanic`.

```python
boat.sex.head()
```

```python
boat['sex_num']=boat.sex.map({'male':0,'female':1})

# Return the dataframe with the new column sex _num
# Intialize sex with 0 and 1

boat.head()
```

```python
boat.shape
```

```python
boat.embarked.count()
```

```python
boat['embarked_num']=boat.embarked.factorize()[0]

# Return the dataframe with the new column embark _num
# Intialize embark 0 as 0 and embark 1 as 1 and embark 2 as 2

boat.head(15)
```

```python
boat['fare_num']=boat.fare.factorize()[0]

# Return the dataframe with the new column age _num
# Intialize age with 0 and so on

boat.head(15)
```

# 22- Transpose a wide dataframe
Here I am using  `transpose ` as variable for primary dataset.


```python
import pandas as pd
import numpy as np
```

```python
# Creating dataframe

trasnpose=pd.DataFrame(np.random.rand(200,25),columns=list('abcdefghijklmnopqrstuvwxy'))

# Return new dataframe with specified columns

trasnpose.head()
```

```python
trasnpose.head(10).T
```

```python
trasnpose.shape
```

```python
trasnpose.describe().T
```

# 23- Reshaping a dataframe
Here I am using `reshape `,`reshape_1` as variable for primary dataset.

```python
reshape=pd.DataFrame([['12345',100,200,400],
                      ['34567',400,500,400],
                      ['67890',700,800,900]],
                     columns=['zip','factory','warehouse','retail'])
reshape.head()

# return the first 5 rows of the dataframe

```

```python
reshape.head().T
```

```python
reshape_1=pd.DataFrame([[1,'12345','factory'],
                        [2,'34567','warehouse'],
                        [3,'67890','retail']],
                       columns=['user_id','zip','location_type'])
reshape_1
```

```python
reshape
```

```python
reshape.melt(id_vars='zip',var_name='location_type',value_name='distance')
```

```python
import seaborn as sns
sns.barplot(x='zip',y='factory',data=reshape)
```

```python
reshape_1=reshape.melt(id_vars='zip',var_name='location_type',value_name='distance')

# Return the result of the melt operation 

reshape_1
```

```python
import seaborn as sns
sns.barplot(x='zip',y='distance',hue='location_type',data=reshape_1)
```

