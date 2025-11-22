- ⚡ **Subject** : 10 Minutes to pandas — Enhanced Guide\
- 🖊️ **Author:** Khurram Shahzad  
- 🎓 **Mentor:** Dr. Aammar Tufail  
- ✉️ **Email:** [khurramamq@gmail.com](mailto:khurramamq@gmail.com)  
- 💻 **GitHub:** [zkskhurram](https://github.com/zkskhurram/Python_-My_Small_knowledge/tree/main)
  

## ✅ 1) Import
```python
import pandas as pd
import numpy as np
```
📌 Pandas is for data handling. Numpy helps with numbers.

---

## ✅ 2) Create Objects

### ➤ Series
```python
s = pd.Series([1,3,5,7,9])
```
📌 *1‑D labeled data*

### ➤ DataFrame
```python
df = pd.DataFrame({
    "A": [1,2,3],
    "B": [4,5,6]
})
```
📌 *2‑D table*

### Random
```python
df = pd.DataFrame(np.random.randn(5,4), columns=list("ABCD"))
```

---

## ✅ 3) Viewing Data
```python
df.head()
df.tail()
df.info()
df.describe()
df.shape
```
👀 Quick look at structure.

---

## ✅ 4) Selecting

### Columns
```python
df["A"]
df[["A","B"]]
```

### Rows
```python
df.loc[0]    
df.iloc[0]    
df[1:3]     
```

---

## ✅ 5) Filtering
```python
df[df["A"] > 1]
df[(df["A"] > 1) & (df["B"] < 6)]
```

✅ *Rows meeting conditions*

---

## ✅ 6) Assign
```python
df["C"] = df["A"] * 2
```
🆕 adds new column

---

## ✅ 7) Missing Data
```python
df.dropna()
df.fillna(0)
```

---

## ✅ 8) Stats
```python
df.mean()
df.count()
df.std()
```

---

## ✅ 9) Apply function
```python
df["A"].apply(lambda x: x+1)
```

---

## ✅ 10) Merge / Join
```python
pd.merge(df1, df2, on="key")
df1.join(df2, lsuffix="_l", rsuffix="_r")
```

---

## ✅ 11) Concat
```python
pd.concat([df1, df2])
```

---

## ✅ 12) GroupBy
```python
df.groupby("A").sum()
df.groupby("A")["B"].mean()
```

---

## ✅ 13) Sorting
```python
df.sort_values(by="A")
df.sort_index()
```

---

## ✅ 14) Read / Write
```python
pd.read_csv("file.csv")
df.to_csv("output.csv")
```

---

# ✅ Examples

## Example 1 — Filtering
```python
df = pd.DataFrame({
    "City": ["Kuwait","Dubai","Toronto"],
    "Temp": [41,38,12]
})

df[df["Temp"] > 20]
```

---

## Example 2 — Grouping
```python
sales = pd.DataFrame({
    "Store": ["A","A","B","B"],
    "Sales": [10,15,20,25]
})

sales.groupby("Store").sum()
```

---

# 🎯 Exercises

### 1️⃣ Create DataFrame of Students (name, marks). Show top 2.
### 2️⃣ Add column grade based on marks.
### 3️⃣ Count cities in a DataFrame.
### 4️⃣ Show rows where marks > 80.
### 5️⃣ Group students by city → average marks.

---
