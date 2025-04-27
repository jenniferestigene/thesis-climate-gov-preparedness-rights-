This folder contains cleaned and analysis-ready datasets.

# 📘 Data Dictionary: Preprocessed Datasets

This folder contains cleaned and analysis-ready datasets.

---

## 1. `emdat_wgi_rights.csv`

Merged dataset combining EM-DAT disaster records with Worldwide Governance Indicators and human rights-related variables.

| Variable Name              | Description |
|----------------------------|-------------|
| ISO                        | Country ISO alpha-3 code |
| Country                    | Country name |
| Year                       | Year of observation |
| Region                     | Geographic region (e.g., Asia, Africa) |
| Subregion                  | Geographic subregion (e.g., South Asia, Sub-Saharan Africa) |
| Disaster Group             | Broad disaster classification (e.g., Natural, Technological) |
| Disaster Subgroup          | More specific disaster grouping (e.g., Climatological) |
| Disaster Type              | Type of disaster (e.g., Flood, Drought, Epidemic) |
| Disaster Subtype           | Specific subtype of the disaster (e.g., Flash Flood, Heat Wave) |
| Num_Disasters              | Number of disaster events recorded in that country and year |
| Total_Deaths               | Total number of reported deaths |
| Total_Injured              | Total number of people injured |
| Total_Affected             | Total number of people affected (excluding homeless and injured) |
| Total_Homeless             | Number of people reported homeless due to disasters |
| Combined_Affected          | Sum of affected, homeless, and injured |
| Total_Damage_USD           | Estimated total economic damage (USD) |
| Num_OFDA_BHA_Response      | Number of OFDA/BHA humanitarian responses |
| Num_Appeals                | Number of appeals for international assistance |
| Num_Declarations           | Number of government emergency declarations |
| Avg_Magnitude              | Average magnitude of disasters (where applicable) |
| Common_Magnitude_Scale     | Type of scale used (e.g., Richter, Category) |
| Gov_Effectiveness_Estimate| Estimate from Worldwide Governance Indicators (WGI) |
| Rights_Violation_Risk      | Binary indicator for high rights risk in that context |
| Rights_Risk_Score          | Aggregated human rights risk score (scale varies) |
| Gov_Effectiveness_Imputed | Indicator whether governance estimate was imputed |

---

## 2. `phase1_disaster_data_with_preparedness.csv`

Prepared dataset used for modeling the relationship between disaster severity, governance, and government preparedness classification.

| Variable Name              | Description |
|----------------------------|-------------|
| ISO                        | Country ISO alpha-3 code |
| Country                    | Country name |
| Year                       | Year of observation |
| Region                     | Geographic region |
| Subregion                  | Geographic subregion |
| Disaster Group             | Broad disaster classification |
| Disaster Subgroup          | Subgroup within the disaster group |
| Disaster Type              | Specific disaster type |
| Disaster Subtype           | Specific subtype of the disaster |
| Num_Disasters              | Number of disaster events in the year |
| Total_Deaths               | Total deaths reported |
| Total_Injured              | Total number injured |
| Total_Affected             | Number of people affected |
| Total_Homeless             | Number of people left homeless |
| Combined_Affected          | Combined total of affected, homeless, and injured |
| Total_Damage_USD           | Economic damages in USD |
| Num_OFDA_BHA_Response      | Number of OFDA/BHA humanitarian responses |
| Num_Appeals                | Number of international aid appeals |
| Num_Declarations           | Number of emergency declarations issued |
| Avg_Magnitude              | Average disaster magnitude (if applicable) |
| Common_Magnitude_Scale     | Type of magnitude scale used |
| Gov_Effectiveness_Estimate| Estimate from Worldwide Governance Indicators (WGI) |
| Rights_Violation_Risk      | Binary indicator for high rights risk |
| Rights_Risk_Score          | Score representing human rights risk level |
| Gov_Effectiveness_Imputed | Indicates if governance score was imputed |
| Preparedness_Level         | Final preparedness classification (Prepared, Not Prepared, Somewhat Prepared) |

---

## 3. `preparedness_index_by_country.csv`

Summary-level dataset showing each country’s disaster preparedness classification breakdown and a composite preparedness index score.

| Variable Name         | Description |
|------------------------|-------------|
| Country                | Country name |
| Not Prepared           | Count of years classified as "Not Prepared" |
| Prepared               | Count of years classified as "Prepared" |
| Somewhat Prepared      | Count of years classified as "Somewhat Prepared" |
| Total                  | Total number of years observed for that country |
| Preparedness_Index     | Composite score summarizing preparedness across all years 

---
