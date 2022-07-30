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

## 140

bigmac.index.names

bigmac.index = bigmac.index.set_names(names=['Day','Location'])

world_stats.index = world_stats.index.set_names(names=['Country', 'Year'])

import os
cwd = os.getcwd() + '\\' + 'section_08\\'

bigmac.index.get_level_values('Country')

**bigmac.loc[(slice(None),'United States'),:]**

## 141
bigmac.sort_index(level=1, ascending=False)

## 146
world_stats.stack().to_frame()

## 147

world_stats.unstack().unstack().unstack().to_frame()

## 148

world_statistics_stacked.unstack(-3)

world_statistics_stacked.unstack('country')

## 149

world_statistics.unstack(level=['year', 'country'])

world_statistics.unstack(level=[1,0])

world_statistics.unstack('year', fill_value=0)

## 150

salesmen = salesmen.pivot(index='Date', columns='Salesman', values='Revenue')

## 151

foods = foods.pivot_table(values='Spend', index=['Gender', 'Item'], columns=['Frequency', 'City'], aggfunc='mean')
pd.pivot_table(**data=foods**, values='Spend',index='City', aggfunc='max')

## 152

sales = pd.melt(sales, id_vars='Salesman', var_name='Quarter', value_name='Revenue')

## 156

sectors = fortune.groupby('Sector')
len(sectors)
sectors.groups
sectors.size()
sectors.first()
sectors.last()
sectors.get_group('Apparel')

## 159

sectors.agg({'Profits': 'sum',
                'Employees':'mean'})
sectors.agg(['size', 'sum', 'min'])
sectors.agg({'Revenue': ['sum','mean'],
            'Profits': 'sum',
            'Employees': 'mean'})

## 163

sales = pd.concat(objs=[week_1, week_2], keys=['week_1', 'week_2'])
sales.loc[('week_1', 240), 'Customer ID']

## 164

week_1.merge(week_2, how='inner', on='Customer ID', suffixes=[' - A', ' - B'])

## 166 

week_1.merge(week_2, how='outer', on='Customer ID')

week_1.merge(week_2, how='outer', on='Customer ID', suffixes=[' - Week 1', '  -  Week 2'])

week_1.merge(week_2, how='outer', on='Customer ID', suffixes=[' - Week 1', ' - Week 2'], indicator=True)

**Full outer join:**

mask_merge = merged_work_week['_merge'].isin(['left_only', 'right_only'])

merged_work_week[mask_merge]

## 167 

week_1.merge(foods, how='left', on='Food ID')

week_1.merge(foods, how='left', on='Food ID', sort=True)

## 168

week_2.merge(customers, how='left', left_on='Customer ID', right_on='ID')

week_2.merge(customers, how='left', left_on='Customer ID', right_on='ID').drop('ID', axis='columns')

## 171

pd.merge(left=week_1, right=customers, how='left', left_on='Customer ID', right_on='ID')

## 176

pd.to_datetime(['2015-01-03','2014-02-08','2022 2 22','July 4th, 1996','2020','2199-01','2200','2262'])

times = pd.Series(['2022-12-31','2023-01-01','2024,06,06'])

pd.to_datetime(times)
pd.to_datetime(tates, **errors='coerce'**)
pd.to_datetime(unix_times, unit='s')

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
