# Water Pollution Disease Analysis
### Global Study of Water Pollution & Waterborne Disease Burden | Excel | Python | Power BI

## Project Summary
An end-to-end analysis of the relationship between water pollution and waterborne disease prevalence across 10 countries spanning 26 years (2000–2025). Using a multi-tool pipeline of Excel,Python, and Power BI, this project identifies patterns, disparities, and trends in global disease burden and evaluates whether pollution, water quality, and socio-economic factors predict health outcomes.

**Key finding: Every single country in the dataset is classified as High Risk. Disease burden has shown no meaningful improvement over 25 years of global monitoring.**

## Dataset Overview
| Field | Detail |
|---|---|
| **Records** | 3,000 unique entries |
| **Countries** | 10 (USA, India, China, Brazil, Nigeria, Bangladesh, Mexico, Indonesia, Pakistan, Ethiopia) |
| **Regions** | 5 per country (North, South, East, West, Central) |
| **Period** | 2000 — 2025 |
| **Columns** | 24 original + 9 engineered |
| **Source** | Water Pollution Disease Dataset (Kaggle) |

## Key Columns in the Dataset
| Column | Description |
|---|---|
| **Country / Region / Year** | Geographic and temporal identifiers |
| **Water_Source** | Lake, Pond, River, Spring, Tap, Well |
| **Contaminant_Level / pH_Level / Turbidity** | Water quality indicators |
| **Dissolved_Oxygen / Nitrate_Level / Lead_Concentration** | Chemical composition |
| **Bacteria_Count** | Microbial contamination measure |
| **Water_Treatment_Method** | Boiling, Chlorination, Filtration, Unknown |
| **Clean_Water_Access_Rate** | % population with clean water access |
| **Diarrhea_Rate / Cholera_Rate / Typhoid_Rate** | Disease prevalence rates |
| **Infant_Mortality_Rate** | Health outcome indicator |
| **GDP_per_Capita / Healthcare_Index** | Socio-economic variables |
| **Urbanization_Rate / Sanitation_Rate** | Infrastructure indicators |
| **Rainfall / Temperature / Population_Density** | Environmental variables |

## Tools Used
| Tool | Purpose | Stage |
|---|---|---|
| **Microsoft Excel** | Data profiling, cleaning, initial feature engineering | Stage 1 |
| **Python (pandas, numpy, matplotlib, seaborn)** | EDA, advanced feature engineering, visualisation | Stage 2 |
| **Microsoft Power BI** | Data modelling, DAX measures, dashboard | Stage 3 |
| **DAX** | Custom KPI measures and aggregations | Stage 3 |

## Data Cleaning & Preparation
**Excel:**
- Verified 3,000 rows and 24 columns with zero missing values
- Confirmed zero duplicate records
- Engineered 5 calculated columns:
  - **`Total_Disease_Burden`** — Diarrhea + Cholera + Typhoid rates combined
  - **`Clean_Water_Gap`** — % population without clean water access
  - **`Pollution_Index`** — Overall pollution composite measure
  - **`Disease_per_Pollution`** — Disease burden relative to pollution
  - **`Risk_Level`** — Low / Medium / High classification
