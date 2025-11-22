- 💡 **Subject** : Pandas tips and tricks\
- 🖊️ **Author:** Khurram Shahzad  
- 🎓 **Mentor:** Dr. Aammar Tufail  
- ✉️ **Email:** [khurramamq@gmail.com](mailto:khurramamq@gmail.com)  
- 💻 **GitHub:** [zkskhurram](https://github.com/zkskhurram/Python_-My_Small_knowledge/tree/main)
  
⚙️ Overview\
When working in Python, libraries make your life easier — they’re ready-made toolkits that save time, prevent code repetition, and bring powerful functions for data, AI, and automation.




```python
# import pandas library

import pandas as pd
```


```python
# load dataset from seaborn

import seaborn as sns

# titanic kay datset ko load karyn using variable name 'boat'

boat=sns.load_dataset('titanic')

# dataset ko print karyn

boat

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
# load tips dataset form seaborn library using variable `time`

time=sns.load_dataset('tips')

# print the dataset

time
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
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>239</th>
      <td>29.03</td>
      <td>5.92</td>
      <td>Male</td>
      <td>No</td>
      <td>Sat</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>240</th>
      <td>27.18</td>
      <td>2.00</td>
      <td>Female</td>
      <td>Yes</td>
      <td>Sat</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>241</th>
      <td>22.67</td>
      <td>2.00</td>
      <td>Male</td>
      <td>Yes</td>
      <td>Sat</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>242</th>
      <td>17.82</td>
      <td>1.75</td>
      <td>Male</td>
      <td>No</td>
      <td>Sat</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>243</th>
      <td>18.78</td>
      <td>3.00</td>
      <td>Female</td>
      <td>No</td>
      <td>Thur</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
<p>244 rows × 7 columns</p>
</div>




```python
# display information about the titanic dataset

boat.info()
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
    memory usage: 80.7+ KB



```python
# display first 10 rows of the titanic dataset

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
  </tbody>
</table>
</div>




```python
# load iris dataset from seaborn library using variable name 'flower'

flower=sns.load_dataset('iris')
flower
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
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>145</th>
      <td>6.7</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>146</th>
      <td>6.3</td>
      <td>2.5</td>
      <td>5.0</td>
      <td>1.9</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>147</th>
      <td>6.5</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.0</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>148</th>
      <td>6.2</td>
      <td>3.4</td>
      <td>5.4</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>149</th>
      <td>5.9</td>
      <td>3.0</td>
      <td>5.1</td>
      <td>1.8</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
<p>150 rows × 5 columns</p>
</div>




```python
# print 10 random samples from the flower dataset

print(flower.sample(10))

# display information about the flower dataset

print(flower.info())

```

         sepal_length  sepal_width  petal_length  petal_width     species
    47            4.6          3.2           1.4          0.2      setosa
    65            6.7          3.1           4.4          1.4  versicolor
    101           5.8          2.7           5.1          1.9   virginica
    44            5.1          3.8           1.9          0.4      setosa
    113           5.7          2.5           5.0          2.0   virginica
    52            6.9          3.1           4.9          1.5  versicolor
    79            5.7          2.6           3.5          1.0  versicolor
    6             4.6          3.4           1.4          0.3      setosa
    62            6.0          2.2           4.0          1.0  versicolor
    104           6.5          3.0           5.8          2.2   virginica
    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 150 entries, 0 to 149
    Data columns (total 5 columns):
     #   Column        Non-Null Count  Dtype  
    ---  ------        --------------  -----  
     0   sepal_length  150 non-null    float64
     1   sepal_width   150 non-null    float64
     2   petal_length  150 non-null    float64
     3   petal_width   150 non-null    float64
     4   species       150 non-null    object 
    dtypes: float64(4), object(1)
    memory usage: 6.0+ KB
    None



```python
# save both datasets to excel files same directory

boat.to_excel('boat.xlsx') 

flower.to_excel('flower.xlsx') 
```


```python
# save both datasets to excel files in day_08 folder

flower.to_excel('../day_08/flower.xlsx')

boat.to_excel('../day_08/boat.xlsx')
```


```python
# Import data titanic dataset from excel file another folder

dfb = pd.read_excel('../day_08/boat.xlsx')

dfb
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
      <td>...</td>
    </tr>
    <tr>
      <th>886</th>
      <td>886</td>
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
      <td>887</td>
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
      <td>888</td>
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
      <td>889</td>
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
      <td>890</td>
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
<p>891 rows × 16 columns</p>
</div>




```python
# display columns of the dataframe titanic

dfb.columns
```




    Index(['Unnamed: 0', 'survived', 'pclass', 'sex', 'age', 'sibsp', 'parch',
           'fare', 'embarked', 'class', 'who', 'adult_male', 'deck', 'embark_town',
           'alive', 'alone'],
          dtype='object')




```python
# Return specific columns from the dataframe due to 1 dimensional array
# 1 dimensional array mean only ek column return karna ho
# we use single square brackets [] to access the columns

dfb['embark_town'].head(10)

```




    0    Southampton
    1      Cherbourg
    2    Southampton
    3    Southampton
    4    Southampton
    5     Queenstown
    6    Southampton
    7    Southampton
    8    Southampton
    9      Cherbourg
    Name: embark_town, dtype: object




```python
# Return specific columns from the dataframe due to 2 dimensional array
# 2 dimensional array mean ek se zyada column return karna ho aur row bhi
# we use double square brackets [[]] to access the columns

dfb[['embark_town','sex']].head(10)

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
      <th>embark_town</th>
      <th>sex</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Southampton</td>
      <td>male</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Cherbourg</td>
      <td>female</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Southampton</td>
      <td>female</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Southampton</td>
      <td>female</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Southampton</td>
      <td>male</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Queenstown</td>
      <td>male</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Southampton</td>
      <td>male</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Southampton</td>
      <td>male</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Southampton</td>
      <td>female</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Cherbourg</td>
      <td>female</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Return unique values from the 'embark_town' column

dfb.embark_town.unique()
```




    array(['Southampton', 'Cherbourg', 'Queenstown', nan], dtype=object)




```python
# Return unique values from the 'deck' column

dfb.deck.unique()
```




    array([nan, 'C', 'E', 'G', 'D', 'A', 'B', 'F'], dtype=object)




```python
# display statistical summary of the dataframe

dfb.describe()
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
      <td>891.000000</td>
      <td>714.000000</td>
      <td>891.000000</td>
      <td>891.000000</td>
      <td>891.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>445.000000</td>
      <td>0.383838</td>
      <td>2.308642</td>
      <td>29.699118</td>
      <td>0.523008</td>
      <td>0.381594</td>
      <td>32.204208</td>
    </tr>
    <tr>
      <th>std</th>
      <td>257.353842</td>
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
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.420000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>222.500000</td>
      <td>0.000000</td>
      <td>2.000000</td>
      <td>20.125000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>7.910400</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>445.000000</td>
      <td>0.000000</td>
      <td>3.000000</td>
      <td>28.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>14.454200</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>667.500000</td>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>38.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>31.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>890.000000</td>
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
# remove unnamed column from the dataframe

dfb=dfb.drop(columns='Unnamed: 0') 

dfb.describe()
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
# Return total number in each columns

dfb.count()
```




    survived       891
    pclass         891
    sex            891
    age            714
    sibsp          891
    parch          891
    fare           891
    embarked       889
    class          891
    who            891
    adult_male     891
    deck           203
    embark_town    889
    alive          891
    alone          891
    dtype: int64




```python
# describe dataset based on sex column using groupby method

dfb.groupby(['sex']).describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="8" halign="left">survived</th>
      <th colspan="2" halign="left">pclass</th>
      <th>...</th>
      <th colspan="2" halign="left">parch</th>
      <th colspan="8" halign="left">fare</th>
    </tr>
    <tr>
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>...</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
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
      <td>314.0</td>
      <td>0.742038</td>
      <td>0.438211</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>314.0</td>
      <td>2.159236</td>
      <td>...</td>
      <td>1.0</td>
      <td>6.0</td>
      <td>314.0</td>
      <td>44.479818</td>
      <td>57.997698</td>
      <td>6.75</td>
      <td>12.071875</td>
      <td>23.0</td>
      <td>55.00</td>
      <td>512.3292</td>
    </tr>
    <tr>
      <th>male</th>
      <td>577.0</td>
      <td>0.188908</td>
      <td>0.391775</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>577.0</td>
      <td>2.389948</td>
      <td>...</td>
      <td>0.0</td>
      <td>5.0</td>
      <td>577.0</td>
      <td>25.523893</td>
      <td>43.138263</td>
      <td>0.00</td>
      <td>7.895800</td>
      <td>10.5</td>
      <td>26.55</td>
      <td>512.3292</td>
    </tr>
  </tbody>
</table>
<p>2 rows × 48 columns</p>
</div>




```python
# describe dataset based on sex and age column using groupby method

dfb.groupby(['sex','age']).describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th></th>
      <th colspan="8" halign="left">survived</th>
      <th colspan="2" halign="left">pclass</th>
      <th>...</th>
      <th colspan="2" halign="left">parch</th>
      <th colspan="8" halign="left">fare</th>
    </tr>
    <tr>
      <th></th>
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>...</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
    <tr>
      <th>sex</th>
      <th>age</th>
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
      <th rowspan="5" valign="top">female</th>
      <th>0.75</th>
      <td>2.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>...</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>19.258300</td>
      <td>0.000000</td>
      <td>19.2583</td>
      <td>19.258300</td>
      <td>19.2583</td>
      <td>19.25830</td>
      <td>19.2583</td>
    </tr>
    <tr>
      <th>1.00</th>
      <td>2.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>...</td>
      <td>1.75</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>13.437500</td>
      <td>3.258631</td>
      <td>11.1333</td>
      <td>12.285400</td>
      <td>13.4375</td>
      <td>14.58960</td>
      <td>15.7417</td>
    </tr>
    <tr>
      <th>2.00</th>
      <td>6.0</td>
      <td>0.333333</td>
      <td>0.516398</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.75</td>
      <td>1.0</td>
      <td>6.0</td>
      <td>2.5</td>
      <td>...</td>
      <td>2.00</td>
      <td>2.0</td>
      <td>6.0</td>
      <td>43.245833</td>
      <td>53.738575</td>
      <td>10.4625</td>
      <td>15.715625</td>
      <td>26.9500</td>
      <td>30.43125</td>
      <td>151.5500</td>
    </tr>
    <tr>
      <th>3.00</th>
      <td>2.0</td>
      <td>0.500000</td>
      <td>0.707107</td>
      <td>0.0</td>
      <td>0.25</td>
      <td>0.5</td>
      <td>0.75</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>2.5</td>
      <td>...</td>
      <td>1.75</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>31.327100</td>
      <td>14.498659</td>
      <td>21.0750</td>
      <td>26.201050</td>
      <td>31.3271</td>
      <td>36.45315</td>
      <td>41.5792</td>
    </tr>
    <tr>
      <th>4.00</th>
      <td>5.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>5.0</td>
      <td>2.6</td>
      <td>...</td>
      <td>1.00</td>
      <td>2.0</td>
      <td>5.0</td>
      <td>22.828340</td>
      <td>9.853082</td>
      <td>13.4167</td>
      <td>16.700000</td>
      <td>22.0250</td>
      <td>23.00000</td>
      <td>39.0000</td>
    </tr>
    <tr>
      <th>...</th>
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
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th rowspan="5" valign="top">male</th>
      <th>70.00</th>
      <td>2.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>1.5</td>
      <td>...</td>
      <td>0.75</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>40.750000</td>
      <td>42.779960</td>
      <td>10.5000</td>
      <td>25.625000</td>
      <td>40.7500</td>
      <td>55.87500</td>
      <td>71.0000</td>
    </tr>
    <tr>
      <th>70.50</th>
      <td>1.0</td>
      <td>0.000000</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
      <td>...</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.750000</td>
      <td>NaN</td>
      <td>7.7500</td>
      <td>7.750000</td>
      <td>7.7500</td>
      <td>7.75000</td>
      <td>7.7500</td>
    </tr>
    <tr>
      <th>71.00</th>
      <td>2.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>1.0</td>
      <td>...</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>2.0</td>
      <td>42.079200</td>
      <td>10.500536</td>
      <td>34.6542</td>
      <td>38.366700</td>
      <td>42.0792</td>
      <td>45.79170</td>
      <td>49.5042</td>
    </tr>
    <tr>
      <th>74.00</th>
      <td>1.0</td>
      <td>0.000000</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
      <td>...</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.775000</td>
      <td>NaN</td>
      <td>7.7750</td>
      <td>7.775000</td>
      <td>7.7750</td>
      <td>7.77500</td>
      <td>7.7750</td>
    </tr>
    <tr>
      <th>80.00</th>
      <td>1.0</td>
      <td>1.000000</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>...</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>30.000000</td>
      <td>NaN</td>
      <td>30.0000</td>
      <td>30.000000</td>
      <td>30.0000</td>
      <td>30.00000</td>
      <td>30.0000</td>
    </tr>
  </tbody>
</table>
<p>145 rows × 40 columns</p>
</div>




```python
# describe dataset based on sex and survived column using groupby method

dfb.groupby(['sex','survived']).describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th></th>
      <th colspan="8" halign="left">pclass</th>
      <th colspan="2" halign="left">age</th>
      <th>...</th>
      <th colspan="2" halign="left">parch</th>
      <th colspan="8" halign="left">fare</th>
    </tr>
    <tr>
      <th></th>
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>...</th>
      <th>75%</th>
      <th>max</th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
    <tr>
      <th>sex</th>
      <th>survived</th>
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
      <th rowspan="2" valign="top">female</th>
      <th>0</th>
      <td>81.0</td>
      <td>2.851852</td>
      <td>0.450309</td>
      <td>1.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>64.0</td>
      <td>25.046875</td>
      <td>...</td>
      <td>2.0</td>
      <td>6.0</td>
      <td>81.0</td>
      <td>23.024385</td>
      <td>24.821287</td>
      <td>6.750</td>
      <td>8.8500</td>
      <td>15.24580</td>
      <td>27.9000</td>
      <td>151.5500</td>
    </tr>
    <tr>
      <th>1</th>
      <td>233.0</td>
      <td>1.918455</td>
      <td>0.834211</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>197.0</td>
      <td>28.847716</td>
      <td>...</td>
      <td>1.0</td>
      <td>5.0</td>
      <td>233.0</td>
      <td>51.938573</td>
      <td>64.102256</td>
      <td>7.225</td>
      <td>13.0000</td>
      <td>26.00000</td>
      <td>76.2917</td>
      <td>512.3292</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">male</th>
      <th>0</th>
      <td>468.0</td>
      <td>2.476496</td>
      <td>0.761411</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>360.0</td>
      <td>31.618056</td>
      <td>...</td>
      <td>0.0</td>
      <td>5.0</td>
      <td>468.0</td>
      <td>21.960993</td>
      <td>32.409799</td>
      <td>0.000</td>
      <td>7.7958</td>
      <td>9.41665</td>
      <td>26.0000</td>
      <td>263.0000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>109.0</td>
      <td>2.018349</td>
      <td>0.922774</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>93.0</td>
      <td>27.276022</td>
      <td>...</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>109.0</td>
      <td>40.821484</td>
      <td>71.355967</td>
      <td>0.000</td>
      <td>9.5000</td>
      <td>26.28750</td>
      <td>39.0000</td>
      <td>512.3292</td>
    </tr>
  </tbody>
</table>
<p>4 rows × 40 columns</p>
</div>




```python
# count number of sex and survived column using groupby method

dfb.groupby(['survived','sex']).count()
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
      <th>survived</th>
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
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="2" valign="top">0</th>
      <th>female</th>
      <td>81</td>
      <td>64</td>
      <td>81</td>
      <td>81</td>
      <td>81</td>
      <td>81</td>
      <td>81</td>
      <td>81</td>
      <td>81</td>
      <td>6</td>
      <td>81</td>
      <td>81</td>
      <td>81</td>
    </tr>
    <tr>
      <th>male</th>
      <td>468</td>
      <td>360</td>
      <td>468</td>
      <td>468</td>
      <td>468</td>
      <td>468</td>
      <td>468</td>
      <td>468</td>
      <td>468</td>
      <td>61</td>
      <td>468</td>
      <td>468</td>
      <td>468</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">1</th>
      <th>female</th>
      <td>233</td>
      <td>197</td>
      <td>233</td>
      <td>233</td>
      <td>233</td>
      <td>231</td>
      <td>233</td>
      <td>233</td>
      <td>233</td>
      <td>91</td>
      <td>231</td>
      <td>233</td>
      <td>233</td>
    </tr>
    <tr>
      <th>male</th>
      <td>109</td>
      <td>93</td>
      <td>109</td>
      <td>109</td>
      <td>109</td>
      <td>109</td>
      <td>109</td>
      <td>109</td>
      <td>109</td>
      <td>45</td>
      <td>109</td>
      <td>109</td>
      <td>109</td>
    </tr>
  </tbody>
</table>
</div>




```python
# count number of survival and sex survial base usning groupby method 

dfb.groupby(['survived','sex','who'])['survived'].count()
```




    survived  sex     who  
    0         female  child     15
                      woman     66
              male    child     19
                      man      449
    1         female  child     28
                      woman    205
              male    child     21
                      man       88
    Name: survived, dtype: int64




```python
# Returns number of survival ,sex and who on who and survial base using groupby method
 
dfb.groupby(['survived','sex','who'])[['survived','who']].count()
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
      <th>survived</th>
      <th>who</th>
    </tr>
    <tr>
      <th>survived</th>
      <th>sex</th>
      <th>who</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="4" valign="top">0</th>
      <th rowspan="2" valign="top">female</th>
      <th>child</th>
      <td>15</td>
      <td>15</td>
    </tr>
    <tr>
      <th>woman</th>
      <td>66</td>
      <td>66</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">male</th>
      <th>child</th>
      <td>19</td>
      <td>19</td>
    </tr>
    <tr>
      <th>man</th>
      <td>449</td>
      <td>449</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">1</th>
      <th rowspan="2" valign="top">female</th>
      <th>child</th>
      <td>28</td>
      <td>28</td>
    </tr>
    <tr>
      <th>woman</th>
      <td>205</td>
      <td>205</td>
    </tr>
    <tr>
      <th rowspan="2" valign="top">male</th>
      <th>child</th>
      <td>21</td>
      <td>21</td>
    </tr>
    <tr>
      <th>man</th>
      <td>88</td>
      <td>88</td>
    </tr>
  </tbody>
</table>
</div>




```python
# plot countplot of survived column using seaborn plotting library

sns.countplot(x='survived',data=dfb)
```




    <Axes: xlabel='survived', ylabel='count'>




    
![png](output_25_1.png)
    



```python
# plot countplot of survived column based on sex using hue parameter 

sns.countplot(x='survived',hue='sex',data=dfb)
```




    <Axes: xlabel='survived', ylabel='count'>




    
![png](output_26_1.png)
    



```python
# plot countplot of survived column based on sex using hue parameter

sns.countplot(y='survived',hue='sex',data=dfb)
```




    <Axes: xlabel='count', ylabel='survived'>




    
![png](output_27_1.png)
    

