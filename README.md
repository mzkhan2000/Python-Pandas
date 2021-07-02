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

#================================================================
import glob

# assign dataset names
PUBLIC_DISPATCHSCADA_list_of_files = []

# all dataset names with starting PUBLIC_DISPATCHSCADA
PUBLIC_DISPATCHSCADA_list_of_files = glob.glob('PUBLIC_DISPATCHSCADA*.csv')

# create empty list
dataframes_list = []

#================================================================
# import module
import pandas as pd
  
# assign dataset names
list_of_names = ['crime','username']
  
# create empty list
dataframes_list = []
  
# append datasets into teh list
for i in range(len(list_of_names)):
    temp_df = pd.read_csv("./csv/"+list_of_names[i]+".csv")
    dataframes_list.append(temp_df)
```
