# Notebooks

This folder contains the **core analysis notebooks** for the thesis project:  

The notebooks are divided thematically to reflect different stages of the research and modeling process.

---

## Notebook Overview

### 1. `THESIS_Government_Preparedness_Analysis.ipynb`

This notebook performs the classification and evaluation of government disaster preparedness from 2000 to 2023. Key tasks include:

- Data preprocessing and log transformations of disaster severity indicators (e.g., deaths, injuries, homelessness, affected populations)
- Rule-based preparedness scoring model using thresholds and international response triggers
- Classification of disaster events into **Prepared**, **Somewhat Prepared**, or **Not Prepared**
- Aggregation and visualization of preparedness trends by:
  - Country, region, subregion, and year
  - Disaster type and subtype
- Choropleth maps of the **Global Preparedness Index**
- Export of classification results and summary tables

---

### 2. `THESIS_Human_Rights_Protection_Analysis.ipynb`

This notebook explores the human rights impacts of disaster events and how they relate to government preparedness. Key tasks include:

- Mapping disaster subtypes to specific human rights (e.g., right to water, shelter, life, aid, health, food, education, and healthy environment)
- Exploding multi-right events for disaggregated analysis
- Heatmaps of rights impacted by subregion and disaster type
- Clustering of countries by disaster-specific preparedness profiles using **KMeans**
- Regression analysis (OLS) to test whether higher preparedness scores predict fewer rights violations
- Export of normalized metrics: rights per disaster, average preparedness per country

---

## Reproducibility Notes

- All visualizations (figures) and outputs (tables) are exported to the `/outputs/figures` and `/outputs/tables` folders respectively.
- The notebooks rely on data from the `/data/preprocessed/` folder and write outputs used in the final thesis.

---

## Suggested Execution Order

1. Run `THESIS_Government_Preparedness_Analysis.ipynb` first to prepare the classified dataset and all preparedness metrics.
2. Then run `THESIS_Human_Rights_Protection_Analysis.ipynb` for the rights analysis, clustering, and regression steps.

---
