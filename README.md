[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/cERkRA-7)
# Project Repo

This is the team repository you will be use for your project. All your team's work will happen here. 

Links of interest:
* The project requirements are in the [`instructions.md`](instructions.md) document
* The repository structure is described in the [repository structure section](#repository-structure) below
* You **will** make changes to this `README.md` file within your repository. These changes are described in the [instructions section](#instructions-for-modifying-this-readmemd-file) below.

## Repository structure

You will work within an **organized** repository and apply coding and development best practices. The repository has the following structure:

```.
├── README.md
├── code/
├── data/
├── img/
└── website/
```

* The `code/` directory is where you will develop all your code.  You may add additional sub-directories as needed to modularize your development.

* The `data/` directory should contain your data files and should have multiple sub-directories (i.e. raw, processed, analytical, etc.) as needed.

* The `img/` directory should contain any external images that you need for your site. However, all your viz's should be generated programmatically in your source code.

* The `website/` directory where the website will be deployed. It must be self-contained and accessible via an index.html within this sub-directory.  Any website asset (images, html, css, JavaScript source code) must be added to this directory. 

There is an empty placeholder file in each subdirectory called `.keep`. This file may be deleted **after** you save other files in those subdirectories. This file is needed to be able to keep the empty directory in the repo.

Other files we expect to see at the top level of this repo may include:
- `.gitignore`


## Instructions

# 🏠 Housing Behavior Analysis (2015–2023)

## 📌 Objective

This project analyzes how various **economic, demographic, and social factors** influence **rental rates** and **homeownership rates** across U.S. metropolitan areas (MSAs) between 2015 and 2023.

Each dataset below should be **visualized and statistically compared** against:

- `Rental Rate`
- `Homeownership Rate`

From the file:  
`DP04_Rent_Home_Rate_2015_2023.csv`

---

## 🧹 Preprocessing Guidelines (Required Before Analysis)

Before visualization or merging, all datasets **must be cleaned and standardized**:

- ✅ **Clean missing values**, remove metadata rows or non-MSA aggregates (e.g., "United States", "Geographic Area")
- ✅ **Unify time format** to **yearly intervals** across all datasets
- ✅ **Standardize geographic names** to match the MSA format used in the rental/homeownership dataset
- ✅ Ensure all datasets are in **long format**: one row per MSA per year

---

## 📁 Dataset Overview & Analytical Notes

| File Name | Description | Comparison Recommendation |
|-----------|-------------|----------------------------|
| `DP04_Rent_Home_Rate_2015_2023.csv` | Primary dataset with rental/homeownership rates by MSA/year | **Main target** for all comparisons |
| `HomeValues_byMSA(2015–2023).csv` | Home values by MSA | ❗️️ Use **year-over-year change**, not raw value |
| `income_byMSA(2015–2023).csv` | Median income levels by MSA | ✅ Use **both raw values and changes** |
| `national_unemployment(2015–2023).csv` | National unemployment rate | ✅ Use **both raw values and changes** |
| `Mortage_rate(2015–2023).csv` | National mortgage interest rate | ✅ Use **both raw and change** |
| `CPI(2015–2023).csv` | Consumer Price Index (Inflation) | ❗️ Use **change only**, not raw value |
| `Elderly_Rate_by_MSA (2015–2023).csv` | % population age 65+ by MSA | ✅ Use **raw rate** |
| `Non-Single_Household_byMSA(2015–2023).csv` | Family households by MSA | ✅ Use **raw count or %** |
| `Education_Attainment_by_MSA(2015–2023).csv` | Education breakdown by MSA | ✅ Use **raw proportions** |
| `Homeowneraffordability_byMSA(2015–2023).csv` | Home affordability index by MSA | ✅ Use raw index |
| `Renteraffordability_byMSA(2015–2023).csv` | Rent affordability index by MSA | ✅ Use raw index |
| `Salestotal_byMSA(2015–2023).csv` | Number of home sales per year | ❗️ Use **change over time** |
| `GDP(2015–2023).csv` | GDP by MSA | ❌ Don’t use raw value<br>✅ Use **GDP change** |

---

## 📊 Visualization & Analysis Guidelines

1. **Visualize Over Time**
   - Use time series plots

2. **Raw vs. Change Comparison**
   - For some factors (like GDP, CPI), **changes** better reflect influence
   - Others (like education level, elderly rate) can be directly compared using raw 
