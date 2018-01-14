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
4.9499202444295829
```Python
PearsonMedianSkewness(sample)
```
0.7361258019141782

The results depend on the upper bound because it eliminates certain outliers. A higher upper bound allows more outliers to exert an effect on the statistics.

The skewness more than doubles when the upper bound is 10 million.
