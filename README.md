# Pandas Cheatsheet

## Setup

1. Import Pandas

```Python
import pandas as pd
```

## Dataframes

### I/O

```python
# read dataframe from excel
pd.read_excel(./<file-path>)
```
### Filter/Query

```python
# create new dataframe based on specific columns
new_df = old_df.filter(["column_1", "column_2"], axis=1)

# group by column value and sum
df.groupby("column-to-groupby")["column-to-sum"].sum()

# group by column value and sum (drop other columns)
df["column1", "column2"].gropuby["column1"].sum("column2")

# filter to rows with specific column values
values = [
    "value1",
    "value2",
    "value3"
]
df = df[df["Column1"].isin(values)]

# filter based off values in multiple columns
df.loc[(df["Column1"].isin(["Value1"])) & (df["Column2"] == "Value2"), : ]

# filter to rows where column value matches regex patter
new_df = df[df["column"].str.match(r"^(PREFIX1|PREFIX2)")==1]
```

### Transform

```python 
# new boolean column based off condition
df["new_boolean_column"] =  df["column1"].map(lambda x: x == "something").astype('boolean')

# drop rows based on column value
df =  df[df.column_name != "value"]
```

### Pivot/View

```python
# unique value counts for column
item_counts = df["col1"].value_counts()

# count specific values in column
df[df["ColumnName"].isin(["Value1", "Value2", "Value3"])].ColumnName.value_counts()

# count total rows in dataframe
len(df.index)

# get column data types
df.dtypes

# get first and last rows of dataset
df.head()
df.head(n=100)
df.tail()
df.tail(n=100)

# get n number of rows anywhere in dataframe
df.iloc[[<row_start_index>:<row_end_index>], : ]

# get row based on max value in particular column
df.loc[[df["Column"].idxmax()], : ]
```
