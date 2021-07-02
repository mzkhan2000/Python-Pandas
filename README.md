# Python-Pandas-Dataframe
Python-Pandas necessary-code-for-me



```python
# Find out your current working directory
import os
print(os.getcwd())

# Skiprows
df = pd.read_csv("data/cereal.csv", skiprows = 1)

# skipfooter
df = pd.read_csv("data/cereal.csv", skipfooter = 1)

# Skiprows and skipfooter
df = pd.read_csv("data/cereal.csv", skiprows = 1, skipfooter = 1)
```
