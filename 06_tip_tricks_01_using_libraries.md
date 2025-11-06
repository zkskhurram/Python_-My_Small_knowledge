💡 **Subject** : tip_tricks_01_using_libraries\
🖊️ **Author**  : Khurram Shahzad \
🎓 **Mentor**  : Dr. Aammar Tufail\
🔗 **Contact** : khurramamq@gmail.com // [https://github.com/zkskhurram/Python_-My_Small_knowledge/edit/main](https://github.com/zkskhurram/Python_-My_Small_knowledge/tree/main)

⚙️ Overview\
When working in Python, libraries make your life easier — they’re ready-made toolkits that save time, prevent code repetition, and bring powerful functions for data, AI, and automation.

# 01 - How to find the version of pandas


```python
# First cell to check pandas version

import pandas as pd
pd.__version__
```




    '2.3.3'




```python
# Second cell to show pandas version details

pd.show_versions ()
```

    
    INSTALLED VERSIONS
    ------------------
    commit                : 9c8bc3e55188c8aff37207a74f1dd144980b8874
    python                : 3.13.7
    python-bits           : 64
    OS                    : Windows
    OS-release            : 11
    Version               : 10.0.26200
    machine               : AMD64
    processor             : Intel64 Family 6 Model 186 Stepping 2, GenuineIntel
    byteorder             : little
    LC_ALL                : None
    LANG                  : None
    LOCALE                : English_United States.1252
    
    pandas                : 2.3.3
    numpy                 : 2.3.4
    pytz                  : 2025.2
    dateutil              : 2.9.0.post0
    pip                   : 25.3
    Cython                : None
    sphinx                : None
    IPython               : 9.6.0
    adbc-driver-postgresql: None
    adbc-driver-sqlite    : None
    bs4                   : 4.14.2
    blosc                 : None
    bottleneck            : None
    dataframe-api-compat  : None
    fastparquet           : None
    fsspec                : None
    html5lib              : None
    hypothesis            : None
    gcsfs                 : None
    jinja2                : 3.1.6
    lxml.etree            : 6.0.2
    matplotlib            : 3.10.7
    numba                 : None
    numexpr               : None
    odfpy                 : None
    openpyxl              : 3.1.5
    pandas_gbq            : None
    psycopg2              : None
    pymysql               : None
    pyarrow               : None
    pyreadstat            : None
    pytest                : None
    python-calamine       : None
    pyxlsb                : None
    s3fs                  : None
    scipy                 : 1.16.3
    sqlalchemy            : 2.0.44
    tables                : None
    tabulate              : 0.9.0
    xarray                : None
    xlrd                  : 2.0.2
    xlsxwriter            : None
    zstandard             : None
    tzdata                : 2025.2
    qtpy                  : None
    pyqt5                 : None


# 02- Make a data frame
Here I am using `df` as variable for my primary dataset.


```python
# primary dataframe creation

df=pd.DataFrame({'A Col':[1,2,3,4,5,6,7,8],'B Col':[11,12,13,14,15,16,17,18]})

df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A Col</th>
      <th>B Col</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>13</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>16</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>17</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>18</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Numpy array use to create Primary Dataframe

import numpy as np

arr=np.array([[1,2,3],[4,5,6],[7,8,9]]) # 3x3 array in numpy list format

print(arr) # print numpy array

pd.DataFrame(arr) # convert numpy array to dataframe
```

    [[1 2 3]
     [4 5 6]
     [7 8 9]]





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>5</td>
      <td>6</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7</td>
      <td>8</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Numpy array Dataframe

pd.DataFrame(np.random.rand(4,8)) 

# Create DataFrame from random numbers using numpy array
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
      <th>6</th>
      <th>7</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.470845</td>
      <td>0.669496</td>
      <td>0.793166</td>
      <td>0.449860</td>
      <td>0.871447</td>
      <td>0.522599</td>
      <td>0.776271</td>
      <td>0.053605</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.694611</td>
      <td>0.552129</td>
      <td>0.687445</td>
      <td>0.566531</td>
      <td>0.592473</td>
      <td>0.354374</td>
      <td>0.756098</td>
      <td>0.595249</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.259069</td>
      <td>0.635381</td>
      <td>0.223484</td>
      <td>0.858385</td>
      <td>0.150136</td>
      <td>0.457272</td>
      <td>0.714424</td>
      <td>0.102523</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.705466</td>
      <td>0.443104</td>
      <td>0.523620</td>
      <td>0.322079</td>
      <td>0.702496</td>
      <td>0.038182</td>
      <td>0.177618</td>
      <td>0.026360</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Numpy array Dataframe with Columns using list

pd.DataFrame(np.random.rand(4,8),columns=list('ABCDEFGH'))

# Create DataFrame from random numbers using numpy array with column names assigned
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
      <th>F</th>
      <th>G</th>
      <th>H</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.049266</td>
      <td>0.861110</td>
      <td>0.145276</td>
      <td>0.093828</td>
      <td>0.437284</td>
      <td>0.789518</td>
      <td>0.367485</td>
      <td>0.985546</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.341928</td>
      <td>0.248265</td>
      <td>0.303095</td>
      <td>0.342576</td>
      <td>0.416396</td>
      <td>0.336814</td>
      <td>0.465429</td>
      <td>0.367441</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.490955</td>
      <td>0.561133</td>
      <td>0.137149</td>
      <td>0.563419</td>
      <td>0.858775</td>
      <td>0.152394</td>
      <td>0.278929</td>
      <td>0.967698</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.537007</td>
      <td>0.798320</td>
      <td>0.690655</td>
      <td>0.969945</td>
      <td>0.039491</td>
      <td>0.669120</td>
      <td>0.905382</td>
      <td>0.763768</td>
    </tr>
  </tbody>
</table>
</div>



# 3- How to rename columns
Here I am using `rename_column` as variable for my primary dataset.


```python
# Primary Dataframe using dictionary

rename_column=pd.DataFrame({'A Col':[1,2,3,4,5,6],'B Col':[11,12,13,14,15,16]})
rename_column
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A Col</th>
      <th>B Col</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>13</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
</table>
</div>




```python
# First way to rename column

rename_column.rename(columns={'A Col': 'Col_A', 'B Col':'Col_B'},inplace=True)
rename_column

# To rename multiple columns at once, you can pass a dictionary to the rename() function.
# The keys of the dictionary are the current column names, and the values are the new column names.
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Col_A</th>
      <th>Col_B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>13</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Second way to rename column

rename_column.columns=['column _ a','column _ b']
rename_column

# To get the column names as a list of lists 
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>column _ a</th>
      <th>column _ b</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>13</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
</table>
</div>




```python
# to replace any character, string

rename_column.columns = rename_column.columns.str.replace('_', '*', regex=False)
print(rename_column)

# Use the str.replace() method on the columns attribute to replace characters in column names.


```

       column * a  column * b
    0           1          11
    1           2          12
    2           3          13
    3           4          14
    4           5          15
    5           6          16



```python
# Adding Prefix to column

rename_column=rename_column.add_prefix('this is ') # adding prefix to column names
rename_column
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>this is column * a</th>
      <th>this is column * b</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>13</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Adding Suffix to column
rename_column=rename_column.add_suffix(' #') # adding suffix to column names
rename_column
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>this is column * a #</th>
      <th>this is column * b #</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>13</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Rename Column
rename_column.columns=['Column 1','Column 2']
rename_column
# use the column names as a list of lists
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Column 1</th>
      <th>Column 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>13</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>15</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>16</td>
    </tr>
  </tbody>
</table>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
# summary statistics

boat.describe()

# columns of dataframe

boat.columns
```




    Index(['survived', 'pclass', 'sex', 'age', 'sibsp', 'parch', 'fare',
           'embarked', 'class', 'who', 'adult_male', 'deck', 'embark_town',
           'alive', 'alone'],
          dtype='object')




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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
  </tbody>
</table>
</div>




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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>total_bill</th>
      <th>tip</th>
      <th>sex</th>
      <th>smoker</th>
      <th>day</th>
      <th>time</th>
      <th>size</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16.99</td>
      <td>1.01</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.34</td>
      <td>1.66</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>21.01</td>
      <td>3.50</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>23.68</td>
      <td>3.31</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24.59</td>
      <td>3.61</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Summry statistics

tip.describe
```




    <bound method NDFrame.describe of      total_bill   tip     sex smoker   day    time  size
    0         16.99  1.01  Female     No   Sun  Dinner     2
    1         10.34  1.66    Male     No   Sun  Dinner     3
    2         21.01  3.50    Male     No   Sun  Dinner     3
    3         23.68  3.31    Male     No   Sun  Dinner     2
    4         24.59  3.61  Female     No   Sun  Dinner     4
    ..          ...   ...     ...    ...   ...     ...   ...
    239       29.03  5.92    Male     No   Sat  Dinner     3
    240       27.18  2.00  Female    Yes   Sat  Dinner     2
    241       22.67  2.00    Male    Yes   Sat  Dinner     2
    242       17.82  1.75    Male     No   Sat  Dinner     2
    243       18.78  3.00  Female     No  Thur  Dinner     2
    
    [244 rows x 7 columns]>




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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>6</th>
      <td>6</td>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7</td>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8</td>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>9</th>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>30.0708</td>
      <td>C</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>



# 6- Reverse Row order
Here I am using `reverse_order` as variable for `seaborn` librariry dataset `titanic`.


```python
# Import libraries and load dataset using seaborn

import seaborn as sns   
import pandas as pd

reverse_order = sns.load_dataset('titanic')
reverse_order.head()

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Reverse all rows bottom to top without skipping

