# Feature Selection Optimization for Glioma Grade Differentiation
Gliomas are the most common primary tumors of the brain arising from supportive glial cells. There are 2 main types as low-grade glioma (LGG) and glioblastoma (GBM). The accurate distinction between LGG and GBM is crucial for patient care and prognosis.
Despite advances in imaging and pathological assessment, accurate differentiation between LGG and GBM remains challenging. Standard imaging techniques show considerable overlap in features, especially with certain molecular subtypes that do not follow typical patterns. Pathological analysis, while traditionally providing definitive diagnosis, has limitations in addressing tumor heterogeneity, with single biopsies potentially missing high-grade areas that would change classification and treatment. 


The molecular classification of gliomas has transformed our understanding of these tumors, with the 2016 and 2021 WHO classifications including molecular parameters alongside histological features, recognizing that molecular signatures often better predict tumor behavior than appearance alone. But current molecular diagnostic approaches are costly and complex due to large gene panels.
This project explores whether a smaller subset of genes can achieve comparable predictive performance to differentiate between LGG and GBM using machine learning.

Here, we achieved the following.
- Identify the best-performing ML model for glioma classification.
- Identify the optimum gene panel for molecular diagnostics.
- Maintain strong predictive performance with a minimal diagnostic panel.

# Problem Statement

Can we reduce the number of genes required for glioma classification while preserving accuracy?

Minimum size gene panel has real world implications:
- Lower diagnostic costs
- Faster testing turnaround
- Increased accessibility in low-resource settings

# Dataset

- Source: UCI Machine Learning Repository
- Name: Glioma Grading Clinical and Mutation Features
- Includes:
  - Patient demographics
  - Mutation status of most frequently mutated 20 genes
    
- Task:
  - Determine whether a patient is LGG or GBM with a given clinical and molecular/mutation features.
 
# Methodology

1. Data preprocessing
  - Rows containing missing values were identified and removed from the dataset
  - Entries marked as 'not reported' were excluded from the analysis
  - No imputation methods were applied, ensuring that only complete cases were used for model training
  - The resulting cleaned dataset contained only high-quality, complete gene expression profiles

2. Model selection
  - Multiple machine learning models were evaluated
    - Logistic regression
    - Decision trees
    - Random forests
    - SVM
    - XGBoost
   
  The best performing model was selected based on,
  - ROC-AUC (Quantifies the model's ability to discriminate between low and high-grade gliomas assessing both sensitivity and specificity)
  - Accuracy
  - F1-score
  - Precision
  - Specificity
  - Sensitivity

3. Feature selection

   
 
