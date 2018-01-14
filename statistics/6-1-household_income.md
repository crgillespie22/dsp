[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

>> 
```Python
RawMoment(sample, 1)
```
74278.707531187334
```Python
Median(sample)
```
51226.454478940461
```Python
StandardizedMoment(sample,3)
```
1.054840012109306
```Python
PearsonMedianSkewness(sample)
```
0.26436733816180391
```Python
cdf.Prob(Mean(sample))
```
0.66000587956687196

The results depend on the upper bound because it eliminates certain outliers. A higher upper bound allows more outliers to exert an effect on the statistics.

The skewness increases dramatically when the upper bound is 10 million.