reverse_order.loc[::-1].head(10)

# we reverse all rows from bottom to top using .loc with slicing.
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>885</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>39.0</td>
      <td>0</td>
      <td>5</td>
      <td>29.1250</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>884</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>25.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>883</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>28.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>882</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>22.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5167</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>881</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>33.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.8958</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Reverse rows bottom to top with skipping 5 rows

reverse_order.loc[::-5].head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>885</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>39.0</td>
      <td>0</td>
      <td>5</td>
      <td>29.1250</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>880</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>25.0</td>
      <td>0</td>
      <td>1</td>
      <td>26.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>875</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>15.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.2250</td>
      <td>C</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>870</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.8958</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>865</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>42.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>860</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>41.0</td>
      <td>2</td>
      <td>0</td>
      <td>14.1083</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>855</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>18.0</td>
      <td>0</td>
      <td>1</td>
      <td>9.3500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>850</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>4.0</td>
      <td>4</td>
      <td>2</td>
      <td>31.2750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>845</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>42.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.5500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Reset all dataframe index after reversing

reverse_order.loc[::-1].reset_index(drop=True).head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>39.0</td>
      <td>0</td>
      <td>5</td>
      <td>29.1250</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>25.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>28.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>8</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>22.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5167</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>9</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>33.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.8958</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>



# 7- Reverse Column Order
Here I am using `reverse_order` as variable for `seaborn` librariry dataset `titanic`.


```python
# Reverse all column names in a given DataFrame

reverse_order.loc[:,::-1]

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>alone</th>
      <th>alive</th>
      <th>embark_town</th>
      <th>deck</th>
      <th>adult_male</th>
      <th>who</th>
      <th>class</th>
      <th>embarked</th>
      <th>fare</th>
      <th>parch</th>
      <th>sibsp</th>
      <th>age</th>
      <th>sex</th>
      <th>pclass</th>
      <th>survived</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>False</td>
      <td>no</td>
      <td>Southampton</td>
      <td>NaN</td>
      <td>True</td>
      <td>man</td>
      <td>Third</td>
      <td>S</td>
      <td>7.2500</td>
      <td>0</td>
      <td>1</td>
      <td>22.0</td>
      <td>male</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>False</td>
      <td>yes</td>
      <td>Cherbourg</td>
      <td>C</td>
      <td>False</td>
      <td>woman</td>
      <td>First</td>
      <td>C</td>
      <td>71.2833</td>
      <td>0</td>
      <td>1</td>
      <td>38.0</td>
      <td>female</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>True</td>
      <td>yes</td>
      <td>Southampton</td>
      <td>NaN</td>
      <td>False</td>
      <td>woman</td>
      <td>Third</td>
      <td>S</td>
      <td>7.9250</td>
      <td>0</td>
      <td>0</td>
      <td>26.0</td>
      <td>female</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>False</td>
      <td>yes</td>
      <td>Southampton</td>
      <td>C</td>
      <td>False</td>
      <td>woman</td>
      <td>First</td>
      <td>S</td>
      <td>53.1000</td>
      <td>0</td>
      <td>1</td>
      <td>35.0</td>
      <td>female</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>True</td>
      <td>no</td>
      <td>Southampton</td>
      <td>NaN</td>
      <td>True</td>
      <td>man</td>
      <td>Third</td>
      <td>S</td>
      <td>8.0500</td>
      <td>0</td>
      <td>0</td>
      <td>35.0</td>
      <td>male</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>True</td>
      <td>no</td>
      <td>Southampton</td>
      <td>NaN</td>
      <td>True</td>
      <td>man</td>
      <td>Second</td>
      <td>S</td>
      <td>13.0000</td>
      <td>0</td>
      <td>0</td>
      <td>27.0</td>
      <td>male</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>887</th>
      <td>True</td>
      <td>yes</td>
      <td>Southampton</td>
      <td>B</td>
      <td>False</td>
      <td>woman</td>
      <td>First</td>
      <td>S</td>
      <td>30.0000</td>
      <td>0</td>
      <td>0</td>
      <td>19.0</td>
      <td>female</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>888</th>
      <td>False</td>
      <td>no</td>
      <td>Southampton</td>
      <td>NaN</td>
      <td>False</td>
      <td>woman</td>
      <td>Third</td>
      <td>S</td>
      <td>23.4500</td>
      <td>2</td>
      <td>1</td>
      <td>NaN</td>
      <td>female</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>889</th>
      <td>True</td>
      <td>yes</td>
      <td>Cherbourg</td>
      <td>C</td>
      <td>True</td>
      <td>man</td>
      <td>First</td>
      <td>C</td>
      <td>30.0000</td>
      <td>0</td>
      <td>0</td>
      <td>26.0</td>
      <td>male</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>890</th>
      <td>True</td>
      <td>no</td>
      <td>Queenstown</td>
      <td>NaN</td>
      <td>True</td>
      <td>man</td>
      <td>Third</td>
      <td>Q</td>
      <td>7.7500</td>
      <td>0</td>
      <td>0</td>
      <td>32.0</td>
      <td>male</td>
      <td>3</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 15 columns</p>
</div>



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




    survived          int64
    pclass            int64
    sex              object
    age             float64
    sibsp             int64
    parch             int64
    fare            float64
    embarked         object
    class          category
    who              object
    adult_male         bool
    deck           category
    embark_town      object
    alive            object
    alone              bool
    dtype: object




```python
# Only Select Numeric types

select_column.select_dtypes(include='number').head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Only Select object types

select_column.select_dtypes(include='object').head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sex</th>
      <th>embarked</th>
      <th>who</th>
      <th>embark_town</th>
      <th>alive</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>male</td>
      <td>S</td>
      <td>man</td>
      <td>Southampton</td>
      <td>no</td>
    </tr>
    <tr>
      <th>1</th>
      <td>female</td>
      <td>C</td>
      <td>woman</td>
      <td>Cherbourg</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>2</th>
      <td>female</td>
      <td>S</td>
      <td>woman</td>
      <td>Southampton</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>3</th>
      <td>female</td>
      <td>S</td>
      <td>woman</td>
      <td>Southampton</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>male</td>
      <td>S</td>
      <td>man</td>
      <td>Southampton</td>
      <td>no</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Only Select character types

select_column.select_dtypes(include='character')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
    </tr>
    <tr>
      <th>1</th>
    </tr>
    <tr>
      <th>2</th>
    </tr>
    <tr>
      <th>3</th>
    </tr>
    <tr>
      <th>4</th>
    </tr>
    <tr>
      <th>...</th>
    </tr>
    <tr>
      <th>886</th>
    </tr>
    <tr>
      <th>887</th>
    </tr>
    <tr>
      <th>888</th>
    </tr>
    <tr>
      <th>889</th>
    </tr>
    <tr>
      <th>890</th>
    </tr>
  </tbody>
</table>
<p>891 rows × 0 columns</p>
</div>




```python
# Only Select multiple datatypes

select_column.select_dtypes(include=['object','character']).head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sex</th>
      <th>embarked</th>
      <th>who</th>
      <th>embark_town</th>
      <th>alive</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>male</td>
      <td>S</td>
      <td>man</td>
      <td>Southampton</td>
      <td>no</td>
    </tr>
    <tr>
      <th>1</th>
      <td>female</td>
      <td>C</td>
      <td>woman</td>
      <td>Cherbourg</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>2</th>
      <td>female</td>
      <td>S</td>
      <td>woman</td>
      <td>Southampton</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>3</th>
      <td>female</td>
      <td>S</td>
      <td>woman</td>
      <td>Southampton</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>male</td>
      <td>S</td>
      <td>man</td>
      <td>Southampton</td>
      <td>no</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Only Select multiple Cdatatypes

select_column.select_dtypes(include=['number','object']).head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>who</th>
      <th>embark_town</th>
      <th>alive</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>man</td>
      <td>Southampton</td>
      <td>no</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>woman</td>
      <td>Cherbourg</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>woman</td>
      <td>Southampton</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>woman</td>
      <td>Southampton</td>
      <td>yes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>man</td>
      <td>Southampton</td>
      <td>no</td>
    </tr>
  </tbody>
</table>
</div>




```python
# exclude multiple datatypes

select_column.select_dtypes(exclude=['number','character']).head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sex</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>male</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>female</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>female</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>female</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>male</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>



# 9- Convert string to number
Here I am using `type_casting` as variable for primary dataset.


```python
# Create Primary data using dictionary

type_casting = pd.DataFrame ({'A': [11, 12, 13], 
                              'B': [14, 15,16] , 
                              'C': [17, 18, 9]})
type_casting
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>11</td>
      <td>14</td>
      <td>17</td>
    </tr>
    <tr>
      <th>1</th>
      <td>12</td>
      <td>15</td>
      <td>18</td>
    </tr>
    <tr>
      <th>2</th>
      <td>13</td>
      <td>16</td>
      <td>9</td>
    </tr>
  </tbody>
</table>
</div>




```python
# All Datatypes

type_casting.dtypes
```




    A    int64
    B    int64
    C    int64
    dtype: object




```python
# Covert all data types to string

type_casting.astype({'A':'object','B':'object','C':'object'}).dtypes
```




    A    object
    B    object
    C    object
    dtype: object




```python
# convert dataset to original data types

type_casting.astype({'A':'int','B':'int','C':'int'}).dtypes
```




    A    int64
    B    int64
    C    int64
    dtype: object




```python
# Second way to convert dataset to original data types

pd.to_numeric(type_casting['A'], errors='coerce')
# type_casting.dtypes
```




    0    11
    1    12
    2    13
    Name: A, dtype: int64



# 10- Reduce dataframe size
Here I am using `boat_01` as variable for `seaborn` librariry dataset `titanic`.


```python
# Load secondary data using the `load_secondary_data` function  

