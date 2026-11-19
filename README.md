# Understanding Home Sale Prices in King County

### A Multiple Regression Analysis of Living Area and Construction Quality, Controlling for Geographic Location

**R | OLS Regression | Statistical Inference | Exploratory Data Analysis**

**[View Full Analytical Report (PDF)](king_county_housing_price_analysis.pdf)**

## Project Overview

This study examines the associations between construction grade, living area, and residential home sale prices in King County, Washington, while controlling for geographic location.

The objective is to identify and quantify statistical associations rather than establish causal relationships or develop a predictive model.

## Research Questions

1. Is construction grade associated with home sale prices, controlling for living area and geographic location?
2. How is living area associated with home sale prices, controlling for construction grade and geographic location?

## Dataset

- **Source:** [House Sales in King County, USA — Kaggle](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)
- **Period:** May 28, 2014 – May 27, 2015
- **Analytical sample:** ~20,000 residential properties
- **Exploration sample:** 30%
- **Confirmation sample:** 70%

## Methodology

- Data cleaning and preprocessing
- Exploratory data analysis
- Correlation analysis
- Logarithmic transformations
- LOESS smoothing and functional form assessment
- Multiple regression analysis
- Quadratic log-log specification
- ZIP code fixed effects
- HC3 heteroskedasticity-robust standard errors
- Statistical hypothesis testing
- Regression diagnostics

An exploration-confirmation split was implemented to reduce the risk of false-positive findings arising from data-driven model selection.

## Key Findings

- Construction grade remains positively and statistically significantly associated with home sale prices after controlling for living area and geographic location.
- Living area exhibits a positive, nonlinear association with home sale prices across the primary observed range.
- The curvature of the relationship between living area and home sale price on the log-log scale decreases by approximately 65% after controlling for construction grade and geographic location.
- The complete regression model explains approximately 85% of the variation in log home sale prices in the confirmation sample.

## Repository Contents

| File / Folder | Description |
|---|---|
| [Analytical Report (PDF)](king_county_housing_price_analysis.pdf) | Complete analytical report and findings |
| [Analytical Report (Rmd)](king_county_housing_price_analysis.Rmd) | R Markdown source code |
| [exploration_confirmation/](exploration_confirmation/) | Data exploration, model selection, and confirmation analysis |
| [data/raw/](data/raw/) | Original source dataset |
| [data/processed/](data/processed/) | Cleaned and transformed datasets |

## Tools and Technologies

R, R Markdown, tidyverse, ggplot2, lmtest, sandwich, emmeans, stargazer, patchwork
