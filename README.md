# Responsible_Machine_Learning

## 1. Purpose of the Analysis

This repository contains assignments and analysis for the Responsible Machine Learning (RML) course. The main purpose of the analysis is to explore, implement, and evaluate responsible and ethical practices in machine learning, including fairness, transparency, and bias mitigation in predictive models.

## Quick Start

- Clone this repository locally.
- Create and activate a Conda environment with Python 3.11.
- Install dependencies from the reproducibility section in this README.
- Register/select the `Python (chat-env)` Jupyter kernel.
- Open a notebook and run cells in order from top to bottom.
- If installation fails, check the compatibility notes before changing package versions.

## 2. Python Libraries Used

The following Python libraries are used throughout the analysis:

- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- patsy
- scikit-learn
- dice-ml
- shap
- lime

--------------------------------

## Assignment 1 Folder

### Purpose

Assignment 1 focuses on analyzing the fairness and bias in recidivism risk scores using the COMPAS dataset. The goal is to assess whether the risk assessment tool produces disparate outcomes across demographic groups, particularly race and gender.

### Analysis

The analysis involves data cleaning, exploratory data analysis, and logistic regression modeling to investigate the relationship between demographic variables and the assigned risk scores. Statistical tests and visualizations are used to compare outcomes for different groups and to quantify disparities.

### Outcome and Conclusion

The results indicate that there are significant differences in risk scores assigned to individuals based on race and age, even after controlling for relevant covariates. The analysis highlights the presence of bias in the COMPAS algorithm, underscoring the importance of responsible and transparent machine learning practices in high-stakes decision-making contexts.

---------------------------------

## Assignment 2 Folder

### Purpose

Assignment 2 focuses on the application of SHAP (Shapley Additive Explanations) and fairness analysis in machine learning models. The goal is to understand how local explanation methods like SHAP can be used to interpret model predictions and to evaluate fairness, particularly in the context of protected attributes such as race.

### Analysis

The analysis involves using SHAP to decompose model predictions into feature attributions for individual instances. It explores the efficiency axiom, the interpretation of zero SHAP values for protected attributes, and the limitations of local explanations in ensuring fairness. The assignment also examines group-level fairness metrics, such as false positive rate (FPR) parity, and discusses the potential for proxy discrimination.

### Modeling

Machine learning models are trained to predict outcomes using features that may include or exclude protected attributes. SHAP values are computed for these models to analyze the contribution of each feature to individual predictions. The assignment demonstrates how SHAP can reveal or obscure the influence of protected attributes and highlights the importance of combining local explanations with group-level fairness checks.

### Outcome and Conclusion

The results show that a zero SHAP value for a protected attribute (e.g., race) in a specific instance does not guarantee overall fairness or race-blindness in the model. Proxy variables and distributional differences can still lead to disparate impacts. The assignment concludes that both local explanation tools like SHAP and group-level fairness metrics are necessary for a comprehensive fairness audit in responsible machine learning.

-------------------------------------------

## 3. Instructions for Reproducing the Results

To reproduce the results in this repository:

1. Clone the repository to your local machine.
2. Ensure you have Python 3.8 or higher installed.
3. Install the required libraries using pip:
	```bash
	pip install pandas numpy matplotlib seaborn statsmodels patsy scikit-learn lifelines lime dice_ml shap solas_ai
	```
4. Open the relevant Jupyter notebooks (`.ipynb` files) in your preferred environment (e.g., JupyterLab, VS Code, or Google Colab).
5. Run the cells in order to reproduce the analysis and results.

If you encounter any issues or missing packages, please refer to the notebook's first cell or requirements section for additional dependencies.

-------------------------------------------

## 4. Reproducibility Caution (Tested Environments and Compatibility)

To help others run `Assignment_3/Individual_Homework_3.ipynb` without dependency errors, use the tested setup below.

### What was tested

- System Python: 3.10.19
- Anaconda `base`: Python 3.13.x
- Anaconda `chat-env`: Python 3.11.11

### Compatibility notes

- `lifelines==0.30.3` requires Python >= 3.11.
	- Fails on Python 3.10.
- `solas-ai` did not resolve in the tested Python 3.13 kernel (`base`).
	- Worked in Python 3.11 (`chat-env`).
- `pydantic==1.10.26` is pinned for assignment compatibility and may differ from newer default environments.

### Recommended reproducible setup (Anaconda)

Use a Python 3.11 Conda environment and run the notebook with that kernel:

```bash
conda create -n chat-env python=3.11 -y
conda activate chat-env
python -m pip install --upgrade pip
python -m pip install solas-ai lifelines==0.30.3 pydantic==1.10.26 --force-reinstall lime dice_ml shap
python -m pip install ipykernel
python -m ipykernel install --user --name chat-env --display-name "Python (chat-env)"
```

Then, in Jupyter or VS Code, select the `Python (chat-env)` kernel before running notebook cells.

### Why this caution matters

Small version changes (especially Python minor version and fairness/XAI package versions) can change install behavior or break imports. For reproducible grading and analysis outputs, keep the environment close to the tested matrix above.