boat_01=sns.load_dataset('titanic')
boat_01.shape
```




    (891, 15)




```python
# to check memory usage of dataframe 

boat_01.info(memory_usage='deep')
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 891 entries, 0 to 890
    Data columns (total 15 columns):
     #   Column       Non-Null Count  Dtype   
    ---  ------       --------------  -----   
     0   survived     891 non-null    int64   
     1   pclass       891 non-null    int64   
     2   sex          891 non-null    object  
     3   age          714 non-null    float64 
     4   sibsp        891 non-null    int64   
     5   parch        891 non-null    int64   
     6   fare         891 non-null    float64 
     7   embarked     889 non-null    object  
     8   class        891 non-null    category
     9   who          891 non-null    object  
     10  adult_male   891 non-null    bool    
     11  deck         203 non-null    category
     12  embark_town  889 non-null    object  
     13  alive        891 non-null    object  
     14  alone        891 non-null    bool    
    dtypes: bool(2), category(2), float64(2), int64(4), object(5)
    memory usage: 278.9 KB



```python
# Check fraction of data with function by fraction 

boat_01.sample(frac=0.1).shape

# boat_01.sample(frac=0.1).shape --- IGNORE ---
```




    (89, 15)



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Khu978#</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>




```python
df=pd.read_clipboard()
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Khu978#</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>30.0708</td>
      <td>C</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>16.7000</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Length of dataset function show rows in dataset

len(split_data)  
```




    891




```python
# shape of dataset function show rows and columns
split_data.shape
```




    (891, 15)




```python
# Use random number generator to generate a random number between 1 and 100

from random import random
split_data_1 = split_data.sample(frac=0.50, random_state=1)
split_data_1.shape

# Data split into half 
```




    (446, 15)




```python
# Retrive left split data 

split_data_2=split_data.drop(split_data_1.index)
split_data_2.shape
```




    (445, 15)




```python
# random head data of split 1st dataset

split_data_1.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>862</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>48.0</td>
      <td>0</td>
      <td>0</td>
      <td>25.9292</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>D</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>223</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>7.8958</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>84</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>17.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5000</td>
      <td>S</td>
      <td>Second</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>680</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.1375</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>535</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>7.0</td>
      <td>0</td>
      <td>2</td>
      <td>26.2500</td>
      <td>S</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
# random head data of split 2nd dataset

split_data_2.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>16.7000</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>15</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>55.0</td>
      <td>0</td>
      <td>0</td>
      <td>16.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>18</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>31.0</td>
      <td>1</td>
      <td>0</td>
      <td>18.0000</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Column Length of each split dataset

len(split_data_2) + len(split_data_1)
```




    891



# 13- Join two data sets


```python
# Combine both split datasets to get original dataset

split_data_join = pd.concat([split_data_1, split_data_2])
split_data_join.shape
```




    (891, 15)




```python
# Reorders rows in dataset from most recent to oldest base on index

split_data_join.sort_index(ascending=True)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 15 columns</p>
</div>




```python
# Reorders rows in dataset from highest to lowest based on index

split_data_join.sort_index(ascending=False)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 15 columns</p>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
filter_data.shape
```




    (891, 15)




```python
filter_data.sex.unique()
```




    array(['male', 'female'], dtype=object)




```python
filter_data.sex.unique()
filter_data

# Return array of unique sex values
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 15 columns</p>
</div>




```python
filter_data[(filter_data.sex=='male')]

# Return the array of male individuals
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>883</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>28.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>884</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>25.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
<p>577 rows × 15 columns</p>
</div>




```python
filter_data.age.unique()

# Return the array of unique ages
```




    array([22.  , 38.  , 26.  , 35.  ,   nan, 54.  ,  2.  , 27.  , 14.  ,
            4.  , 58.  , 20.  , 39.  , 55.  , 31.  , 34.  , 15.  , 28.  ,
            8.  , 19.  , 40.  , 66.  , 42.  , 21.  , 18.  ,  3.  ,  7.  ,
           49.  , 29.  , 65.  , 28.5 ,  5.  , 11.  , 45.  , 17.  , 32.  ,
           16.  , 25.  ,  0.83, 30.  , 33.  , 23.  , 24.  , 46.  , 59.  ,
           71.  , 37.  , 47.  , 14.5 , 70.5 , 32.5 , 12.  ,  9.  , 36.5 ,
           51.  , 55.5 , 40.5 , 44.  ,  1.  , 61.  , 56.  , 50.  , 36.  ,
           45.5 , 20.5 , 62.  , 41.  , 52.  , 63.  , 23.5 ,  0.92, 43.  ,
           60.  , 10.  , 64.  , 13.  , 48.  ,  0.75, 53.  , 57.  , 80.  ,
           70.  , 24.5 ,  6.  ,  0.67, 30.5 ,  0.42, 34.5 , 74.  ])




```python
filter_data.embark_town.unique()

# Return the number of unique embark towns
```




    array(['Southampton', 'Cherbourg', 'Queenstown', nan], dtype=object)




```python

filter_data[(filter_data.embark_town=='Southampton')].shape

# Return the number of passengers who embarked from Southampton
```




    (644, 15)




```python
filter_data[(filter_data.embark_town=='Southampton')
   & (filter_data.sex=="female")]

# Return the number of female passengers who embarked at Southampton
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>16.7000</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>26.5500</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>871</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>47.0</td>
      <td>1</td>
      <td>1</td>
      <td>52.5542</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>D</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>880</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>25.0</td>
      <td>0</td>
      <td>1</td>
      <td>26.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>882</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>22.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5167</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>203 rows × 15 columns</p>
</div>




```python
filter_data[((filter_data.embark_town=='Southampton') | 
   (filter_data.embark_town=='Queenstown') )
   & (filter_data.sex=="female")]

# Return the number  of female passengers who embarked at Southampton and Queenstown
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>16.7000</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>26.5500</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>880</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>25.0</td>
      <td>0</td>
      <td>1</td>
      <td>26.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>882</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>22.0</td>
      <td>0</td>
      <td>0</td>
      <td>10.5167</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>885</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>39.0</td>
      <td>0</td>
      <td>5</td>
      <td>29.1250</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>239 rows × 15 columns</p>
</div>




```python
filter_data[filter_data.embark_town.isin(['Queenstown'])].head()

# Return the number of passengers who embarked in Queenstown 
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>16</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>4</td>
      <td>1</td>
      <td>29.1250</td>
      <td>Q</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>22</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>15.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0292</td>
      <td>Q</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>7.8792</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>32</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




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

    (891, 15)
    (305, 15)
    (384, 15)
    (631, 15)
    (78, 15)


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

    embark_town
    Southampton    644
    Cherbourg      168
    Queenstown      77
    Name: count, dtype: int64
    sex
    male      577
    female    314
    Name: count, dtype: int64
    age
    24.0    30
    22.0    27
    18.0    26
    28.0    25
    30.0    25
    19.0    25
    Name: count, dtype: int64



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

    embark_town
    Southampton    644
    Cherbourg      168
    Name: count, dtype: int64
    sex
    male      577
    female    314
    Name: count, dtype: int64
    age
    24.0    30
    22.0    27
    18.0    26
    Name: count, dtype: int64



```python
# Second way

count=filter_data.embark_town.value_counts(2)

# Returns : {'Southampton': 2, 'Cherbourg': 1, 'Queenstown': 1} 

count.nlargest(2).index

# Returns 2
```




    Index(['Southampton', 'Cherbourg'], dtype='object', name='embark_town')




