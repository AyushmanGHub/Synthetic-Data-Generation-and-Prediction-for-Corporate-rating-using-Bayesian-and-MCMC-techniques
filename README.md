# Synthetic Data Generation and Prediction for Corporate Rating using Bayesian and MCMC Techniques

### 📌 Abstract

This project focuses on building a **robust synthetic data generation pipeline** and **Bayesian credit-rating prediction models** for corporate credit datasets.
Corporate credit rating data is often scarce, confidential, and difficult to obtain, which limits the performance of machine learning models.
To address this challenge, this project combines:

* **Gaussian Mixture Modelling**
* **Rank-based Quantile Matching**
* **MCMC-based Correlation Refinement**
* **Bayesian Logistic & Multinomial Rating Models**

to create **statistically accurate synthetic datasets** and **uncertainty-aware rating predictions**.

The final system enhances small datasets, captures uncertainty, and provides credible intervals for every prediction, making it suitable for high-risk financial modelling tasks.

### 📌 Problem Statement and Solution

**The Challenge:**
Corporate credit data is limited, noisy, and belongs to multiple rating agencies with inconsistent methodologies.
Traditional ML models retrain from scratch on every update and cannot quantify uncertainty — a major drawback in finance.

**My Solution:**
This project builds a comprehensive Bayesian–MCMC pipeline that:

* Generates **high-fidelity synthetic financial data**
* Preserves marginals, correlations, categorical patterns
* Utilizes **posterior predictive distributions** for classification
* Provides **95% credible intervals** per prediction
* Performs well even with limited real-world data

This enables more reliable modelling and improves generalization under data scarcity.

<!-- <img src="Resources/synthetic_overview.png" alt="pipeline" width="1000" height="420"/> -->


### 📌 Introduction

This repository provides a complete framework for:

* Synthetic data generation for corporate financial ratios
* Bayesian binary and multiclass credit rating classification
* MCMC-based refinement of statistical structure
* Model comparison between classical ML and Bayesian methods

The goal is to show how **Bayesian inference and MCMC sampling significantly enhance prediction stability** in low-data, high-risk domains like credit rating.


### 📌 How It Works

The system follows a structured 4-stage pipeline:

1. **Data Preprocessing**

   * Cleaning, one-hot encoding, rating compression (24 → 5 major classes)
   * Splitting into numeric/categorical subsets

2. **Synthetic Data Generation**

   * **GMM modelling** for numeric features
   * **Component-wise categorical probability modelling**
   * **Quantile matching** to real data
   * **MCMC refinement** to repair covariance structure

3. **Bayesian Prediction Models**

   * Binary: Bayesian logistic regression + residual GMM penalty
   * Multiclass: Bayesian multinomial logistic regression
   * Extraction of **posterior samples**, **credible intervals**, and **uncertainty-aware predictions**

4. **Model Comparison**

   * Baseline ML: Logistic Regression, Linear Discriminant Analysis
   * Proposed Bayesian models
   * Evaluation on **both real and synthetic data**


### 📌 Tools and Technologies Used

* **Programming Language:** Python
* **Data Handling:** Pandas, NumPy
* **Synthetic Modelling:** scikit-learn (GMM), SciPy, MCMC sampling
* **Bayesian Methods:** Custom Metropolis–Hastings sampler
* **Evaluation:** KL Divergence, Jensen–Shannon Similarity, F1, Accuracy
* **Visualization:** Matplotlib, Seaborn
* **Notebooks:** Jupyter Notebook

### 📌 Results Summary

* **Binary Bayesian model** outperforms classical Logistic Regression
* **Synthetic data closely matches** real data distributions
* **Multiclass performance is lower** mainly due to inconsistent rating styles across agencies
  * A dataset from a **single agency** would significantly improve multiclass performance
* **Credible intervals** allow uncertainty-aware decision-making
* Final pipeline is robust, extensible, and suitable for financial risk modelling

---

## 🤝 Let’s Connect!

If you're interested in Bayesian modelling, synthetic data, credit risk, or MCMC techniques — feel free to reach out anytime!

**Happy to collaborate, discuss ideas, or extend this work further 🚀**

