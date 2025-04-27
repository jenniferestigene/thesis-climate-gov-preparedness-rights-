This folder contains the original/raw datasets used in this thesis.

# 📘 Data Dictionary: Raw Datasets

This folder contains the original, unprocessed datasets used for generating the final analysis-ready files. No transformations, filtering, or imputations have been applied here.

---

## 1. `EMDAT_Disaster_Data.xlsx`

Raw dataset downloaded from EM-DAT (The International Disaster Database), detailing global disaster events by country and year.

| Variable Name                        | Description |
|--------------------------------------|-------------|
| DisNo.                               | Unique EM-DAT disaster ID |
| Historic                             | Indicator if the event is marked as historic |
| Classification Key                   | EM-DAT internal classification key |
| Disaster Group                       | Broad classification of disaster (e.g., Natural, Technological) |
| Disaster Subgroup                    | Subgroup of the disaster group (e.g., Climatological) |
| Disaster Type                        | Specific type of disaster (e.g., Flood, Earthquake) |
| Disaster Subtype                     | More specific subtype of the disaster (e.g., Flash Flood) |
| External IDs                         | External references or disaster IDs from other databases |
| Event Name                           | Name given to the disaster (e.g., "Cyclone Idai") |
| ISO                                  | ISO alpha-3 country code |
| Country                              | Country where the disaster occurred |
| Subregion                            | Subregional classification of the country |
| Region                               | Geographic region (e.g., Africa, Asia) |
| Location                             | Subnational location affected (e.g., province or city) |
| Origin                               | Origin of the disaster (e.g., natural, technological) |
| Associated Types                     | Other disaster types associated with the event |
| OFDA/BHA Response                    | Indicator if OFDA/BHA provided humanitarian response |
| Appeal                               | Whether there was an international aid appeal |
| Declaration                          | Whether an emergency declaration was issued |
| AID Contribution ('000 US$)          | Total aid received in thousands of USD |
| Magnitude                            | Reported magnitude of the disaster (if applicable) |
| Magnitude Scale                      | Type of scale used (e.g., Richter, Category) |
| Latitude                             | Latitude of the disaster location |
| Longitude                            | Longitude of the disaster location |
| River Basin                          | Name of river basin (if applicable) |
| Start Year                           | Year when the disaster began |
| Start Month                          | Month when the disaster began |
| Start Day                            | Day when the disaster began |
| End Year                             | Year when the disaster ended |
| End Month                            | Month when the disaster ended |
| End Day                              | Day when the disaster ended |
| Total Deaths                         | Total number of deaths reported |
| No. Injured                          | Total number of people injured |
| No. Affected                         | Total number of people affected (excluding injured and homeless) |
| No. Homeless                         | Number of people reported homeless |
| Total Affected                       | Combined number of affected, injured, and homeless |
| Reconstruction Costs ('000 US$)      | Estimated reconstruction costs in thousands of USD |
| Reconstruction Costs, Adjusted ('000 US$) | Inflation-adjusted reconstruction costs |
| Insured Damage ('000 US$)            | Value of insured damages (non-adjusted) |
| Insured Damage, Adjusted ('000 US$)  | Value of insured damages (adjusted) |
| Total Damage ('000 US$)              | Total economic damage (non-adjusted) |
| Total Damage, Adjusted ('000 US$)    | Total economic damage (adjusted for inflation) |
| CPI                                  | Consumer Price Index used for inflation adjustment |
| Admin Units                          | Number of administrative units affected |
| Entry Date                           | Date when the disaster entry was added to EM-DAT |
| Last Update                          | Date of the most recent update to the entry |

---

## 2. `wgidataset.xlsx`

Raw Worldwide Governance Indicators (WGI) dataset providing governance estimates by country and year for six dimensions.

| Variable Name   | Description |
|------------------|-------------|
| codeindyr        | Unique code for indicator and year |
| code             | WGI indicator code (e.g., GE, VA, RL) |
| countryname      | Full country name |
| year             | Year of estimate |
| indicator        | Full name of the WGI indicator (e.g., Government Effectiveness) |
| estimate         | Point estimate of governance performance |
| stddev           | Standard deviation of the estimate |
| nsource          | Number of data sources used for the estimate |
| pctrank          | Percentile rank (0–100) |
| pctranklower     | Lower bound of the confidence interval |
| pctrankupper     | Upper bound of the confidence interval |


---

📎 These files serve as the original source for all processed data and are not modified in any way. For cleaned and merged versions, see `data/preprocessed/`.
