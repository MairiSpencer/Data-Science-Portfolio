### Histogram Plot Visualization
This histogram plot showcases the log reaction of a specific condition. Visualization acts as an important component for the interpretation of the overall data set.


```python
sns.displot(data=df, x='log_rt', hue='flankers')
plt.show()
```

![Screenshot 2021-11-18 3 53 36 PM](https://user-images.githubusercontent.com/94637758/142496814-3e39311a-5918-4ccd-8526-dfb3539c37dd.png)