```python

filter_data[filter_data.embark_town.isin(count.nlargest(1).index)].head()

# Returns the first row of the dataframe where the embark_town is the most common embark_town.
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
filter_data[filter_data.embark_town.isin(count.nlargest(2).index)].head(10)

# Returns the top 3 embark towns with the most passengers.
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>30.0708</td>
      <td>C</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>16.7000</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
filter_data[filter_data.embark_town.isin(count.nsmallest(1).index)].head(10)

# Returns the first 5 rows of the dataframe where the embark_town is in the 3 smallest towns
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>16</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>4</td>
      <td>1</td>
      <td>29.1250</td>
      <td>Q</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>22</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>15.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0292</td>
      <td>Q</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>7.8792</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>32</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>44</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.8792</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>46</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>1</td>
      <td>0</td>
      <td>15.5000</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>47</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>82</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>7.7875</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>109</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>0</td>
      <td>24.1500</td>
      <td>Q</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>yes</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>Age</th>
      <th>Marks</th>
      <th>locations</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Muhammad Kashif</td>
      <td>20</td>
      <td>90</td>
      <td>Farwaniya,Kuwait</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Muhammad Hanif</td>
      <td>21</td>
      <td>85</td>
      <td>Dubai,UAE</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Khurram Shahzad</td>
      <td>19</td>
      <td>88</td>
      <td>Qatar,Qatar</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Wazir Ahmed</td>
      <td>22</td>
      <td>92</td>
      <td>Karachi,Pakistan</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Splitting Name data frame into Two Column  

pm_df.name.str.split(' ',expand=True)
 
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Muhammad</td>
      <td>Kashif</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Muhammad</td>
      <td>Hanif</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Khurram</td>
      <td>Shahzad</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Wazir</td>
      <td>Ahmed</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Adding those splits into new cloumn

pm_df[["First Name","Second Name"]]=pm_df.name.str.split(' ',expand=True)
pm_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>Age</th>
      <th>Marks</th>
      <th>locations</th>
      <th>First Name</th>
      <th>Second Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Muhammad Kashif</td>
      <td>20</td>
      <td>90</td>
      <td>Farwaniya,Kuwait</td>
      <td>Muhammad</td>
      <td>Kashif</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Muhammad Hanif</td>
      <td>21</td>
      <td>85</td>
      <td>Dubai,UAE</td>
      <td>Muhammad</td>
      <td>Hanif</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Khurram Shahzad</td>
      <td>19</td>
      <td>88</td>
      <td>Qatar,Qatar</td>
      <td>Khurram</td>
      <td>Shahzad</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Wazir Ahmed</td>
      <td>22</td>
      <td>92</td>
      <td>Karachi,Pakistan</td>
      <td>Wazir</td>
      <td>Ahmed</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Splitting Locations data frame into Two Column  

pm_df.locations.str.split(',',expand=True)

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Farwaniya</td>
      <td>Kuwait</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Dubai</td>
      <td>UAE</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Qatar</td>
      <td>Qatar</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Karachi</td>
      <td>Pakistan</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Adding those splits into new cloumn

pm_df[["City","Country"]]=pm_df.locations.str.split(',',expand=True)
pm_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
      <th>Age</th>
      <th>Marks</th>
      <th>locations</th>
      <th>First Name</th>
      <th>Second Name</th>
      <th>City</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Muhammad Kashif</td>
      <td>20</td>
      <td>90</td>
      <td>Farwaniya,Kuwait</td>
      <td>Muhammad</td>
      <td>Kashif</td>
      <td>Farwaniya</td>
      <td>Kuwait</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Muhammad Hanif</td>
      <td>21</td>
      <td>85</td>
      <td>Dubai,UAE</td>
      <td>Muhammad</td>
      <td>Hanif</td>
      <td>Dubai</td>
      <td>UAE</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Khurram Shahzad</td>
      <td>19</td>
      <td>88</td>
      <td>Qatar,Qatar</td>
      <td>Khurram</td>
      <td>Shahzad</td>
      <td>Qatar</td>
      <td>Qatar</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Wazir Ahmed</td>
      <td>22</td>
      <td>92</td>
      <td>Karachi,Pakistan</td>
      <td>Wazir</td>
      <td>Ahmed</td>
      <td>Karachi</td>
      <td>Pakistan</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Refine data manipulation

pm_df = pm_df[["First Name","Second Name", "Age","Marks","City","Country"]]
pm_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>First Name</th>
      <th>Second Name</th>
      <th>Age</th>
      <th>Marks</th>
      <th>City</th>
      <th>Country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Muhammad</td>
      <td>Kashif</td>
      <td>20</td>
      <td>90</td>
      <td>Farwaniya</td>
      <td>Kuwait</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Muhammad</td>
      <td>Hanif</td>
      <td>21</td>
      <td>85</td>
      <td>Dubai</td>
      <td>UAE</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Khurram</td>
      <td>Shahzad</td>
      <td>19</td>
      <td>88</td>
      <td>Qatar</td>
      <td>Qatar</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Wazir</td>
      <td>Ahmed</td>
      <td>22</td>
      <td>92</td>
      <td>Karachi</td>
      <td>Pakistan</td>
    </tr>
  </tbody>
</table>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 15 columns</p>
</div>




```python
agg_data.groupby('who').count()

# Return the count of group by object 'who'
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
    <tr>
      <th>who</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>child</th>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
      <td>13</td>
      <td>83</td>
      <td>83</td>
      <td>83</td>
    </tr>
    <tr>
      <th>man</th>
      <td>537</td>
      <td>537</td>
      <td>537</td>
      <td>413</td>
      <td>537</td>
      <td>537</td>
      <td>537</td>
      <td>537</td>
      <td>537</td>
      <td>537</td>
      <td>99</td>
      <td>537</td>
      <td>537</td>
      <td>537</td>
    </tr>
    <tr>
      <th>woman</th>
      <td>271</td>
      <td>271</td>
      <td>271</td>
      <td>218</td>
      <td>271</td>
      <td>271</td>
      <td>271</td>
      <td>269</td>
      <td>271</td>
      <td>271</td>
      <td>91</td>
      <td>269</td>
      <td>271</td>
      <td>271</td>
    </tr>
  </tbody>
</table>
</div>




```python
agg_data.groupby('sex').count()

# Return the count of each sex 
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
    <tr>
      <th>sex</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>female</th>
      <td>314</td>
      <td>314</td>
      <td>261</td>
      <td>314</td>
      <td>314</td>
      <td>314</td>
      <td>312</td>
      <td>314</td>
      <td>314</td>
      <td>314</td>
      <td>97</td>
      <td>312</td>
      <td>314</td>
      <td>314</td>
    </tr>
    <tr>
      <th>male</th>
      <td>577</td>
      <td>577</td>
      <td>453</td>
      <td>577</td>
      <td>577</td>
      <td>577</td>
      <td>577</td>
      <td>577</td>
      <td>577</td>
      <td>577</td>
      <td>106</td>
      <td>577</td>
      <td>577</td>
      <td>577</td>
    </tr>
  </tbody>
</table>
</div>




```python
print(agg_data.groupby('pclass')['age'].sum())

# Return the sum of 'age' for each 'pclass' in the DataFrame .

print(agg_data.groupby('pclass')['age'].mean())

# Return the mean of 'age' for each 'pclass' group.  # noqa: E501
```

    pclass
    1    7111.42
    2    5168.83
    3    8924.92
    Name: age, dtype: float64
    pclass
    1    38.233441
    2    29.877630
    3    25.140620
    Name: age, dtype: float64



```python
len(agg_data.groupby('who'))

# Returns numbers of rows in group by 'who' column
```




    3




```python
len(agg_data.groupby('fare'))

# Returns numbers of rows in group by fare column
```




    248




```python
agg_data.groupby(['sex','who','pclass','embarked']).count()

# Returns a DataFrame with the count of each unique combination of the specified columns.
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th>survived</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>class</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
    <tr>
      <th>sex</th>
      <th>who</th>
      <th>pclass</th>
      <th>embarked</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="15" valign="top">female</th>
      <th rowspan="6" valign="top">child</th>
      <th>1</th>
      <th>S</th>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">2</th>
      <th>C</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>S</th>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>1</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">3</th>
      <th>C</th>
      <td>11</td>
      <td>11</td>
      <td>11</td>
      <td>11</td>
      <td>11</td>
      <td>11</td>
      <td>11</td>
      <td>0</td>
      <td>11</td>
      <td>11</td>
      <td>11</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>S</th>
      <td>18</td>
      <td>18</td>
      <td>18</td>
      <td>18</td>
      <td>18</td>
      <td>18</td>
      <td>18</td>
      <td>2</td>
      <td>18</td>
      <td>18</td>
      <td>18</td>
    </tr>
    <tr>
      <th rowspan="9" valign="top">woman</th>
      <th rowspan="3" valign="top">1</th>
      <th>C</th>
      <td>43</td>
      <td>38</td>
      <td>43</td>
      <td>43</td>
      <td>43</td>
      <td>43</td>
      <td>43</td>
      <td>35</td>
      <td>43</td>
      <td>43</td>
      <td>43</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>S</th>
      <td>45</td>
      <td>41</td>
      <td>45</td>
      <td>45</td>
      <td>45</td>
      <td>45</td>
      <td>45</td>
      <td>40</td>
      <td>45</td>
      <td>45</td>
      <td>45</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">2</th>
      <th>C</th>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>1</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>2</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>S</th>
      <td>59</td>
      <td>58</td>
      <td>59</td>
      <td>59</td>
      <td>59</td>
      <td>59</td>
      <td>59</td>
      <td>7</td>
      <td>59</td>
      <td>59</td>
      <td>59</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">3</th>
      <th>C</th>
      <td>12</td>
      <td>5</td>
      <td>12</td>
      <td>12</td>
      <td>12</td>
      <td>12</td>
      <td>12</td>
      <td>1</td>
      <td>12</td>
      <td>12</td>
      <td>12</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>32</td>
      <td>9</td>
      <td>32</td>
      <td>32</td>
      <td>32</td>
      <td>32</td>
      <td>32</td>
      <td>0</td>
      <td>32</td>
      <td>32</td>
      <td>32</td>
    </tr>
    <tr>
      <th>S</th>
      <td>70</td>
      <td>58</td>
      <td>70</td>
      <td>70</td>
      <td>70</td>
      <td>70</td>
      <td>70</td>
      <td>3</td>
      <td>70</td>
      <td>70</td>
      <td>70</td>
    </tr>
    <tr>
      <th rowspan="15" valign="top">male</th>
      <th rowspan="6" valign="top">child</th>
      <th>1</th>
      <th>S</th>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">2</th>
      <th>C</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>S</th>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
      <td>3</td>
      <td>8</td>
      <td>8</td>
      <td>8</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">3</th>
      <th>C</th>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>0</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>0</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
    </tr>
    <tr>
      <th>S</th>
      <td>20</td>
      <td>20</td>
      <td>20</td>
      <td>20</td>
      <td>20</td>
      <td>20</td>
      <td>20</td>
      <td>1</td>
      <td>20</td>
      <td>20</td>
      <td>20</td>
    </tr>
    <tr>
      <th rowspan="9" valign="top">man</th>
      <th rowspan="3" valign="top">1</th>
      <th>C</th>
      <td>42</td>
      <td>36</td>
      <td>42</td>
      <td>42</td>
      <td>42</td>
      <td>42</td>
      <td>42</td>
      <td>31</td>
      <td>42</td>
      <td>42</td>
      <td>42</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>S</th>
      <td>76</td>
      <td>61</td>
      <td>76</td>
      <td>76</td>
      <td>76</td>
      <td>76</td>
      <td>76</td>
      <td>59</td>
      <td>76</td>
      <td>76</td>
      <td>76</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">2</th>
      <th>C</th>
      <td>9</td>
      <td>7</td>
      <td>9</td>
      <td>9</td>
      <td>9</td>
      <td>9</td>
      <td>9</td>
      <td>1</td>
      <td>9</td>
      <td>9</td>
      <td>9</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>S</th>
      <td>89</td>
      <td>82</td>
      <td>89</td>
      <td>89</td>
      <td>89</td>
      <td>89</td>
      <td>89</td>
      <td>2</td>
      <td>89</td>
      <td>89</td>
      <td>89</td>
    </tr>
    <tr>
      <th rowspan="3" valign="top">3</th>
      <th>C</th>
      <td>39</td>
      <td>21</td>
      <td>39</td>
      <td>39</td>
      <td>39</td>
      <td>39</td>
      <td>39</td>
      <td>0</td>
      <td>39</td>
      <td>39</td>
      <td>39</td>
    </tr>
    <tr>
      <th>Q</th>
      <td>35</td>
      <td>10</td>
      <td>35</td>
      <td>35</td>
      <td>35</td>
      <td>35</td>
      <td>35</td>
      <td>1</td>
      <td>35</td>
      <td>35</td>
      <td>35</td>
    </tr>
    <tr>
      <th>S</th>
      <td>245</td>
      <td>194</td>
      <td>245</td>
      <td>245</td>
      <td>245</td>
      <td>245</td>
      <td>245</td>
      <td>4</td>
      <td>245</td>
      <td>245</td>
      <td>245</td>
    </tr>
  </tbody>
