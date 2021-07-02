# Python-Pandas-Dataframe
Final Python-Pandas necessary-code-for-me

```python
# 1 import necessary libraries - Monir
import pandas as pd
import os
import glob
import numpy as np

# 2 assign dataset names
PUBLIC_DISPATCHSCADA_list_of_files = []

# all dataset names with starting PUBLIC_DISPATCHSCADA
PUBLIC_DISPATCHSCADA_list_of_files = glob.glob('PUBLIC_DISPATCHSCADA*.csv')

# create empty list
dataframes_list = []

list_of_names = PUBLIC_DISPATCHSCADA_list_of_files

# 3 append datasets into teh list
for i in range(len(list_of_names)):
    temp_df = pd.read_csv(list_of_names[i], skiprows = 1, skipfooter = 1)
    #dataframes_list[i]=temp_df
    dataframes_list.append(temp_df)
# 4
dataframes_list[2].tail()

# 5
PUBLIC_DISPATCHSCADA_df = pd.concat(dataframes_list)

#6
PUBLIC_DISPATCHSCADA_df.tail()

#7
PUBLIC_DISPATCHSCADA_df.shape

# 8
PUBLIC_DISPATCHSCADA_df.to_csv("PUBLIC_DISPATCHSCADA_all.csv") # Saving as csv file/ Monir 
```
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


#================================================================
 # assign dataset names
PUBLIC_DISPATCHSCADA_list_of_files = []

# all dataset names with starting PUBLIC_DISPATCHSCADA
PUBLIC_DISPATCHSCADA_list_of_files = glob.glob('PUBLIC_DISPATCHSCADA*.csv')

# create empty list
dataframes_list = []

 list_of_names = PUBLIC_DISPATCHSCADA_list_of_files
# append datasets into teh list
for i in range(len(list_of_names)):
    # temp_df = pd.read_csv("./csv/"+list_of_names[i]+".csv")
    if i==0:
        dataframes_list[i] = pd.read_csv(list_of_names[i], skiprows = 1, skipfooter = 1)
    else:   
        dataframes_list[i] = pd.read_csv(list_of_names[i], skiprows = 2, skipfooter = 1)
    #dataframes_list.append(temp_df)   
    
    
PUBLIC_DISPATCHSCADA_df = pd.concat(dataframes_list)
```
