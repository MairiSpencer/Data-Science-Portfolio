### Single-Unit Data
This block of code demonstrates a raster plot for single-unit data. This spike data had been retrieved from neurons within the primary visual cortex of mice using single electrodes to record. This raster plot represents both the control and adaptation condition for a specific neuron and tracks the number of firings.  


```
fig, axs = plt.subplots(len(contr_levels), len(conditions[::-1]), figsize=[15,15], sharex=True, sharey=True)

for l, x in enumerate(contr_levels):
    for m, c in enumerate(conditions):
        for r in trials:
            spike_times = df[(df.neuron == 'm1_6') & (df.condition == c) & (df.contrast == x) & (df.repetition == r)]['spiketime']
            axs[l, m].vlines(spike_times, r - 0.4, r + 0.4)
        axs[l, m].axvspan(stim_on_time, stim_off_time,
                      alpha= x / (max(contr_levels) * 1.5),
                      color='grey')
        axs[l, m].set_yticks(trials)
        axs[l, 0].set_ylabel(str(x) + "%")
        axs[l, 1].set_ylabel("Trial Num")
        if l == 0:
            axs[l, 0].set_title('Control Condition', fontsize=10)
            axs[l, 1].set_title('Adaptation Condition', fontsize=10)
        if l == 9:
            axs[l, 1].set_xlabel('Time (ms)')
            axs[l, 0].set_xlabel('Time (ms)')

       
fig.suptitle('m1_6 neuron')
plt.tight_layout()
plt.show() 
```
![Screenshot 2021-11-18 4 39 11 PM](https://user-images.githubusercontent.com/94637758/142497426-c6a43404-97b3-476e-8145-ed49f7d754a7.png)
![Screenshot 2021-11-18 5 13 10 PM](https://user-images.githubusercontent.com/94637758/142497850-9f2da43f-bcb4-4f3f-954f-ed8c6feb95ef.png)
![Screenshot 2021-11-18 5 14 13 PM](https://user-images.githubusercontent.com/94637758/142497930-b6b751d7-cf35-4a50-8a87-225c3612fa4f.png)


