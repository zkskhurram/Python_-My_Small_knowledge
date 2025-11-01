# 🧠 Python Essential Libraries – Explained with Examples

## 📑 Table of Contents
1. [Introduction](#introduction)
2. [Requests](#1-requests)
3. [Pandas](#2-pandas)
4. [NumPy](#3-numpy)
5. [Matplotlib](#4-matplotlib)
6. [BeautifulSoup (bs4)](#5-beautifulsoup4)
7. [Scikit-learn](#6-scikit-learn)
8. [TensorFlow](#7-tensorflow)
9. [Install All at Once](#8-install-all-at-once)

---

## Introduction
This guide provides a concise and professional overview of essential Python libraries used in data analysis, visualization, machine learning, and web development. Each section includes the library’s purpose, main uses, and sample code to demonstrate its functionality.

---

## 1. Requests
**Definition:**  
A Python library for sending HTTP requests to web servers. It’s ideal for working with APIs or fetching web data.

**Common Uses:**
- Connect to APIs (e.g., GitHub, OpenWeather)
- Retrieve web data in JSON or text format

**Example:**
```python
import requests
response = requests.get("https://api.github.com")
print(response.status_code)
```
---

## 2. Pandas
**Definition:**  
A powerful library for data manipulation and analysis using DataFrames and Series.

**Common Uses:**
- Handle CSV, Excel, or SQL data
- Data cleaning, transformation, and analysis

**Example:**
```python
import pandas as pd

df = pd.DataFrame({
    'Name': ['Ali', 'Sara'],
    'Age': [25, 30]
})
print(df)
```
---

## 3. NumPy
**Definition:**  
Provides efficient array operations and mathematical functions for numerical computing.

**Common Uses:**
- Matrix and array operations
- Fast numerical calculations
- Foundation for Pandas, Scikit-learn, and TensorFlow

**Example:**
```python
import numpy as np

arr = np.array([1, 2, 3, 4])
print(np.mean(arr))
```
---

## 4. Matplotlib
**Definition:**  
A plotting library used for creating static, animated, and interactive visualizations in Python.

**Common Uses:**
- Create charts and graphs
- Add labels, legends, and titles
- Save visualizations as images

**Example:**
```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3, 4], [10, 20, 25, 30])
plt.title("Simple Line Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```
---

## 5. BeautifulSoup4
**Definition:**  
A library for web scraping — extracting data from HTML and XML documents.

**Common Uses:**
- Extracting titles, links, or text from web pages
- Parsing and cleaning HTML content

**Example:**
```python
from bs4 import BeautifulSoup

html = '<html><body><h1>Hello</h1></body></html>'
soup = BeautifulSoup(html, 'html.parser')
print(soup.h1.text)
```
---

## 6. Scikit-learn
**Definition:**  
A machine learning library that provides tools for training, testing, and evaluating models.

**Common Uses:**
- Regression, classification, and clustering
- Model evaluation and feature scaling

**Example:**
```python
from sklearn.linear_model import LinearRegression

X = [[1], [2], [3], [4]]
y = [2, 4, 6, 8]

model = LinearRegression().fit(X, y)
print(model.predict([[5]]))
```
---

## 7. TensorFlow
**Definition:**  
An open-source deep learning and machine learning framework developed by Google.

**Common Uses:**
- Building and training neural networks
- Computer vision, NLP, and AI research

**Example:**
```python
import tensorflow as tf
print(tf.__version__)
```
---

## 8. Install All at Once
Install all libraries together using this single command:
```bash
pip install requests pandas numpy matplotlib beautifulsoup4 scikit-learn tensorflow
```

---

### 📘 Author Note
Created by         **Khurram Shahzad**  
Mentored by        **Dr.Aammar Tufail**
Professional educational reference for learning and practical development use.
