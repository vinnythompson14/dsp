[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)


## Imports
```python
import nsfg 
import thinkstats2
import thinkplot
```
## Create actual and biased PMFs
```python
numkdhh = nsfg.ReadFemResp()['numkdhh']
numkdhh_pmf = thinkstats2.Pmf(numkdhh, label = 'actual')
biased_pmf = numkdhh_pmf.Copy(label='biased')
for x, p in numkdhh_pmf.Items():
    biased_pmf.Mult(x, x)
biased_pmf.Normalize()
```

## Plot actual and biased distributions
```python
thinkplot.PrePlot(2)
thinkplot.Pmfs([numkdhh_pmf, biased_pmf])
thinkplot.Config(xlabel='# of Kids Per Household', ylabel='PMF')
```

## Compute and print means
```python
print('Actual Mean', numkdhh_pmf.Mean())
print('Observed Mean', biased_pmf.Mean())
```
Actual mean: **1.0242**
Biased mean: **2.4037**




