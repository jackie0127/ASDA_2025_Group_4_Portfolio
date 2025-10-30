# Basic EDA of two datasets - Report Structure for week 2 

## 1. Dataset Overview 

first dataset (earthquake) 

| Item | Description |
| :--- | :--- |
| Dataset name |GEOFON Earthquake event catalogue (up to 2025-10-21, 1796 records) |
| Number of rows |1796|
| Number of columns |15 |
| Format file (.csv, .txt, etc) |.csv |
| Authors of the dataset |GFZ Helmholtz Centre for Geosciences, Potsdam |
| Source (name) |GEOFON |
| Source (link) |https://geofon.gfz.de/fdsnws/event/1/query?end=2025-10-21&limit=1796&format=csv |

**Short description (what is it about?)** 

This dataset contains a subset of global earthquake events recorded by the GEOFON Seismic Network and retrieved via the FDSNWS Event Service (Federation of Digital Seismograph Networks Web Services). The dataset includes 1796 earthquake records collected up to October 21, 2025. 

second dataset (weather)

| Item | Description |
| :--- | :--- |
| Dataset name |Weather prediction |
| Number of rows |1461 |
| Number of columns |6 |
| Format file (.csv, .txt, etc) |.csv |
| Authors of the dataset |Ananth R (Kaggle user) |
| Source (name) |Kaggle |
| Source (link) |https://www.kaggle.com/datasets/ananthr1/weather-prediction/data |

**Short description (what is it about?)** 

This dataset contains daily weather data from Seattle, including precipitation, maximum and minimum temperature, and wind speed. It is used to predict the weather condition such as drizzle, rain, sun, snow, or fog.

---

## 2. Structure of the dataset 

| Column name | Data type | Non-null count | Unique values | Example values |
| :--- | :--- | :--- | :--- | :--- |
| | | | | |

---

## 3. Descriptive statistics **(STEFAN SMID)**

### Numeric columns
#### earthquake:
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

#### weather:
|  | precipitation | temp\_max | temp\_min | wind |
| :--- | :--- | :--- | :--- | :--- |
| count | 1461.0 | 1461.0 | 1461.0 | 1461.0 |
| mean | 3.02943189596167 | 16.43908281998631 | 8.234770704996578 | 3.24113620807666 |
| std | 6.680194322314738 | 7.349758097360177 | 5.023004179961266 | 1.4378250588746193 |
| min | 0.0 | -1.6 | -7.1 | 0.4 |
| 25% | 0.0 | 10.6 | 4.4 | 2.2 |
| 50% | 0.0 | 15.6 | 8.3 | 3.0 |
| 75% | 2.8 | 22.2 | 12.2 | 4.0 |
| max | 55.9 | 35.6 | 18.3 | 9.5 |


### Categorical/object columns
#### earthquake:
|  | #EventID | Time | Contributor | ContributorID | MagType | EventLocationName | EventType |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| count | 1796 | 1796 | 1796 | 1796 | 1796 | 1796 | 7 |
| unique | 1796 | 1796 | 1 | 1796 | 5 | 255 | 3 |
| top | gfz2025upgl | 2025-10-20T23:00:55.01 | GFZ | gfz2025upgl | mb | Off East Coast of Kamchatka | quarry blast |
| freq | 1 | 1 | 1796 | 1 | 1457 | 358 | 3 |

#### weather:
|  | date | weather |
| :--- | :--- | :--- |
| count | 1461 | 1461 |
| unique | 1461 | 5 |
| top | 2012-01-01 | rain |
| freq | 1 | 641 |


---

## 3. Missing values and duplicates

Missing values and duplicates: GEOFON Earthquake Data (eq_df)
------------------------------------------------------------
| Column name | Missing count | % Missing |
|-------------|---------------|-----------|
| Author      | 1796          | 100.0     |
| Catalog     | 1796          | 100.0     |
| MagAuthor   | 1796          | 100.0     |
| EventType   | 1789          | 99.61     |

Total missing values: 7177

Percentage of dataset affected: 26.64%

Duplicated rows found: 0

Percentage of rows in dataset affected: 0.00%

Missing values and duplicates: Seattle Weather Data (weather_df)
------------------------------------------------------------
| Column name | Missing count | % Missing |
|-------------|---------------|-----------|
|             |               |           |

Total missing values: 0

Percentage of dataset affected: 0.00%

Duplicated rows found: 0

Percentage of rows in dataset affected: 0.00%

---

## 4. Data consistency

