# Experiment-11
Name : Madhur Gupta
PRN:25070123070
 ## Aim of Experiment: Create Dataset and Load Dataset.
 ## Theory:
 Dataset creation / upload

Theory: load the data into a pandas.DataFrame so it can be inspected and manipulated.

Why: subsequent analysis and transformations require an in-memory representation.

df.shape

Theory: returns (n_rows, n_columns).

Why: quick sense of dataset scale — influences compute/time considerations and modelling choices.

df.size

Theory: total number of elements (n_rows × n_columns).

Why: complements shape to reason about total data volume.

df.info()

Theory: prints data types, non-null counts, and memory usage.

Why: reveals incorrect dtypes (e.g., numeric stored as object), identifies columns with missing values,
and helps plan data type optimizations.

df.describe()

Theory: summary statistics for numeric columns (count, mean, std, min, 25/50/75 percentiles, max).
Can be extended to include='all' for categorical summaries.

Why: reveals distributions, outliers, and ranges — useful for normalization/scaling decisions and spotting anomalies.

df.head() and df.tail()

Theory: show the first and last rows.

Why: sanity check for file header issues, presence of trailing garbage rows, and to quickly inspect representative rows.

df.columns

Theory: lists column names.

Why: check for unexpected characters or duplicate names and to plan column selection/renaming.

df.sample(n)

Theory: returns random rows.

Why: intermittently useful to inspect random examples and verify variability.

df.isnull().sum()

Theory: per-column count of missing values.

Why: informs imputation strategy (e.g., mean/median/mode, model-based, or dropping), and whether
missingness itself is informative.

df.duplicated().sum()

Theory: count of duplicate rows.

Why: duplicates can bias analyses and models; decide whether to drop duplicates or investigate why they appear.

df.nunique()

Theory: number of unique values per column.

Why: helps identify categorical vs continuous variables, cardinality issues (high-cardinality categorical features), and potential ID-like columns that should be excluded from modelling.
