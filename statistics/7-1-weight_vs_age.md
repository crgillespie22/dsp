[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

>> 
```Python
ages, weights = live.agepreg, live.totalwgt_lb
thinkplot.Scatter(ages, weights, alpha=.2)
thinkplot.Config(xlabel='Age (yrs)',
                 ylabel='Weight (lbs)',
                 axis=[10, 50, 0, 15],
                 legend=False)
```
