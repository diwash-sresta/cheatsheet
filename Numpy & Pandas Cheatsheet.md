# 📦 NumPy & pandas Cheatsheet
- ### 🐼[Pandas](#-pandas--data-analysis)
## ✨ NumPy – Numerical computing

```python
import numpy as np
```
### ✅ Create arrays
```python
a = np.array([1, 2, 3])
b = np.zeros((2, 3))
c = np.ones(5)
d = np.arange(0, 10, 2)    # [0,2,4,6,8]
e = np.linspace(0, 1, 5)   # [0,0.25,0.5,0.75,1]
```
### 📏 Array properties
```
a.shape        # dimensions
a.size         # total elements
a.dtype        # data type
```
### 🔄 Reshape & combine
```
a.reshape(3, 1)
np.concatenate([a, a])
np.vstack([a, a])
np.hstack([a, a])
```

### ⚙ Operations & stats
```
np.mean(a)
np.median(a)
np.std(a)
np.sum(a)
np.max(a)
np.min(a)
np.dot(a, a)
```
### 🎭 Masking & filtering
```
a[a > 1]           # elements greater than 1
np.isnan(a)        # check for NaN
np.isinf(a)        # check for inf
```
# 🐼 Pandas – Data analysis
```
import pandas as pd
```
### 📥 Create DataFrame
```
df = pd.DataFrame({
    'Name': ['Alice', 'Bob'],
    'Age': [25, 30]
})
 ```
### 📊 Load & save
```
pd.read_csv('data.csv')
df.to_csv('data.csv', index=False)

```
### 🔍 Inspect data
```
df.head()
df.tail()
df.info()
df.describe()
df.shape
df.columns

```
### 🧹 Clean data
```
df.dropna()                    # remove missing rows
df.fillna(0)                   # fill missing with 0
df.replace(np.inf, np.nan)     # replace inf with nan
df.drop_duplicates()           # remove duplicates

```
### ⚙ Filtering & selection
```
df['Age']                   # select column
df[['Name', 'Age']]         # multiple columns
df.loc[0]                   # by label / index
df.iloc[0]                  # by position
df[df['Age'] > 25]          # filter rows

```
### 🛠 Group & aggregate
```
df.groupby('Name').mean()
df.groupby('Name')['Age'].sum()

```
### 🔄 Merge & concat
```
pd.merge(df1, df2, on='ID', how='inner')
pd.concat([df1, df2], axis=0, ignore_index=True)

```
