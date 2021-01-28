# Pandas Cheatsheet
## Indexing
`.loc` is used for label-based indexing:

```python 
df.loc[['rowA', 'rowB', 'rowC'], ['colA', 'colB']]
```

`.iloc` is used for positional indexing:

```python
df.iloc[[0,1,2],[0,1]]
```
`.ix` is deprecated

## Filtering Dataframes
### Drop Columns if any row contains a specific value
```python
df = df.drop([col for col in df.columns if x[col].eq(1.0).any()], axis=1) 
```

## Charting Data
### Histogram of non-numeric data
```python 
histo = df.groupby('column').size()
plt.figure();
histo.plot.bar(); plt.axhline(0, color='k')
```

### Histogram of all columns in a DF, regardless of numeric values 
``` python 
for colname in df: 
    histo = df.groupby(colname).size()
    plt.figure();
    histo.plot.bar(); plt.axhline(0, color='k')
    ```
