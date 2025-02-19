# Tumor-Classification
Overview:
This project focuses on accurately classifying tumors into benign or malignant categories using Discriminant Analysis and Genetic Algorithm-based feature selection. Early identification of tumor types significantly improves diagnosis and treatment planning, making this an essential application of machine learning in healthcare.

Dataset:
Source: Kaggle
Size: 570 rows
Features: 30 different attributes representing tumor characteristics such as size, shape, texture, perimeter, and area.
Target Variable: Binary classification (Benign or Malignant).
Methodology:
Feature Selection using Genetic Algorithm (GA):

Since not all 30 features contribute significantly to tumor classification, GA was used to identify the top 5 most relevant features.
Implemented using 'GeneticSelectionCV' module from sklearn-genetic package.
The selected features: area_worst, area_mean, area_se, perimeter_worst, and perimeter_mean.
Discriminant Analysis for Classification:

Linear Discriminant Analysis (LDA) was applied to classify tumors based on the selected features.
LDA maximized the separability between benign and malignant tumors by finding a decision boundary.
Optimization Constraints:

The objective function was to maximize accuracy.
A cutoff score constraint was set between -7735.3 and 7735.3, ensuring meaningful classification.
Feature weights were constrained between -1 and 1 to maintain interpretability.
Results & Performance:
Initial Accuracy (using all 30 features): 70%
Final Accuracy (after feature selection & optimization): 92.27%
The use of feature selection via Genetic Algorithm significantly improved model performance by removing irrelevant features and focusing on the most informative ones.
Key Learnings & Future Work:
Comparison with Other Models: Future iterations could explore Multiple Linear Regression and compare results with Discriminant Analysis.
Further Optimizations: Hyperparameter tuning of Genetic Algorithm parameters could further refine feature selection.
Real-world Deployment: Integrating the model into a diagnostic tool for hospitals and research centers.
This project demonstrates the power of machine learning in medical diagnosis and showcases how feature selection can dramatically improve predictive accuracy.
