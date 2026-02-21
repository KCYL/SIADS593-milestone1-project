# Pre-Covid Analysis of Zoonotic Outbreaks and Global Production  
#### *This project examines relationships between agricultural/livestock output and zoonotic disease outbreaks from 2015-2019.*

By [Blythe Weng](https://github.com/blythe1215), [Tahreem Karim](https://github.com/TahreemK13), and [Che-Yu Liu (Kevin)](https://github.com/KCYL) 


## Overview

We explore whether **country level agricultural and livestock production patterns** are associated with the occurrence of zoonotic disease outbreaks. By combining production statistics with outbreak records, our analysis investigates potential relationships (if any) that may help characterize/contextualize zoonotic outbreaks, before Covid 19 changed everything.

This is a portfolio project for the Master's of Applied Data Science ([MADS](https://www.si.umich.edu/programs/master-applied-data-science)) program at the University of Michigan, Ann Arbor. Course: SIADS 593 Milestone 1 ([syllabus](https://www.si.umich.edu/sites/default/files/inline-files/2023.Winter_%20SIADS%20593%20Syllabus.pdf)).


## Project Slides

[![Zoonotic Outbreaks – Slide Preview](figures/slide_preview.png)](slides/Zoonotic_Outbreaks.pdf)

*Click the image to view the full presentation (PDF) on GitHub.*


## Motivations

Zoonotic diseases — illnesses transmitted between animals and humans — pose significant public health, economic, and ecological challenges. Events such as avian influenza, Ebola, and COVID-19 highlight the importance of understanding upstream risk factors. This project asks whether agricultural and livestock production indicators show meaningful associations with reported zoonotic outbreaks across countries.





## Data Summary

**Primary data sources include:**
- Country-level agricultural and livestock production data
- Country-level zoonotic outbreak records

**Dataset characteristics:**
- Multiple years of observations per country
- Production quantities for major livestock and agricultural goods
- Counts and classifications of zoonotic outbreaks

Each row represents a country-year observation, enabling cross-country comparison and exploratory modeling.



## Analysis Workflow

1. **Data cleaning and preprocessing**
   - Standardized country names and regions
   - Aggregated production values across years
   - Addressed missing and inconsistent records

2. **Exploratory analysis**
   - Distributional analysis of production outputs
   - Visualization of outbreak frequency by country and region

3. **Modeling and inference**
   - Simple regression and correlation analyses
   - Examination of associations between production intensity and outbreak frequency

4. **Interpretation**
   - Assessment of patterns, uncertainty, and potential confounders



## Key Findings

- Certain livestock and agricultural products appear frequently in countries with higher reported zoonotic outbreak counts
- Associations vary substantially by region and product category
- Results suggest correlation rather than causation and are sensitive to reporting practices and data aggregation choices

These findings are exploratory and intended to support discussion rather than definitive causal claims.



## Notebooks & Reproducibility

The analysis is organized into Jupyter notebooks:

- `01_exploration.ipynb` — data inspection and initial visualizations  
- `02_modeling.ipynb` — regression and statistical analysis  
- `03_visualizations.ipynb` — summary charts and figures  

> **Note:** Some visualizations do not render inline on GitHub due to notebook rendering limitations. For full interactivity, download the notebooks and run them locally in JupyterLab or VS Code. 



## How to Run Locally

```bash
git clone https://github.com/KCYL/SIADS593-milestone1-project.git
cd SIADS593-milestone1-project
jupyter lab
```

[Download Zoonotic Outbreaks and Trade Slides_PDF](https://github.com/user-attachments/files/25432428/18-bweng-tahreemk-cheyuliu2026winter.pdf) 


Preview below:

[![Project slides preview](figures/slides_preview.png)](slides/Zoonotic_Outbreaks.pdf)
<img width="1440" height="900" alt="Screenshot 2026-02-19 at 8 05 03 PM" src="https://github.com/user-attachments/assets/d9f0d38a-fa3e-49cf-883e-5e514d138a3a" />
