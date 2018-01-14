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
![Scatter](7_1_Scatter)
```Python
bins = np.arange(10, 50, 4)
indices = np.digitize(live.agepreg, bins)
groups = live.groupby(indices)

ages = [group.agepreg.mean() for i, group in groups][1:-1]
cdfs = [thinkstats2.Cdf(group.totalwgt_lb) for i, group in groups][1:-1]

thinkplot.PrePlot(3)
for percent in [75, 50, 25]:
    weights = [cdf.Percentile(percent) for cdf in cdfs]
    label = '%dth' % percent
    thinkplot.Plot(ages, weights, label=label)

thinkplot.Config(xlabel="Mother's age (yrs)",
                    ylabel='Birth weight (lbs)',
                    xlim=[12, 45], legend=True)
```
![Percentile](7_1_Percentile)
```Python
print("Pearson's Corr: ", Corr(ages, weights))
print("Spearman's Corr: ", SpearmanCorr(ages, weights))
```
Pearson's Corr:  0.0688339703541

Spearman's Corr:  0.0946100410966

Due to the relative difference between Pearson's and Spearman's correlations, outliers likely affect the data. There appears to be a weak relationship between the two variables, which may imply nonlinearity.
