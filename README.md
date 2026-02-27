# 🌍 Conservation Funding Optimization in Africa  
---

## 📌 Project Overview

This project analyzes biodiversity records, conservation funding data, and geospatial biodiversity intactness metrics across African countries to evaluate whether conservation funding is aligned with ecological value.

Using Python-based data analysis and geospatial techniques, the project identifies funding inefficiencies and highlights under-supported biodiversity-rich regions.

---

## 🎯 Problem Statement

Conservation funding across Africa is unevenly distributed.

This project answers the following questions:

- Are biodiversity-rich countries receiving adequate funding?
- Does conservation funding align with biodiversity intactness?
- Which countries should be prioritized for future funding allocation?

---

## 🗂️ Dataset Description

The analysis integrates three primary datasets:

### 1️⃣ Biodiversity Dataset
- 11 Excel sheets combined into one dataset
- 1,930 species records after cleaning
- Species categorized as **Plant** or **Mammal**
- 53 African countries represented

### 2️⃣ Conservation Funding Dataset
- Funding values in **Million USD**
- 53 country-level records
- Missing values handled
- Negative outliers corrected

### 3️⃣ Biodiversity Intactness Index (BII)
- Raster dataset
- Country-level mean extracted using zonal statistics
- CRS: WGS 1984
- Index range: `0.116 – 0.995`
- Africa-wide mean: `0.756`

---

## 🛠️ Technical Approach

### Data Cleaning & Preparation

- Merged 11 biodiversity sheets into one DataFrame
- Removed duplicate species records
- Standardized country names using fuzzy string matching (FuzzyWuzzy)
- Handled:
  - Missing funding values
  - Negative funding outliers
  - Inconsistent naming (e.g., Ivory Coast → Côte d'Ivoire)
- Merged datasets with African country shapefile
- Renamed shapefile columns for consistency

### Feature Engineering

Generated country-level metrics:
- Species count
- Species type count
- Mean Biodiversity Intactness Index
- Total conservation funding

### Geospatial Analysis

- Performed zonal statistics (mean) on raster dataset
- Created choropleth maps for:
  - Biodiversity count
  - Conservation funding
  - Biodiversity intactness index
- Identified geographic mismatches between funding and biodiversity

---

## 📊 Key Insights

### 🔎 Funding Distribution
- Mean funding: **$8.34M**
- Right-skewed distribution
- Few countries receive disproportionately high funding

---

### 🌱 High Biodiversity, Low Funding Countries

| Country   | Species Count | Funding (M USD) |
|------------|--------------|-----------------|
| Ethiopia   | 70           | 4.01            |
| Zimbabwe   | 60           | 4.07            |
| Tunisia    | 59           | 0.00            |
| Uganda     | 58           | 2.86            |
| Nigeria    | 57           | 2.64            |

➡ Indicates underinvestment in biodiversity-dense regions.

---

### 🌿 High Biodiversity Intactness, Low Funding

| Country      | BII   | Funding (M USD) |
|--------------|--------|-----------------|
| Namibia      | 0.871 | 1.52            |
| Eritrea      | 0.807 | 0.88            |
| South Sudan  | High  | Low             |

➡ Ecologically stable countries may lack adequate financial protection.

---

## 🗺️ Visualizations

The project includes:

- Funding distribution histogram
- Top & bottom countries by species count
- Top & bottom countries by funding
- Africa biodiversity choropleth map
- Africa conservation funding map
- Africa biodiversity intactness map
- Priority country comparison tables

---

## 🧠 Conclusions

- Conservation funding does not consistently align with biodiversity richness or intactness.
- Several biodiversity-rich countries receive low financial support.
- Funding distribution is heavily skewed toward a few countries.
- Preventative investment in high-BII countries may reduce future biodiversity loss.

---

## 💡 Recommendations

- Reassess funding allocation thresholds based on biodiversity metrics.
- Improve country-level data consistency (e.g., Congo vs DR Congo distinction).
- Collect missing biodiversity and funding data for Western Sahara.
- Apply predictive modeling to identify biodiversity loss risk.
- Develop an optimization framework for funding allocation.

---

## 💻 Tech Stack

### Programming
- Python

### Data Analysis
- Pandas
- NumPy
- Pandas Profiling

### Geospatial Analysis
- GeoPandas
- Rasterio
- Zonal Statistics
- Shapefile integration

### Visualization
- Matplotlib

### Environment
- Jupyter Notebook

---


