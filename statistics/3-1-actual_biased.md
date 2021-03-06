[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>>
```Python
resp = nsfg.ReadFemResp()
pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')

def biaspmf(pmf, label):
    new_pmf = pmf.Copy(label=label)
    
    for x, p in pmf.Items():
        new_pmf.Mult(x,x)
        
        new_pmf.Normalize()
    return new_pmf
    
biased_pmf = biaspmf(pmf, 'observed')
    
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Number of Kids', ylabel='PMF')
```

![plot](3_1_Plot.png)
```Python
print('Actual Mean', pmf.Mean())
print('Observed Mean', biased_pmf.Mean())
```
**Actual Mean 1.02420515504**

**Observed Mean 2.40367910066**
