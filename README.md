# Employee Attrition Prediction

## Overview

This project analyzes data from the Stack Overflow 2025 Developer Survey to examine factors associated with developers’ decisions to consider or make a career change. Using predictive modeling techniques (Naive Bayes, Logistic Regression, and Random Forest), the project evaluates model performance and explores how demographic, experiential, and work-related factors influence career mobility.

## Folder Structure

### Data Folder (`data/`)
The dataset is too large to include in this repository. It is the **Stack Overflow Developer Survey 2025**, available [here](https://survey.stackoverflow.co). The survey includes these files: 
- **survey_results_public.csv**: The 2025 Stack Overflow Developer Survey.  
- **survey_results_schema.csv**: Description of all variables in the dataset.  
- **2025_Developer_Survey_Tool.pdf**: Survey methodology and documentation.

### Code Folder (`code/`)

-   **final_report.qmd**\
    Quarto source file containing data cleaning, exploratory analysis, modeling, evaluation, and written discussion.

-   **final_report.html**\
    Rendered HTML version of the final report with tables, figures, and model results. This file can be opened directly in a web browser.

## Project Overview

1. **Data Cleaning & Processing**
   - Selected relevant predictors: demographics, job attributes, experience, compensation, and attitudinal measures.
   - Transformed variables to suitable formats; handled missing values with median imputation or "Unknown" categories.
   - Binary target variable (`NewRole`): Change vs. No_Change.

2. **Exploratory Data Analysis**
   - Visualized distributions for continuous and categorical variables.
   - Checked correlations and patterns related to career change.

3. **Modeling**
   - **Naive Bayes:** Simple baseline, interpretable.  
   - **Logistic Regression:** Predictive, interpretable coefficients, ROC-based optimal thresholds.  
   - **Random Forest:** Non-linear relationships, robust, handles categorical features, feature importance analysis.  
   - Evaluated models both including and excluding job satisfaction to understand influence of key predictors.

4. **Key Findings**
   - Younger developers (25–44) are more likely to consider career changes.  
   - Job satisfaction is the strongest predictor; AI threat perception, work experience, compensation, and tool usage also important.  
   - Logistic Regression provides interpretability; Random Forest achieves higher sensitivity for detecting likely changers.  

5. **Limitations**
   - Self-reported survey data may be biased.
   - Models are correlational, not causal.
   - External factors like market conditions or personal circumstances are not captured.

## How to Run the Analysis

1.  Install **R** and **RStudio**.
2.  Install required R packages:
    -   `tidyverse`
    -   `caret`
    -   `pROC`
    -   `ranger`
    -   `naivebayes`
    -   `cutpointr`
    -   `forcats`
    -   `ggplot2`
3.  Open `final_report.qmd` in RStudio.
4.  Set the working directory to the project root.
5.  Render the report using: \`\`\`r quarto::quarto_render("code/final_report.qmd")

## Repository
[GitHub Repository](https://github.com/yenne1345/employee-attrition-classification)
Contains all code, data, and final report for reproducibility.
