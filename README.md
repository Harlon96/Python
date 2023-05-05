# Python
# Jupyther_Notebook_pyhton_Code

!date

# this is a picture of a tesla vehicle
from IPython import display
display.Image("/home/harlohutch77/gif/tesla.jpeg")

#imports so this project is possible
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import cufflinks as cf
%matplotlib inline

#reading the tesla csv file and putting the data into a dataframe
tesla = pd.read_csv("/home/harlohutch77/python/python_master/TSLA.csv")
tesla

#this dataframe is showing data that is obtained from the top rows of the dataset
tesla.head()

#this dataframe is showing data that is from the bottom rows of the dataset
tesla.tail()

# this information below is to import and make the visualizations possible in this project
from plotly import __version__
from plotly.offline import download_plotlyjs, init_notebook_mode, plot, iplot

print(__version__) # requires version >= 1.9.0

import cufflinks as cf

# For Notebooks
init_notebook_mode(connected=True)

# For offline use
cf.go_offline()

<div class="pirk">
#this line of code is specifing the High and Low data from the dataset to give you a better perspective of
#what is transpiring with Tesla's stock
tesla[['High','Low']].iplot(kind='spread')</div><i class="fa fa-lightbulb-o "></i>

#this line of code is also giving you a better perspective of the data given from the dataset in a different 
#visualiziation
import plotly.express as px
fig = px.line(tesla, x="Date", y="Adj Close",title = 'Tesla Stock')
fig.show()


