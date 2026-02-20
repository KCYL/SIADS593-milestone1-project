# Zoonotic Outbreaks and Agricultural Production Analysis  
###*Examining relationships between livestock and crop production and zoonotic disease outbreaks across countries*
By [Blythe Weng](https://github.com/blythe1215), [Tahreem Karim](https://github.com/TahreemK13), and [Che-Yu Liu (Kevin)](https://github.com/KCYL) 

**Note** that the Visualizations in the notebooks don't show up unless the notebook is downloaded then re-uploaded to Jupyter Labs due to an issue with rendering on GitHub.

---

## 📌 Overview

This project explores whether country-level agricultural and livestock production patterns are associated with the occurrence of zoonotic disease outbreaks. By combining production statistics with outbreak records, the analysis investigates potential structural relationships that may help contextualize global health risks tied to agriculture.

---

## 🧠 Motivation

Zoonotic diseases — illnesses transmitted between animals and humans — pose significant public health, economic, and ecological challenges. Events such as avian influenza, Ebola, and COVID-19 highlight the importance of understanding upstream risk factors. This project asks whether agricultural and livestock production indicators show meaningful associations with reported zoonotic outbreaks across countries.

---

## 📊 Data Summary

**Primary data sources include:**
- Country-level agricultural and livestock production data
- Country-level zoonotic outbreak records

**Dataset characteristics:**
- Multiple years of observations per country
- Production quantities for major livestock and agricultural goods
- Counts and classifications of zoonotic outbreaks

Each row represents a country-year observation, enabling cross-country comparison and exploratory modeling.

---

## 🔍 Analysis Workflow

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

---

## 📈 Key Findings

- Certain livestock and agricultural products appear frequently in countries with higher reported zoonotic outbreak counts
- Associations vary substantially by region and product category
- Results suggest correlation rather than causation and are sensitive to reporting practices and data aggregation choices

These findings are exploratory and intended to support discussion rather than definitive causal claims.

---

## 📂 Notebooks & Reproducibility

The analysis is organized into Jupyter notebooks:

- `01_exploration.ipynb` — data inspection and initial visualizations  
- `02_modeling.ipynb` — regression and statistical analysis  
- `03_visualizations.ipynb` — summary charts and figures  

> **Note:** Some visualizations do not render inline on GitHub due to notebook rendering limitations. For full interactivity, download the notebooks and run them locally in JupyterLab or VS Code.

---

## 🚀 How to Run Locally

```bash
git clone https://github.com/KCYL/SIADS593-milestone1-project.git
cd SIADS593-milestone1-project
jupyter lab

[Download Zoonotic Outbreaks and Trade Slides_PDF](https://github.com/user-attachments/files/25432428/18-bweng-tahreemk-cheyuliu2026winter.pdf)
<img width="1440" height="900" alt="Screenshot 2026-02-19 at 8 05 03 PM" src="https://github.com/user-attachments/assets/d9f0d38a-fa3e-49cf-883e-5e514d138a3a" />
