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
