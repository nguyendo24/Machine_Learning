# Basic Python Tricks

## Updating Python Packages 

```sh 
pip install -U [package name]
```

Includes materials from DataCamp.com 

## Random Tips
### Bool to num
To convert Boolean True and False list into 1s and 0s.

```py
bool_list*1
```
### Force print
To force print all elements in jupyternotebook 

```py
pd.options.display.max_seq_items = 100
```

https://stackoverflow.com/questions/23388810/ipython-notebook-output-cell-is-truncating-contents-of-my-list

### Datetime conversion 
```py
df.acq_date.apply(lambda x: datetime.strptime(x,'%Y-%m-%d'))
datetime(2018, 1, 7)
```

### Drop Null 
https://pandas.pydata.org/pandas-docs/version/0.21/generated/pandas.DataFrame.dropna.html
```py 
# drop rows if it has any nulls 
df.dropna(axis=0, how='any')
```

### List subtraction 
https://stackoverflow.com/questions/3462143/get-difference-between-two-lists

```py
set([1, 2]) - set([2, 3])
### set([1]) 
```

### Combine Multile Rows into One String

https://stackoverflow.com/questions/33279940/how-to-combine-multiple-rows-of-strings-into-one-using-pandas/41408038

```py
df.[column name].(sep=',')
```

### drop cols with low var/std
```py
df.loc[:, df.std() > .3]
```

### Shuffle Pandas DataFrame 
```py 
df.sample(frac=1)
```

## Reverse Dict Mapping 

```py 
inv_map = {v: k for k, v in my_map.items()}
```

## Print Version 

```py 
# python version 
import sys
print('python version:', sys.version[:31])
# or 
print('python version:', sys.version[:3])
# out: python version: 3.6
```