</table>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 15 columns</p>
</div>




```python
row_column.head()

# Print the first 5 rows of the DataFrame
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
# select Column

row_column[['sex','class']].head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sex</th>
      <th>class</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>male</td>
      <td>Third</td>
    </tr>
    <tr>
      <th>1</th>
      <td>female</td>
      <td>First</td>
    </tr>
    <tr>
      <th>2</th>
      <td>female</td>
      <td>Third</td>
    </tr>
    <tr>
      <th>3</th>
      <td>female</td>
      <td>First</td>
    </tr>
    <tr>
      <th>4</th>
      <td>male</td>
      <td>Third</td>
    </tr>
    <tr>
      <th>5</th>
      <td>male</td>
      <td>Third</td>
    </tr>
    <tr>
      <th>6</th>
      <td>male</td>
      <td>First</td>
    </tr>
    <tr>
      <th>7</th>
      <td>male</td>
      <td>Third</td>
    </tr>
    <tr>
      <th>8</th>
      <td>female</td>
      <td>Third</td>
    </tr>
    <tr>
      <th>9</th>
      <td>female</td>
      <td>Second</td>
    </tr>
  </tbody>
</table>
</div>




```python
row_column.describe()

# Returns description  of the data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>891.000000</td>
      <td>891.000000</td>
      <td>714.000000</td>
      <td>891.000000</td>
      <td>891.000000</td>
      <td>891.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>0.383838</td>
      <td>2.308642</td>
      <td>29.699118</td>
      <td>0.523008</td>
      <td>0.381594</td>
      <td>32.204208</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.486592</td>
      <td>0.836071</td>
      <td>14.526497</td>
      <td>1.102743</td>
      <td>0.806057</td>
      <td>49.693429</td>
    </tr>
    <tr>
      <th>min</th>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.420000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>0.000000</td>
      <td>2.000000</td>
      <td>20.125000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>7.910400</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>0.000000</td>
      <td>3.000000</td>
      <td>28.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>14.454200</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>38.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>31.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>80.000000</td>
      <td>8.000000</td>
      <td>6.000000</td>
      <td>512.329200</td>
    </tr>
  </tbody>
</table>
</div>




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

         survived  pclass     age  sibsp  parch      fare
    min       0.0     1.0   0.420    0.0    0.0    0.0000
    25%       0.0     2.0  20.125    0.0    0.0    7.9104
    50%       0.0     3.0  28.000    0.0    0.0   14.4542
    75%       1.0     3.0  38.000    1.0    0.0   31.0000
    max       1.0     3.0  80.000    8.0    6.0  512.3292
         survived  pclass     age  sibsp  parch      fare
    min       0.0     1.0   0.420    0.0    0.0    0.0000
    25%       0.0     2.0  20.125    0.0    0.0    7.9104
    50%       0.0     3.0  28.000    0.0    0.0   14.4542
    75%       1.0     3.0  38.000    1.0    0.0   31.0000
    max       1.0     3.0  80.000    8.0    6.0  512.3292
         survived  pclass    age  sibsp  parch      fare
    min       0.0     1.0   0.42    0.0    0.0    0.0000
    max       1.0     3.0  80.00    8.0    6.0  512.3292



```python
print(agg_data.describe().loc['min':'max','survived':'age'])

# Return the summary statistics for the 'survived' , 'pclass' and 'age' columns of the DataFrame df, excluding th
```

         survived  pclass     age
    min       0.0     1.0   0.420
    25%       0.0     2.0  20.125
    50%       0.0     3.0  28.000
    75%       1.0     3.0  38.000
    max       1.0     3.0  80.000



```python
print(agg_data.describe().loc['min':'max',['survived','age']])

# return the summary statistics for the 'survived' and 'age' columns of the dataframe
```

         survived     age
    min       0.0   0.420
    25%       0.0  20.125
    50%       0.0  28.000
    75%       1.0  38.000
    max       1.0  80.000


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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>0</td>
      <td>2</td>
      <td>male</td>
      <td>27.0</td>
      <td>0</td>
      <td>0</td>
      <td>13.0000</td>
      <td>S</td>
      <td>Second</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
    <tr>
      <th>887</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>19.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>B</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>888</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>NaN</td>
      <td>1</td>
      <td>2</td>
      <td>23.4500</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>889</th>
      <td>1</td>
      <td>1</td>
      <td>male</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>30.0000</td>
      <td>C</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>890</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>32.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.7500</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
<p>891 rows × 15 columns</p>
</div>




```python
reshape.survived.mean()

# Return the mean of the survived column in the titanic dataframe
```




    np.float64(0.3838383838383838)




```python
reshape.groupby('sex').survived.mean()

# Return the mean survival rate for each sex
```




    sex
    female    0.742038
    male      0.188908
    Name: survived, dtype: float64




```python
reshape.groupby(['sex','class']).survived.mean()

# Return the mean survival rate for each sex and class 
```

    C:\Users\khurr\AppData\Local\Temp\ipykernel_6404\3083093482.py:1: FutureWarning: The default of observed=False is deprecated and will be changed to True in a future version of pandas. Pass observed=False to retain current behavior or observed=True to adopt the future default and silence this warning.
      reshape.groupby(['sex','class']).survived.mean()





    sex     class 
    female  First     0.968085
            Second    0.921053
            Third     0.500000
    male    First     0.368852
            Second    0.157407
            Third     0.135447
    Name: survived, dtype: float64




```python
agg_data.groupby(['sex','class']).survived.mean().unstack()

# Return the mean survival rate for each sex and class as a reshaped DataFrame
```

    C:\Users\khurr\AppData\Local\Temp\ipykernel_6404\3951748357.py:1: FutureWarning: The default of observed=False is deprecated and will be changed to True in a future version of pandas. Pass observed=False to retain current behavior or observed=True to adopt the future default and silence this warning.
      agg_data.groupby(['sex','class']).survived.mean().unstack()





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>class</th>
      <th>First</th>
      <th>Second</th>
      <th>Third</th>
    </tr>
    <tr>
      <th>sex</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>female</th>
      <td>0.968085</td>
      <td>0.921053</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>male</th>
      <td>0.368852</td>
      <td>0.157407</td>
      <td>0.135447</td>
    </tr>
  </tbody>
</table>
</div>



# 20- Continous to categorical data convesion
Here I am calling again `boat ` as variable for `seaborn` librariry dataset `titanic`.


```python
boat.head()

# Return the first 5 rows of the DataFrame
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>




```python
print(boat.age.head())
print(boat.shape)
```

    0    22.0
    1    38.0
    2    26.0
    3    35.0
    4    35.0
    Name: age, dtype: float64
    (891, 15)



```python
pd.cut(boat.age, bins= [0,10,18,25,50,99], labels=['Infant','child','young_adult','Adult','old']).head()

# Return the bins and labels

boat['New _Age'] = pd.cut(boat.age, bins= [0,10,18,25,50,99], labels=['Infant','child','young_adult','Adult','old'])

# Add a new column with the age group

boat.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
      <th>New _Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>young_adult</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>Adult</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>Adult</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>old</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>Infant</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>30.0708</td>
      <td>C</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>child</td>
    </tr>
  </tbody>
</table>
</div>




```python
boat.shape
```




    (891, 16)



# 21- Covert one set vlue to another set value
Here I am calling again `boat ` as variable for `seaborn` librariry dataset `titanic`.


```python
boat.sex.head()
```




    0      male
    1    female
    2    female
    3    female
    4      male
    Name: sex, dtype: object




```python
boat['sex_num']=boat.sex.map({'male':0,'female':1})

# Return the dataframe with the new column sex _num
# Intialize sex with 0 and 1

boat.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
      <th>New _Age</th>
      <th>sex_num</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>young_adult</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>Adult</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>Adult</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
boat.shape
```




    (891, 17)




```python
boat.embarked.count()
```




    np.int64(889)




