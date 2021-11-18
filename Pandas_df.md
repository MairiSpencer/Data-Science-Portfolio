### Reading in Panda Dataframe Files 
The pandas read function worked to merge and read in the data into a single dataframe. Here this code demonstrates the knowledge of extracting data into a jupyter notebook.


```
import glob
file = glob.glob('s??/s??.txt')
df_list = [pd.read_csv(s, sep='\t') for s in file]
df = pd.concat(df_list)
df.sample(8)
```