![image descriptin](https://github.com/afodunrinbikunmi-data/Water_Pollution_Disease_Analysis/blob/main/water%20pollution%20excel.PNG)

## Data Engineering (Power Query)
The project follows a three-stage analytical pipeline - Excel for initial cleaning and feature engineering, Python for EDA and advanced feature creation, Power BI for modelling and visualisation. The final enriched dataset containing all 24 original columns plus 9 engineered features was exported from Python and loaded into Power BI as a single flat table. 

## Data Modeling
No relational joins or data model relationships were required. Seven DAX measures were created in a dedicated measures table: 
- **Avg Disease Burden**
- **Avg Health Risk Index**
- **Avg Clean Water Access**
- **Avg Pollution Index**
- **Avg Water Quality Score**
- **Avg Sanitation Rate**
- **Avg Healthcare Index**

**Python:**
- Conducted full EDA including country, regional, pollution and trend analysis
- Engineered 4 advanced features:
  - **`Health_Risk_Index`** — Disease burden + pollution + healthcare composite
  - **`Water_Quality_Score`** — Aggregated water quality measure
  - **`Risk_Level_Advanced`** — Advanced risk categorisation
  - **`Log_Pollution`** — Log-transformed pollution for normalized analysis
![image description]()
- **Generated visualisations**: bar chart, line trend, boxplot, scatter plot
![image description](https://github.com/afodunrinbikunmi-data/Water_Pollution_Disease_Analysis/blob/main/python%20eda%20water%20pollution%20analysis.png)


## Key Questions & Analysis
1. Which countries carry the highest average disease burden?
2. Which regions show the most severe disease and pollution levels?
3. Is there a meaningful trend in disease burden over 25 years?
4. Does pollution level predict disease burden?
5. Does clean water access reduce disease burden?
6. What does the Water Quality Score reveal about global water conditions?
7. Are high-risk conditions concentrated in specific countries or globally distributed?

## Key Insights
- **100% of countries classified High Risk** — no exceptions including developed nations
- **Nigeria leads disease burden** but USA ranks second — confirming this is a global problem
- **No improvement trend over 25 years** — disease burden fluctuates with no sustained decline
- **Pollution does not reliably predict disease** — Mexico leads pollution but not disease burden
- **Negative Water Quality Scores across all countries** — systemic global water quality failure
- **Clean water access weakly correlated with disease** — access alone is insufficient
- **Diarrhea dominates disease type** across every country in the dataset
- **Regional variation is minimal** — disease burden is broadly distributed not geographically concentrated

## Recommendations
1. Multi-factor interventions only — single variables do not predict or reduce disease burden
2. Prioritise water treatment in Mexico, Indonesia, Ethiopia — highest pollution index countries
3. Build a global real-time disease burden surveillance system — 25 years of no progress demands a new approach

![image description](https://github.com/afodunrinbikunmi_data/Water_Pollution_Disease_Analysis/blob/main/water%20pollution%20dashboard.png)
## Dashboard / Visualization
The Power BI dashboard contains 2 report pages:

| Page | Focus |
|---|---|
| **Disease Burden Analysis** | KPIs, country ranking, 25yr trend, regional spread, disease type breakdown, scatter |
![image description](https://github.com/afodunrinbikunmi-data/Water_Pollution_Disease_Analysis/blob/main/disease%20burden.png)
| **Pollution & Water Quality** | KPIs, pollution by country, water quality trend, water source breakdown, risk matrix |
![image description](https://github.com/afodunrinbikunmi-data/Water_Pollution_Disease_Analysis/blob/main/pollution%20risk%20dashboard.png)

## Project Structure
```text
├── data/
│   ├── water_pollution_raw.xlsx
│   └── water_pollution_engineered.csv
├── notebooks/
│   └── water_pollution_eda.ipynb
├── dashboard/
│   └── water_pollution_dashboard.pbix
├── report/
│   └── Water_Pollution_Disease_Analysis.pptx
├── screenshots/
│   ├── dashboard_1_disease_burden.png
│   └── dashboard_2_pollution_quality.png
└── README.md
```
## About me
Afodunrinbi Samad Akinkunmi
I am a Certified Data Analyst with a strong passion for transforming raw data into meaningful insights that support informed decision-making. My work focuses on exploring datasets, identifying patterns, and communicating findings in a clear and impactful way. I enjoy approaching problems analytically, breaking them down into structured steps, and uncovering the story behind the data. Beyond data analysis, I am actively expanding towards becoming a Data Scientist, with an interest in building predictive modeling and advanced analytics.

Data Analyst | Excel | Power BI | Python | SQL | Figma

Connect With Me On - [LinkedIn](https://www.linkedin.com/in/akinkunmiafod) | [Medium](https://medium.com/@afodunrinbikunmi) | [Gmail](afodunrinbikunmi@gmail.com)
