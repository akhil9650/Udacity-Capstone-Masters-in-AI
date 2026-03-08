# PROJECT
This repository analyzes the housing patterns and trends for New York city. We use the ‘New York City Airbnb Open Data | Airbnb listings and metrics in NYC, NY, USA (2019)’ dataset obtained from Kaggle. The Jupyter Notebook for the project along with environment setup instructions is hosted on this Github link. 

## SCOPE
This project involves creating a virtual environment for Jupyter Notebook to run, loading the data into our notebook and performing data analysis and visualization on it. The notebook also contains reports and metrics for the data. Ony data analysis is done, no ML training steps are added here. 

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

# Future Scope
You can use the analysis from this repository for a future Machine Learning training project to predict listing prices. The cleaned up data is compliant with data safety rules as PII is removed. A continuous training and inference pipeline on the listings can help anyone get ahead of the trends and be able to understand the NYC housing market better. Further, AI agentic workflows can be enabled for listing agents, who can add LLM integrations which can help them generate reports and trends for their sales. 