# Dissecting Recycling Dynamics: A Two-Way ANOVA Analysis of Trends in Minnesota’s County-Level Waste Management from 1991 to 2017

## Project Overview

This project investigates recycling trends in Minnesota's counties over a span of 26 years (1991-2017) using a dataset named `waste1data`. By leveraging a two-way ANOVA, we aim to understand the dynamics of recycling behaviors based on different sources and material categories. The dataset comprises 49,019 entries from 86 counties, covering five key variables: Year, County, Category, Res Tons (Residential Tons), and CII Tons (Commercial/Institutional/Industrial Tons).

## Dataset

- **Source:** Minnesota's county-level waste management data
- **Size:** 49,019 entries, 5 variables
- **Description:**
  - **Year:** Numerical and discrete, indicating the year of data collection.
  - **County:** Categorical and nominal, indicating the county name.
  - **Category:** Categorical and nominal, indicating the type of recycling material (Paper, Metal, Glass, Plastic, Hazardous, Other, Organic).
  - **Res Tons:** Continuous and numerical, representing the weight of residential recycling.
  - **CII Tons:** Continuous and numerical, representing the weight of commercial/institutional/industrial recycling.

## Research Questions

1. Is there a significant difference in the mean weight of waste recycled between residential and commercial/industrial/institutional sources?
2. Are there significant differences in the mean weight of waste recycled across different material categories?

## Hypotheses

### Main Effect of Category
- **Null Hypothesis (H0):** The means across all categories are equal.
  - \( H0: \text{Paper} = \text{Metal} = \text{Glass} = \text{Plastic} = \text{Hazardous} = \text{Other} = \text{Organic} \)
- **Alternative Hypothesis (Ha):** Not all category means are equal.
  - \( Ha: \text{At least two means are different} \)

### Main Effect of Type
- **Null Hypothesis (H0):** The mean weight of recycled tons is the same for residential and commercial/industrial/institutional (CII) collections.
  - \( H0: \text{Res} = \text{CII} \)
- **Alternative Hypothesis (Ha):** The mean weight of recycled tons for residential collection is not equal to that for CII.
  - \( Ha: \text{Res} \neq \text{CII} \)

### Interaction Between Type and Category
- **Null Hypothesis (H0):** There is no interaction between Type and Category.
- **Alternative Hypothesis (Ha):** There is an interaction between Type and Category.

## Methodology

1. **Data Preprocessing:**
   - Checked for and addressed missing values, outliers, or anomalies.
   - Transformed data from wide to long format to better suit analysis needs.
   - Created two new variables: `Type` (identifying recycling source as residential or CII) and `Recycle Tons` (representing the weight of recycling).

2. **Statistical Analysis:**
   - Conducted a two-way ANOVA to analyze the effects of Type and Category on recycling amounts.
   - Investigated interaction effects between Type and Category.

## Results

- **Category Effect:** Significant main effect with F-value of 342.1 and p-value < 2e-16, indicating that mean weights of recycled tons vary significantly among different categories.
- **Type Effect:** Significant main effect with F-value of 143.4 and p-value < 2e-16, showing a significant difference in mean weights of recycled tons between Residential and CII sources.
- **Interaction Effect:** Significant interaction with F-value of 109.3 and p-value < 2e-16, suggesting that the relationship between Category and Type significantly influences recycling behaviors.

## Conclusion

The study reveals significant differences in recycling amounts based on material categories and sources (residential vs. commercial/industrial/institutional). The interaction effect between Category and Type underscores the need for targeted recycling programs. This analysis provides insights that can enhance recycling strategies and improve environmental sustainability.

## Repository Contents

- `data/`: Contains the dataset used for the analysis.
- `notebooks/`: Jupyter notebooks detailing each step of the analysis, from data preprocessing to statistical testing.
- `src/`: Source code for data transformation, preprocessing, and analysis.
- `visualizations/`: Graphs and charts used for data exploration and result presentation.
- `README.md`: Project overview and instructions.

