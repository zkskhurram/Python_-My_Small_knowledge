- ⚡ **Subject** : 10 Minutes to pandas — Enhanced Guide
- 🖊️ **Author:** Khurram Shahzad  
- 🎓 **Mentor:** Dr. Aammar Tufail  
- ✉️ **Email:** [khurramamq@gmail.com](mailto:khurramamq@gmail.com)  
- 💻 **GitHub:** [zkskhurram](https://github.com/zkskhurram/Python_-My_Small_knowledge/tree/main)

# 🚢 EDA & Data Wrangling on Titanic Dataset (`sns.load_dataset('titanic')`)

This notebook performs a full **Exploratory Data Analysis (EDA)** and **data wrangling** pipeline
on the Titanic dataset available in seaborn.


## 0. Import Libraries



```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

%matplotlib inline
sns.set(style="whitegrid")

print("Libraries imported successfully.")
```

## 1. Load Titanic Dataset

We use seaborn's built-in Titanic dataset.



```python
import seaborn as sns

# Load Titanic dataset
df = sns.load_dataset('titanic')
print("Titanic dataset loaded.")
display(df.head())
print("Shape:", df.shape)
```

## 2. Basic Info, Data Types, Missing Values



```python
print("DataFrame Info:")
print("-" * 40)
df.info()

print("\nData Types:")
print("-" * 40)
print(df.dtypes)
```


```python
print("Missing Values (Count):")
missing_counts = df.isnull().sum()
print(missing_counts)

print("\nMissing Values (Percentage):")
missing_pct = df.isnull().mean() * 100
print(missing_pct)
```

## 3. Descriptive Statistics & Random Samples



```python
print("Numeric Summary:")
display(df.describe())

print("\nCategorical Summary:")
display(df.describe(include=['object', 'category']))

print("\nRandom Sample Rows:")
display(df.sample(5, random_state=42))
```

## 4. Understand Variables

- Identify numeric & categorical columns
- Target variable: `survived`



```python
numeric_cols = df.select_dtypes(include=["int64", "float64"]).columns.tolist()
cat_cols = df.select_dtypes(include=["object", "category", "bool"]).columns.tolist()

print("Numeric Columns:", numeric_cols)
print("Categorical Columns:", cat_cols)

target_col = 'survived'  # target for modeling
print("Target Column:", target_col)
```

## 5. Relationships Between Variables (Correlation, Heatmap, Pairplot)



```python
# Correlation heatmap
corr = df.corr(numeric_only=True)
plt.figure(figsize=(10, 8))
sns.heatmap(corr, annot=True, fmt=".2f", linewidths=0.5)
plt.title("Titanic: Correlation Heatmap")
plt.show()
```


```python
# Pairplot on a subset of numeric columns
num_cols_subset = ['age', 'fare', 'sibsp', 'parch']
sns.pairplot(df[num_cols_subset].dropna())
plt.show()
```

## 6. Brainstorming: Scaling & Outliers

### 6.1 Example: Scaling `age` and `fare`



```python
from sklearn.preprocessing import MinMaxScaler

cols_to_scale = ['age', 'fare']
df_scaled = df.copy()

scaler = MinMaxScaler()
df_scaled[cols_to_scale] = scaler.fit_transform(df_scaled[cols_to_scale])
print("Applied MinMax scaling on:", cols_to_scale)
df_scaled[cols_to_scale].head()
```

### 6.2 Outlier Detection on `fare` using IQR



```python
col = 'fare'
Q1 = df[col].quantile(0.25)
Q3 = df[col].quantile(0.75)
IQR = Q3 - Q1
lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR

print(f"{col} | Q1={Q1:.2f}, Q3={Q3:.2f}, IQR={IQR:.2f}")
print(f"Lower bound={lower:.2f}, Upper bound={upper:.2f}")

df_no_outliers = df[(df[col] >= lower) & (df[col] <= upper)]
print("Original shape:", df.shape)
print("Without outliers:", df_no_outliers.shape)
```

## 7. Tidy & Clean Data

- Fill missing values
- Drop highly-missing column `deck`



```python
df_clean = df.copy()

# Fill missing age with median
df_clean['age'] = df_clean['age'].fillna(df_clean['age'].median())

# Fill embarked & embark_town with mode
df_clean['embarked'] = df_clean['embarked'].fillna(df_clean['embarked'].mode()[0])
df_clean['embark_town'] = df_clean['embark_town'].fillna(df_clean['embark_town'].mode()[0])

# Drop 'deck' due to many missing values
if 'deck' in df_clean.columns:
    df_clean = df_clean.drop(columns=['deck'])

print("Original shape:", df.shape)
print("Cleaned shape:", df_clean.shape)
df_clean.head()
```

## 8. Basic Statistical Analysis



```python
print("Mean of numeric columns:")
print(df_clean.mean(numeric_only=True))

print("\nAverage age by sex:")
print(df_clean.groupby('sex')['age'].mean())

print("\nSurvival rate by class:")
print(df_clean.groupby('class')['survived'].mean())
```

## 9. Prepare Data for Prediction (Train/Test Split)



```python
from sklearn.model_selection import train_test_split

target_col = 'survived'
X = df_clean.drop(target_col, axis=1)
y = df_clean[target_col]

# One-hot encode categorical variables
X = pd.get_dummies(X, drop_first=True)

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

print("Train shape:", X_train.shape)
print("Test shape:", X_test.shape)
```

## 10. Simple Visualization Examples



```python
# Distribution of age
sns.histplot(df_clean['age'], kde=True)
plt.title('Age Distribution')
plt.show()

# Survival count
sns.countplot(x='survived', data=df_clean)
plt.title('Survival Count')
plt.show()

# Fare vs Class
sns.boxplot(x='class', y='fare', data=df_clean)
plt.title('Fare by Class')
plt.show()
```

## 11. Machine Learning – RandomForest Classifier



```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report

clf = RandomForestClassifier(random_state=42)
clf.fit(X_train, y_train)
y_pred = clf.predict(X_test)

print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nClassification Report:")
print(classification_report(y_test, y_pred))
```
