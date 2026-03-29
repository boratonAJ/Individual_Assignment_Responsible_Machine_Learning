# Responsible_Machine_Learning

## 1. Purpose of the Analysis

This repository contains assignments and analysis for the Responsible Machine Learning (RML) course. The main purpose of the analysis is to explore, implement, and evaluate responsible and ethical practices in machine learning, including fairness, transparency, and bias mitigation in predictive models.

## 2. Python Libraries Used

The following Python libraries are used throughout the analysis:
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- patsy
- scikit-learn

## Assignment 1 Folder

### Purpose

Assignment 1 focuses on analyzing the fairness and bias in recidivism risk scores using the COMPAS dataset. The goal is to assess whether the risk assessment tool produces disparate outcomes across demographic groups, particularly race and gender.

### Analysis

The analysis involves data cleaning, exploratory data analysis, and logistic regression modeling to investigate the relationship between demographic variables and the assigned risk scores. Statistical tests and visualizations are used to compare outcomes for different groups and to quantify disparities.

### Outcome and Conclusion

The results indicate that there are significant differences in risk scores assigned to individuals based on race and age, even after controlling for relevant covariates. The analysis highlights the presence of bias in the COMPAS algorithm, underscoring the importance of responsible and transparent machine learning practices in high-stakes decision-making contexts.

## 3. Instructions for Reproducing the Results

To reproduce the results in this repository:

1. Clone the repository to your local machine.
2. Ensure you have Python 3.8 or higher installed.
3. Install the required libraries using pip:
	```bash
	pip install pandas numpy matplotlib seaborn statsmodels patsy scikit-learn
	```
4. Open the relevant Jupyter notebooks (`.ipynb` files) in your preferred environment (e.g., JupyterLab, VS Code, or Google Colab).
5. Run the cells in order to reproduce the analysis and results.

If you encounter any issues or missing packages, please refer to the notebook's first cell or requirements section for additional dependencies.