first dataset (earthquake) 
| Item | Description |
| :--- | :--- |
| **Does the dataset contain unnecessary columns? Which?** | Yes, multiple columns are not filled with data: "Unnamed: 0" is a duplicate of the row index; "Author", "Catalog" and "MagAuthor" are completely empty. "EventType" is mostly empty. |
| **Do the data types correspond to the columns?** | Mostly. Only the time column has an incorret datatype (object instead of datetime).|
| **Is the labelling of the columns appropriate?** | The Column "Unnamed: 0" is not named appropriate.|
| **Are there mixed values in column (e.g., number and characters)?** | No |
| **Are string column clean?** | Yes |
| **Does the dataset look machine generated?** | No |
| **Other** | |

second dataset (weather)

| Item | Description |
| :--- | :--- |
| **Does the dataset contain unnecessary columns? Which?** | No |
| **Do the data types correspond to the columns?** | Mostly. Only the time column has an incorret datatype (object instead of datetime).|
| **Is the labelling of the columns appropriate?** | Yes |
| **Are there mixed values in column (e.g., number and characters)?** | No |
| **Are string column clean?** | Yes |
| **Does the dataset look machine generated?** | No |
| **Other** | |

---
## GEOFON data set
## 5. Overall assessment 
**Is it worth it to further analyze the dataset?** 
**Yes.**  
This dataset has high value for further analysis because:
- All essential columns have complete data (100% completeness).
- Robust sample size (1,796 events, 80 days).
- Wide global coverage.
- Good precision for coordinates and magnitude.
- No duplicate records.
- Diverse event locations and magnitude types.

**What possible analysis can be performed?** 

**Possible Analysis**

- **Temporal Analysis:** frequency/time trends, daily/weekly patterns, forecasting.
- **Spatial Analysis:** hotspot mapping, regional activity, clustering.
- **Magnitude Analysis:** distribution, scale comparison, statistical modeling.
- **Depth Analysis:** analysis of shallow/deep earthquakes.
- **Geophysical Modeling:** patterns in relation to tectonic settings.
- **Machine Learning:** prediction, clustering, anomaly detection.


## 6. Next steps
**Handling Missing Values**

- Remove fully empty columns: `Author`, `Catalog`, `MagAuthor` (100% missing).
- Drop (or impute) `EventType` (99.6% missing).
- Essential columns need no missing value treatment.

**Removing Duplicates**

- No duplicates found (by row or EventID).
- No action needed.

**Cleaning Columns**

- Drop: `Unnamed: 0` (row index).
- Convert: `Time` to datetime format.
- Rename: `Depth/km` to `Depth_km` (remove special characters).
- Create: Magnitude categories if needed.
- Retain: Essential columns for analysis.

**Creating Dataframe Subsets**

- High-magnitude (`Magnitude >= 6.0`)
- Shallow earthquakes (`Depth ≤ 70 km`)
- Recent events (last 30 days)
- Regional focus (e.g. Kamchatka)
- Magnitude type subset (`mb`, `Mw`)
- Depth category (shallow/intermediate/deep)
---
## Seattle Weather Dataset Analysis

**Is it worth further analyzing the dataset?**

**Yes.** This weather dataset is a solid candidate for further analysis because:
- All columns are 100% complete.
- No duplicate records.
- Clean structure, consistent types.
- Represents 4 years of daily weather (2012–2015, 1,461 days).
- Core attributes cover essential climate variables (precipitation, min/max temp, wind, weather type).

**Possible Analysis**

- **Temporal Analysis:** trends, seasonality, year-to-year or month-to-month climate variations.
- **Weather Event Analysis:** frequency and extremity of rain, fog, snow, drizzle, sun.
- **Temperature Analysis:** distribution, extremes, patterns in max/min change.
- **Precipitation Analysis:** distribution, identifying wettest/driest periods, outlier events.
- **Wind Analysis:** wind pattern behavior, correlation with weather types.
- **Correlations:** investigate connections between temperature, precipitation, and weather types.
- **Anomaly/Outlier Analysis:** highlight and interpret uncommon/extreme values.

## 6. Next Steps

**Handling Missing Values**

- No missing values in any column.
- No action needed.

**Removing Duplicates**

- No duplicate rows present.
- No action needed.

**Cleaning the Columns**

- **Convert:** `date` column to datetime format for better temporal analysis.
- **Standardize:** Check for consistency in `weather` naming if expanding.
- **Retain:** All variables are valuable for analysis; no columns to remove.

**Creating Dataframe Subsets**

- Precipitation event analysis (`precipitation > 0` vs. dry days).
- Temperature extremes (`temp_max > 30` for heat waves, `temp_min < 0` for freezing spells).
- Seasonal/Monthly subsets.
- Subset by specific `weather` types (e.g., only "snow" or "fog" days).
- High wind events (`wind` above top quartile).
