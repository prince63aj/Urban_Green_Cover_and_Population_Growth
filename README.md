# 🌳 Urban Green Cover and Population Growth

## 📌 Project Overview

This project investigates the relationship between urban green cover, population growth, and urban expansion across cities worldwide.

The study uses satellite-based vegetation data (NDVI) and population statistics to understand how city greenness changes over time as urban populations grow.

The analysis covers approximately **1,038 cities across 172 countries**, using data from 2010, 2015, 2020, and 2021.

The project uses Python for data cleaning, exploratory data analysis, statistical analysis, data visualization, and geographical comparisons.

---

## 🎯 Problem Statement

Urbanization and population growth are increasing rapidly across the world. As cities expand, understanding how their green cover changes becomes important for sustainable urban development.

This project aims to investigate whether population growth and urban area expansion are associated with changes in urban green cover.

It also explores how geographical regions, climate conditions, and Human Development Index (HDI) levels influence urban greenness.

---

## 🎯 Project Objectives

- Analyze urban green cover using the Normalized Difference Vegetation Index (NDVI).
- Examine population growth across different cities and countries.
- Study changes in NDVI between 2015 and 2020.
- Investigate the relationship between population growth and green cover changes.
- Examine the relationship between urban area growth and green cover changes.
- Compare urban greenness across geographical regions and climate zones.
- Analyze differences in green cover across HDI categories.
- Visualize geographical patterns of urban greenness and population growth.
- Conduct a separate analysis of Indian cities.

---

## 📂 Dataset Information

The project uses a prepared dataset containing information about urban greenness, population, population density, and geographical characteristics.

### Dataset Details

| Attribute | Description |
|---|---|
| Cities | Approximately 1,038 |
| Countries | 172 |
| Time Period | 2010, 2015, 2020, 2021 |
| Green Cover Indicator | NDVI |
| Population Data | Population in thousands |
| Population Density | People per sq. km |
| Land Area | Derived from population and density |

### Data Sources

**1. Green Cover Data**
- City-level NDVI (Normalized Difference Vegetation Index).
- Satellite-based vegetation greenness indicator.
- Years: 2010, 2015, 2020, 2021.

**2. Population and Density Data**
- UN DESA – World Urbanization Prospects 2025.
- Population and population density indicators.

**3. Land Area**
- Derived using population and population density.
- Calculated because the separate UN land-area dataset was not used.

### Dataset Workbook Structure

The Excel dataset contains four sheets:

- `City_Summary_Wide` – City-level summary and growth indicators.
- `City_Year_Long` – City-level observations for individual years.
- `Unmatched_Cities` – Cities that could not be matched with UN population records.
- `Data_Dictionary` – Descriptions of dataset variables.

---

## 🛠️ Technologies & Libraries Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| SciPy | Statistical analysis |
| Jupyter Notebook | Interactive analysis |

---

## 🔍 Project Workflow

### 1. Data Collection and Understanding
- Loaded the prepared Excel dataset.
- Examined dataset dimensions and data types.
- Identified important indicators and their measurement units.

### 2. Data Cleaning and Preparation
- Checked missing values.
- Identified duplicate city-country combinations.
- Standardized city and country labels.
- Matched city records with UN population data.
- Excluded unmatched cities from population-related analysis.
- Prepared a common analysis dataset.

### 3. Data Quality and Assumptions
- Investigated unmatched and ambiguous city records.
- Selected the largest city when multiple UN cities shared the same name in a country.
- Examined the unusual NDVI increase between 2010 and 2015.
- Used 2015–2020 for the main growth analysis to avoid relying on potentially incompatible 2010 observations.

### 4. Exploratory Data Analysis
- Analyzed average NDVI over time.
- Examined average and total population trends.
- Compared greener and less-green cities.
- Calculated population and urban area growth statistics.

### 5. Statistical Analysis
- Applied Spearman rank correlation to examine relationships between:
  - NDVI change and population growth.
  - NDVI change and urban area growth.
- Divided cities into four population growth groups.
- Compared average NDVI changes across these groups.

### 6. Data Visualization
Created different visualizations to understand trends and geographical patterns.

### 7. India-Specific Analysis
- Filtered the dataset to include Indian cities.
- Analyzed population growth against NDVI change.
- Identified geographical differences in urban greenness.

---

## 📊 Visualizations

The project includes the following visualizations:

