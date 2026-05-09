# District-Level Analysis of Nutrition, SES, and Academic Performance

This project analyzes district-level relationships between school meal nutrition measures, socioeconomic factors, and academic performance in Illinois public schools. The analysis was completed for **STAT 427: Statistical Consulting** in collaboration with **Dr. Ru Liu** from the **Department of Health & Kinesiology, UIUC**.

The main goal was to understand how nutrition-related variables and socioeconomic indicators are associated with academic proficiency outcomes in:

- ELA
- Math
- Science

The results are interpreted as **associations only**, not causal effects.

---

## Dataset

The main dataset used in this project is:

```text
academic_meals_elementary_district.csv
```

The dataset contains district-level information on:

Academic proficiency outcomes
Socioeconomic indicators
HEI 2015 nutrition scores
Macro- and micronutrient variables
Other school meal nutrition-related measures

Project Motivation

The dataset has many nutrition predictors but only a small number of school districts. This creates a high-dimensional modeling problem where ordinary regression can become unstable due to multicollinearity and influential observations.

Because of this, the project focused on:

Cleaning and preparing the dataset
Reducing redundant predictors
Handling multicollinearity
Comparing multiple regression-based models
Running model diagnostics
Selecting interpretable models for ELA, Math, Science, and average academic score


Repository Files

The main files in this repository are:

```bash
academic_meals_elementary_district.csv
ELA Model.ipynb
Math Model.ipynb
Science Model.ipynb
Final Average Model.ipynb
File Descriptions
academic_meals_elementary_district.csv
```

This is the main district-level dataset used for the analysis.

ELA Model.ipynb

This notebook contains the full modeling workflow for ELA proficiency.
It includes:

Data cleaning and preprocessing
Predictor filtering
Multicollinearity checks
Baseline OLS regression
Ridge regression
Lasso regression
Diagnostic checks
Final model interpretation
Math Model.ipynb

This notebook contains the full modeling workflow for Math proficiency.

It includes the same modeling steps as the ELA notebook, but with Math proficiency as the response variable.

Science Model.ipynb

This notebook contains the full modeling workflow for Science proficiency.
It includes preprocessing, regression models, regularized models, diagnostics, and final model selection for Science.

Final Average Model.ipynb

This notebook creates an average academic score using ELA, Math, and Science proficiency outcomes.

It then fits models on the average score to understand broad cross-subject academic patterns.



How to Run the Code
1. Clone the repository
git clone <your-repository-link>
cd <your-repository-name>
2. Create a virtual environment
python -m venv venv

Activate the environment:

For Mac/Linux:

source venv/bin/activate

For Windows:

venv\Scripts\activate
3. Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels scipy jupyter
4. Open Jupyter Notebook
jupyter notebook
5. Run the notebooks

Run the notebooks in this order:

1. ELA Model.ipynb
2. Math Model.ipynb
3. Science Model.ipynb
4. Final Average Model.ipynb

Each notebook is self-contained for its respective outcome, but all notebooks use the same dataset:

academic_meals_elementary_district.csv
Main Libraries Used
pandas
numpy
matplotlib
seaborn
scikit-learn
statsmodels
scipy
jupyter
Modeling Methods Used

The project used:

Ordinary Least Squares regression
Ridge regression
Lasso regression
Correlation filtering
Variance Inflation Factor filtering
Cross-validation
Residual diagnostics
Influence diagnostics
