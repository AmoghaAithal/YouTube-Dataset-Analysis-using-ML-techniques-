# Predicting trending videos in YouTube (Machine Learning in R)

## Overview

This repository contains **a complete machine learning project** implemented across **three R Markdown files**. The project focuses on **predicting outcomes related to YouTube trending videos** using a progression of supervised learning models in **R**.

The three files together form an end-to-end workflow, starting from data preparation and baseline models, moving through regularization and tree-based methods, and finally applying more advanced models for improved predictive performance.

All files are part of **a single project** and should be read and run **together**.

---

## Repository Structure

```
Project 1.Rmd   # Data cleaning, preprocessing, EDA, baseline models
Project 2.Rmd   # Regularized regression and decision tree models
Project 3.Rmd   # Advanced models (ensemble methods)
```

---

## Dataset Description

The project uses a **large-scale YouTube Trending Videos dataset** with more than **100,000 observations**. Each row corresponds to a video and includes metadata such as:

* Video category
* Channel information
* Video duration
* Engagement metrics (views, likes, comments)
* Country and publishing details

### Dataset Files

* `yt_training_X.csv` – Training feature set
* `yt_training_y.csv` – Training labels
* `yt_test_X.csv` – Test feature set (unlabeled)

### Dataset Availability

Due to GitHub file size limitations, the datasets (over **150 MB**) are not included in this repository.

To run the project locally:

1. Obtain the datasets from the original source (course-provided or external)
2. Place all CSV files in the project working directory
3. Knit the R Markdown files in order

---

## Project 1: Data Preparation & Baseline Models

### Description

This stage focuses on preparing the data and establishing baseline predictive performance.

### Key Components

* Data loading and inspection
* Handling missing and inconsistent values
* Feature transformation and encoding
* Exploratory data analysis (EDA)
* Baseline regression and classification models

### Outcome

A clean modeling dataset and baseline results used for comparison with more advanced methods.

---

## Project 2: Regularization & Tree-Based Models

### Description

This stage introduces methods to control model complexity and capture non-linear relationships.

### Models Implemented

* Lasso Regression (L1 regularization)
* Ridge Regression (L2 regularization)
* Elastic Net (via `glmnet`)
* Decision Trees (`rpart`)

### Techniques Used

* Cross-validation for hyperparameter tuning
* Shrinkage-based feature selection
* Model comparison against baseline performance

### Outcome

Improved predictive performance and better generalization compared to baseline models.

---

## Project 3: Advanced Tree-Based Models

### Description

This stage applies more advanced tree-based models to further improve prediction accuracy.

### Models Implemented

* Random Forest (`ranger`)
* Gradient Boosting (`xgboost`)

### Techniques Used

* Hyperparameter tuning
* Model evaluation and comparison
* Final model selection for prediction on test data

### Outcome

Ensemble methods achieve stronger performance than earlier approaches and are used for final predictions.

---

## Results Summary

Multiple models were evaluated across the three stages of the project.

* Baseline linear models provided an initial performance benchmark.
* Regularized regression and decision tree models improved generalization and handled feature complexity more effectively.
**Ensemble methods**, particularly the **Random Forest** achieved the **highest validation accuracy (75.14% accuracy)** among all models tested and was selected for final prediction.

---

## Libraries & Tools

The project uses the following R packages:

* `tidyverse`
* `dplyr`, `stringr`
* `glmnet`
* `rpart`
* `ranger`
* `xgboost`
* `knitr`

CRAN mirrors are explicitly set to ensure reproducibility.

---

## How to Run the Project

1. Install R (version 4.0 or higher)
2. Install the required packages
3. Place the dataset CSV files in the working directory
4. Knit the files **in the following order**:

```r
Project 1.Rmd → Project 2.Rmd → Project 3.Rmd
```

---

## Key Learning Outcomes

* End-to-end machine learning workflow in R
* Data preprocessing and feature engineering
* Regularization techniques inlcuing Tree-based and advanced Ensemble models
* Model evaluation and comparison
* Handling large real-world datasets

---

## Contact

**Name:** **Amogha Aithal G V**

**Email:** getamogha@gmail.com

**Linkedin:** www.linkedin.com/in/amogha-aithal-539449317

