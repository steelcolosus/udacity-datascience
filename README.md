# Absolute Trick
*For a point above the rect*
![enter image description here](https://github.com/steelcolosus/udacity-datascience/blob/master/images/below.png?raw=true)

$$
y = (w_1 + p\alpha)x + (w_2 + \alpha)
$$

for a point beneath the line
![Beneath](https://github.com/steelcolosus/udacity-datascience/blob/master/images/below.png?raw=true)
$$
y = (w_1 - p\alpha)x + (w_2 - \alpha)
$$

# Square Trick


![Beneath](https://github.com/steelcolosus/udacity-datascience/blob/master/images/squaretrick.png?raw=true)

$$
y = (w_1 - p(q-q')\alpha)x + (w_2 - (q-q')\alpha)
$$

# Closed  Form

> *Closed form solution math:*

$$W=(X^T X)^{-1} X^Ty$$

# Regularization

A regression model that uses L1 regularization technique is called **_Lasso Regression_** and model which uses L2 is called **_Ridge Regression_**.

### L1 Regularization 
Least Absolute Shrinkage and Selection Operator adds “_absolute value of magnitude_” of coefficient as penalty term to the loss function.

### L2 Regularization
**Ridge regression** adds “_squared magnitude_” of coefficient as penalty term to the loss function.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDM0MjQxNTA1LC0xNTQ2MTU1NDkyLC0xMz
Q4MDk2NzY4LDE4Njk1MjcxNTMsLTY5NDAxNTE2NSwxMTY3NDcx
NDIxLDE4MjUxNzk5NzMsLTE5ODQ1NzIyMDFdfQ==
-->