```python
boat['embarked_num']=boat.embarked.factorize()[0]

# Return the dataframe with the new column embark _num
# Intialize embark 0 as 0 and embark 1 as 1 and embark 2 as 2

boat.head(15)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
      <th>New _Age</th>
      <th>sex_num</th>
      <th>embarked_num</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>young_adult</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>Adult</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>Adult</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
      <td>NaN</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>old</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>Infant</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>30.0708</td>
      <td>C</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>child</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>16.7000</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Infant</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>26.5500</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>old</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>20.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>young_adult</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>39.0</td>
      <td>1</td>
      <td>5</td>
      <td>31.2750</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>Adult</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>14.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.8542</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>child</td>
      <td>1</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
boat['fare_num']=boat.fare.factorize()[0]

# Return the dataframe with the new column age _num
# Intialize age with 0 and so on

boat.head(15)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>survived</th>
      <th>pclass</th>
      <th>sex</th>
      <th>age</th>
      <th>sibsp</th>
      <th>parch</th>
      <th>fare</th>
      <th>embarked</th>
      <th>class</th>
      <th>who</th>
      <th>adult_male</th>
      <th>deck</th>
      <th>embark_town</th>
      <th>alive</th>
      <th>alone</th>
      <th>New _Age</th>
      <th>sex_num</th>
      <th>embarked_num</th>
      <th>fare_num</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>7.2500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>young_adult</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>71.2833</td>
      <td>C</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.9250</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>Adult</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>53.1000</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>Adult</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>NaN</td>
      <td>0</td>
      <td>0</td>
      <td>8.4583</td>
      <td>Q</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Queenstown</td>
      <td>no</td>
      <td>True</td>
      <td>NaN</td>
      <td>0</td>
      <td>2</td>
      <td>5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>1</td>
      <td>male</td>
      <td>54.0</td>
      <td>0</td>
      <td>0</td>
      <td>51.8625</td>
      <td>S</td>
      <td>First</td>
      <td>man</td>
      <td>True</td>
      <td>E</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>old</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>2.0</td>
      <td>3</td>
      <td>1</td>
      <td>21.0750</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>Infant</td>
      <td>0</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>27.0</td>
      <td>0</td>
      <td>2</td>
      <td>11.1333</td>
      <td>S</td>
      <td>Third</td>
      <td>woman</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Adult</td>
      <td>1</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1</td>
      <td>2</td>
      <td>female</td>
      <td>14.0</td>
      <td>1</td>
      <td>0</td>
      <td>30.0708</td>
      <td>C</td>
      <td>Second</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Cherbourg</td>
      <td>yes</td>
      <td>False</td>
      <td>child</td>
      <td>1</td>
      <td>1</td>
      <td>9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>1</td>
      <td>3</td>
      <td>female</td>
      <td>4.0</td>
      <td>1</td>
      <td>1</td>
      <td>16.7000</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>G</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>False</td>
      <td>Infant</td>
      <td>1</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>1</td>
      <td>1</td>
      <td>female</td>
      <td>58.0</td>
      <td>0</td>
      <td>0</td>
      <td>26.5500</td>
      <td>S</td>
      <td>First</td>
      <td>woman</td>
      <td>False</td>
      <td>C</td>
      <td>Southampton</td>
      <td>yes</td>
      <td>True</td>
      <td>old</td>
      <td>1</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <th>12</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>20.0</td>
      <td>0</td>
      <td>0</td>
      <td>8.0500</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>young_adult</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <th>13</th>
      <td>0</td>
      <td>3</td>
      <td>male</td>
      <td>39.0</td>
      <td>1</td>
      <td>5</td>
      <td>31.2750</td>
      <td>S</td>
      <td>Third</td>
      <td>man</td>
      <td>True</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>False</td>
      <td>Adult</td>
      <td>0</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <th>14</th>
      <td>0</td>
      <td>3</td>
      <td>female</td>
      <td>14.0</td>
      <td>0</td>
      <td>0</td>
      <td>7.8542</td>
      <td>S</td>
      <td>Third</td>
      <td>child</td>
      <td>False</td>
      <td>NaN</td>
      <td>Southampton</td>
      <td>no</td>
      <td>True</td>
      <td>child</td>
      <td>1</td>
      <td>0</td>
      <td>13</td>
    </tr>
  </tbody>
</table>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>a</th>
      <th>b</th>
      <th>c</th>
      <th>d</th>
      <th>e</th>
      <th>f</th>
      <th>g</th>
      <th>h</th>
      <th>i</th>
      <th>j</th>
      <th>...</th>
      <th>p</th>
      <th>q</th>
      <th>r</th>
      <th>s</th>
      <th>t</th>
      <th>u</th>
      <th>v</th>
      <th>w</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.312185</td>
      <td>0.759857</td>
      <td>0.785469</td>
      <td>0.790171</td>
      <td>0.917300</td>
      <td>0.255756</td>
      <td>0.534178</td>
      <td>0.829463</td>
      <td>0.282479</td>
      <td>0.528905</td>
      <td>...</td>
      <td>0.765168</td>
      <td>0.816579</td>
      <td>0.297229</td>
      <td>0.728562</td>
      <td>0.370228</td>
      <td>0.220852</td>
      <td>0.076066</td>
      <td>0.432253</td>
      <td>0.679345</td>
      <td>0.556398</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.215947</td>
      <td>0.262042</td>
      <td>0.252489</td>
      <td>0.839078</td>
      <td>0.035190</td>
      <td>0.439831</td>
      <td>0.870099</td>
      <td>0.073469</td>
      <td>0.526713</td>
      <td>0.024814</td>
      <td>...</td>
      <td>0.362505</td>
      <td>0.714559</td>
      <td>0.292751</td>
      <td>0.859524</td>
      <td>0.607786</td>
      <td>0.485211</td>
      <td>0.191092</td>
      <td>0.691071</td>
      <td>0.935755</td>
      <td>0.737135</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.419566</td>
      <td>0.846532</td>
      <td>0.532264</td>
      <td>0.518754</td>
      <td>0.901134</td>
      <td>0.333348</td>
      <td>0.696998</td>
      <td>0.506755</td>
      <td>0.718735</td>
      <td>0.240628</td>
      <td>...</td>
      <td>0.806073</td>
      <td>0.665919</td>
      <td>0.762262</td>
      <td>0.915762</td>
      <td>0.210725</td>
      <td>0.667012</td>
      <td>0.456732</td>
      <td>0.595605</td>
      <td>0.272982</td>
      <td>0.921855</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.121948</td>
      <td>0.765014</td>
      <td>0.210878</td>
      <td>0.775115</td>
      <td>0.417464</td>
      <td>0.860609</td>
      <td>0.714851</td>
      <td>0.254403</td>
      <td>0.771660</td>
      <td>0.579848</td>
      <td>...</td>
      <td>0.000041</td>
      <td>0.237328</td>
      <td>0.715867</td>
      <td>0.165053</td>
      <td>0.100696</td>
      <td>0.670154</td>
      <td>0.473300</td>
      <td>0.994668</td>
      <td>0.798456</td>
      <td>0.336976</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.477667</td>
      <td>0.726454</td>
      <td>0.025687</td>
      <td>0.562962</td>
      <td>0.308544</td>
      <td>0.304222</td>
      <td>0.113057</td>
      <td>0.800701</td>
      <td>0.684454</td>
      <td>0.061851</td>
      <td>...</td>
      <td>0.605899</td>
      <td>0.624772</td>
      <td>0.302757</td>
      <td>0.412686</td>
      <td>0.199707</td>
      <td>0.466476</td>
      <td>0.296738</td>
      <td>0.681750</td>
      <td>0.165399</td>
      <td>0.887966</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 25 columns</p>
</div>




```python
trasnpose.head(10).T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>5</th>
      <th>6</th>
      <th>7</th>
      <th>8</th>
      <th>9</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>0.312185</td>
      <td>0.215947</td>
      <td>0.419566</td>
      <td>0.121948</td>
      <td>0.477667</td>
      <td>0.360740</td>
      <td>0.931044</td>
      <td>0.953874</td>
      <td>0.557457</td>
      <td>0.762424</td>
    </tr>
    <tr>
      <th>b</th>
      <td>0.759857</td>
      <td>0.262042</td>
      <td>0.846532</td>
      <td>0.765014</td>
      <td>0.726454</td>
      <td>0.928959</td>
      <td>0.423455</td>
      <td>0.076674</td>
      <td>0.340048</td>
      <td>0.346804</td>
    </tr>
    <tr>
      <th>c</th>
      <td>0.785469</td>
      <td>0.252489</td>
      <td>0.532264</td>
      <td>0.210878</td>
      <td>0.025687</td>
      <td>0.456040</td>
      <td>0.906710</td>
      <td>0.767356</td>
      <td>0.152915</td>
      <td>0.886380</td>
    </tr>
    <tr>
      <th>d</th>
      <td>0.790171</td>
      <td>0.839078</td>
      <td>0.518754</td>
      <td>0.775115</td>
      <td>0.562962</td>
      <td>0.295590</td>
      <td>0.741157</td>
      <td>0.902775</td>
      <td>0.280671</td>
      <td>0.428476</td>
    </tr>
    <tr>
      <th>e</th>
      <td>0.917300</td>
      <td>0.035190</td>
      <td>0.901134</td>
      <td>0.417464</td>
      <td>0.308544</td>
      <td>0.732828</td>
      <td>0.098020</td>
      <td>0.087984</td>
      <td>0.449097</td>
      <td>0.645875</td>
    </tr>
    <tr>
      <th>f</th>
      <td>0.255756</td>
      <td>0.439831</td>
      <td>0.333348</td>
      <td>0.860609</td>
      <td>0.304222</td>
      <td>0.262383</td>
      <td>0.620133</td>
      <td>0.206141</td>
      <td>0.757956</td>
      <td>0.270991</td>
    </tr>
    <tr>
      <th>g</th>
      <td>0.534178</td>
      <td>0.870099</td>
      <td>0.696998</td>
      <td>0.714851</td>
      <td>0.113057</td>
      <td>0.929749</td>
      <td>0.997177</td>
      <td>0.671495</td>
      <td>0.902079</td>
      <td>0.170542</td>
    </tr>
    <tr>
      <th>h</th>
      <td>0.829463</td>
      <td>0.073469</td>
      <td>0.506755</td>
      <td>0.254403</td>
      <td>0.800701</td>
      <td>0.254778</td>
      <td>0.851118</td>
      <td>0.282112</td>
      <td>0.413396</td>
      <td>0.507712</td>
    </tr>
    <tr>
      <th>i</th>
      <td>0.282479</td>
      <td>0.526713</td>
      <td>0.718735</td>
      <td>0.771660</td>
      <td>0.684454</td>
      <td>0.801717</td>
      <td>0.853368</td>
      <td>0.357408</td>
      <td>0.965238</td>
      <td>0.418907</td>
    </tr>
    <tr>
      <th>j</th>
      <td>0.528905</td>
      <td>0.024814</td>
      <td>0.240628</td>
      <td>0.579848</td>
      <td>0.061851</td>
      <td>0.598666</td>
      <td>0.274169</td>
      <td>0.205382</td>
      <td>0.239518</td>
      <td>0.176646</td>
    </tr>
    <tr>
      <th>k</th>
      <td>0.676444</td>
      <td>0.323557</td>
      <td>0.849943</td>
      <td>0.807204</td>
      <td>0.716339</td>
      <td>0.579339</td>
      <td>0.773822</td>
      <td>0.608305</td>
      <td>0.477573</td>
      <td>0.752239</td>
    </tr>
    <tr>
      <th>l</th>
      <td>0.721265</td>
      <td>0.214803</td>
      <td>0.201666</td>
      <td>0.851556</td>
      <td>0.593993</td>
      <td>0.110867</td>
      <td>0.242329</td>
      <td>0.973102</td>
      <td>0.793496</td>
      <td>0.181322</td>
    </tr>
    <tr>
      <th>m</th>
      <td>0.579796</td>
      <td>0.368860</td>
      <td>0.145801</td>
      <td>0.173394</td>
      <td>0.193499</td>
      <td>0.516271</td>
      <td>0.687640</td>
      <td>0.259323</td>
      <td>0.516133</td>
      <td>0.098394</td>
    </tr>
    <tr>
      <th>n</th>
      <td>0.121146</td>
      <td>0.487799</td>
      <td>0.222486</td>
      <td>0.204854</td>
      <td>0.327343</td>
      <td>0.296322</td>
      <td>0.146250</td>
      <td>0.265024</td>
      <td>0.924702</td>
      <td>0.949603</td>
    </tr>
    <tr>
      <th>o</th>
      <td>0.245519</td>
      <td>0.949857</td>
      <td>0.458977</td>
      <td>0.367278</td>
      <td>0.623035</td>
      <td>0.574563</td>
      <td>0.198075</td>
      <td>0.367382</td>
      <td>0.849290</td>
      <td>0.771110</td>
    </tr>
    <tr>
      <th>p</th>
      <td>0.765168</td>
      <td>0.362505</td>
      <td>0.806073</td>
      <td>0.000041</td>
      <td>0.605899</td>
      <td>0.117370</td>
      <td>0.950759</td>
      <td>0.511540</td>
      <td>0.425132</td>
      <td>0.729115</td>
    </tr>
    <tr>
      <th>q</th>
      <td>0.816579</td>
      <td>0.714559</td>
      <td>0.665919</td>
      <td>0.237328</td>
      <td>0.624772</td>
      <td>0.772975</td>
      <td>0.034046</td>
      <td>0.532020</td>
      <td>0.195897</td>
      <td>0.892498</td>
    </tr>
    <tr>
      <th>r</th>
      <td>0.297229</td>
      <td>0.292751</td>
      <td>0.762262</td>
      <td>0.715867</td>
      <td>0.302757</td>
      <td>0.060740</td>
      <td>0.383637</td>
      <td>0.109517</td>
      <td>0.312228</td>
      <td>0.631955</td>
    </tr>
    <tr>
      <th>s</th>
      <td>0.728562</td>
      <td>0.859524</td>
      <td>0.915762</td>
      <td>0.165053</td>
      <td>0.412686</td>
      <td>0.055033</td>
      <td>0.921264</td>
      <td>0.819021</td>
      <td>0.451322</td>
      <td>0.513265</td>
    </tr>
    <tr>
      <th>t</th>
      <td>0.370228</td>
      <td>0.607786</td>
      <td>0.210725</td>
      <td>0.100696</td>
      <td>0.199707</td>
      <td>0.781130</td>
      <td>0.890890</td>
      <td>0.871303</td>
      <td>0.728177</td>
      <td>0.702790</td>
    </tr>
    <tr>
      <th>u</th>
      <td>0.220852</td>
      <td>0.485211</td>
      <td>0.667012</td>
      <td>0.670154</td>
      <td>0.466476</td>
      <td>0.963352</td>
      <td>0.262301</td>
      <td>0.145793</td>
      <td>0.750082</td>
      <td>0.321978</td>
    </tr>
    <tr>
      <th>v</th>
      <td>0.076066</td>
      <td>0.191092</td>
      <td>0.456732</td>
      <td>0.473300</td>
      <td>0.296738</td>
      <td>0.170725</td>
      <td>0.439412</td>
      <td>0.237072</td>
      <td>0.743053</td>
      <td>0.198227</td>
    </tr>
    <tr>
      <th>w</th>
      <td>0.432253</td>
      <td>0.691071</td>
      <td>0.595605</td>
      <td>0.994668</td>
      <td>0.681750</td>
      <td>0.294188</td>
      <td>0.625547</td>
      <td>0.216695</td>
      <td>0.679731</td>
      <td>0.850527</td>
    </tr>
    <tr>
      <th>x</th>
      <td>0.679345</td>
      <td>0.935755</td>
      <td>0.272982</td>
      <td>0.798456</td>
      <td>0.165399</td>
      <td>0.370602</td>
      <td>0.129017</td>
      <td>0.678888</td>
      <td>0.919386</td>
      <td>0.971830</td>
    </tr>
    <tr>
      <th>y</th>
      <td>0.556398</td>
      <td>0.737135</td>
      <td>0.921855</td>
      <td>0.336976</td>
      <td>0.887966</td>
      <td>0.882009</td>
      <td>0.158962</td>
      <td>0.690300</td>
      <td>0.888924</td>
      <td>0.408252</td>
    </tr>
  </tbody>
