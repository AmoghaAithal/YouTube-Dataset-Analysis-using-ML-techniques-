# YouTube Video Performance Prediction

## Project Overview

This project analyzes YouTube trending video metadata to predict **success** using machine learning techniques in R. The analysis demonstrates a complete ML workflow from data preprocessing through advanced ensemble modeling.

**Academic Context:** This project was developed as part of my Data Mining course (BUDT758) at University of Maryland's Robert H. Smith School of Business. The analysis is organized across three sequential R Markdown notebooks, each building upon the previous stage.

---

## Business Problem

Understanding what drives video performance on YouTube enables content creators and marketers to:
- Optimize content strategy based on trending patterns
- Predict potential reach before publishing
- Identify key factors influencing the video success
- Allocate resources to high-performing content categories

---

## Repository Structure
```
Project 1.Rmd / Project-1.html   # Data cleaning, EDA, baseline models
Project 2.Rmd / Project-2.html   # Regularized regression and tree models
Project 3.Rmd / Project-3.html   # Advanced ensemble methods
README.md                            # This file
```

**Note:** Each stage builds upon the previous one. Files should be reviewed in sequence.

---

## Dataset

### Description
Large-scale YouTube Trending Videos dataset containing **100,000+ observations** with metadata including:

- **Video Attributes:** Category, duration, title characteristics
- **Channel Information:** Subscriber count, channel age, upload frequency
- **Engagement Metrics:** Views, likes, comments, shares
- **Publishing Details:** Country, publish time, trending date

### Dataset Files
- `yt_training_X.csv` – Training features (100K+ rows)
- `yt_training_y.csv` – Training labels
- `yt_test_X.csv` – Test features (unlabeled)

### Data Availability
**Note:** Due to GitHub file size limitations (datasets exceed 150 MB), the CSV files are not included in this repository.

**To run locally:**
1. Obtain datasets from course source / Kaggle / etc.
2. Place CSV files in project working directory
3. Knit R Markdown files in sequence

---

## Analysis Workflow (stages do not strictly correspond to project numbers)

### Stage 1: Data Preparation & Baseline Models
**File:** Project 1.Rmd / Project-1.html

**Key Steps:**
- Data loading and quality assessment
- Missing value treatment and outlier detection
- Feature engineering (temporal features, text processing, categorical encoding)
- Exploratory data analysis with visualizations
- Baseline models: Linear regression, logistic regression

**Outcome:** Clean modeling dataset and baseline performance benchmarks

---

### Stage 2: Regularization & Tree-Based Models
**File:** Project 2.Rmd` / Project-2.html

**Models Implemented:**
- **Lasso Regression** (L1 regularization for feature selection)
- **Ridge Regression** (L2 regularization for coefficient shrinkage)
- **Elastic Net** (combined L1/L2 penalty via `glmnet`)
- **Decision Trees** (`rpart` with pruning)

**Techniques:**
- K-fold cross-validation for hyperparameter tuning
- Regularization path analysis
- Model comparison using validation metrics

**Outcome:** Improved generalization through regularization; identification of key predictive features

---

### Stage 3: Advanced Ensemble Methods
**File:** Project 3.Rmd / Project-3.html

**Models Implemented:**
- **Random Forest** (`ranger` package) - bagging with feature randomness
- **Gradient Boosting** (`xgboost`) - sequential error correction

**Techniques:**
- Grid search for optimal hyperparameters
- Feature importance analysis
- Final model evaluation on holdout test set

**Outcome:** Ensemble methods achieve best performance; Random Forest selected for final predictions due to highest validation accuracy (75.14%).

---

## Results Summary

### Model Performance Comparison

| Model | Validation Accuracy | Key Strength |
|-------|-------------------|--------------|
| Baseline | 57.14% | Base for comparison |
| Logistic Regression | 64.20% | Simple, interpretable |
| Lasso Regression | 69.96% | Automatic feature selection |
| Ridge Regression | 71.53% | Handles multicollinearity |
| Decision Tree (maxdepth=7) | 67.08% | Captures non-linear patterns |
| Boosting | 73.90% | Boosts performance |
| **Random Forest** | **75.14%** | **Best overall performance** |
| XGBoost | 72.10% | Strong performance, fast training |

**Key Findings:**
- Ensemble methods significantly outperformed linear baselines
- Random Forest achieved **75.14% accuracy**, selected for final predictions, along with XGBoost.

---

## Technical Stack

**Language:** R (version 4.0+)

**Key Libraries:**
- **Data Manipulation:** `tidyverse`, `dplyr`, `stringr`
- **Modeling:** `glmnet` (regularization), `rpart` (trees), `ranger` (Random Forest), `xgboost` (gradient boosting)
- **Utilities:** `knitr` (reporting)

---

## How to Reproduce

### Prerequisites
1. Install R (4.0 or higher)
2. Install RStudio (recommended)
3. Install required packages:
```r
install.packages(c("tidyverse", "dplyr", "stringr", "glmnet", 
                   "rpart", "ranger", "xgboost", "knitr"))
```

### Running the Analysis
1. Clone this repository
2. Place dataset CSV files in working directory
3. Open and knit files **in sequence**:
   - Project 1.Rmd → Project-1.html
   - Project 2.Rmd → Project-2.html
   - Project 3.Rmd → Project-3.html

---

## Key Learning Outcomes

This project demonstrates:
- ✅ End-to-end supervised learning workflow in R
- ✅ Data preprocessing and feature engineering techniques
- ✅ Regularization methods (Lasso, Ridge, Elastic Net)
- ✅ Tree-based models and ensemble methods
- ✅ Model evaluation, comparison, and selection
- ✅ Handling large real-world datasets (100K+ observations)

---

## Contact

**Amogha Aithal**   
Email: getamogha@gmail.com  
LinkedIn: [linkedin.com/in/amogha-aithal-539449317](https://www.linkedin.com/in/amogha-aithal-539449317)  


---

## License

This project was developed for academic purposes as part of BUDT758 (Data Mining) coursework at University of Maryland.

---
