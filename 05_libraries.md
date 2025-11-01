⚙️ **Popular Python Libraries and Their Uses**
| 🧩 **Library**      | 🎯 **Purpose / Use**                                                                   |
| ------------------- | -------------------------------------------------------------------------------------- |
| 🐼 **pandas**       | 📊 Data Analysis — for handling and analyzing structured data (DataFrames, CSVs, etc.) |
| 🔢 **NumPy**        | 🧮 Numerical Computation — for fast mathematical operations on arrays and matrices     |
| 📈 **Matplotlib**   | 🖌️ Plotting — for creating static graphs and visualizations                           |
| 🌈 **Seaborn**      | 🎨 Advanced Visualization — for beautiful, statistical charts built on Matplotlib      |
| 📊 **Plotly**       | 💫 Interactive Plotting — for dynamic, web-ready charts and dashboards                 |
| 📐 **SciPy.stats**  | 📚 Statistical Functions — for probability distributions, hypothesis testing, etc.     |
| 🤖 **Scikit-learn** | 🧠 Machine Learning — for regression, classification, clustering, and preprocessing    |
| 🌍 **Streamlit**    | 💻 Web App Development — for building interactive data apps quickly and easily         |


📦 **pip** = **Python’s tool for managing libraries easily**.

Example:
| 🔧 Command                         | 💡 Description                   |
| ---------------------------------- | -------------------------------- |
| `pip install pandas`               | Installs a package               |
| `pip uninstall pandas`             | Removes a package                |
| `pip list`                         | Shows all installed packages     |
| `pip show numpy`                   | Displays details about a package |
| `pip install --upgrade matplotlib` | Updates an existing package      |


🧠 **Common Ways to Import**

| 🔧 Style                    | 📝 Example                           | 💬 Meaning                    |
| --------------------------- | ------------------------------------ | ----------------------------- |
| **Standard import**         | `import pandas`                      | Import the whole library      |
| **With alias**              | `import pandas as pd`                | Shorter name (commonly used)  |
| **Specific function/class** | `from math import sqrt`              | Import only one function      |
| **Multiple items**          | `from random import randint, choice` | Import several specific items |


```python
# install all required libraries together as follows:

#pip install pandas numpy matplotlib seaborn plotly
!pip install nbformat

```

```python
# Examples of importing popular data science libraries in Python

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import plotly as px
import seaborn as sns
```

```python
data = {
    "Name": ["Ali", "Sara", "Ahmed"],
    "Age": [25, 28, 22],
    "City": ["Kuwait", "Lahore", "Karachi"]
}
df =pd.DataFrame(data)
print(df)
```

```
    Name  Age     City
0    Ali   25   Kuwait
1   Sara   28   Lahore
2  Ahmed   22  Karachi

```

```python
sns.load_dataset("diamonds") # load example dataset from seaborn
```

```
       carat        cut color clarity  depth  table  price     x     y     z
0       0.23      Ideal     E     SI2   61.5   55.0    326  3.95  3.98  2.43
1       0.21    Premium     E     SI1   59.8   61.0    326  3.89  3.84  2.31
2       0.23       Good     E     VS1   56.9   65.0    327  4.05  4.07  2.31
3       0.29    Premium     I     VS2   62.4   58.0    334  4.20  4.23  2.63
4       0.31       Good     J     SI2   63.3   58.0    335  4.34  4.35  2.75
...      ...        ...   ...     ...    ...    ...    ...   ...   ...   ...
53935   0.72      Ideal     D     SI1   60.8   57.0   2757  5.75  5.76  3.50
53936   0.72       Good     D     SI1   63.1   55.0   2757  5.69  5.75  3.61
53937   0.70  Very Good     D     SI1   62.8   60.0   2757  5.66  5.68  3.56
53938   0.86    Premium     H     SI2   61.0   58.0   2757  6.15  6.12  3.74
53939   0.75      Ideal     D     SI2   62.2   55.0   2757  5.83  5.87  3.64

[53940 rows x 10 columns]
```

```python
# --- EXAMPLES OF USING THE LIBRARIES ---

# plotting

import seaborn as sns

sns.set_theme(style="whitegrid")

diamonds = sns.load_dataset("diamonds")
clarity_ranking = ["I1", "SI2", "SI1" ,"VS2" , "VS1" , "VVS2" , "VVS1" , "IF"]

sns.boxenplot ( x="clarity" , y="carat",
              color="b" , order=clarity_ranking,
              scale="linear" , data=diamonds)


```

