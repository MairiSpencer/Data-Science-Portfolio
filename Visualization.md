# Histogram Plot Visualization
This histogram plot showcases the log reaction of a specific condition. Visualization acts as an important component for the interpretation of the data set as it clearly shows the differences between both conditions.


```python
sns.displot(data=df, x='log_rt', hue='flankers')
plt.show()
```

![Screenshot 2021-12-15 11 44 17 AM](https://user-images.githubusercontent.com/94637758/146217957-4dbd1f34-e56b-4c97-9208-46137e582e28.png)


# Boxplot Visualization
Visualization can also be represented via a boxplot as shown below. Here, we can gain better insight into the distribution of data by viewing the minimum, interquartile range, and maxiumum data point. The median is also represented in a boxplot as well as any outliers which can lead to a more accurate interpretation of the data.


![Screenshot 2021-12-15 11 52 37 AM](https://user-images.githubusercontent.com/94637758/146219341-d437d55d-98a6-4d17-9c26-42419f8bb9dc.png)
