# Basic Python Tricks

Includes materials from DataCamp.com 

## Random Tips
### Bool to num
To convert Boolean True and False list into 1s and 0s.

```
bool_list*1
```
### Force print
To force print all elements in jupyternotebook 

```
pd.options.display.max_seq_items = 100
```

https://stackoverflow.com/questions/23388810/ipython-notebook-output-cell-is-truncating-contents-of-my-list

### Datetime conversion 
```
df.acq_date.apply(lambda x: datetime.strptime(x,'%Y-%m-%d'))
datetime(2018, 1, 7)
```

### Any rows with NAN
```
df[df.isnull().any(axis=1)]
```

### List subtraction 
https://stackoverflow.com/questions/3462143/get-difference-between-two-lists

```
set([1, 2]) - set([2, 3])
### set([1]) 
```

### Combine Multile Rows into One String

https://stackoverflow.com/questions/33279940/how-to-combine-multiple-rows-of-strings-into-one-using-pandas/41408038

```
df.[column name].(sep=',')
```