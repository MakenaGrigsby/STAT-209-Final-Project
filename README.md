# STAT-209-Final-Project
This repository contains the full analytical workflow and final report for a statistical investigation into the relationship between climate variability and the incidence of vector-borne diseases, with a focus on malaria and dengue. The analysis leverages global panel data to evaluate how environmental changes may influence disease dynamics under both current and projected climate conditions.

We employed:
- Random Forest for flexible, non-linear prediction.
- Poisson Regression for modeling count data.
- GAM-Negative Binomial for handling overdispersion and smooth nonlinear effects.
  
Climate scenarios modeled include warming, precipitation variability, extreme climate, and increased healthcare
investment.

Project Files
-------------
- climate_disease_complete.qmd: Quarto source file containing all R code, visualizations, simulation results, and
narrative explanation.
- STAT_209_Final_Project_Report.pdf: Formal project report summarizing objectives, methods, results, and
conclusions.
- README.pdf: Project documentation.
- STAT_209_Final_Presentation.pdf: Slides for Final Presentation.

Simulated Scenarios
-------------------
Scenario | Description
----------------------|---------------------------------------------
Baseline | Climate and healthcare as observed in 2000-2020
Case 1: Warming | 10 C increase in average temperature
Case 2: Warm + Rain | 10 C increase + 20% precipitation variability
Case 3: Extreme Climate| Adds UV and AQI increase
Case 4: Budget Increase| 50% increase in healthcare investment

Key Results
-----------
Model | Disease | Max Change | Interpretation
----------------------|---------|------------|----------------------------------------
Random Forest | Dengue | +6.02% | Climate-driven increase
Poisson Regression | Dengue | -0.14% | Less responsive to climate
GAM-Negative Binomial | Malaria | +24.9% | Captures nonlinear, large impacts
GAM-Negative Binomial | Dengue | -6.4% | Budget increase reduces disease burden

R Packages Used
---------------
tidyverse, mgcv, ranger, yardstick, ggplot2, dplyr, tibble, kableExtra

How to Run
----------
1. Open `climate_disease_complete.qmd` in RStudio.
2. Install required packages.
3. Read in .csv file
4. Render via the "Render" button or with `quarto::quarto_render()`

Team Contributions
-------------------
This project was a collaborative effort between two members, combining statistical expertise, modeling, and climate-health research.

Makena Grigsby
-------------------
- Led data cleaning, transformation, and feature engineering
- Conducted exploratory data analysis (EDA) on seasonal trends and climate–disease associations
- Investigated ecological modeling strategies applicable to public health
- Implemented and evaluated the GAM–Negative Binomial (GAM-NB) model for malaria and dengue
- Computed and interpreted model evaluation metrics (RMSE, R²)

Sharvee Joshi
-------------------
- Conducted background research on malaria, dengue, and climate-disease dynamics
- Cleaned data by removing outlier countries and creating lagged climate predictors
- Assembled the literature review and coordinated slide presentation design
- Built initial Poisson and Random Forest models
- Generated spatial visualizations and contributed to interpreting results
- Summarized model performance using RMSE and R² metrics
