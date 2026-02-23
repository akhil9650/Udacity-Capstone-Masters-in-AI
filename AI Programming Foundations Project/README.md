
# Setup
## Clone and navigate to the GIT repository
```
git clone
```

## Create a virtual environment (RECOMMENDED)
```
python3 -m venv .venv
```

## Activate the virtual environment
```
source .venv/bin/activate
```

## Install & Launch JUPYTER
```
pip install jupyter
jupyter notebook
```

## Install libraries and save
### via Jupyter (notice the '!' sign, if running in terminal remove the it and run)
```
!pip install numpy pandas matplotlib seaborn
!pip freeze > requirements.txt
```

## Check if GIT exists
### via Jupyter (notice the '!' sign, if running in terminal remove the it and run)
```
!git --version
```

# Jupyter Notebook
## Imports
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

## Set Visualization Configuration values for libraries
```
import warnings
warnings.filterwarnings('ignore')
warnings.filterwarnings(action='ignore', category=DeprecationWarning)
pd.set_option('display.max_columns', None)
pd.set_option('display.float_format', lambda x: '%.2f' % x) 
sns.set(rc={'figure.figsize':(10,8)})
sns.set_style('white')
```

## Import Dataset
```
df = pd.read_csv("airbnb-data/AB_NYC_2019.csv")
```

# Process
Once data is loaded, we do the following in the Jupyter Notebook
1. Explore dataset columns, properties and NULL values
2. Clean the data
3. Do EDA on the cleaned dataset
4. Visualize the dataset using Matplotlib and Searbon libraries
5. Give a final analysis of the dataset