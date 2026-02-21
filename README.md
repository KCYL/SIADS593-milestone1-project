# Pre-Covid Analysis of Zoonotic Outbreaks and Global Production  
#### *This project examines relationships between agricultural/livestock output and zoonotic disease outbreaks from 2015-2019.*

By [Blythe Weng](https://github.com/blythe1215), [Tahreem Karim](https://github.com/TahreemK13), and [Che-Yu Liu (Kevin)](https://github.com/KCYL) 


## Overview

We explore whether **country level agricultural and livestock production patterns** are associated with the occurrence of zoonotic disease outbreaks. By combining production statistics with case records, our analysis explores the data to uncover any patterns that may aid epidimeological characterizations of zoonotic outbreaks, before Covid 19 changed everything.

This is a portfolio project for the Master's of Applied Data Science ([MADS](https://www.si.umich.edu/programs/master-applied-data-science)) program at the **University of Michigan, Ann Arbor**.\
Course: SIADS 593 Milestone 1 ([syllabus](https://www.si.umich.edu/sites/default/files/inline-files/2023.Winter_%20SIADS%20593%20Syllabus.pdf)). Go Blue!

## Title Slide
*Click image to view full presentation on GitHub or [download here](https://github.com/user-attachments/files/25432428/18-bweng-tahreemk-cheyuliu2026winter.pdf) in PDF.*

<a href="slides/Zoonotic_Outbreaks_and_Trade_Slides.pdf">
  <img
    width="900"
    alt="Zoonotic Outbreaks – Slide Preview"
    src="https://github.com/user-attachments/assets/d9f0d38a-fa3e-49cf-883e-5e514d138a3a"
  />
</a>

[cdc.gov](www.cdc.gov/) (link from slide, above) 

---



## Data Summary

**Primary data sources include:**
- [`WAHIS15-19.csv`](data/WAHIS15-19.csv)
  - "Crops and livestock products" [dataset](https://www.fao.org/faostat/en/#data/QCL) from [FAOSTAT](https://www.fao.org/faostat/).\
    Provided by the Food and Agriculture Organization of the United Nations ([FAO](https://www.fao.org/home/)). 
- [`Production_Crops_Livestock_E_All_Data_NOFLAG`](figures/Production_Crops_Livestock_E_All_Data_NOFLAG.csv)
  - Country level zoonotic outbreak records from the World Animal Health Information System ([WAHIS](https://www.woah.org/en/what-we-do/animal-health-and-welfare/disease-data-collection/world-animal-health-information-system/)).\
    Provided by the World Organisation for Animal Health ([WOAH](https://www.woah.org/)).
> Each dataset is provided as a CSV in the `data` folder but may be too large to **preview** on GitHub. It can be downloaded along with the Jupyter notebook `annotPythonNtbk.ipynb` for reproduction. 

**Dataset characteristics (pre-cleaning):**
- Multiple years (2015-2019) of observations per country
- Production volumes and value for major livestock and agricultural goods
- Counts of zoonotic cases by outbreaks per country

The rows represent country/year data points, enabling cross referencing via country. Both datasets were merged, then cleaned for each **exploratory visualization**. Finally, the top 25 goods of each country & their zoonotic cases were extracted from the merged dataset and a **linear regression** was run to check for correlation. *More detailed explanations can be found in the slideshow linked above*. 




## Workflow

1. **Data processing**
   - Standardized country names and split regions between datasets. Ultimately, a **merged dataframe** was produced. 
   All outputs were sourced from this.
   - Averaged zoonotic cases across years for Lollipop graph (2nd exploratory visualization).
   - Aggregated production values across years and broken in two three groups corresponding to frequency, for regression & accompanying visuals.

2. **Exploratory analysis w/ Altair**
   - [`heatmapZoonbyCountry`](/figures/heatmapZoonbyCountry.png) - Heatmap of Zoonotic cases by Country and Year: shows trends and outliers in case numbers.
   - [`lollipopZoonCountryAvg`](figures/lollipopZoonCountryAvg.png) - Lollipop Graph: top 10 countries reporting Zoonotic cases, averaged for 2015-2019.

4. **Modeling and inference**
   - Simple regression and correlation analysis examining associations between production intensity and outbreak frequency.
   - [`corrMatrixProdTiersZoonCases`](/figures/corrMatrixProdTiersZoonCases.png) - Correlation Matrix of zoonotic cases and three groups of products, representing the frequency w/ which they are found in the top 25 goods produced by each country (represented in **both** datasets). 

---

## Key Findings

- *The correlation btw zoonotic cases and goods produced during 2015 - 2019 is **very weak**. However, the least frequently produced goods do have a significantly higher correlation than the most frequently produced goods per country.*
- There are two significant outliers when it comes to case numbers.
  - **Egypt** had the most cases by far, with an average of ~forty thousand reported per year. This can be seen in `heatmapZoonbyCountry` and `lollipopZoonCountryAvg` located in the`figures` folder.
    - Preliminary research attributes this to Salmonellosis and Campylobacteriosis: \
    "Another study in Egypt detected higher rates of Salmonella at 60% (37/62) and 64% (14/20) in chicken parts and skin, respectively, whereas none of the tested table eggs samples (n = 60) were positive for Salmonella" \
    [Current State of Salmonella, Campylobacter and Listeria in the Food Chain across the Arab Countries: A Descriptive Review](https://pmc.ncbi.nlm.nih.gov/articles/PMC8535026/)

  - **Poland** had an outbreak in 2019. This can also be attributed to Salmonellosis. \
    [Salmonellosis in Poland in 2018 and 2019](https://pubmed.ncbi.nlm.nih.gov/35543609/)
- These findings are exploratory.



## Notebooks & Reproducibility

The analysis was created w/ [Jupyter](https://jupyter.org/) notebooks:

- `annotPythonNtbk` — data inspection and initial visualizations with Python & [Vega-Altair](https://altair-viz.github.io/). 
- Part 2 of `annotPythonNtbk` — regression, statistical analysis, and summary charts. 

1. Download CSV files from `data`.
2. Download `annotPythonNtbk`.
3. Upload `annotPythonNtbk.ipynb`, `WAHIS15-19.csv`, & `Production_Crops_Livestock_E_All_Data_NOFLAG.csv` \
   to **any notebook tool w/ Python**.
5. Run all cells and enjoy. Please reach out for thoughts and/or improvements!

> **Note:** The notebook visualizations do not render inline on GitHub due to rendering limitations. For full interactivity, download the notebooks and run them locally in JupyterLab or VS Code. Otherwise, static verisions are available in `figures`.



## How to Run Locally via Terminal

```bash
git clone https://github.com/KCYL/SIADS593-milestone1-project.git
cd SIADS593-milestone1-project
jupyter lab
```

