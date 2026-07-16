
# Predictive Customer Analytics for Banking Campaigns

> **Predicting Customer Subscription Behavior Using Machine Learning to Improve Marketing Campaign Effectiveness and Customer Segmentation**

[![R](https://img.shields.io/badge/Language-R-276DC3?style=flat&logo=r&logoColor=white)](https://www.r-project.org/)
[![Quarto](https://img.shields.io/badge/Report-Quarto-4A90D9?style=flat)](https://quarto.org/)
[![ML Models](https://img.shields.io/badge/Models-Regression%20%7C%20Classification-brightgreen?style=flat)]()


---

# Executive Summary

This project demonstrates the development of an end-to-end predictive analytics solution that helps financial institutions identify customers most likely to subscribe to term deposits while also understanding the factors influencing customer account balances.

Using statistical modeling and machine learning techniques, the project provides actionable insights that improve customer segmentation, optimize marketing resource allocation, and support data-driven decision-making.

---

# Business Problem

Banks invest heavily in direct marketing campaigns, yet broad customer targeting often results in:

- Low conversion rates
- Inefficient marketing spending
- Poor customer segmentation
- Missed revenue opportunities

This project addresses two critical business questions:

1. Which customers are financially valuable?
2. Which customers are most likely to subscribe to a term deposit?

---

# Project Highlights

- Dataset: 45,211 banking customers
- 16 demographic and campaign variables
- Six predictive models developed
- Approximately 92% classification accuracy
- Near-perfect ROC performance
- Actionable recommendations for marketing optimization

---

# Solution Overview

The solution consists of two complementary analytical tracks.

## Track 1 — Predicting Customer Account Balance

**Objective**

Estimate customer account balances using demographic and campaign information.

**Models Evaluated**

- Multiple Linear Regression
- Lasso Regression
- Generalized Additive Model (GAM)

**Best Performing Model**

- Generalized Additive Model (GAM)

---

## Track 2 — Predicting Term Deposit Subscription

**Objective**

Predict whether a customer is likely to subscribe to a term deposit.

**Models Evaluated**

- Logistic Regression
- Random Forest
- Gradient Boosted Trees

**Best Performing Models**

- Tuned Random Forest

- Tuned Gradient Boosted Trees

---

# Key Results

- Achieved approximately 92% classification accuracy.
- Contact duration was the strongest predictor of subscription.
- Campaign frequency negatively impacted conversion rates.
- Previous campaign success significantly increased subscription likelihood.
- Generalized Additive Models captured non-linear balance relationships better than traditional linear regression.

---

#  Business Insights

## Regression Analysis: Customer Account Balance

**1. Customer Financial Value Increases Non-Linearly with Age**
- Generalized Additive Models (GAMs) revealed that account balances increase non-linearly with age. Traditional linear models underestimate financial value among older customers, making age-based segmentation a more effective strategy.

**2. Customer Engagement Reflects Financial Value**
- Longer customer interactions were associated with higher account balances, suggesting that engagement quality is an indicator of customer financial value.

**3. Additional Financial Variables Are Needed**
- Although GAM outperformed the other regression models, all regression models produced relatively low explanatory power (R²). This indicates that variables such as income, credit score, savings behavior, and transaction history would significantly improve balance prediction.

## Classification Analysis: Term Deposit Subscription

**4. Customer Engagement Drives Subscription Success**
- Call duration was the strongest predictor of term deposit subscription. Customers who remained engaged in longer conversations were significantly more likely to subscribe.

**5. Excessive Customer Contact Reduces Conversion**
- Higher campaign frequency negatively affected subscription rates. Customers contacted repeatedly during the same campaign were less likely to convert, suggesting diminishing returns from aggressive outreach.

**6. Previous Campaign Success Predicts Future Conversion**
- Customers who responded positively to previous campaigns were substantially more likely to subscribe again, making historical campaign performance an effective indicator for prioritizing future marketing efforts.

**7. Ensemble Machine Learning Models Delivered Superior Performance**
- Tuned Random Forest and Gradient Boosted Trees achieved approximately 92% classification accuracy, outperforming traditional statistical approaches and providing reliable prediction of customer subscription behavior.

---

#  Strategic Business Recommendations

## Recommendations from the Regression Analysis

**1. Develop an Age-Based Customer Segmentation Strategy**
- Replace traditional demographic segmentation with age-based segments that reflect the non-linear relationship between age and account balance identified by the Generalized Additive Model (GAM).

*Expected Impact*
- More accurate identification of high-value customer segments and improved targeting of premium financial products.

**2. Incorporate Additional Financial Variables**
- Enhance future predictive models by integrating variables such as income, credit score, savings behavior, and transaction history.

*Expected Impact*
- Improved prediction accuracy and more reliable identification of financially valuable customers.

**3. Prioritize Customers with Higher Financial Engagement**
- Use customer engagement indicators, such as longer interaction duration, alongside demographic information to better identify customers with greater financial value.

*Expected Impact*
- More effective customer profiling and improved prioritization of relationship management efforts.

## Recommendations from the Classification Analysis

**4. Prioritize Call Quality Over Call Volume**
- Train campaign teams to focus on meaningful, high-quality customer conversations rather than maximizing the number of outbound calls.

*Expected Impact*
- Higher subscription rates and improved customer engagement.

**5. Implement Contact Frequency Limits**
- Limit the number of campaign contacts per customer to reduce diminishing returns and customer fatigue.

*Expected Impact*
- Lower marketing costs and improved campaign conversion rates.

**6. Prioritize Previously Responsive Customers**
- Develop a re-engagement strategy targeting customers who responded positively to previous campaigns.

*Expected Impact*
- Higher return on marketing investment through improved customer targeting.


**7. Deploy the Best-Performing Machine Learning Model**
- Integrate the Tuned Random Forest or Gradient Boosted Trees model into campaign planning to score customers based on their probability of subscribing.

*Expected Impact*
- More efficient allocation of marketing resources and higher campaign effectiveness.

---

# Business Impact


| Recommendation | Expected Business Impact |
|----------------|--------------------------|
| Deploy the classification model to pre-score campaign lists | Improves marketing efficiency by identifying high-probability subscribers before campaign launch, increasing conversion rates while reducing wasted outreach. |
| Implement contact frequency limits | Lowers marketing costs, reduces customer fatigue, and improves campaign effectiveness through more targeted engagement. |
| Prioritize previously responsive customers | Increases return on marketing investment by focusing resources on customers with a proven history of positive campaign responses. |
| Shift from call volume to call quality | Improves customer engagement and increases the likelihood of successful term deposit subscriptions. |
| Implement age-based customer segmentation | Enhances identification of high-value customer segments, supporting more personalized financial product offerings and relationship management. |
| Enrich future models with additional financial variables | Strengthens predictive accuracy for customer valuation, enabling better long-term customer segmentation and strategic planning. |


---

# Technical Skills Demonstrated

## Machine Learning

- Regression Modeling
- Classification Modeling
- Feature Engineering
- Model Evaluation
- Hyperparameter Tuning

## Analytics

- Predictive Analytics
- Statistical Analysis
- Customer Segmentation
- Business Intelligence
- Data Storytelling

## Tools & Technologies

### Programming

- R

### Machine Learning

- tidymodels
- ranger
- xgboost
- glmnet
- mgcv

### Data Preparation

- tidyverse
- dplyr
- recipes
- janitor

### Visualization

- ggplot2
- GGally
- vip
- ggcorrplot

### Reporting

- Quarto
- GitHub

---

# Limitations

All three regression models produced very low R² values, suggesting the dataset lacks key financial predictors necessary for accurate balance prediction
The dataset originates from a Portuguese bank (2008–2013) and may not generalize to other markets or time periods, particularly given the 2008 financial crisis context
The large "unknown" category in poutcome and job may introduce noise into classification predictions
Class imbalance in y required SMOTE intervention — results may differ on naturally balanced or differently distributed datasets

---

# Conclusion

This project successfully addressed two core business challenges through a dual analytical framework. For account balance prediction, GAMs achieved the best performance (RMSE: 2,998.206, R²: 0.015), confirming non-linear relationships between predictors and balance — with age emerging as the dominant factor. For term deposit subscription classification, both Tuned Random Forest and Tuned Gradient Boosted Models achieved 92% accuracy with an AUC near 1.0, identifying contact duration and campaign frequency as the strongest drivers of subscription likelihood.

While the regression models revealed meaningful patterns, the low R² values suggest that additional financial variables would be needed to build a production-ready balance predictor. The classification models, however, demonstrated strong real-world applicability — providing the bank with a reliable tool to identify and prioritize likely subscribers before campaign outreach begins.


<details>
# 📎 Technical Appendix
<summary>📊 Dataset Description (Click to Expand)</summary>

## 📂 Data Source

**Dataset:** Bank Marketing Dataset

**Source:** UCI Machine Learning Repository

**Official Dataset:**  
https://archive.ics.uci.edu/dataset/222/bank+marketing

### Dataset Overview

The dataset contains information collected from direct marketing campaigns conducted by a Portuguese banking institution. The objective is to predict whether a customer will subscribe to a term deposit based on demographic characteristics and previous marketing interactions.

### Dataset Characteristics

| Attribute | Value |
|-----------|--------|
| Records | 45,211 |
| Predictor Variables | 16 |
| Target Variable | `y` (Term Deposit Subscription) |
| Missing Values | None |
| Response Variable | Binary Classification |

### Features Used

- Customer Demographics
- Employment Information
- Financial Attributes
- Previous Campaign Outcomes
- Current Campaign Information

### Data Preparation

- Checked for missing values
- Verified duplicate observations
- Converted categorical variables to factors
- Created training and testing datasets
- Applied SMOTE to address class imbalance
- Standardized data preprocessing using the **recipes** package

</details>

<details>

<summary>🖼️ Model Visualizations (Click to Expand)</summary>

The figures below summarize the key relationships identified during exploratory analysis, model development, and performance evaluation.
# Model Visualizations


### Correlation Heatmap

![Correlation Heatmap](figures/correlation_heatmap.png)


Shows the strength of relationships among key numerical variables and highlights potential multicollinearity.

---

### Subscription Distribution

![Subscription Distribution](figures/03_subscription_distribution.png)

Illustrates the class imbalance between customers who subscribed and those who did not, motivating the use of SMOTE during model training.

---

### Random Forest Variable Importance

![Variable Importance — Random Forest](figures/05_vip_randomforest.png)

Identifies the variables contributing most to subscription prediction, with call duration emerging as the dominant predictor.

---

### Gradient Boosting Variable Importance

![Variable Importance — Gradient Boosted Model](figures/08_vip_gradientboosted.png)

Confirms the importance of customer engagement and campaign-related variables while validating feature consistency across models.

---

### ROC Curve

![ROC Curves — All Classification Models](figures/07_roc_curves.png)

Demonstrates strong model discrimination between subscribers and non-subscribers, indicating excellent predictive performance.

---

### Model Comparison

| Model | Best Use |
|--------|----------|
| Multiple Linear Regression | Baseline Regression |
| Lasso Regression | Feature Selection |
| Generalized Additive Model | ⭐ Best Regression Model |
| Logistic Regression | Baseline Classification |
| Random Forest | High Classification Performance |
| Gradient Boosted Trees | ⭐ Best Overall Classification Model |

Compares regression and classification models to support selection of the best-performing approaches for deployment.

<details>

<details>

<summary>📈 Regression Analysis Details (Click to Expand)</summary>

### Models Evaluated

- Multiple Linear Regression
- Lasso Regression
- Generalized Additive Model (GAM)

### Model Performance

| Model | RMSE | R² | MAE | Key Strength |
|-------|-----:|---:|----:|--------------|
| Multiple Linear Regression | 3,004.647 | 0.010 | 1,505.722 | Interpretable baseline model |
| Lasso Regression | 3,050.961 | 0.008 | 1,505.330 | Performs feature selection through regularization |
| Generalized Additive Model (GAM) ⭐ | **2,998.206** | **0.015** | **1,499.378** | Captures non-linear relationships between predictors and account balance |


### Key Takeaway

The Generalized Additive Model produced the strongest regression performance by capturing non-linear relationships between customer age and account balance.

</details>

<details>

<summary>🤖 Classification Analysis Details (Click to Expand)</summary>

### Models Evaluated

- Logistic Regression
- Random Forest
- Gradient Boosted Trees

### Model Performance

## Model Performance Comparison

| Model | Accuracy | Sensitivity | Specificity | Precision | ROC AUC |
|--------|---------:|------------:|------------:|----------:|--------:|
| Logistic Regression | 0.92 | 0.87 | 0.94 | 0.89 | Slightly lower than ensemble models |
| Random Forest | 0.918 | 0.865 | 0.944 | 0.886 | 0.976 |
| Gradient Boosting | 0.92 | 0.87 | 0.94 | 0.89 | ≈0.98 |

### Key Takeaway

Random Forest and Gradient Boosted Trees achieved the strongest predictive performance and were selected as the preferred models.

</details>





















##  Tools & Technologies

| Category | Tools / Technologies |
|----------|----------------------|
| **Programming Language** | R |
| **Modeling Framework** | tidymodels, parsnip, workflows, tune, rsample, yardstick |
| **Regression Models** | Multiple Linear Regression (`lm`), Lasso Regression (`glmnet`), Generalized Additive Models (`mgcv`, `mgcViz`) |
| **Classification Models** | Logistic Regression (`glm`), Random Forest (`ranger`), Gradient Boosting (`xgboost`) |
| **Class Imbalance Handling** | `themis` (SMOTE) |
| **Data Wrangling** | `dplyr`, `tidyverse`, `janitor`, `recipes`, `skimr` |
| **Data Visualization** | `ggplot2`, `GGally`, `ggcorrplot`, `vip`, `gridExtra` |
| **Reporting & Documentation** | Quarto Dashboard, GitHub README |




