# Pandas Cheatsheet

## Setup

1. Import Pandas

```Python
import pandas as pd
```

## Dataframes

1. Create Dataframe from Excel

```python
pd.read_excel(./<file-path>)
```

2. New Dataframe with Specific Columns

```python
new_df = old_df.filter(["column_1", "column_2"], axis=1)
```

2. Group By Column Value and Sum

```python
df.groupby("<column-to-groupby")["column-to-sum"].sum()
```

3. Count unique values in column

```python
item_counts = df["col1"].value_counts()
```

4. Count specific values in a column

```python
df[df["ColumnName"].isin(["Value1", "Value2", "Value3"])].ColumnName.value_counts()
```

4.  Count total rows in data frame

```python
len(df.index)
```