```
C:\Users\khurr\AppData\Local\Temp\ipykernel_18448\1355862848.py:12: FutureWarning: 

The `scale` parameter has been renamed to `width_method` and will be removed in v0.15. Pass `width_method='linear' for the same effect.
  sns.boxenplot ( x="clarity" , y="carat",

```

```
<Axes: xlabel='clarity', ylabel='carat'>
```

```
<Figure size 640x480 with 1 Axes>
```

```python
# ✅ Clean & Correct Version
import seaborn as sns
import matplotlib.pyplot as plt

# Set the visual theme
sns.set_theme(style="whitegrid")

# Load the built-in "diamonds" dataset
diamonds = sns.load_dataset("diamonds")

# Define clarity order (from lowest to highest quality)
clarity_ranking = ["I1", "SI2", "SI1", "VS2", "VS1", "VVS2", "VVS1", "IF"]

# Create a boxen plot
sns.boxenplot(
    x="clarity",
    y="carat",
    color="b",
    order=clarity_ranking,
    scale="linear",
    data=diamonds
)

# Add title and labels
plt.title("Distribution of Diamond Carat by Clarity", fontsize=14)
plt.xlabel("Clarity Grade", fontsize=12)
plt.ylabel("Carat Weight", fontsize=12)

# Show the plot
plt.show()

```

```
C:\Users\khurr\AppData\Local\Temp\ipykernel_18448\2076279852.py:15: FutureWarning:



The `scale` parameter has been renamed to `width_method` and will be removed in v0.15. Pass `width_method='linear' for the same effect.


```

```
<Figure size 640x480 with 1 Axes>
```

💡 **Explanation**

| 🧩 Part                                 | 💬 Description                                                                  |
| --------------------------------------- | ------------------------------------------------------------------------------- |
| `sns.set_theme(style="whitegrid")`      | Adds a clean white background with grid lines                                   |
| `sns.load_dataset("diamonds")`          | Loads Seaborn’s sample **diamonds dataset** 💎                                  |
| `clarity_ranking`                       | Defines the logical order of clarity levels (from lowest to best)               |
| `sns.boxenplot()`                       | Draws a **Boxen plot** (a detailed version of a box plot — good for large data) |
| `color="b"`                             | Uses blue color                                                                 |
| `scale="linear"`                        | Linear scaling for better visibility of distributions                           |
| `plt.title`, `plt.xlabel`, `plt.ylabel` | Add clear labels and title                                                      |

📊 Result

This will show a beautiful, blue boxen plot illustrating how the carat weight of diamonds varies with clarity grade — the higher the clarity (like IF or VVS1), the general trend of weight can be visually compared.

```python

import plotly.express as px

# Load built-in Gapminder dataset
df = px.data.gapminder()

# Create interactive animated scatter plot
fig = px.scatter(
    df,
    x="gdpPercap",
    y="lifeExp",
    animation_frame="year",
    animation_group="country",
    size="pop",
    color="continent",
    hover_name="country",
    log_x=True,
    size_max=55,
    range_x=[100, 100000],
    range_y=[25, 90],
)

fig.show()

```

💡 **Explanation**

| 🔧 Part                       | 💬 Meaning                                                                 |
| ----------------------------- | -------------------------------------------------------------------------- |
| `import plotly.express as px` | Imports Plotly Express for quick chart creation                            |
| `px.data.gapminder()`         | Loads sample **Gapminder** dataset (countries, life expectancy, GDP, etc.) |
| `px.scatter()`                | Makes a **bubble chart** (scatter plot with circle size = population)      |
| `x="gdpPercap"`               | GDP per person (x-axis, log scale)                                         |
| `y="lifeExp"`                 | Life expectancy (y-axis)                                                   |
| `animation_frame="year"`      | Creates animation by **year** 🕒                                           |
| `animation_group="country"`   | Ensures each country's dots move smoothly                                  |
| `color="continent"`           | Colors by continent                                                        |
| `hover_name="country"`        | Shows country name when hovered                                            |
| `log_x=True`                  | Uses logarithmic scale for better clarity                                  |
| `size_max=55`                 | Controls bubble size                                                       |
| `range_x` & `range_y`         | Set axis limits                                                            |

🌍 **Result**

You’ll get an interactive animated bubble chart showing how:

+ GDP 💰

+ Life expectancy ❤️

+ and population 🌐
changed over time (1952–2007) for every country.

