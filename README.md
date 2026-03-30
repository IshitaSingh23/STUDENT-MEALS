# 📊 School Meal Nutrition Quality & Academic Performance in Illinois

## Overview
School meal programs play a critical role in supporting student health, well-being, and learning outcomes, particularly for students from low-income households. Despite their importance, there is limited integrated evidence examining how the nutritional quality of school meals varies across districts and how this variation aligns with academic performance.

This project analyzes the relationship between **school meal nutrition quality** and **academic proficiency outcomes** across **Illinois public elementary school districts**. By combining multiple datasets on school meals, student demographics, and standardized test performance, the project provides a district-level view of how nutrition quality relates to educational outcomes and equity considerations.

---

## Objectives
The primary objectives of this project are to:
- Characterize variation in school meal nutrition quality across Illinois school districts
- Examine associations between nutrition quality and academic proficiency in:
  - English Language Arts (ELA)
  - Mathematics
  - Science
- Explore how these relationships differ for:
  - Low-income students
  - Students with disabilities
- Provide an integrated, analysis-ready dataset to support policy-relevant evaluation of school meal programs

---

## Data Sources
This project integrates three primary data sources:

1. **School Meal Nutrition Data (MEALS Study)**  
   - Menu-level nutrition composition data
   - Healthy Eating Index (HEI-2015) total and component scores
   - Aggregated to the district level

2. **Academic Performance Data (Illinois State Assessments)**  
   - District-level proficiency rates for ELA, Math, and Science
   - Subgroup proficiency for low-income students and students with disabilities

3. **District Demographic & Contextual Data**
   - Percentage of low-income students
   - Percentage of students with disabilities
   - Regional education office (ROE) identifiers

All datasets are restricted to **public elementary schools** and aggregated to the **district level**.

---

## Key Variables

### Academic Outcomes
- `ELA_Proficiency`
- `Math_Proficiency`
- `Science_Proficiency`
- Subgroup outcomes:
  - Low-income students
  - Children with disabilities (CWD)

### Nutrition Quality Measures
- `HEI 2015 Total Score`
- HEI component scores (fruits, vegetables, whole grains, sodium, added sugars, saturated fats, etc.)

### Covariates
- `student_low_income_percent`
- `student_disabilities_percent`
- `days_entered` (menu sampling coverage)
- `ROE`

---

## Methodology

### Data Processing
- Nutrition data aggregated from menu-level observations to district-level means
- Academic performance data cleaned and harmonized across subjects
- District names standardized to enable accurate merging
- Final dataset restricted to elementary school districts with valid academic and nutrition data

### Exploratory Data Analysis
- Descriptive statistics of nutrition and academic variables
- Visualization of distributions and cross-district variation
- Correlation analysis between nutrition quality and academic outcomes

### Exploratory Modeling
- Linear regression models examining associations between:
  - HEI scores and academic proficiency
- Models adjusted for district-level socioeconomic characteristics
- Subgroup analyses for low-income students and students with disabilities
- Modeling used for **exploratory insight**, not causal inference

---

## Outputs
The project produces:
- A cleaned, integrated district-level dataset
- Descriptive summaries and visualizations
- Exploratory regression results linking nutrition quality and academic outcomes


---

