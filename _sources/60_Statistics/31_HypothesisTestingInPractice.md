# Hypothesis Testing In Practice

## Single Sample t-test in Python 

See [this example](https://github.com/bnorthan/inf-428-data-analytics-online/blob/master/python/notebooks/statistics/HumanBodyTemp.ipynb)

The test can be run, by first importing data using the Pandas library, then passing the data and the value to be tested to the scipy independent t-test function 

``` python
import scipy.stats
import pandas as pd

temps=pd.read_csv("temps.csv")
scipy.stats.ttest_1samp(temps, 98.6)

```

## Independent groups t-test from stats 

This test is used when we have statistics from 2 groups and we want to test if there is a difference between the groups. 

The [documentation can be found here](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind_from_stats.html#scipy.stats.ttest_ind_from_stats)

A good (and relevant) example is a vaccine trial.  See [this example](https://github.com/bnorthan/inf-428-data-analytics-online/blob/master/python/notebooks/statistics/CovidVaccines.ipynb)


## Independent Groups t-test in Python  

This test is used when we have data from 2 groups as a list.  For example a list of weights of a group of people who are on a special diet and those who are not, and we want to test if there is a difference between groups. 

See this example [here](https://github.com/bnorthan/inf-428-data-analytics-online/blob/master/python/notebooks/statistics/Ind.%20T-test%20Simple.ipynb)

([Also look at this detailed example](https://github.com/bnorthan/inf-428-data-analytics-online/blob/master/python/notebooks/statistics/Ind.%20T-Test%20Baseball%20Teams.ipynb)) which shows the data wrangling needed to get the data into the right format.  

Once we have two dataframes representing the two groups the python code is as follows  

``` python
import numpy as np  
import pandas as pd  
losers=pd.read_csv('losers.csv')  
winners=pd.read_csv('winners.csv') 
import scipy.stats as stats
# perform t-test on wins column
stats.ttest_ind(losers.wins,winners.wins) 

```
