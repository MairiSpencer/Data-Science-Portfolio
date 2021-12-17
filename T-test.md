### Exploratory Data Analysis 

The purpose of this code was to find t and p values in order to compare the reaction times between two sets of conditions. This code helped me to reject or fail to reject certain hypotheses. 


```
t, p = stats.ttest_rel(fi_si_acc, fi_sc_acc, alternative='less')

print('Incongruent-Incompatible vs. Incongruent-Compatible t =', str(round(t, 2)), 
      ' p = ', str(round(p / 2, 4)))
```

![Screenshot 2021-12-17 2 09 37 PM](https://user-images.githubusercontent.com/94637758/146589071-0a7eccb6-f415-444e-99dc-789d14bd739e.png)
