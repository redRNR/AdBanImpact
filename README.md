# From Ads to App Ratings: Analyzing the Impact of Google’s Targeted Advertising Ban in Children’s Games

## Overview

This repository contains the materials and analyses for the study, **"From Ads to App Ratings: Consequences of Google’s Targeted Advertising Ban in Children’s Games"**, conducted by Azra Park. The study evaluates the causal impact of Google’s 2019 targeted advertising ban on app ratings in children’s Android games using advanced causal inference techniques.

## Key Highlights

- **Objective**: To determine how Google's advertising ban affected user satisfaction, as measured through app ratings.
- **Data**:
  - **Sources**: AppMonsta (app-level metrics) and Apkmonk (metadata on advertising networks).
  - **Scope**: 5,834 games (2,917 treatment and 2,917 control) over 22 months, spanning pre- and post-policy periods.
- **Methods**:
  - **Difference-in-Differences (DiD)**
  - **Propensity Score Matching (PSM-DID)**
  - **Meta-Learners (S-, T-, X-Learner)**
  - **Inverse Probability Weighting (IPW)**
  - **Doubly Robust Estimation**
  - **Double Machine Learning**
  - **Generalized Random Forest (GRF)**

## Repository Structure

- **`project.ipynb`**: The main Jupyter Notebook for the analysis, includes:
  - Data preprocessing and visualization.
  - Implementation of causal inference methods.
  - Robustness checks and sensitivity analyses.
  - Generation of plots and tables for results.
- **`From Ads to App Ratings.pdf`**: The final report containing detailed discussions, methodologies, results, and references.

## Key Findings

- Games affected by the ban experienced an average improvement of **0.025 stars** in ratings, indicating higher user satisfaction.
- Results were consistent across multiple causal inference methods, demonstrating the robustness of findings.
- Significant predictors of app ratings include:
  - **log(Demand)**: Most influential across all models.
  - **AfterBan**: Reflects the effect of the policy change.
  - **Age** and **log(Firm_Size)**: Important control variables.

## Data Sources

1. **AppMonsta**: Weekly snapshots of app-level metrics (e.g., ratings, prices).
2. **Apkmonk**: Metadata on app advertising networks and permissions.

The data includes 99,714 game-month observations, with key variables such as `Rating`, `log(Demand)`, `Age`, `Price`, and `log(Firm_Size)`.

## Methodology

- **Quasi-Experimental Design**: A Difference-in-Differences (DiD) approach with fixed effects to isolate the causal impact of the ad ban.
- **Advanced Techniques**: Incorporation of causal machine learning models to address potential confounders and enhance robustness.
- **Feature Importance Analysis**: Techniques like LASSO, Ridge, and Random Forest to validate key predictors.
 