</table>
</div>




```python
trasnpose.shape
```




    (200, 25)




```python
trasnpose.describe().T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>200.0</td>
      <td>0.525405</td>
      <td>0.301848</td>
      <td>0.004790</td>
      <td>0.254641</td>
      <td>0.553962</td>
      <td>0.781588</td>
      <td>0.998306</td>
    </tr>
    <tr>
      <th>b</th>
      <td>200.0</td>
      <td>0.499002</td>
      <td>0.298227</td>
      <td>0.010871</td>
      <td>0.237543</td>
      <td>0.505543</td>
      <td>0.764477</td>
      <td>0.998805</td>
    </tr>
    <tr>
      <th>c</th>
      <td>200.0</td>
      <td>0.527150</td>
      <td>0.293464</td>
      <td>0.003188</td>
      <td>0.272912</td>
      <td>0.550182</td>
      <td>0.778227</td>
      <td>0.999786</td>
    </tr>
    <tr>
      <th>d</th>
      <td>200.0</td>
      <td>0.490388</td>
      <td>0.287640</td>
      <td>0.004382</td>
      <td>0.240957</td>
      <td>0.504246</td>
      <td>0.748601</td>
      <td>0.987836</td>
    </tr>
    <tr>
      <th>e</th>
      <td>200.0</td>
      <td>0.485016</td>
      <td>0.310831</td>
      <td>0.001182</td>
      <td>0.218383</td>
      <td>0.454854</td>
      <td>0.788560</td>
      <td>0.993256</td>
    </tr>
    <tr>
      <th>f</th>
      <td>200.0</td>
      <td>0.471442</td>
      <td>0.291553</td>
      <td>0.000996</td>
      <td>0.204871</td>
      <td>0.459052</td>
      <td>0.716126</td>
      <td>0.998939</td>
    </tr>
    <tr>
      <th>g</th>
      <td>200.0</td>
      <td>0.498944</td>
      <td>0.300018</td>
      <td>0.012480</td>
      <td>0.228568</td>
      <td>0.515315</td>
      <td>0.790638</td>
      <td>0.997177</td>
    </tr>
    <tr>
      <th>h</th>
      <td>200.0</td>
      <td>0.461830</td>
      <td>0.291477</td>
      <td>0.000371</td>
      <td>0.213926</td>
      <td>0.455739</td>
      <td>0.698378</td>
      <td>0.999389</td>
    </tr>
    <tr>
      <th>i</th>
      <td>200.0</td>
      <td>0.515581</td>
      <td>0.288719</td>
      <td>0.008894</td>
      <td>0.269040</td>
      <td>0.521910</td>
      <td>0.770613</td>
      <td>0.994153</td>
    </tr>
    <tr>
      <th>j</th>
      <td>200.0</td>
      <td>0.492484</td>
      <td>0.298149</td>
      <td>0.002338</td>
      <td>0.230746</td>
      <td>0.515340</td>
      <td>0.738074</td>
      <td>0.999454</td>
    </tr>
    <tr>
      <th>k</th>
      <td>200.0</td>
      <td>0.498148</td>
      <td>0.277639</td>
      <td>0.000517</td>
      <td>0.273265</td>
      <td>0.489190</td>
      <td>0.724958</td>
      <td>0.997063</td>
    </tr>
    <tr>
      <th>l</th>
      <td>200.0</td>
      <td>0.532916</td>
      <td>0.306905</td>
      <td>0.012063</td>
      <td>0.247850</td>
      <td>0.558948</td>
      <td>0.803074</td>
      <td>0.995989</td>
    </tr>
    <tr>
      <th>m</th>
      <td>200.0</td>
      <td>0.450615</td>
      <td>0.275540</td>
      <td>0.003133</td>
      <td>0.200489</td>
      <td>0.421917</td>
      <td>0.681656</td>
      <td>0.992197</td>
    </tr>
    <tr>
      <th>n</th>
      <td>200.0</td>
      <td>0.520184</td>
      <td>0.293435</td>
      <td>0.006261</td>
      <td>0.279440</td>
      <td>0.516235</td>
      <td>0.767509</td>
      <td>0.996370</td>
    </tr>
    <tr>
      <th>o</th>
      <td>200.0</td>
      <td>0.492555</td>
      <td>0.282853</td>
      <td>0.002816</td>
      <td>0.248330</td>
      <td>0.485345</td>
      <td>0.726671</td>
      <td>0.996873</td>
    </tr>
    <tr>
      <th>p</th>
      <td>200.0</td>
      <td>0.491362</td>
      <td>0.282324</td>
      <td>0.000041</td>
      <td>0.271483</td>
      <td>0.486980</td>
      <td>0.726502</td>
      <td>0.997374</td>
    </tr>
    <tr>
      <th>q</th>
      <td>200.0</td>
      <td>0.499021</td>
      <td>0.295454</td>
      <td>0.001569</td>
      <td>0.229455</td>
      <td>0.511555</td>
      <td>0.762972</td>
      <td>0.994297</td>
    </tr>
    <tr>
      <th>r</th>
      <td>200.0</td>
      <td>0.492360</td>
      <td>0.299956</td>
      <td>0.002052</td>
      <td>0.226110</td>
      <td>0.507646</td>
      <td>0.761669</td>
      <td>0.997807</td>
    </tr>
    <tr>
      <th>s</th>
      <td>200.0</td>
      <td>0.506337</td>
      <td>0.283712</td>
      <td>0.005067</td>
      <td>0.271237</td>
      <td>0.509414</td>
      <td>0.766250</td>
      <td>0.990688</td>
    </tr>
    <tr>
      <th>t</th>
      <td>200.0</td>
      <td>0.530178</td>
      <td>0.285268</td>
      <td>0.009213</td>
      <td>0.287078</td>
      <td>0.514811</td>
      <td>0.798894</td>
      <td>0.990530</td>
    </tr>
    <tr>
      <th>u</th>
      <td>200.0</td>
      <td>0.521140</td>
      <td>0.283428</td>
      <td>0.007259</td>
      <td>0.271238</td>
      <td>0.537179</td>
      <td>0.763127</td>
      <td>0.989247</td>
    </tr>
    <tr>
      <th>v</th>
      <td>200.0</td>
      <td>0.449504</td>
      <td>0.286433</td>
      <td>0.002994</td>
      <td>0.196785</td>
      <td>0.399158</td>
      <td>0.724829</td>
      <td>0.986338</td>
    </tr>
    <tr>
      <th>w</th>
      <td>200.0</td>
      <td>0.514413</td>
      <td>0.276181</td>
      <td>0.008316</td>
      <td>0.273643</td>
      <td>0.527077</td>
      <td>0.721546</td>
      <td>0.997454</td>
    </tr>
    <tr>
      <th>x</th>
      <td>200.0</td>
      <td>0.483571</td>
      <td>0.288590</td>
      <td>0.001688</td>
      <td>0.244087</td>
      <td>0.467251</td>
      <td>0.709383</td>
      <td>0.996317</td>
    </tr>
    <tr>
      <th>y</th>
      <td>200.0</td>
      <td>0.532758</td>
      <td>0.288575</td>
      <td>0.008782</td>
      <td>0.288385</td>
      <td>0.538031</td>
      <td>0.778894</td>
      <td>0.993230</td>
    </tr>
  </tbody>
</table>
</div>



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




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>zip</th>
      <th>factory</th>
      <th>warehouse</th>
      <th>retail</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>12345</td>
      <td>100</td>
      <td>200</td>
      <td>400</td>
    </tr>
    <tr>
      <th>1</th>
      <td>34567</td>
      <td>400</td>
      <td>500</td>
      <td>400</td>
    </tr>
    <tr>
      <th>2</th>
      <td>67890</td>
      <td>700</td>
      <td>800</td>
      <td>900</td>
    </tr>
  </tbody>
</table>
</div>




```python
reshape.head().T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>zip</th>
      <td>12345</td>
      <td>34567</td>
      <td>67890</td>
    </tr>
    <tr>
      <th>factory</th>
      <td>100</td>
      <td>400</td>
      <td>700</td>
    </tr>
    <tr>
      <th>warehouse</th>
      <td>200</td>
      <td>500</td>
      <td>800</td>
    </tr>
    <tr>
      <th>retail</th>
      <td>400</td>
      <td>400</td>
      <td>900</td>
    </tr>
  </tbody>
