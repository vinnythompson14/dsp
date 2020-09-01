[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)


##Import scipy.stats and assign variables for boundary heights in CM
```python
import scipy.stats
five_ten = 177.8 
six_one = 185.42
```

##Solve for percentage between 5'10" and 6'1" as difference of CDFs
```python
dist = scipy.stats.norm(loc=178, scale=7.7)
blue_man_eligible = dist.cdf(six_one) - dist.cdf(five_ten)
blue_man_eligible
```

The result is that 34.27% of the male population is eligible to join the Blue Man Group
