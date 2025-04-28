# Data

This folder contains all datasets used for the thesis analysis. It is divided into two subfolders:

---

## `raw/`

This subfolder includes original data files as obtained from external sources without any modification. These include:

- Disaster event records from [EM-DAT](https://www.emdat.be/)
- Governance indicators from the [World Bank WGI](https://info.worldbank.org/governance/wgi/)

Each dataset in this folder retains its original structure and serves as the starting point for data cleaning.

---

## `preprocessed/`

This subfolder contains cleaned and merged datasets that are ready for analysis. These files have been:

- Filtered for relevant time frames (e.g., 2000–2023)
- Joined across sources (e.g., EM-DAT + WGI)
- Enhanced with:
  - Preparedness classifications
  - Human rights mappings

These files serve as direct inputs for the Jupyter notebooks and exported figures/tables.

---
