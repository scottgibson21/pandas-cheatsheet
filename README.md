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
df.groupby("column-to-groupby")["column-to-sum"].sum()
```

3. Count unique values in column

```python
item_counts = df["col1"].value_counts()
```

4. Count specific values in a column

```python
df[df["ColumnName"].isin(["Value1", "Value2", "Value3"])].ColumnName.value_counts()
```

5.  Count total rows in data frame

```python
len(df.index)
```

6.  Create new boolean column based on condition in specific column

```python
df["new_boolean_column"] =  df["column1"].map(lambda x: x == "something").astype('boolean')
```

7.  Drop rows based on column value

```python
df =  df[df.column_name != "value"]
```

8.  Group and sum

```python
new_df =  df["column1", "column2"].gropuby["column1"].sum("column2")
```

9.  Get Column Data Types

```python
df.dtypes
```

9.  Get first or last rows of dataset
```python
df.head()
df.head(n=100)
df.tail()
df.tail(n=100)
```

