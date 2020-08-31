# Pandas
pandas is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool,built on top of the Python programming language.

![image](../img3/pandas.png)

to import pandas into your project: 

 ``` 
 import numpy as np
 import pandas as pd

 ```
## pandas is well suited for many different kinds of data:

 * Tabular data with heterogeneously-typed columns, as in an SQL table or Excel spreadsheet

 * Ordered and unordered (not necessarily fixed-frequency) time series data.

 * Arbitrary matrix data (homogeneously typed or heterogeneous) with row and column labels

 * Any other form of observational / statistical data sets. The data actually need not be labeled at all to be placed into a pandas data structure

## Object creation 

 * Creating a Series by passing a list of values, letting pandas create a default integer index:
    ``` 
    In [3]: s = pd.Series([1, 3, 5, np.nan, 6, 8])

    In [4]: s
    Out[4]: 
    0    1.0
    1    3.0
    2    5.0
    3    NaN
    4    6.0
    5    8.0
    dtype: float64

    ```

* Creating a DataFrame by passing a NumPy array 

    ```
    In [5]: dates = pd.date_range('20130101', periods=6)

    In [6]: dates
    Out[6]: 
    DatetimeIndex(['2013-01-01', '2013-01-02', '2013-01-03', '2013-01-04',
                   '2013-01-05', '2013-01-06'],
                  dtype='datetime64[ns]', freq='D')

    In [7]: df = pd.DataFrame(np.random.randn(6, 4), index=dates, columns=list('ABCD'))

    In [8]: df
    Out[8]: 
                       A         B         C         D
    2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
    2013-01-02  1.212112 -0.173215  0.119209 -1.044236
    2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
    2013-01-04  0.721555 -0.706771 -1.039575  0.271860
    2013-01-05 -0.424972  0.567020  0.276232 -1.087401
    2013-01-06 -0.673690  0.113648 -1.478427  0.524988
    ```

## Viewing data

to view the top and bottom of a fram :

    ```
    In [15]: df.index
    Out[15]: 
    DatetimeIndex(['2013-01-01', '2013-01-02', '2013-01-03', '2013-01-04',
                   '2013-01-05', '2013-01-06'],
                  dtype='datetime64[ns]', freq='D')
    
    ```
Display the index, columns: 
 ```
    In [16]: df.columns
    Out[16]: Index(['A', 'B', 'C', 'D'], dtype='object')
 ```
## Getting 
* Selecting a single column:

    ```
    df['A']

    ```
* Selecting via [], which slices the rows:

    ```
    df[0:3]

    ```

* Selection by label

    ```
    df.loc[dates[0]]

    ```
* Selecting on a multi-axis by label:

    ```
    df.loc[:, ['A', 'B']]

    ```

## Missing data

   pandas primarily uses the value np.nan to represent missing data

  Reindexing allows you to change/add/delete the index on a specified axis. This returns a copy of the data.

    ```
    df1 = df.reindex(index=dates[0:4], columns=list(df.columns) + ['E'])
    df1.loc[dates[0]:dates[1], 'E'] = 1

    ```
* Filling missing data.
    ```
    df1.fillna(value=5)

    ```

## Operations 

### Stats
    Operations in general exclude missing data.

    Performing a descriptive statistic:

        ``` 
        df.mean()
        
        ```
### Apply 
    Applying functions to the data:

        ```
        df.apply(np.cumsum)

        ```

## ***references:***
**read**
1. [Pandas in 10](https://pandas.pydata.org/pandas-docs/stable/getting_started/10min.html)
1. [Master Pandas](https://towardsdatascience.com/be-a-more-efficient-data-scientist-today-master-pandas-with-this-guide-ea362d27386)
**vedio**
1. [Pandas - Getting Started](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)
1. [Real Python - Pandas Tutorials](https://realpython.com/learning-paths/pandas-data-science/)


Done
---
 
[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)