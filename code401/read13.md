# Linear Regressions

### Exploring Boston Housing Data Set

***The first step is to import the required Python libraries into Ipython Notebook.***

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Explore-1.png)


***This data set is available in sklearn Python module, so I will access it using scikitlearn. I am going to import Boston data set into Ipython notebook and store it in a variable called boston.***

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/sklearn.png)


***The object boston is a dictionary, so you can explore the keys of this dictionary.***

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/boston-keys.png)
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/boston-data-shape1.png)

> I am going to print the feature names of boston data set.

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/boston-features.png)


## Scikit Learn

***In this section I am going to fit a linear regression model and predict the Boston housing prices. I will use the least squares method as the way to estimate the coefficients.***

> Y = boston housing price(also called “target” data in Python)

and

> X = all the other features (or independent variables)

***First, I am going to import linear regression from sci-kit learn module. Then I am going to drop the price column as I want only the parameters as my X values. I am going to store linear regression object in a variable called lm.***


![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Skitlearn-linear-model1.png)


## Fitting a Linear Model


***I am going to use all 13 parameters to fit a linear regression model. Two other parameters that you can pass to linear regression object are fit_intercept and normalize.***

In [20]: lm.fit(X, bos.PRICE)

Out[20]: LinearRegression(copy_X=True, fit_intercept=True, normalize=False)

> I am going to print the intercept and number of coefficients.


![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Estimated-Coeff.png)



## Training and validation data sets


> How not to do train-test split:

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/train-test-split.png)


## Conclusion

> To recap what I have done till now:-


- I explored the boston data set and then renamed its column names.

- I explored the boston data set using .DESCR, my goal was to predict the housing prices using the given features.

- I used Scikit learn to fit linear regression to the entire data set and calculated the mean squared error.

- I made a train-test split and calculated the mean squared error for my training data and test data.

- I then plotted the residuals for my training and test datasets.



