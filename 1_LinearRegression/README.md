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


# Model Types

### Complex Models
Complex models tend to have more coefficient, so the complexity of the model will be added to the error having a bigger combined error

$$
2x_1^3 - 2x_1^2x_2 - 4x_2^3 +3x_1^2+6x_1x_2+4x_2^2 + 5 =0
$$

> Complex model example: 
>  - Model to send a rocket to the moon
>  - Medical model

*Punishment in the complexity should be small in order to reduce the error*

### Simple Models
Simple models tends to generalize better than complex models, also have less coefficients so it will have a smaller combined error than a complex model
$$
3x_1 - 4x_2 + 5 =0
$$

> Simple model example
>  - Video recommendation model
>  - Social recommendation

*Punishment in the complexity should be large in order to tune the model*


### Error tunning 
In order to fix or tune the model punishment we use $\lambda$ parameter and we can pick between

 - **Large $\lambda$** value, we are punishing complexity by a large ammount then we are picking a **simple model**
 - **Small $\lambda$** value, we are punishing complexity by a small ammount then we are ok having  a more **complex model**


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

# Feature Scaling

Feature Scaling your data into a common range of values. There are two common scalings:

 1. Standardizing 
 2. Normalizing

#### Standardizing

Takes each value of a column, substracting the mean o, and the mean of the column, and then dividing by the standard deviation of the column. In Python, you ccould create a standardized value as:
```python
df["height_standard"] = (df["height"] - df["height"].mean()) / df["height"].std()
```

#### Normalizing

A second type of feature scaling that is very popular is known as  **normalizing**. With normalizing, data are scaled between 0 and 1. Using the same example as above, we could perform normalizing in python in the following way:

```python
df["height_normal"] = (df["height"] - df["height"].min()) /     \
                      (df["height"].max() - df['height'].min())
```

### When Should I Use Feature Scaling?

In many machine learning algorithms, the result will change depending on the units of your data. This is especially true in two specific cases:

1.  When your algorithm uses a distance based metric to predict.
2.  When you incorporate regularization.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzkxNzc1MjgzLDE1NjM1MzA0NTAsMjEzMT
MyNjk0MSwtMTU0NjE1NTQ5MiwtMTM0ODA5Njc2OCwxODY5NTI3
MTUzLC02OTQwMTUxNjUsMTE2NzQ3MTQyMSwxODI1MTc5OTczLC
0xOTg0NTcyMjAxXX0=
-->