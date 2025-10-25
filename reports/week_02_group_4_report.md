# Basic EDA of two datasets - Report Structure for week 2 

## 1. Dataset Overview 

| Item | Description |
| :--- | :--- |
| Dataset name | |
| Number of rows | |
| Number of columns | |
| Format file (.csv, .txt, etc) | |
| Authors of the dataset | |
| Source (name) | |
| Source (link) | |

**Short description (what is it about?)** 

---

## 2. Structure of the dataset 

| Column name | Data type | Non-null count | Unique values | Example values |
| :--- | :--- | :--- | :--- | :--- |
| | | | | |

---

## 3. Descriptive statistics **(STEFAN SMID)**

### Numeric columns

|  | Unnamed: 0 | Latitude | Longitude | Depth/km | Author | Catalog | Magnitude | MagAuthor |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| count | 1796.0 | 1796.0 | 1796.0 | 1796.0 | 0.0 | 0.0 | 1796.0 | 0.0 |
| mean | 897.5 | 23.802863585746103 | 84.30529398663697 | 61.71464365256125 | NaN | NaN | 4.909398663697105 | NaN |
| std | 518.6048592136406 | 32.42439271541648 | 104.34450285027032 | 109.7900570483029 | NaN | NaN | 0.4773493144419643 | NaN |
| min | 0.0 | -65.14 | -179.877 | 0.0 | NaN | NaN | 1.85 | NaN |
| 25% | 448.75 | -3.0585 | 24.12875 | 10.0 | NaN | NaN | 4.72 | NaN |
| 50% | 897.5 | 37.542 | 138.861 | 26.0 | NaN | NaN | 4.9 | NaN |
| 75% | 1346.25 | 51.73625 | 159.235 | 55.025 | NaN | NaN | 5.11 | NaN |
| max | 1795.0 | 84.841 | 179.969 | 630.7 | NaN | NaN | 7.79 | NaN |

### Categorical/object columns

|  | #EventID | Time | Contributor | ContributorID | MagType | EventLocationName | EventType |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| count | 1796 | 1796 | 1796 | 1796 | 1796 | 1796 | 7 |
| unique | 1796 | 1796 | 1 | 1796 | 5 | 255 | 3 |
| top | gfz2025upgl | 2025-10-20T23:00:55.01 | GFZ | gfz2025upgl | mb | Off East Coast of Kamchatka | quarry blast |
| freq | 1 | 1 | 1796 | 1 | 1457 | 358 | 3 |

---

## 3. Missing values and duplicates

| Column name | Missing count | % Missing |
| :--- | :--- | :--- |
| | | |

**Total missing values:**   
**Percentage of dataset affected:**   
**Duplicated rows found:**   
**Percentage of rows in dataset affected:**   

---

## 4. Data consistency

| Item | Description |
| :--- | :--- |
| **Does the dataset contain unnecessary columns? Which?** | |
| **Do the data types correspond to the columns?** | |
| **Is the labelling of the columns appropriate?** | |
| **Are there mixed values in column (e.g., number and characters)?** | |
| **Are string column clean?** | |
| **Does the dataset look machine generated?** | |
| **Other** | |

---

## 5. Overall assessment 

**Is it worth it to further analyze the dataset?** 

**What possible analysis can be performed?** 

---

## 6. Next steps

- Handling missing values? How? 
- Removing duplicates?
- Cleaning the columns? Which? 
- Creating a subset of the dataframe? 