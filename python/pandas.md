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