| No. | Visualization | Purpose |
|---|---|---|
| 1 | Average NDVI Over Time | Examine changes in urban greenness |
| 2 | Average Population Over Time | Analyze population trends |
| 3 | NDVI in Selected Large Cities | Compare city-level greenness |
| 4 | Population Growth vs NDVI Change | Examine their relationship |
| 5 | Urban Area Growth vs NDVI Change | Investigate urban expansion |
| 6 | Regional Comparisons | Compare regions, climate and HDI |
| 7 | NDVI Change by HDI Level | Compare greenness changes across HDI groups |
| 8 | NDVI Geographical Map | Visualize city greenness in 2020 |
| 9 | NDVI Change Map | Visualize greenness changes |
| 10 | Population Growth Map | Visualize population growth geographically |
| 11 | India Population Growth Analysis | Examine Indian cities separately |

All generated charts are saved in the `charts/` directory.

---

## 📈 Key Findings

The analysis produced the following observations:

**1. Urban Green Cover Trends**
- Average NDVI remained approximately 0.28 between 2015 and 2021.
- Around half of the analyzed cities experienced an increase in NDVI, while the other half experienced a decrease between 2015 and 2020.

**2. Population Growth**
- Average city population increased consistently over the observed period.
- Population growth did not show a strong relationship with changes in NDVI.

**3. Urban Expansion**
- The relationship between urban area growth and NDVI change was almost zero.
- Cities with higher urban area growth did not consistently experience a decrease in greenness.

**4. Geographical Differences**
- Climate and geographical regions showed noticeable differences in average city greenness.
- Tropical cities generally showed higher NDVI than arid-region cities.
- Northern America and Europe had higher average NDVI than several other geographical regions.

**5. India-Specific Findings**
- Population growth and NDVI change were not significantly related among the analyzed Indian cities.
- Cities in Kerala and other greener geographical areas showed higher NDVI.
- Several cities in western and central India showed comparatively lower NDVI.

---

## 💡 Conclusion

The analysis suggests that increasing urban population does not necessarily result in a measurable decline in urban green cover.

Across approximately 950 matched and usable cities, average NDVI remained relatively stable between 2015 and 2021, even as average population increased.

Statistical analysis also found very weak relationships between NDVI change and both population growth and urban area growth.

Geographical region and climate appeared more strongly associated with differences in the level of urban greenness.

However, these findings do not establish causation. A more detailed study using measured green-space area, consistent city boundaries, within-city observations, and longer time-series data would help provide a clearer understanding of urban expansion and green cover.

---

## ▶️ How to Run This Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/prince63aj/Urban_Green_Cover_and_Population_Growth
```

### Step 2: Navigate to the Project Directory

```bash
cd Urban-Green-Cover-and-Population-Growth
```

### Step 3: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scipy openpyxl jupyter
```

### Step 4: Add the Dataset

Place the Excel dataset in the same directory as the notebook.

The notebook expects the following filename:

```text
Urban_Green_Cover_Final_Dataset.xlsx
```

### Step 5: Open Jupyter Notebook

```bash
jupyter notebook
```

Open `Analysis(1).ipynb` and run the cells sequentially.

The notebook automatically creates a `charts` directory to save the generated visualizations.

---

## 📁 Project Structure

```text
Urban-Green-Cover-and-Population-Growth/
│
├── Analysis(1).ipynb
│
├── Urban_Green_Cover_Final_Dataset.xlsx
│
├── charts/
│   ├── 1_ndvi_over_time.png
│   ├── 2_population_over_time.png
│   ├── 3_big_cities_ndvi.png
│   ├── 4_pop_growth_vs_ndvi_change.png
│   ├── 5_area_growth_vs_ndvi_change.png
│   ├── 6_Major_Geo_Region.png
│   ├── 6_HDI_level.png
│   ├── 6_Climate_region.png
│   ├── 7_ndvi_change_by_hdi.png
│   ├── map1_ndvi_2020.png
│   ├── map2_ndvi_change.png
│   ├── map3_pop_growth.png
│   └── india_pop_growth_vs_ndvi_change.png
│
└── README.md
```

---

## ⚠️ Limitations

- NDVI represents satellite-observed vegetation greenness and is not a direct measurement of green-space area.
- City boundaries differ between the NDVI and UN datasets.
- Some cities could not be matched with UN population records.
- Land area is derived from population and population density.
- The 2010 NDVI observations may not be directly comparable with later years due to possible satellite or methodological differences.
- Population statistics represent city-level averages and do not capture differences within individual cities.
- Correlation does not establish a causal relationship between urban growth and green cover.

---

## 👨‍💻 Project Type

**Domain:** Data Analytics / Exploratory Data Analysis

**Programming Language:** Python

**Tools:** Jupyter Notebook, VS Code

**Project Focus:** Urban Sustainability, Population Growth, Green Cover Analysis and Data Visualization

---

⭐ If you find this project useful, consider giving the repository a star!
