# Data Analysis with Pandas and Python

.dropna(how='all')

.hasnans <-- bool value

.astype(dtype='int')

.nunique()

.dtypes

.info()

.sort_values()

.sort_values(by=['Team', 'Name'], ascending=[False,True])

.value_counts(normalize=True)

.fillna(0).astype('int')

.to_numpy()

.drop_duplicates()

.unique()

~ <-- reverse True to False

.duplicated(keep = False) .duplicated(keep='last')

.drop_duplicates(subset=['First Name'], keep = False)

.reset_index()

.set_index('Film')

.loc['Casino Royale']

.iloc[[15,20,0]]

.str.replace('$','') .str.replace('Mgmnt', 'Management')

.str.strip().str.title()

.str.contains('water')

.str.startswith('water')

.str.endswith('ist')

chicago['Name'].str.split(',').str.get(1).str.strip().str.strip().str.split(' ').str.get(0).str.title().value_counts().head(n=15)

chicago['Position Title'].str.split(' ', expand=True, n=1)

**bigmac.nunique()**

bigmac.index.names

import os
cwd = os.getcwd() + '\\' + 'section_08\\'

bigmac.index.get_level_values('Country')

**bigmac.loc[(slice(None),'United States'),:]**

## Filtering DataFrame

mask = df['Team] == 'Finance

df[mask]

https://nordea.udemy.com/course/data-analysis-with-pandas/

https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

https://www.ibm.com/docs/en/watson-studio-local/1.2.3?topic=notebooks-markdown-jupyter-cheatsheet

https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html

### Test

#### Nice

## Nice

# Nice

---

---

---

---

---

---

_Nice_

**Nice**

~~Not Nice~~
