#### A1 Univariate Analysis: Frequency Counts removed
```py
# filter/select all the columns that are categorical, would have 'string' dtype
categ_columns = jobs_df.select_dtypes(include=['string']).columns.tolist()

for col in categ_columns:
    print(f"\n----- Distribution of {col} -----")
    print(jobs_df[col].value_counts(normalize=True) * 100) # gives proportion of each value, *100 for percentage
    print(f"Number of unique values: {jobs_df[col].nunique()}")
```

