#Neuroimaging of Multiple Brain Slices
This code was for an assignment demonstrating neuroimaging with MRI data. Specifically, this question visualized 3D images of multiple slices of a human brain. It arranged this in a 4 x 4 array and used the enumerate loop variable to create the for loop.  

```
fig, axs = plt.subplots(4, 4, figsize=[8, 8])
start = int((vol.shape[0] - 160) / 2 )
stop = int(vol.shape[0] - start)

for index, mri in enumerate(range(start, stop, 10)):
    axs.flat[index].imshow(vol[mri], cmap='gray')
    axs.flat[index].axis('off')

plt.tight_layout()
plt.show()
```


![Screenshot 2021-12-15 10 43 17 AM](https://user-images.githubusercontent.com/94637758/146208408-9af82384-d545-4d82-9717-30b23c871030.png)

#Reslice an Image
We can also reslice a 3D image to visualize the brain from a different point of view. Using the plt.imshow function we can convert an image from the saggital plane to now represent itself as if viewing from face on in the coronal plane.

```
plt.imshow(vol[:, :, 92], cmap='gray')
plt.axis('off')
plt.tight_layout()
```


![Screenshot 2021-12-15 11 13 25 AM](https://user-images.githubusercontent.com/94637758/146212674-f88f7d09-a282-478f-84d5-1439a0d4b268.png)