</table>
</div>




```python
reshape_1=pd.DataFrame([[1,'12345','factory'],
                        [2,'34567','warehouse'],
                        [3,'67890','retail']],
                       columns=['user_id','zip','location_type'])
reshape_1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>user_id</th>
      <th>zip</th>
      <th>location_type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>12345</td>
      <td>factory</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>34567</td>
      <td>warehouse</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>67890</td>
      <td>retail</td>
    </tr>
  </tbody>
</table>
</div>




```python
reshape
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>zip</th>
      <th>factory</th>
      <th>warehouse</th>
      <th>retail</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>12345</td>
      <td>100</td>
      <td>200</td>
      <td>400</td>
    </tr>
    <tr>
      <th>1</th>
      <td>34567</td>
      <td>400</td>
      <td>500</td>
      <td>400</td>
    </tr>
    <tr>
      <th>2</th>
      <td>67890</td>
      <td>700</td>
      <td>800</td>
      <td>900</td>
    </tr>
  </tbody>
</table>
</div>




```python
reshape.melt(id_vars='zip',var_name='location_type',value_name='distance')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>zip</th>
      <th>location_type</th>
      <th>distance</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>12345</td>
      <td>factory</td>
      <td>100</td>
    </tr>
    <tr>
      <th>1</th>
      <td>34567</td>
      <td>factory</td>
      <td>400</td>
    </tr>
    <tr>
      <th>2</th>
      <td>67890</td>
      <td>factory</td>
      <td>700</td>
    </tr>
    <tr>
      <th>3</th>
      <td>12345</td>
      <td>warehouse</td>
      <td>200</td>
    </tr>
    <tr>
      <th>4</th>
      <td>34567</td>
      <td>warehouse</td>
      <td>500</td>
    </tr>
    <tr>
      <th>5</th>
      <td>67890</td>
      <td>warehouse</td>
      <td>800</td>
    </tr>
    <tr>
      <th>6</th>
      <td>12345</td>
      <td>retail</td>
      <td>400</td>
    </tr>
    <tr>
      <th>7</th>
      <td>34567</td>
      <td>retail</td>
      <td>400</td>
    </tr>
    <tr>
      <th>8</th>
      <td>67890</td>
      <td>retail</td>
      <td>900</td>
    </tr>
  </tbody>
</table>
</div>




```python
import seaborn as sns
sns.barplot(x='zip',y='factory',data=reshape)
```




    <Axes: xlabel='zip', ylabel='factory'>




    
![png](output_143_1.png)
    



```python
reshape_1=reshape.melt(id_vars='zip',var_name='location_type',value_name='distance')

# Return the result of the melt operation 

reshape_1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>zip</th>
      <th>location_type</th>
      <th>distance</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>12345</td>
      <td>factory</td>
      <td>100</td>
    </tr>
    <tr>
      <th>1</th>
      <td>34567</td>
      <td>factory</td>
      <td>400</td>
    </tr>
    <tr>
      <th>2</th>
      <td>67890</td>
      <td>factory</td>
      <td>700</td>
    </tr>
    <tr>
      <th>3</th>
      <td>12345</td>
      <td>warehouse</td>
      <td>200</td>
    </tr>
    <tr>
      <th>4</th>
      <td>34567</td>
      <td>warehouse</td>
      <td>500</td>
    </tr>
    <tr>
      <th>5</th>
      <td>67890</td>
      <td>warehouse</td>
      <td>800</td>
    </tr>
    <tr>
      <th>6</th>
      <td>12345</td>
      <td>retail</td>
      <td>400</td>
    </tr>
    <tr>
      <th>7</th>
      <td>34567</td>
      <td>retail</td>
      <td>400</td>
    </tr>
    <tr>
      <th>8</th>
      <td>67890</td>
      <td>retail</td>
      <td>900</td>
    </tr>
  </tbody>
</table>
</div>




```python
import seaborn as sns
sns.barplot(x='zip',y='distance',hue='location_type',data=reshape_1)
```




    <Axes: xlabel='zip', ylabel='distance'>




    
![png](output_145_1.png)
    

