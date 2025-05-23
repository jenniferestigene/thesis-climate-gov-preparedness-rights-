# Climate Disasters, Government Preparedness & Human Rights Impacts

**MSc Data Science for Public Policy at the Hertie School, Class of 2025**  
**Author:** Jennifer Estigene  

---

## Overview

This thesis investigates the intersection between **climate-related disasters**, **government preparedness**, and **human rights impacts** using data science methods. It explores how well governments respond to natural disasters and how these responses affect fundamental rights such as the **right to shelter, health, water, food, education, life, access to aid, and a healthy environment**.

The thesis builds a preparedness scoring framework and evaluates climate disaster events globally to classify state responses, identify risk patterns, and highlight regional vulnerabilities.

---

## Research Question

> **How effectively do governments protect fundamental human rights in climate disaster-prone regions, and how can data science models assess and improve state preparedness?**

---

## Methods

- **Data Sources:**
  - [EM-DAT: International Disaster Database](https://www.emdat.be/)
  - [World Bank Worldwide Governance Indicators (WGI)](https://info.worldbank.org/governance/wgi/)
  - Custom mapping of disaster subtypes to human rights

### Analytical Steps

1. **Government Preparedness Classification**  
   - Developed a multi-tier scoring system using log-transformed thresholds for:
     - Total deaths
     - Total injuries
     - Total homelessness
     - Total affected population  
   - Integrated binary signals of state stress or failure:  
     - Presence of international appeal, declaration of emergency, and foreign response (OFDA/BHA)
   - Used a rule-based classification to categorize each event as:
     - **Prepared**, **Somewhat Prepared**, or **Not Prepared**

2. **Human Rights Impact Mapping**  
   - Designed a custom framework mapping disaster subtypes (e.g., flood, drought, earthquake) to specific human rights risks (e.g., right to shelter, food, water, health).
   - Applied this mapping programmatically to all disaster events to generate rights impact labels.
   - Exploded and analyzed rights impacts at the event level.

3. **Clustering of Countries**  
   - Created country-level preparedness vectors by disaster type.
   - Normalized the dataset using `StandardScaler`.
   - Applied **KMeans clustering** to group countries into 4 preparedness profiles.
   - Visualized clusters using:
     - Scatterplots (e.g., Flood vs Earthquake Preparedness)
     - Country-cluster assignments

4. **Trend and Distribution Analysis**  
   - Analyzed preparedness scores by:
     - Country, subregion, region, global group (Global North/South)
     - Disaster type and subtype
     - Year (2000–2023)
   - Calculated distribution of preparedness levels over time, normalized by year.

5. **Geospatial and Visual Mapping**  
   - Built **choropleth maps** to display:
     - Global preparedness index
     - Total rights violations per country
   - Constructed **stacked bar charts** and **boxplots** for:
     - Preparedness by subregion
     - Top countries’ performance
     - Regional variation in rights risk
   - Created **heatmaps** for:
     - Rights impacted by disaster type
     - Subregion-disaster-right intersections

6. **Normalization and Comparative Scoring**  
   - Computed:
     - **Rights impacted per disaster** by country
     - **Average preparedness score** (mapped: 0 = Not Prepared, 2 = Fully Prepared)
   - Merged metrics to compare frequency of disaster events, rights impacts, and preparedness performance at the country level.

---

### Key Techniques and Models

- **Data Wrangling and Cleaning:**
  - `pandas`, `numpy`, `re`, `string` operations
  - Log transformations for severity-based indicators

- **Preparedness Scoring Model:**
  - Rule-based scoring incorporating:
    - Severity (log thresholds)
    - Binary international response indicators
    - Human rights risk score
  - Classification into 3 preparedness levels

- **Human Rights Mapping Framework:**
  - Custom dictionary-based mapping of disaster subtypes to 8 rights:
    - Right to Life, Shelter, Water, Food, Health, Aid, Education, Healthy Environment

- **Unsupervised Learning:**
  - **KMeans Clustering** (with elbow method for optimal K)
    - Applied to normalized preparedness vectors
    - Used to uncover cross-country patterns in disaster-specific readiness

- **Regression Analysis:**
  - **Ordinary Least Squares (OLS)** regression to explore:
    - The relationship between **average preparedness scores** and **human rights impacts per disaster**
    - Whether better preparedness predicts fewer rights violations
  - Included control variables such as:
    - Disaster frequency
    - Event severity
  - Interpreted coefficients to assess statistical significance and direction of effects

- **Geospatial Visualization:**
  - `plotly.express` choropleth maps for global overviews
  - Country-level and subregion-level scoring with dynamic hover metrics

- **Time Series & Proportion Analysis:**
  - Year-by-year preparedness level trends (stacked line plots)
  - Event-level normalization (e.g., % Not Prepared per subregion or disaster type)
  - Rights-per-disaster normalization to compare countries on risk per event

- **Advanced Visualization Tools:**
  - `matplotlib`, `seaborn`, `plotly`
  - Annotated heatmaps, exploded bar charts, and cross-tab visualizations

---

##  Results Summary

This thesis presents a global, data-driven assessment of how effectively governments protect human rights during climate-related disasters. Covering over two decades (2000–2023), the study applies a classification framework, geospatial analysis, and regression models to evaluate government preparedness and its relationship to disaster outcomes and rights risks.

This thesis focuses on eight fundamental human rights most at risk during climate-related disasters: the right to life, right to shelter, right to health, right to water, right to food, right to aid, right to education, and the right to a healthy environment.

### Key Findings

- **Over half of all disasters (52.1%)** were classified as “Prepared,” while **15.8%** were categorized as “Not Prepared.” However, preparedness levels varied dramatically by region and disaster type.

- **Floods and earthquakes** were the most frequently well-managed disaster types. In contrast, **droughts and extreme temperatures** showed the highest rates of under-preparedness, highlighting major institutional gaps for slow-onset and climate-driven hazards.

- **Sub-Saharan Africa and South Asia** recorded the highest frequencies of "Not Prepared" events, while Europe, Oceania, and parts of the Americas showed stronger preparedness overall.

- **Human rights violations were widespread**:  
  - Over **88% of disaster events** were associated with high-risk rights impacts.  
  - The most frequently threatened rights were the **right to health, shelter, life, water, and aid**.  
  - Disasters in Africa, Asia, and Latin America accounted for the majority of violations.

- **Even high-preparedness countries (e.g., USA, China, India)** experienced substantial rights violations — suggesting that preparedness alone does not ensure rights protection and that structural, governance, and contextual factors also play critical roles.

- **Regression models** showed:
  - A statistically significant relationship between preparedness and human rights outcomes — but not always in the expected direction.
  - In some regions, **higher preparedness scores were associated with more rights impacts**, possibly reflecting:
    - Reporting bias
    - Structural disaster intensity
    - Gaps between institutional readiness and actual protection delivery

- **Governance effectiveness was a key moderator**:  
  Countries with lower governance scores were consistently less prepared and more rights-vulnerable. Europe was the only region where preparedness was reliably associated with fewer rights violations.

### Conclusion

Preparedness reduces disaster severity but is not sufficient to protect rights. Institutional capacity, governance quality, disaster type, and regional context all shape whether governments can fulfill their obligations to protect life, shelter, health, and dignity during climate emergencies. The thesis introduces a scalable classification model and rights-risk framework that can inform global monitoring and policy reform.

---

## Repository Structure

This repository is organized to clearly separate raw data, analysis workflows, and generated outputs for a transparent and fully reproducible thesis project.

- The **`data/`** folder contains all datasets used in the thesis. It is divided into two subfolders:
  - `raw/`: This folder stores original datasets, such as EM-DAT disaster records and World Bank governance indicators, as downloaded or acquired.
  - `preprocessed/`: This includes cleaned, merged, and structured data ready for analysis — such as disaster events with severity measures, assigned preparedness levels, and mapped human rights impacts.

- The **`notebooks/`** folder houses the core analytical workflow files:
  - Jupyter Notebooks (`.ipynb`) are used for data exploration, classification modeling, visualization, and clustering.
    - `THESIS_Government_Preparedness_Analysis.ipynb` focuses on scoring disaster events and classifying country preparedness.
    - `THESIS_Human_Rights_Protection_Analysis.ipynb` performs human rights mapping, clustering, and regression.
  - R Markdown (`.Rmd`) file used for data cleaning and additional analysis using R.

- The **`outputs/`** folder includes all files generated from the analysis and is structured into:
  - `figures/`: Contains all final visualizations, such as choropleth maps, boxplots, charts, and heatmaps.
  - `tables/`: Contains all CSV and txt files with summary statistics, classification results, rights violations, and other exported tables used in the thesis.

- The **`scripts/`** folder is for Python code from the notebooks.

This structure reflects the full research pipeline — from raw inputs to final outputs — and supports transparency, modularity, and reproducibility throughout the thesis project.

---
## How to Reproduce

This repository is fully reproducible and structured for modular execution. To run the analysis locally, follow these steps:

### 1. Clone the Repository
```bash
git clone https://github.com/jenniferestigene/thesis-climate-gov-preparedness-rights-.git
cd thesis-climate-gov-preparedness-rights-
```

### 2. Set Up the Python Environment
Install required packages using:
```bash
pip install -r requirements.txt
```

> Python version used: 3.10+  
> Ensure you have `jupyter` for working with the notebooks.

---

### 3. Add Data Files

Place your data files in the following locations:

- Raw EM-DAT and WGI files → `data/raw/`
- Cleaned and merged data → `data/preprocessed/`

Refer to the `/data/README.md` file for a detailed description of the expected datasets and formats.

---

### 4. Run the Analysis Notebooks

In this order:

1. `notebooks/THESIS_Government_Preparedness_Analysis.ipynb`  
   - Classifies disaster events into preparedness levels  
   - Exports metrics by country, region, year, and disaster type

2. `notebooks/THESIS_Human_Rights_Protection_Analysis.ipynb`  
   - Maps disaster subtypes to human rights  
   - Explodes multi-right events  
   - Applies clustering and performs regression  
   - Generates heatmaps and normalized outputs

---

### 5. Outputs

All generated outputs will be saved automatically to:

- `outputs/figures/` → All maps, charts, and visualizations
- `outputs/tables/` → All exported tables (classification, clustering, regression-ready data)

---

> For help interpreting results, see the “Results Summary” in the main `README.md`.
