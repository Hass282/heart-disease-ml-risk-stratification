# Machine Learning-Based Risk Prediction & Patient Stratification in Heart Disease

## Overview
Cardiovascular disease remains one of the leading causes of mortality worldwide, yet risk prediction models often rely on aggregate patterns that may not reflect individual variation.

This project explores how machine learning can be used not only to predict heart disease risk, but also to better understand heterogeneity across patients. The goal was to build reliable predictive models while investigating whether different patient subgroups exhibit distinct risk patterns and model behavior.

Rather than focusing purely on performance, this work also examines interpretability, robustness, and the practical implications of model choice in a clinical context.

---

## Motivation
A recurring issue in predictive modelling is that models perform well "on average" while masking important variation across individuals.

This project was motivated by two key questions:
- Can we build accurate models for heart disease prediction using clinical data?
- Do different patient groups respond differently to these models, and what does that imply for real-world use?

---

## Dataset
- Combined dataset of ~900 patient observations from multiple sources  
- Includes demographic, clinical, and diagnostic variables  
- Preprocessing included:
  - Handling missing values  
  - Feature scaling  
  - One-hot encoding for categorical variables  

---

## Methods

### Predictive Modelling
Several classification models were implemented and compared:
- Logistic Regression  
- Random Forest  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  

Models were evaluated using:
- Cross-validation  
- ROC-AUC  
- Sensitivity & specificity  

---

### Dimensionality Reduction
- Principal Component Analysis (PCA) was used to reduce dimensionality and mitigate multicollinearity.

---

### Patient Stratification
To explore heterogeneity:
- Clustering techniques (k-means / hierarchical clustering) were applied  
- Patients were grouped based on feature similarity  
- Model performance was evaluated within each subgroup  

---

## Results

- All models achieved strong predictive performance (AUC ≈ 0.93–0.95)  
- Logistic Regression performed comparably to more complex models while offering greater interpretability  
- Clustering revealed distinct patient subgroups with different:
  - Risk profiles  
  - Model performance behavior  

---

## Key Insights

- **Model complexity vs interpretability trade-off:**  
  More complex models did not significantly outperform simpler ones, suggesting that interpretable models may be preferable in clinical settings.

- **Heterogeneity matters:**  
  Model performance varied across patient clusters, indicating that aggregate evaluation can obscure meaningful subgroup differences.

- **Data limitations are critical:**  
  Merging datasets introduced potential biases, highlighting the importance of careful preprocessing and critical evaluation of data sources.

---

## Tools & Technologies
- Python / R  
- Scikit-learn / caret  
- Data preprocessing & visualization libraries  
- R Shiny (for interactive application)

---

## Interactive Application
An interactive web application was developed to:
- Allow real-time risk prediction  
- Visualize model outputs  
- Communicate results to both technical and non-technical users


## Why this project is interesting

While predictive models achieved high performance (AUC ≈ 0.95), a key observation was that more complex models did not significantly outperform simpler ones such as logistic regression.

This raises an important question: in high-stakes domains like healthcare, should interpretability be prioritized when performance gains from complex models are marginal?

Additionally, clustering revealed that model performance varied across patient subgroups, suggesting that aggregate evaluation may mask clinically meaningful heterogeneity.

## Limitations

- Dataset size (~900 observations) may limit generalizability  
- Merged datasets introduce potential bias  
- Lack of longitudinal data restricts temporal insights  



