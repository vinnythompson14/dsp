[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

Looking at the distributions, it is clear that the function is actually producing random numbers.

##Imports and generate numpy array 
```python
import numpy as np
import matplotlib.pyplot as plt
x = np.random.random(1000 , )*10
```
##Generate PMF
```python
plt.figure(0)
plt.hist(x, bins = 10, density = True)
plt.xlabel('Value ')
plt.ylabel('Probability')
```
##Generate CDF
```python
plt.figure(1)
plt.hist(x, bins=100, density = True, cumulative = True)
plt.xlabel('Value')
plt.ylabel('CDF')
```
