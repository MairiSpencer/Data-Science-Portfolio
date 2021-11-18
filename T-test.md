### Exploratory Data Analysis 

This purpose of this code was to find t and p values in order to compare the reaction times between two sets of conditions. This code helped me to reject or fail to reject certain hypotheses. 


```
t, p = stats.ttest_rel(fi_si_acc, fi_sc_acc, alternative='less')

print('Incongruent-Incompatible vs. Incongruent-Compatible t =', str(round(t, 2)), 
      ' p = ', str(round(p / 2, 4)))
```
