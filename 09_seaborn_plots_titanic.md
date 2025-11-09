
# 📚 Seaborn Plots — Complete Guide (Titanic Dataset)

## 📑 Table of Contents
- [Distribution Plots](#distribution-plots)
- [Categorical Plots](#categorical-plots)
- [Relational Plots](#relational-plots)
- [Regression Plots](#regression-plots)
- [Matrix / Heatmap](#matrix--heatmap)
- [Multivariate Plots](#multivariate-plots)
- [Styling](#styling)
- [Side-by-Side Comparison](#side-by-side-comparison)

---

## 📦 Setup
```python
import seaborn as sns
import matplotlib.pyplot as plt
df = sns.load_dataset("titanic")
sns.set_theme(style="whitegrid")
```

---

## 📊 Distribution Plots

### Histogram
```python
sns.histplot(data=df, x="age", kde=True)
plt.show()
```

### KDE
```python
sns.kdeplot(data=df, x="age", fill=True)
plt.show()
```

### ECDF
```python
sns.ecdfplot(data=df, x="age")
plt.show()
```

---

## 🎯 Categorical Plots

### Countplot
```python
sns.countplot(data=df, x="class")
plt.show()
```

### Barplot
```python
sns.barplot(data=df, x="class", y="fare", hue="sex")
plt.show()
```

### Boxplot
```python
sns.boxplot(data=df, x="class", y="age")
plt.show()
```

### Violinplot
```python
sns.violinplot(data=df, x="class", y="age", hue="sex", split=True)
plt.show()
```

---

## 🔵 Relational Plots

### Scatterplot
```python
sns.scatterplot(data=df, x="age", y="fare", hue="sex")
plt.show()
```

### Lineplot
```python
sns.lineplot(data=df, x="age", y="fare")
plt.show()
```

---

## 📈 Regression Plots

### regplot
```python
sns.regplot(data=df, x="age", y="fare")
plt.show()
```

### lmplot
```python
sns.lmplot(data=df, x="age", y="fare", hue="sex")
```

---

## 🔗 Matrix / Heatmap

### Heatmap
```python
corr = df.corr(numeric_only=True)
sns.heatmap(corr, annot=True)
plt.show()
```

### Clustermap
```python
sns.clustermap(corr, annot=True)
```

---

## 🌐 Multivariate Plots

### pairplot
```python
sns.pairplot(df[["age", "fare", "survived", "pclass"]].dropna(), hue="survived")
plt.show()
```

### jointplot
```python
sns.jointplot(data=df, x="age", y="fare", kind="reg")
plt.show()
```

---

## 🎨 Styling

### Palette
```python
sns.set_palette("coolwarm")
sns.scatterplot(data=df, x="age", y="fare", hue="sex")
plt.show()
```

### Theme
```python
sns.set_theme(style="darkgrid")
sns.boxplot(data=df, x="class", y="fare")
plt.show()
```

---

## 🆚 Side-by-Side Comparison

```python
fig, axes = plt.subplots(1, 2, figsize=(12,5))

sns.boxplot(data=df, x="class", y="fare", ax=axes[0])
axes[0].set_title("Boxplot")

sns.violinplot(data=df, x="class", y="fare", ax=axes[1])
axes[1].set_title("Violinplot")

plt.show()
```

---
