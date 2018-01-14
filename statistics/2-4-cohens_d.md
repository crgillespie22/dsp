[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> ```Python
   preg = nsfg.ReadFemPreg()
   live = preg[preg.outcome == 1]
   
   firsts = live[live.birthord == 1]
   others = live[live.birthord != 1]

   def CohenEffectSize(group1, group2):
       diff = group1.mean() - group2.mean()
       var1 = group1.var()
       var2 = group2.var()
       n1, n2 = len(group1), len(group2)
       pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
       d = diff / np.sqrt(pooled_var)
       return d```
   
   ```Python
   firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()```
   result: (7.201094430437772, 7.325855614973262)
   **First babies are lighter than others**
    
   ```Python
   CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)```
   result: -0.088672927072602006
   **Cohen's D for birth weight is negative and of a larger magnitude than that of pregnancy length**
