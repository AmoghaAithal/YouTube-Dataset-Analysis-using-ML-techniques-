# YouTube Video Performance Prediction

## Project Overview

This project analyzes YouTube trending video metadata to predict **success** using machine learning techniques in R. The analysis demonstrates a complete ML workflow from data preprocessing through advanced ensemble modeling.

**Academic Context:** This project was developed as part of my Data Mining course (BUDT758) at University of Maryland's Robert H. Smith School of Business. The analysis is organized across three sequential R Markdown notebooks, each building upon the previous stage.

### Viewing the Reports
GitHub shows the HTML source code when opened inside the repo.  
To view the rendered report with plots/tables, download the `.html` file and open it in a browser.
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
Project 2.Rmd / Project-2.html   # Feature engineering and tree models
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

## Analysis Workflow

### Stage 1: Classification Models & Model Selection
**File:** Project 1.Rmd / Project-1.html

**Key Steps:**
- Data loading and preprocessing
- Exploratory analysis of the YouTube trending videos dataset
- Feature preparation for classification tasks
- Logistic Regression for binary classification
- Classification Trees for non-linear decision boundaries
- Model evaluation and selection using validation techniques

**Outcome:**  
Initial classification models built and evaluated, establishing baseline performance and introducing tree-based methods for comparison.

---

### Stage 2: Model Validation & Feature Engineering
**File:** Project 2.Rmd / Project-2.html

**Key Steps:**
- Model validation strategies
- Performance evaluation using ROC curves and AUC
- Feature engineering to improve predictive power
- Comparative assessment of model performance

**Outcome:**  
Improved understanding of model diagnostics and validation, with enhanced features leading to better classification performance.

---

### Stage 3: Regularization & Ensemble Methods
**File:** Project 3.Rmd / Project-3.html

**Models Implemented:**
- Ridge Regression
- Lasso Regression
- Ensemble Methods:
  - Random Forest
  - Gradient Boosting (XGBoost)

**Techniques:**
- Comparison of Ridge and Lasso regularization
- Ensemble learning for improved predictive accuracy
- Feature importance analysis
- Final model evaluation

**Outcome:**  
Regularization techniques reduce overfitting, and ensemble models deliver the strongest overall performance, with Random Forest and Gradient Boosting achieving the best results.


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
