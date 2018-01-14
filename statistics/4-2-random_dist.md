[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> 
```Python
t = np.random.random(1000)
pmf = thinkstats2.Pmf(t)
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='Random Number', ylabel='PMF')
```
![Plot1]
```Python
cdf = thinkstats2.Cdf(t)
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='Random Number', ylabel='CDF')
```
![Plot2]
