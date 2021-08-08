# 10 minutes to pandas


***This is a short introduction to pandas, geared mainly for new users. You can see more complex recipes in the Cookbook.***

> Customarily, we import as follows:

In [1]: import numpy as np

In [2]: import pandas as pd

## Object creation


> Creating a Series by passing a list of values, letting pandas create a default integer index:

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


## Missing data

***pandas primarily uses the value np.nan to represent missing data. It is by default not included in computations. See the Missing Data section.***

> Reindexing allows you to change/add/delete the index on a specified axis. This returns a copy of the data.



## Merge

> **Concat**
pandas provides various facilities for easily combining together Series and DataFrame objects with various kinds of set logic for the indexes and relational algebra functionality in the case of join / merge-type operations.


## Grouping

> By “group by” we are referring to a process involving one or more of the following steps:

- **Splitting** the data into groups based on some criteria

- **Applying** a function to each group independently

- **Combining** the results into a data structure


## Pandas for Data Science

***Pandas is a game-changer for data science and analytics, particularly if you came to Python because you were searching for something more powerful than Excel and VBA. Pandas uses fast, flexible, and expressive data structures designed to make working with relational or labeled data both easy and intuitive.***



# master pandas

> Python is open source. It’s great, but has the inherent problem of open source: many packages do (or try to do) the same thing. If you’re new to Python, it’s hard to know the best package for a specific task. You need someone who has experience to tell you. And I tell you today: there’s one package you absolutely need to learn for data science, and it’s called **pandas**.


### tqdm, the one and only

***When working with large datasets, pandas can take some time running .map(), .apply(), .applymap() operations. tqdm is a very useful package that helps predict when theses operations will finish executing (yes I lied, I said we would use only pandas).***



### Overall pandas is one of the reason why Python is such a great language

***There are many other interesting pandas features I could have shown, but it’s already enough to understand why a data scientist cannot do without pandas.***

> To sum up, pandas is

- simple to use, hiding all the complex and abstract computations behind

- (generally) intuitive

- fast, if not the fastest data analysis package (it highly optimized in C)



