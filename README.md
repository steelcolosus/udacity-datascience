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



### Difference

The **key difference** between these techniques is that Lasso shrinks the less important feature’s coefficient to zero thus, removing some feature altogether. So, this works well for **feature selection** in case we have a huge number of features.



## L1 vs L2
|L1 Regularization	|L2 Regularization  |
|--|--|
|Computationally Inefficient|Computationally Efficient|
|Sparce Outputs |  Non-Sparse Outputs  |
|Feature Selection | No Feature Selection|
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjEzMTMyNjk0MSwtMTU0NjE1NTQ5MiwtMT
M0ODA5Njc2OCwxODY5NTI3MTUzLC02OTQwMTUxNjUsMTE2NzQ3
MTQyMSwxODI1MTc5OTczLC0xOTg0NTcyMjAxXX0=
-->